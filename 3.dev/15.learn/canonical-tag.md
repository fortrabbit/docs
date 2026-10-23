---
created: 2024-11-29
updated: 2026-10-23
reviewed: 2026-10-23
reviewer: fl
naviTitle: Canonical tag
title: Using a canonical tag
description: 'A canonical tag tells search engines which URL is the preferred one when several domains serve the same content — useful next to a default domain.'
navigation.excerpt: Landing directory for public access
lead: A canonical tag in the HTML head names the preferred URL of a page that is reachable under several URLs or domains. Search engines index that URL.
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
topics:
  - frontend
  - http
---

## Canonical tags

A canonical tag names the preferred URL of a page that is reachable under several URLs. Search engines then rank that URL and treat the others as duplicates. Add it to the `<head>` of every page:

```html
<link rel="canonical" href="https://www.example.com/current-page" />
```

The `href` is the full URL of the page itself on the preferred domain, not the home page. Most CMS and SEO plugins generate the tag.

## Canonical tag or redirect

With two domains serving the same content, such as `example.com` and `example.net` on one [environment](/1.platform/13.domains/03.external-domains.md), both work:

- A [redirect](/3.dev/21.htaccess/02.redirects.md) sends visitors and search engines to the preferred domain. Use it when the second domain needs no own visitors.
- A canonical tag keeps both domains reachable and only tells search engines which one to index.

See [Google on canonical URLs](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).
