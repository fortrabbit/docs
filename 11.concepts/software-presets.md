---
reviewed: 2023-07-07 09:07:46
title: Software presets
navigation.excerpt: Pre-configuration for quick setup
lead: While creating an app you can choose from a variety of popular open source PHP software types. This article explain what it does and what not.
---

## What it does not do

The software preset will **not install** the selected software on your behalf. There are no one-click installers here. fortrabbit is hosting for developers. Installing software with composer is so easy. We expect you to have a local development running before. In many cases developers bring existing projects.

## What it does do

- Set a matching PHP version, if required
- Enable/disable PHP extensions — for best performance, if required
- Set a root path — to serve the App from the right location
- Populate [ENV vars](/11.concepts/env-vars.md) — to connect to the database automatically

So, the software preset saves you some work and helps to prevent errors. It's non-destructive, you can change all settings later on as you wish.

This is especially handy with modern software that supports [ENV var](/11.concepts/env-vars.md) configuration and environment detection — like Laravel or Craft CMS do. It makes the application really portable, you can deploy the same code base to any App and it will work out of the box.

## Software presets by software

Not all software requires a software preset, for example WordPress is not using a custom root path or ENV vars. See what will be pre-populated by software:

### Laravel based

:SoftwarePreset{software="laravel" :show-info="false"}

This will apply to Laravel but also software based on Laravel, such as October CMS and Statamic.

### Symfony

:SoftwarePreset{software="symfony" :show-info="false"}

### Craft CMS

:SoftwarePreset{software="symfony" :show-info="false"}
