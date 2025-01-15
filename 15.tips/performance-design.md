---
reviewed: 2024-11-24 10:47:05
title: Performance design
navigation.excerpt: Optimize code for speed
lead: Make it fast - from development to production, from backend to frontend. Do it for your wallet, your users and the environment.
---

You can always throw more hardware on [performance problems](/15.tips/performance-problems.md). But that won't always help when the problem is in the code somewhere. We want you to encourage to **design for performance** and scalability. And that is all about thinking a bit ahead.

## Backend performance design

This is the part where fortrabbit is involved the most. The TTFB depends on how fast the service can compute. Your code plays a major role. Also see the [PHP processes article](/15.tips/php-processes.md) to learn about limits when executing PHP. See our [performance problems article](/15.tips/performance-problems.md) on how to analyze backed performance problems.

### Prepare to cache

If you begin developing, you might not instantly utilize a pair of multi gigabyte Redis servers. Still: make sure to implement caching early on and to use abstraction, so you can later on switch to those caching machines when you need them. Available caching solutions on fortrabbit:

- File: Disk storage is not very fast.
- Database: Faster than disk. Use if you need to cache data for a long time.
- APC: Aside from opcode caching which happens automatically, you can use APC as an object cache very similar to Memcache or Redis.
- Redis: Modern key value im memory caching service, see the [Redis component article](/9.components/8.redis.md)

### Reduce I/O

It's always a good idea to reduce file input/output operations on the disk to the minimum. In PHP this means:

- **PHP includes**: Reduce amount of includes as much as possible. Always use absolute path names, which reduces the amount of lookups.
- **Avert files**: Don't use file-sessions, file-caches or anything `file-*`, if you can replace it with an in-memory cache or even the database.
- **Outsource static files**: Put your static files on an object storage. Sure, they could be delivered very fast from local, but still, they will create I/O which your (PHP) App will be missing.
- **Shrink your loader chain**: Make sure you load only the classes (files) you need. For a production App (in which code changes do not occur often) you can set `apc.stat` or `pcache.validate_timestamps` to `0`, which reduces I/O on `.php` files even further, but requires an APC/OPcache flush for changed files to apply.

### Decouple, but loosely

Leverage the power of the cloud: Span your App across multiple services. If you need image or video encoding: use an external service for this. If you want to send mass mails: use an external service for this. Why? Because it balances the load of your App and thereby gives it more resources for each individual task it has to perform.

However, if one of those external service (temporarily) breaks, make sure you can switch it off in seconds! You still want your shopping basket to run, if your image transformation has a problem.

### Prepare for CDN

If you're planning on growing large and expect a lot of traffic, you will end up putting your static files (images, videos, css and js files, ...) behind a Content Delivery Network. Nowadays, you can do this pretty effortless with specialized services. Some services work best with a dedicated (sub)domain for your static contents, such as _img.yourdomain.com_. If you expect to use them in the future, you should implement the required structure from the start. Also a good precaution is to setup your cache headers properly from the start.

### Database considerations

Very common: check your JOIN queries! If they ran fast when your dataset was small, it doesn't mean they still do with a bigger dataset. Utilize caches to buffer costly databases results. Database optimization could easily fill a whole book — or books. Read our [dedicated MySQL performance tips](/mysql/performance).

### Static file separation

Sure, a request to a static file can be delivered faster than a request handled by a dynamic script - nonetheless, the more static requests are performed by your App, the more it has to do overall. More is more in the end. If you split up the traffic in dynamic and static requests, by utilizing a cloud hosting service, all the requests for static files are not handled by your App anymore but by another server somewhere else. Resulting, your App on fortrabbit acts as the motor for your PHP scripts, while a host dedicated to delivering static files takes care of the rest.

### Profile your code

Web applications are usually fast after the launch, but degrade over time. They receive more requests and process more data. You add more features and at some point everything or some parts of your app become slow. Profilers give you deep insights of your code and all dependencies that are involved to handle requests. XDEBUG profiler and XHPROF are the defacto open source standard, but you need additional tools to visualize the data. The [blackfire profiler](/14.integrations/blackfire.md) makes it really easy to start profiling in minutes.

### Reduce the max execution time

This is an opinionated topic. If you come from searching 504 time out errors, you will often read to increase the `max_execution_time` setting to allow a certain process to finish it's task.

By the way: You can adjust this setting with your app environment under "PHP settings" in the dashboard.

