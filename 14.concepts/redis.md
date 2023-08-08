---
reviewed: 2023-08-01 13:07:39
title: Redis usage
naviTitle: Using Redis
excerpt: Options 
lead: 
sidebar: 
---


## Using Redis

Redis is supported by many PHP frameworks and CMS's out of the box, it's popular among [Laravel](/2.laravel/1.setup.md) developers. For specific integrations check out the install guides and find out how to use it with your favorite framework or CMS.

### Dashboard settings

TODO

### Session handler

If you don't use a framework, configure `session.save_handler` and `session.save_path` in your php.ini to tell phpredis where to store the sessions. Make sure to do it very early in your application, before accessing session data.

```php
// Read the secrects you've set in the Dashboard
$secrets = json_decode(file_get_contents($_SERVER["APP_SECRETS"]), true);
$host    = $secrets['CUSTOM']['REDIS_HOST'];
$port    = $secrets['CUSTOM']['REDIS_PORT'];
$auth    = $secrets['CUSTOM']['REDIS_PASSWORD'];

// Change the session handler
ini_set('session.save_handler', 'redis');
ini_set("session.save_path", "tcp://{$host}:{$port}?persistent=1&timeout=2&auth={$auth}"); 
```

### Persistent connections

We recommend using persistent connections. Most adapters are configurable with a setting like `persistent: 1`.
