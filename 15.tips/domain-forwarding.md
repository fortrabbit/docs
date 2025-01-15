---
reviewed: 2024-08-09 10:05:26
title: Forwarding domains
naviTitle: Forwarding domains
navigation.excerpt: Redirect one domain to another
lead: Redirect one domain to another. Here are your options.
head:
  meta:
    - name: 'keywords'
      content: 'TLD, Top Level Domain, top-level-domain, registrastion, ordering, zone apex, apex domain, root domain, subdomain, domain masking, domain name server, DNS, ns, lookup'
---

Let's say you have `your-domain.com` pointed to your app environment already. Now that other TLD, the domain `your-domain.co.uk` is registered as well. You want your app environment to show up under this domain as well. Now there are two main ways how this can be implemented:

1. `your-domain.co.uk/pricing` will forward to `your-domain.com/pricing`
2. `your-domain.co.uk/pricing` and `your-domain.com/pricing` will both show the same content

What you want, in most scenarios, is the first one: forwarding. Serving the same content under multiple domains is confusing — not only for humans but also for bots: The SEO spider bot might down-rank your content as a duplicate. You want a primary domain — one canonical name.

### Forwarding domains with your domain provider

You can forward one domain to another domain without any involvement of fortrabbit at all. Please check your domain provider to see if forwarding is allowed. The configuration should be dead simple. You point one domain to another and that's it.

- Do: forward using a HTTP `301 Moved Permanently` code.
- Don't: use a "masked forward" where the other domain is loaded into an iframe

Please keep an eye on HTTPS when forwarding. HTTPS will most likely not be provided by your domain provider. In most cases this is not issue.

### Forwarding domains within your app environment

You might also do the forwarding programmatically within your App. The most common approach here is to work with `.htaccess` rules to redirect all requests to that other domain. You register each domain within the fortrabbit dashboard and then catch all the requests with your code and config.
