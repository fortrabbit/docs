---
reviewed: 2025-12-11
title: ENV vars
navigation.excerpt: Working with environment variables
lead: Working with environment variables on fortrabbit.
navigation: false
draft: false
---

ENV vars are how you pass configuration into your app without committing it to your repository: database credentials, API keys, feature flags, and anything else that differs between local, staging, and production.

The pages below cover the [environment variables fortrabbit sets for you](/3.dev/19.env-vars/01.intro.md), how to [access them from PHP and the shell](/3.dev/19.env-vars/10.access.md), how [.env files](/3.dev/19.env-vars/15.dotenv.md) interact with the dashboard, and the [security trade-offs](/3.dev/19.env-vars/20.security.md) you should know about before storing secrets there.
