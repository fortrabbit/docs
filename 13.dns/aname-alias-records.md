---
reviewed: 2024-11-29 11:57:06
naviTitle: ANAME/ALIAS records
title: ANAME / APEX records
navigation.excerpt: Serve APEX domains with fortrabbit
lead: To serve APEX domain directly with fortrabbit you need a domain provider that supports so called ALIAS or ANAME records.
hideExamples: yes
links:
  - title: Domain intro
    route: /objects/domain
    property: docs
  - title: External domains
    route: /dns/external-domains
    property: docs
  - title: APEX domains
    route: /dns/apex-domains
    property: docs
  - title: WWW forwarding
    route: /dns/www-forwarding
    property: docs
---

The functionality is also called CNAME flattening (the hostname target is resolved to the IP). More and more [domain / dns providers](/14.integrations/10.domain-providers.md) are supporting ANAME / ALIAS records:

- [AWS Route53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosing-alias-non-alias.html)
- [Cloudflare: CNAME flattening](https://developers.cloudflare.com/dns/cname-flattening/), also see [Cloudflare integration](/14.integrations/cloudflare.md)
- [DNS made easy: ANAME records](https://support.dnsmadeeasy.com/support/solutions/articles/47001001412-aname-records)
- [DNSimple: ALIAS records](https://support.dnsimple.com/articles/alias-record/)
- [Dreamhost: Custom DNS records](https://help.dreamhost.com/hc/en-us/articles/360035516812-Adding-custom-DNS-records)
- [Easy DNS: ANAME records](https://kb.easydns.com/knowledge/aname-records/)
- [Google domains: ALIAS records](https://cloud.google.com/dns/docs/records-overview#alias-records)
- [Namecheap: ALIAS records](https://www.namecheap.com/support/knowledgebase/article.aspx/10128/2237/how-to-create-an-alias-record/)
- [Porkbun: ALIAS records](https://kb.porkbun.com/article/68-how-to-edit-dns-records)

As far as we know, by the time of this writing, the following providers do not support ANAME records:

- GoDaddy - see [this SO question](https://webmasters.stackexchange.com/questions/141075/aname-record-not-accepted) ☠️

If your provider does not support CNAME flattening, but you would like to take advantage of it, we recommend switching to that does or consider using our [www forwarding service](/11.concepts/www-forwarding.md).
