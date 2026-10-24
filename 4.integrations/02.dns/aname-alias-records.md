---
created: 2024-11-29
updated: 2026-10-24
reviewed: 2026-10-24
reviewer: fl
naviTitle: ANAME / ALIAS records
title: ANAME / ALIAS records
description: 'ANAME and ALIAS records give apex domains CNAME-like behavior. For fortrabbit the WWW forwarding service is currently the better route.'
navigation.excerpt: Serve apex domains via host target
lead: ANAME and ALIAS records, also called CNAME flattening, point an apex domain such as example.com to a host name. fortrabbit recommends its www forwarding service for apex domains instead.
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
    route: /platform/domains/external-domains
    property: docs
  - title: Apex domains
    route: /platform/domains/apex-domains
    property: docs
  - title: WWW forwarding
    route: /platform/domains/domain-forwarding-service
    property: docs
topics:
  - dns
  - https
---

::CallOut{alert}
fortrabbit recommends the [www forwarding service](/1.platform/13.domains/05.domain-forwarding-service.md) for apex domains, not ANAME or ALIAS records.
::

## Domain providers with ANAME support

These providers support ANAME or ALIAS records, see also the [domain providers](/4.integrations/02.dns/02.providers.md):

- [AWS Route53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosing-alias-non-alias.html)
- [Cloudflare: CNAME flattening](https://developers.cloudflare.com/dns/cname-flattening), also see [Cloudflare integration](/4.integrations/02.dns/05.cloudflare.md)
- [DNS made easy: ANAME records](https://support.dnsmadeeasy.com/hc/en-us/articles/34327231731227-What-is-an-ANAME-Record)
- [DNSimple: ALIAS records](https://support.dnsimple.com/articles/alias-record)
- [Dreamhost: Custom DNS records](https://help.dreamhost.com/hc/en-us/articles/360035516812-Adding-custom-DNS-records)
- [Easy DNS: ANAME records](https://kb.easydns.com/knowledge/aname-records)
- [Google Cloud DNS: ALIAS records](https://cloud.google.com/dns/docs/records-overview#alias-records)
- [Namecheap: ALIAS records](https://www.namecheap.com/support/knowledgebase/article.aspx/10128/2237/how-to-create-an-alias-record)
- [Porkbun: ALIAS records](https://kb.porkbun.com/article/68-how-to-edit-dns-records)

GoDaddy does not support ANAME records, see [this question on Webmasters Stack Exchange](https://webmasters.stackexchange.com/questions/141075/aname-record-not-accepted).
