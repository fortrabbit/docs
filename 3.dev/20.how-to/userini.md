---
created: 2025-06-05
updated: 2026-10-24
reviewed: 2026-10-24
reviewer: fl
title: Configure .user.ini
description: 'Set PHP directives the fortrabbit dashboard does not expose with a .user.ini file in the root path. php_value in .htaccess does not work with PHP-FPM.'
naviTitle: Configure .user.ini
navigation.excerpt: Control advanced PHP settings
figure:
  emoji: ⚙️
  text: Fine-tune PHP settings beyond dashboard defaults.
  color: rgb(120, 53, 15)
  textColor: rgb(254, 243, 199)
lead: A .user.ini file in the root path sets PHP directives the fortrabbit dashboard does not offer, such as the timezone or session lifetimes. It works for per-directory settings only, and PHP reads changes within five minutes.
links:
  - title: .htaccess intro
    route: /dev/htaccess/intro
    property: docs
  - title: PHP settings in dashboard
    route: /platform/settings/php
    property: docs
  - title: PHP component
    route: /platform/components/php
    property: docs
head:
  meta:
    - name: keywords
      content: '.user.ini, PHP settings, php.ini, PHP-FPM, fortrabbit'
topics:
  - php
---

fortrabbit runs PHP with PHP-FPM, so `php_value` and `php_flag` lines in `.htaccess` have no effect. A `.user.ini` file takes their place for settings the [PHP settings](/1.platform/07.settings/06.php.md) in the dashboard do not cover.

## What .user.ini can change

PHP reads `.user.ini` for settings of the modes `PHP_INI_PERDIR` and `PHP_INI_USER`, see the [php.ini directives list](https://www.php.net/manual/en/ini.list.php). Examples:

- `date.timezone`
- `default_charset`, `short_open_tag`
- `session.*`, such as `session.gc_maxlifetime`
- `display_errors`, `error_reporting`
- `max_file_uploads`

Settings of the mode `PHP_INI_SYSTEM` are ignored, among them `opcache.*`, `apc.*` and `realpath_cache_size`. Set the values the dashboard offers there: `upload_max_filesize`, `post_max_size`, `max_execution_time`, `max_input_vars` and `output_buffering`.

## Create the file

Put `.user.ini` in the [root path](/1.platform/07.settings/12.root-path.md), such as `public/` for Laravel or `web/` for Craft CMS. It applies to the PHP scripts in that folder and below. Commit it to Git, so it deploys with the code.

```ini
; .user.ini
date.timezone = "Europe/Berlin"
session.gc_maxlifetime = 7200
session.cookie_lifetime = 7200
```

PHP caches the file and reads it again after up to five minutes (`user_ini.cache_ttl`), so a change does not show at once.

## Memory

`memory_limit` follows the [PHP plan](/1.platform/09.components/01.php.md). A higher value in `.user.ini` does not add memory: a PHP process that uses more than the plan holds is killed, see [out of memory](/3.dev/02.performance/10.out-of-memory.md). Book a larger plan instead.

## Check the result

[phpinfo](/3.dev/15.learn/10.php-info.md) shows the active value of each setting in the "Local Value" column. A setting that keeps its old value is either of the `PHP_INI_SYSTEM` mode, or the file sits outside the root path, or the cache has not expired yet. A syntax error in the file makes PHP skip it.

See the [PHP docs on .user.ini files](https://www.php.net/configuration.file.per-user).
