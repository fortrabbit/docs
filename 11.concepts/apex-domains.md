---
reviewed: 2024-11-29 11:57:06
naviTitle: APEX domains
title: APEX domains
navigation.excerpt: Naked, bare, root domains
lead: APEX domains, also called 'naked domain', 'root domain' or even 'bare domain', have no prefix and look like 'fortrabbit.com'.
hideExamples: yes
# figure:
#   emoji: 🌐
#   text: APEX domains deep dive
links:
  - title: Domain
    route: /objects/domain
    property: docs
  - title: ANAME / ALIAS records
    route: /tips/aname-alias-records
    property: docs
head:
  meta:
    - name: 'keywords'
      content: 'TLD, Top Level Domain, top-level-domain, registration, ordering, zone apex, apex domain, root domain, naked domain, subdomain, domain masking, domain name server, DNS, ns, lookup'
---

## APEX routing at fortrabbit

Direct routing of APEX domains to environments is not supported at fortrabbit. You can:

- Use a www domain, the [www forwarding service](/11.concepts/www-forwarding.md) will redirect all requests
- Use a DNS provider that supports [ALIAS / ANAME records](/14.tips/aname-alias-records.md)

### No CNAME for APEX domains

Although not impossible, APEX domains should really not be routed using a CNAME record. Use an A-Record instead. This is because of [DNS specs](https://www.ietf.org/rfc/rfc1035.txt). Receiving e-mails like `info@fortrabbit.com` would not be possible when DNS entries have CNAME record at the same time. Modern DNS providers support [ANAME/ALIAS records](#alias--aname-routing) for this.

### No direct A-record routing here

A host name is more flexible than an IP. Any domain routed to an IP is bound to that IP. This doesn't give us the flexibility to move app environments around, in case of scaling or incidents, for example with a DDoS attack.

## Our opinion on APEX domains

Some think that the minimal look of an APEX domain is aesthetically more pleasing than their subdomain counterparts. But as described above, APEX domains don't play well with flexible host name routing. Big players like Google use a `www.` subdomain without you noticing, and most bigger sites do the same. Safari and Chrome don't show the `www.` prefix in the address bar anymore. Firefox greys out the protocol of this trivial domain. The `www.` prefix is so common, you hardly recognize it. Some people think, moving from bare to `www.` will impact SEO negatively. This should not be the case if done properly, as long as the APEX domain will forward all requests.
