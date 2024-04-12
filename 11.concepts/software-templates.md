---
reviewed: 2024-04-11 17:21:08
title: Software templates
navigation.excerpt: Pre-configuration for quick setup
lead: While creating an app you can choose from a variety of popular open source PHP software types, which will pre-configure your app. This article explain what it does and what not.
---

## What it does not do

The software template will **not install** the selected software on your behalf. Installing software with composer is easy. We expect you to have a local development running before. In many cases developers bring existing projects.

## What it does do

- Set a matching PHP version, if required
- Enable/disable PHP extensions — for best performance, if required
- Set a root path — to serve the App from the right location
- Populate [ENV vars](/11.concepts/env-vars.md) — to connect to the database automatically

The software template saves you some work and helps to prevent errors. It's non-destructive, you can change all settings later on as you wish.

This is especially handy with modern software that supports [ENV var](/11.concepts/env-vars.md) configuration and environment detection — like Laravel or Craft CMS do. It makes the application really portable, you can deploy the same code base to anywhere else and it will work out of the box.
