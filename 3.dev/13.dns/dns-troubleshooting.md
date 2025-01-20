---
reviewed: 2024-08-09 09:50:04
title: DNS and domain troubleshooting
naviTitle: DNS troubleshooting
navigation.excerpt: Solving domain routing issues.
lead: Solving common DNS problems when connecting an external domain to fortrabbit.
links:
  - title: Domain intro
    route: /objects/domain
    property: docs
  - title: External domains
    route: /dns/external-domains
    property: docs
---

## Common issues

Here are the most common reasons why domain routing is not working. Start with this list first.

### Wrong DNS settings

Most domain issues are related to wrong DNS settings. Carefully check if your actual target DNS settings match the desired DNS settings. It's possible that you have additional contradicting rules.

### Time delays

Many domain providers default to a long TTL (Time To Live). The TTL value is in seconds. Often it's 3600 meaning one hour. The TTL caching itself is actually a good thing as it helps to reduce round trips. Most domain providers let you set down the TTL, which is very useful to do before moving domains. See below on how to query the current DNS settings.

### Internal routing issues

When you see a 404 - file not found error after the domain is correctly via DNS and ending up at fortrabbit, then most likely your code configuration is not setup to receive traffic for the domain. This can be a wrong root path setting, or a siteUrl setting that is wrong. Also check our [404 tips](/3.dev/http-errors/404.md).

### No DNS settings

Depending on your browser you might see a _DNS_PROBE_FINISHED_NXDOMAIN_ or _This site can't be reached_ or _This webpage is not available_ error. In such cases, it is likely that the domain is not registered or there are no DNS settings for that domain. You need to fix that with your domain provider.

### Certificate errors

Once a domain is correctly routed, the [TLS certificate](/3.dev/13.dns/4.https.md) needs to be installed. This takes some additional time in which requests to the https version of the website will display a certificate warning in the browser. This is actually not a DNS issue, see the [HTTPS troubleshooting guide](/3.dev/https-troubleshooting.md).

### No domain configured with fortrabbit

Sometimes people forget to register and configure the domain with fortrabbit. Check if the domain is correctly setup with fortrabbit as well.

## Debugging DNS issues

The following tips can help you to verify DNS settings for your domain. This is useful especially with time delays and wrong DNS settings.

### Use the dashboard as a guidance

When visiting your external domain within the [dashboard](/1.platform/11.concepts/dashboard.md), you'll see the desired and the currently active DNS values for the domain. Those two settings should match.

### Use dig to verify current DNS values

You can verify DNS settings with the [dig command](/3.dev/dig.md).

### Use a DNS checker website

You can also use DNS test websites to rule out caching, those can query your DNS entries from different locations at once.
