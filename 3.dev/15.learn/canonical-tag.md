---
reviewed: 2024-11-29 11:57:06
naviTitle: Canonical tag
title: Using a canonical tag
navigation.excerpt: Landing directory for public access
lead: In the cases above you forward all requests to the ONE main domain you are using. In some cases you might have two domains serving the same content. Now, search engines need to know which page is the one they should show the results for. To help the search bots, you can use a canonical tag.
hideExamples: yes
figure:
  emoji: 🌐
  text: Apex domains deep dive
links:
  - title: Domain
    route: /objects/domain
    property: docs
head:
  meta:
    - name: 'keywords'
      content: 'TLD, Top Level Domain, top-level-domain, registration, ordering, zone apex, apex domain, root domain, naked domain, subdomain, domain masking, domain name server, DNS, ns, lookup'
---

Let's say you have the page `fortrabbit.com` and `fort-rabbit.com` registered. And you want both to display the same content but still keep the originally entered URL. Actually, for this example you might want to create a redirect to the domain that matters most to you, but whatever. Now you want the search engines to prefer and link to the first domain, so you add in the head of each HTML page delivered:

```html
<head>
  …
  <link
    rel="canonical"
    href="https://www.fortrabbit.com"
  />
</head>
```

More on [canonical URLs on Google webmasters](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls)
