---
reviewed:  2023-08-30 08:09:43
title:     Web Application Firewall
excerpt:   'Incoming firewall: Protection against common attacks and harmful requests'
lead:      Bots and crawlers scan your website for vulnerabilities and content. Even unsuccessful requests do harm by consuming hosting resources and spamming logs.
---

By default "WAF" are enabled; you can disable them in the Dashboard.

### Blocked files

* common dotfiles
* autodiscover.xml
* wallet.dat
* wlwmanifest.xml
* xmlrpc.php

### Blocked file extensions

* .asp
* .aspx
* .cgi
* .sql
* .swf

## Write your own rules using .htaccess

Intentionally we don't block every possible attack we've seen in the past. There are rules which may be specific to your use case but which are not necessarily required for everyone. Use an `.htaccess` file to write your own rules.

See our [htaccess](/#htaccess) section for more.
