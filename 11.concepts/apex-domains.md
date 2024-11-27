---
reviewed: 2024-11-27 08:56:51
naviTitle: APEX domains
title: APEX domains and www forwarding
navigation.excerpt: Landing directory for public access
lead: How to configure the naked domain for forwarding and how the redirect service works.
hideExamples: yes
links:
  - title: Domain
    route: /objects/domain
    property: docs
head:
  meta:
    - name: 'keywords'
      content: 'TLD, Top Level Domain, top-level-domain, registration, ordering, zone apex, apex domain, root domain, naked domain, subdomain, domain masking, domain name server, DNS, ns, lookup'
---

APEX domains are also called "naked domain", "APEX domain" or "root domain. They have no prefix and look like so: `fortrabbit.com`. Some think that they are aesthetically more pleasing than their subdomain counterparts. But they don't play well with flexible host name routing.

APEX domains should not be routed using a `CNAME` record; they should be routed using an `A`-Record. This is because of the specifications of DNS. You may want to have e-mails with your domain like `info@fortrabbit.com`, it is not possible to have with a CNAME record at the same time. Any domain routed to an IP is bound to that IP. This doesn't give us the flexibility to move your App around in case of incidents, for example with a DDoS attack.

### Our opinion about APEX domains

Bare domains may look pleasing, but don't take this too seriously. Big players like Google use a `www.` subdomain without you noticing, and most bigger sites do the same. Safari and Chrome don't show the `www.` prefix in the address bar anymore. Firefox greys out the protocol of this trivial domain. The `www.` prefix is so common, you hardly recognize it.

We provide a forwarding service so that all requests on the APEX domain will get forwarded to the `www.` domain, including deep-links and https links. So you can still print the bare domain on flyers or in your email signature.

Sometimes, moving from bare to `www.` is thought to impact SEO negatively. This should not be the case if done properly. As long as the APEX domain works and forwards all requests, don't worry too much.

If your boss insists, use an external DNS provider that supports CNAME flattening (sometimes called ANAME).

### Practices to avoid for APEX domains

**Use the IP of the environment**: You could grab the IP of your app environment and use that as an `A`-record for your domain. It's technically possible, but then your App will be offline once we move it to a another Node (which changes the IP address).

**Just use the CNAME with the APEX domain**: It's theoretically possible, but not recommended by the [DNS specs](http://www.ietf.org/rfc/rfc1035.txt), and would also break any e-mail delivery for your domain.

## Domain forwarding service explained

Optional but highly recommended: The fortrabbit domain forwarding service redirects all incoming requests on the bare domain to the `www.` version of the domain using `301 Moved Permanently` headers. It also works for deeplinks, so `http://your-domain.com/page` will be forwarded to `http://www.your-domain.com/page`. A custom SSL cert for each bare domain will be issued, so that ALL communication can be secure (best combined with [.htaccess](/htaccess) rules on the `www.` side to force https). It needs to be set up as an `A`-record, you can not use `CNAME` on a bare domain, as that would possibly break your DNS settings (especially if you want to send e-mails). The service itself is independent from the App; it's the same IP for all Apps in one region.

### Recommendations for our redirect service

- Use `www.domain.tld` instead of just `domain.tld` in all links
- Configure your CMS to use the <www>. subdomain for all links (e.g. `site_url`)
- Send your external traffic (e.g. advertisement clicks) to the <www>. domain
- Configure your uptime checks with A URL to the the <www.domain.tld/foobar>
- Setup the redirect within CloudFlare if you are using it

In general you can expect our redirect service to work. However, in case of a redirect service outage if all or your links depend on it - by pointing to `http://naked.domain/foobar` instead of `http://www.naked.domain/foobarz` - your whole website will stop working.

Even more importantly, requesting a resource via the redirect service forces an additional http-redirect making your website function slower. For SEO purposes, keep in mind that all redirects on the redirect service are marked as 301 (moved permanently). That way search engines will pick up the <www>. subdomain as the primary address or URL for the website.

## Alternative ways to use a APEX domain

You don't have to use our free domain forwarding service, here are some alternative options:

### ALIAS / ANAME routing

In the fortrabbit Dashboard you can add a bare domain. To make this work you need a domain provider that supports so called "ALIAS" or "ANAME" records. They allow you to have the functionality of CNAME routing (hostname target instead of IP). This is a list of domain / DNS providers who offer these special records:

- **[DNSimple: ALIAS records](https://support.dnsimple.com/articles/alias-record/)**
- [DNS made easy: ANAME records](http://help.dnsmadeeasy.com/managed-dns/records/aname-records/)
- [Easy DNS: ANAME records](https://fusion.easydns.com/index.php?/Knowledgebase/Article/View/190/7/aname-records/)

### Forwarding, using your domain provider

Some domain providers also support a simple HTTP redirect. Please see your domain provider's documentation. Here are some examples:

- [GoDaddy: domain forwarding](https://support.godaddy.com/help/article/422/manually-forwarding-or-masking-your-domain-name)
- [Gandi: domain forwarding](https://wiki.gandi.net/en/domains/management/domain-as-website/forwarding)
- [1&1: domain forwarding](http://help.1and1.com/domains-c36931/manage-domains-c79822/domain-destination-c38672redirectforward-your-domain-a594868.html)

## Using a canonical tag

In the cases above you forward all requests to the ONE main domain you are using. In some cases you might have two domains serving the same content. Now, search engines need to know which page is the one they should show the results for. To help the search bots, you can use a canonical tag.

Let's say you have the page `fortrabbit.com` and `fort-rabbit.com` registered with your fortrabbit App. And you want both to display the same content but still keep the originally entered URL. _Actually, for this example you might want to create a redirect to the domain that matters most to you._ Now you want the search engines to prefer and link to the first domain, so you add in the head of each HTML page delivered:

```html
<head>
  …
  <link
    rel="canonical"
    href="https://www.fortrabbit.com"
  />
</head>
```

More on [canonical URLs on Google webmasters](https://support.google.com/webmasters/answer/139066?hl=en)