In some cases that makes sense, but it's often a poor design decision. Image transformations with imageMagick are often long running, therefore you might want to increase the execution time to avoid time outs. But, as stated here often: long running tasks should best be separated from the frontend tasks into the background. With the [jobs](/9.components/7.jobs.md) component you can outsource jobs.

Frontend requests should always return a swift answer. The number of PHP processes is limited. When all PHP processes are occupied with long running tasks, new requests need to wait. That can easily pile up. A lower max execution time limit often results in faster errors. And that's often what you want. When making an API call to an external service, usually that reply should be there within a second, how long should you wait for it max? Maybe 10 seconds is reasonable. It's not likely that there will be an answer when you wait longer.

So for most cases, short is better.

### Block and limit bots

A lot of web traffic is generated by crawling bots. There are bad ones and good ones. Did you know: A wrongly configured navigation plugin can cause a bot to get stuck in a loop visiting an endless number of pages within your website. This can cause high load, traffic and ultimately spam your template caching folder.

Enable our [WAF feature](/11.concepts/waf.md).

Set a crawl delay to limit unnecessary crawling of your website if it is not updated very frequently. The craw-delay directives in `robots.txt` are supported by good bots such as search engines, commercial bots, SEO bots.

## Frontend performance design

Are you a full-stack developer? A lot of delivery can be optimized in the front facing side of your application. Let's have a look what can be done on the last meters and how to optimize content efficiency:

### JS & CSS

Assets are static files, such as JS, CSS, SVG and some images. It's common to have two versions of your asset files:

- the original files, that you can edit, probably SASS, POSTCSS, TS … (included in Git)
- the optimized files that are served in production (usually not included in Git)

Minifying JS/CSS files removes unnecessary extra spaces, line breaks and indentations. Modern tools support tree shaking as well. Another technique is to combine — concating — different JS or CSS files into one file. This brings you: less requests and probably better GZIP compression ratios. Finally, there are specific techniques to further reduce size: For JS, variable names can be changed automatically for shorter ones, in CSS you can use shorthands and short notations of colors and values.

You can hook in Node.js pipelining tasks during [deployment build steps](/6.deployment/3.build-commands.md).

### Images

Images (JPG, PNG, SVG, WebP …) represent around 70% of the total footprint of an average website. Most images are user generated content, for example when an editor uploads a photo to a CMS. Invest some time to tune your image transformations. Deliver only required sizes to the website visitor. Try different compression settings and even image formats. Consider using a third party service to host images, if your website needs a lot or if it has many visitors or you need to serve large versions og images.

### Videos

Our [traffic tiers](/9.components/4.traffic.md) are not designed to host local videos. It's recommended to outsource video hosting to a 3rd party. That will also help with compression and delivery.

### Web fonts

Web fonts are nice but they also come with a footprint. The file size is determined by the number of glyphs, metadata and compression. On top of that, there are four different formats and you probably need to include all to have the best coverage. External services can help to optimize font size and delivery.

### Caching assets

Don't serve the same content to the same client twice. Cache it with their browser. While modern browsers are already doing great work here. You can further control the caching by altering the Cache-Control with the HTTP headers.

GZIP provides lossless compression for text files such as HTML, CSS or JS. It's implemented on the web server — Apache in our case otherwise nginx — as a module. You can enable and configure it in your `.htaccess` file (see also our [htaccess GZIP article](/15.tips/htaccess/4.gzip.md)).

It works like this: after all the HTML is rendered on the server side it gets compressed and send to the browser in such a minified format. The browser then has to decompress everything on the fly. So as you can imagine: that of course saves bandwidth but also costs a little bit of CPU on both sides. It is in general recommended to use it but can cause strange effects when combined with other techniques, like caching.

### Cookies

Eat diet Cookies! Cookies are sent in the HTTP headers in every single request, always. Use a different domain for serving static assets can help to reduce the cookie traffic.

### DNS lookups

You might parallelize downloads across host names. This may help speed up delivery, but if the number of host names is too long the time that the client spends to resolve the domain can affect negatively. The concurrent connections of web browsers is limited.

### Check your speed

Faster websites and apps are more fun to use and are better ranked in search engines. Measure the performance of your App. Master the web developer tools of your browser and use external services such as Google PageSpeed (Lighthouse), YSlow and GTmetrix.

### External data sources

If you are integrating external services, for example for any kind of REST API, make sure it does not slow you down. Set proper but very small timeouts and log response times once they exceed the threshold.

Congrats. You came all the way to the bottom.
