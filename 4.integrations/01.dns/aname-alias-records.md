---
reviewed: 2024-12-05 11:28:02
naviTitle: ANAME / ALIAS records
title: ANAME / ALIAS records
navigation.excerpt: Serve apex domains via host target
lead: To serve apex domain directly some domain providers allow ALIAS or ANAME records to resolve host names to IPs. It is sometimes called CNAME flattening. The host name is resolved to an IP.
hideExamples: yes
links:
  - title: Domain intro
    route: /platform/objects/domain
    property: docs
  - title: External domains
    route: /platform/dns/external-domains
    property: docs
  - title: Apex domains
    route: /platform/dns/apex-domains
    property: docs
  - title: WWW forwarding
    route: /platform/dns/domain-forwarding
    property: docs
---

::CallOut{alert}
Due to potential upcoming changes, we recommend using the [WWW forwarding service](/1.platform/13.dns/5.domain-forwarding-service.md) instead of ANAME/ALIAS records with our service at this time.
::

## Domain providers with ANAME support

More and more [domain / dns providers](/4.integrations/01.dns/01.intro.md) are supporting ANAME / ALIAS records:

- [AWS Route53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosing-alias-non-alias.html)
- [Cloudflare: CNAME flattening](https://developers.cloudflare.com/dns/cname-flattening), also see [Cloudflare integration](/4.integrations/01.dns/05.cloudflare.md)
- [DNS made easy: ANAME records](https://support.dnsmadeeasy.com/support/solutions/articles/47001001412-aname-records)
- [DNSimple: ALIAS records](https://support.dnsimple.com/articles/alias-record)
- [Dreamhost: Custom DNS records](https://help.dreamhost.com/hc/en-us/articles/360035516812-Adding-custom-DNS-records)
- [Easy DNS: ANAME records](https://kb.easydns.com/knowledge/aname-records)
- [Google domains: ALIAS records](https://cloud.google.com/dns/docs/records-overview#alias-records)
- [Namecheap: ALIAS records](https://www.namecheap.com/support/knowledgebase/article.aspx/10128/2237/how-to-create-an-alias-record)
- [Porkbun: ALIAS records](https://kb.porkbun.com/article/68-how-to-edit-dns-records)

As far as we know, by the time of this writing, the following providers do not support ANAME records:

- GoDaddy - see [this SO question](https://webmasters.stackexchange.com/questions/141075/aname-record-not-accepted) ☠️

If your provider does not support CNAME flattening, but you would like to take advantage of it, we recommend switching to that does or consider using our [www forwarding service](/1.platform/13.dns/5.domain-forwarding-service.md).
