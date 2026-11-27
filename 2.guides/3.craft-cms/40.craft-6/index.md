---
created: 2026-11-27
updated: 2026-11-27
reviewed: 2026-11-27
reviewer: fl
ai: co-authored
title: Craft CMS 6 beta guides
description: 'Install, deploy and run the Craft CMS 6 beta on fortrabbit: the Laravel-based Craft with a public webroot, PHP 8.5 and Artisan commands.'
naviTitle: Craft CMS 6 beta
navigation.excerpt: Laravel-based Craft, in beta
lead: Craft CMS 6 runs on Laravel. These guides cover what is different from Craft 5 when hosting it on fortrabbit.
subject: craft-cms
head:
  meta:
    - name: keywords
      content: 'craft cms 6, craft 6 beta, laravel, deploy, fortrabbit'
topics:
  - craft-cms
  - cms
  - php
---

::CallOut{alert}
Craft CMS 6 is in beta, with a stable release planned for March 2027. Pixel & Tonic says it is not ready for production use. These guides follow the beta and change with it.
::

## Differences to Craft 5

Craft 6 is a rewrite on Laravel 13. The deploy setup follows Laravel, not Craft 5:

- PHP 8.5 or newer
- Webroot `public`, not `web`
- Commands run with `php artisan craft:…`, for example `php artisan craft:up`
- Database settings in `DB_*` ENV vars, not `CRAFT_DB_*`
- Craft filesystems are Laravel disks, set up in `config/filesystems.php`
- Queue and scheduler are Laravel's

The Craft CMS [software template](/1.platform/03.concepts/05.software-templates.md) has a version 6 with these settings, and the [stack detector](/1.platform/03.concepts/04.stack-detector.md) picks it for a Craft 6 repository.

## Install and deploy run down

1. [Install Craft CMS 6 locally](/2.guides/3.craft-cms/40.craft-6/01.install.md)
2. [Set up an app at fortrabbit](/2.guides/3.craft-cms/40.craft-6/02.setup.md)
3. [Deploy code via Git](/2.guides/3.craft-cms/40.craft-6/03.deployment.md)
4. [Database syncing](/2.guides/3.craft-cms/40.craft-6/05.database.md)
5. [Assets](/2.guides/3.craft-cms/40.craft-6/06.assets.md)

Performance, caching and plugins are covered for Craft 5 only so far, in the [Craft CMS 5 guides](/2.guides/3.craft-cms/index.md). Moving from Craft 5 to 6? See the [Craft upgrade guide](https://craftcms.com/docs/6.x/upgrade.html).
