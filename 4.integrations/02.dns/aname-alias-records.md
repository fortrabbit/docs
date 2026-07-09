---
reviewed: 2026-07-09
reviewer: fl
naviTitle: ANAME / ALIAS records
title: ANAME / ALIAS records
navigation.excerpt: Serve apex domains via host target
lead: ANAME and ALIAS records allow you to serve apex domains with CNAME-like functionality, also known as CNAME flattening.
hideExamples: yes
head:
  meta:
    - name: keywords
      content: ANAME records, ALIAS records, CNAME flattening, apex domain, DNS, fortrabbit
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
    route: /platform/dns/domain-forwarding-service
    property: docs
---

::CallOut{alert}
Due to potential upcoming changes, we recommend using the [WWW forwarding service](/1.platform/13.dns/04.domain-forwarding-service.md) instead of ANAME/ALIAS records with our service at this time.
::

## Domain providers with ANAME support

Many domain providers now support ANAME / ALIAS records. See our [DNS provider intro](/4.integrations/02.dns/01.intro.md) for an overview:

- [AWS Route53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosing-alias-non-alias.html)
- [Cloudflare: CNAME flattening](https://developers.cloudflare.com/dns/cname-flattening), also see [Cloudflare integration](/4.integrations/02.dns/05.cloudflare.md)
- [DNS made easy: ANAME records](https://support.dnsmadeeasy.com/hc/en-us/articles/34327231731227-What-is-an-ANAME-Record)
- [DNSimple: ALIAS records](https://support.dnsimple.com/articles/alias-record)
- [Dreamhost: Custom DNS records](https://help.dreamhost.com/hc/en-us/articles/360035516812-Adding-custom-DNS-records)
- [Easy DNS: ANAME records](https://kb.easydns.com/knowledge/aname-records)
- [Google domains: ALIAS records](https://cloud.google.com/dns/docs/records-overview#alias-records)
- [Namecheap: ALIAS records](https://www.namecheap.com/support/knowledgebase/article.aspx/10128/2237/how-to-create-an-alias-record)
- [Porkbun: ALIAS records](https://kb.porkbun.com/article/68-how-to-edit-dns-records)

As we know, the following providers do not support ANAME records:

- GoDaddy - see [this SO question](https://webmasters.stackexchange.com/questions/141075/aname-record-not-accepted) ☠️

If your provider does not support CNAME flattening, we recommend switching to one that does or consider using our [www forwarding service](/1.platform/13.dns/04.domain-forwarding-service.md).
