---
reviewed:      2023-07-07 09:07:46
title:         Software presets
excerpt:       Pre-configuration for quick setup
lead:          While creating an app you can choose from a variety of popular open source PHP software types. This article explain what it does and what not.
---

## What it does not do

The software preset will **not install** the selected software on your behalf. There are no one-click installers here. fortrabbit is hosting for developers. Installing software with composer is so easy. We expect you to have a local development running before. In many cases developers bring existing projects.

## What it does do

* Set a matching PHP version
* Enable/disable PHP extensions — for best performance
* Set a [root path](#root-path) — to serve the App from the right location
* Populate [ENV vars](../env-vars.md) — to connect to the database automatically

So, the software preset saves you some work and helps to prevent errors.

It's non-destructive, you can change all settings later on as you wish.

This is especially handy with modern software that supports [ENV var](../env-vars.md) configuration and environment detection — like [Laravel](../install-laravel) or [Craft CMS](../craft-deploy-git) do. It makes the application really portable, you can deploy the same code base to any App and it will work out of the box.
