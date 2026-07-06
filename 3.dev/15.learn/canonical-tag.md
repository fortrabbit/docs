---
reviewed: 2026-07-06
reviewer: fl
naviTitle: Canonical tag
title: Using a canonical tag
navigation.excerpt: Landing directory for public access
lead: A canonical tag tells search engines which version of a page is the preferred one when you have multiple domains or URLs serving the same content. Use the rel="canonical" link element in your HTML head to consolidate indexing signals.
hideExamples: yes
figure:
  emoji: ⚔️
  text: There can only be one.
links:
  - title: Domain
    route: /platform/objects/domain
    property: docs
head:
  meta:
    - name: 'keywords'
      content: 'canonical tag, canonical URL, duplicate content, rel=canonical, search engine optimization, SEO, fortrabbit'
---

## Handling duplicate content with canonical tags

A canonical tag is a link element in your HTML that specifies the preferred URL when you have multiple domains or pages with identical content. Search engines use this signal to consolidate duplicate content and avoid diluting your SEO ranking across multiple versions.

Suppose you have `fortrabbit.com` and `fort-rabbit.com` registered, and both display the same content. You want to keep both URLs active but tell search engines that `fortrabbit.com` is the authoritative version. Instead of creating a [redirect](/3.dev/21.htaccess/02.redirects.md) (which might break existing links), you can add a canonical tag to the head of every HTML page:

```html
<head>
  …
  <link
    rel="canonical"
    href="https://www.fortrabbit.com"
  />
</head>
```

This approach is gentler than redirects when you need [multiple domains serving the same environment](/1.platform/13.dns/02.external-domains.md). For more technical details, see [Google's guide to canonical URLs](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).
