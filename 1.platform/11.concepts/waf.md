---
reviewed: 2024-11-24 18:45:10
title: Web Application Firewall BETA
naviTitle: WAF
beta: true
navigation.excerpt: 'Incoming firewall: Protection against common attacks and harmful requests'
lead: Bots and crawlers scan your website for vulnerabilities and content. Keep out the bad actors.
---

Even unsuccessful requests do harm by consuming hosting resources and spamming logs. This can be bad for performance and consumes unnecessary energy. By default the "WAF" setting is enabled for each app environment. This can disable in the dashboard.

We use [nG Firewall](https://perishablepress.com/ng-firewall/) by Perishable Press. It blocks out bad requests and most bad bots.

The feature is currently in BETA testing. We are testing performance impacts. While this keeps the Apache more busy with each request, fewer requests will reach the PHP engine.

There are rules which may be specific to your use case but which are not necessarily required for everyone. Use an `.htaccess` file to write your own rules. See our [htaccess section](/15.tips/htaccess/) for more.
