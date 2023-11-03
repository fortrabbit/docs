---
title:     PHP performance problems
naviTitle: PHP performance problems
navigation.excerpt:  Optimize code for speed
lead:     "What you may want to know about PHP related performance issues."
---

## Understand Time To First Byte and PHP response time

For web server performance "PHP response time" is an important metric. It can be roughly translated to the Time To First Byte ([Wikipedia](https://en.wikipedia.org/wiki/Time_to_first_byte)), which also includes network latency effects. Most websites should be able to attain a "PHP response time" of 250ms or even less. This is possible  with attention to best practices - see our [performance design article](/14.tips/performance-design.md) as well.

## Understand PHP processes and execution time

Please see our dedicated [PHP processes article](/14.tips/php-processes.md).

## How to identify PHP performance problems

Not every website performance problem is backend server problem. Yet PHP performance is a common culprit. Here is how to PHP execution problems.

### Experience it yourself

Your website is slow, you will feel it. Common signs of performance issues are:

- Pages are slow to load - the browser loading icon spins
- You see timeout errors - a 504 error printed on screen

### Check the hosting metrics

The fortrabbit dashboard offers a metric section (your hosting provider likely will have something similar) including the following vital data points:

- **PHP response time**: Aim for less than 250ms on average. In our experience, it's more likely that a website with an average high repsonse time will have problems. Slow websites that are getting some more visits than usual are tending to break down (504) faster.
- **5xx error metric**: See if there are any peaks in 5xx errors. If there are, see if at the same time, the PHP response time went up, in that case those 5xx errors are likely 504 time out errors.
- **Memory usage**: The memory used should not come to close to the hosting resources you have booked on average, 80% average usage and single peaks are Ok.
- **Memory swap usage**: Swap is when there is no (fast) RAM available anymore and data needs to be accessed from disc (slow). This should be within bounds, which depends on your website.
- **OpCache**: This should not max out. Aim for 80% or less.

## Common sources for PHP performance issues

Most slow websites can be backtraced to a PEBCAK - problem exists between chair and keyboard. In other words: It's the website developers responsibility to create code that ships fast. Most often it's oversight or missing experience and attention about [performance design](/14.tips/performance-design.md).

## Swap issues

In some cases swap usage by the application is not possible. In these cases you might see dreaded white-pages and along going error messages in the log: "Allowed memory size of 1234.. bytes exhausted (tried to allocate 234 bytes)." This should be understand as an urgent reminder to scale up the [PHP plan](/9.components/1.php.md).

## What to do on PHP performance problems

### Use load testing

We advise to put your website under some controlled stress to see when it will break. There are tools you can use from your computer to fire up a couple of simultaneous requests. This way you can see how the website will behave before your first unlucky visitors will find the bottleneck for you.

### Use external profilers

There are also commercial, professional profiling services providing helpful detailed low-level profiling information. They can be useful for bigger projects with some more traffic. On the server side, they are integrated as PHP extensions (pre-installed on fortrabbit). The most popular ones are [Blackfire](/13.integrations/blackfire.md) (recommended by us) and [NewRelic](/13.integrations/new-relic.md).

### Refactor code

Only good code can fly. Review your code. Make it perform better. See our [performance design article](/14.tips/performance-design.md) for inspiration.

### Book more hosting resources

Of course, we - as our hosting provider - have an interest in selling you bigger servers. But our experience shows that it usually needs a lot of money to compensate coding and config mistakes and is usually also not a good fix. You can try shopping more PHP memory, better CPU power, and more PHP process.
