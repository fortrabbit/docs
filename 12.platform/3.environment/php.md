---

reviewed:      2023-06-02 10:31:13
title:         PHP
excerpt:       Book, configure, understand concepts
lead:          PHP is — as you are probably aware — a popular web programming language. It's also the core Component here on fortrabbit. See here how to use and scale PHP.

keywords:
  - app-design

---
<!-- TODO: merge (maybe partly) with scaling-pro article (to similar topics) -->

## Booking PHP

When you create a new [environment](/environment) in the [Dashboard](/dashboard) you'll be presented with a plan chooser for the PHP component. See below to select the correct initial scaling.

## Configuring PHP

You'll find a PHP settings page with your App in the Dashboard. Here you can switch the PHP version and configure various PHP extensions.

## Scaling

When first creating your App, you might or might not know how much memory (PHP memory limit) your application will need. The amount determines the [vertical scaling](scaling-pro#toc-vertical-scaling) plan you should choose.

We offer three main PHP scaling plan sizes: **PHP s, PHP m, PHP l**. Which of those fits your App best depends on the technology stack (framework, CMS …) and on the code you write. For the latter you should read our [application design](app-design) guide on how you can get the most performance out of your application.

Don't be afraid to test and experiment with different scaling settings: You can instantly scale up and down to find the best match.

### When to upgrade

Once you have found the perfect vertical size you usually don't need to change it. However, if your App grows strongly in terms of increasing functionality (i.e. code size) or if your code does not scale well with increasing amounts of visitors, then you might need to upgrade the vertical size.

To be ready for that: watch the memory and swap metrics in the [Dashboard](dashboard): if the memory is maxed out and you are seeing an increasing swap usage then your App needs more memory.

In some cases swap usage by the application is not possible. In these cases you might see dreaded white-pages and along going error messages in the log: "Allowed memory size of 1234.. bytes exhausted (tried to allocate 234 bytes)." This should be understand as an urgent reminder to scale to the next vertical size.

## PHP memory

The memory of each PHP plans is only for PHP usage - no Apache, no MySQL, no nothing. So 128 MB, 256 MB and even 512 MB of memory might sound small, but it is actually quite a lot, because it is not shared with other resources.

How much memory your App will require depends on multiple factors. Let's start with the theory:

**Extensions**: Each enabled PHP extension must be loaded into memory. Extension have a different size, so a full fledged framework such as Phalcon uses more memory than a simple driver such as Memcached.

**OPcache 1: PHP libraries**: You most likely are using Composer to manage your dependencies. This implies a set of PHP files which need to be interpreted and loaded into memory - specifically into the OPcache.

**OPcache 2: PHP code**: The code you write yourself consumes memory in the OPcache as well. The more code you have, i.e. the more functions and complexity, the more memory is required.

**Runtime variables**: In each request your App fills variables (`$foo = "bar"`), which consumes memory. How much it will use depends on the amount of data used in variables. You can measure how much you are by calling [memory_get_peak_usage()](http://php.net/manual/en/function.memory-get-peak-usage.php).

Now, the memory used by extensions and OPcache is shared. This means: If you run an App on a single process and use 10 MB OPcache, then you will also only use 10 MB of OPcache with two processes. The memory consumed by runtime variables is not shared.

It's hard to pre-calculate the expected memory usage of your App. However, you can make educated guesses.

For example, using [Slim Framework](install-slim) does require (big surprise) far less memory than using a full scale framework such as CakePHP or [Laravel](install-laravel). A form + email based mini-eshop requires far less memory than a Magento installation with plugins.

An approximation, although with some exceptions, is to look at the size of the source code to guesstimate the expected memory usage. Using the same example: the source code (especially including Composer package files) of a Laravel installation is larger than that of Slim Framework, so you can expect Laravel's memory consumption to be larger, and you would be right.

The tricky part is the runtime data. Say you have a blog with comments using a database. Now rendering a small blog entry with no comments will utilize less memory than rendering a large blog entry with thousands of comments. Or does it? Well, it really strongly depends on your design and actual code. For example, you could load all of the thousands of comments into a PHP array and then render the site or you could load them one by one and print them out immediately - both would have a different impact on memory. In general the memory usage will change over the lifetime of your App - expect it to increase with growing data size.
