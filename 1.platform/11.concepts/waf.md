---
reviewed: 2024-11-24 18:45:10
title: Web application firewall
naviTitle: WAF
beta: true
navigation.excerpt: Protect against common attacks and harmful requests
lead: Bots and crawlers scan your website for vulnerabilities and content. Keep out the bad actors.
---

::CallOut{alert}
This feature implementation is currently in testing. See [quirks](#quirks).
::

Even unsuccessful requests do harm by consuming hosting resources and spamming logs. This can be bad for performance and consumes unnecessary energy. Specifically AI bots that ignore `robots.txt` can hammer websites considerably.

### Implementation

The current WAF implementation is a 'poor mans WAF'. [nG Firewall](https://perishablepress.com/ng-firewall/) by Perishable Press is used. It blocks out bad requests and most bad bots on the web server level by using a standard set of .htaccess rules.

## Usage

We provide an easy to use interface to turn on/off a WAF. Visit the PHP settings of the app environment to enable or disable the setting.

:BlockLink{title="Set WAF for {{app-env-id}}" path="/environments/{{app-env-id}}/settings/firewall-incoming"}

## Quirks

Bots are a major problem. The current solution provided is in testing while we are also exploring alternative approaches.

### Possible performance impacts

We are testing performance impacts. While this keeps the Apache more busy with each request, fewer requests will reach the PHP engine.

### Chicken egg problems

The firewall should only be activated after a software has been installed. An active WAF setting may prevent software to be installed.

## Alternatives

There are plenty of alternatives to using the WAF setting.

### Create your own .htaccess

There are rules which may be specific to your use case but which are not necessarily required for everyone. Use an `.htaccess` file to write your own rules. See our [htaccess section](/3.dev/htaccess/) for more.

### Use an external service

Some DNS infrastructure providers offer 'bot control' services where bad traffic will be filtered before it even reaches the web server.

- [Cloudflare bot management](https://www.cloudflare.com/application-services/products/bot-management/)
- [AWS WAF Bot control](https://aws.amazon.com/waf/features/bot-control/)
