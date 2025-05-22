---
reviewed: 2025-01-13 17:05:49
title: Software templates
navigation.excerpt: Pre-configuration for quick setup
lead: While creating an app you can choose from a variety of popular open source PHP software types, which will pre-configure your app. This article explain what it does and what not.
---

## What it does not do

The software template will **NOT install** the selected software on your behalf. Installing software with composer is easy. We expect you to have a local development running before. In many cases developers bring existing projects.

## What it does do

- Choose matching components
- Set a matching PHP version
- Enable PHP extensions
- Apply desired [root path](/1.platform/11.concepts/root-path.md) — to serve from the right location
- Populate [ENV vars](/3.dev/19.env-vars) — to connect to the database automatically

The software template saves some work and helps to prevent errors. It's non-destructive, change all settings later on. This is especially handy with modern software that supports [ENV var](/3.dev/19.env-vars/2.usage.md) configuration and environment detection — like Laravel or Craft CMS do. It makes the application really portable, you can deploy the same code base to anywhere else and it will work out of the box.
