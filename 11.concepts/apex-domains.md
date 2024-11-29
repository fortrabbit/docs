---
reviewed: 2024-11-29 11:57:06
naviTitle: APEX domains
title: APEX domains
navigation.excerpt: Landing directory for public access
lead: APEX domains, also called 'naked domain', 'root domain' or even 'bare domain', have no prefix and look like 'fortrabbit.com'. Learn about APEX domains and how to deal with them at fortrabbit.
hideExamples: yes
figure:
  emoji: 🌐
  text: APEX domains deep dive
links:
  - title: Domain
    route: /objects/domain
    property: docs
head:
  meta:
    - name: 'keywords'
      content: 'TLD, Top Level Domain, top-level-domain, registration, ordering, zone apex, apex domain, root domain, naked domain, subdomain, domain masking, domain name server, DNS, ns, lookup'
---

## APEX routing at fortrabbit

Like with other cloud providers, routing APEX domains directly by IP to environments is not supported. A [forwarding service](#fortrabbit-domain-forwarding) is provided, redirecting all requests to the `www.` domain, including deep-links and https links.

### No CNAME for APEX domains

Although not impossible, APEX domains should really not be routed using a CNAME record. Use an A-Record instead. This is because of [DNS specs](https://www.ietf.org/rfc/rfc1035.txt). Receiving e-mails like `info@fortrabbit.com` would not be possible when DNS entries have CNAME record at the same time. Modern DNS providers support [ANAME/ALIAS records](#alias--aname-routing) for this.

### No direct A-record routing here

A host name is more flexible than an IP. Any domain routed to an IP is bound to that IP. This doesn't give us the flexibility to move app environments around, in case of scaling or incidents, for example with a DDoS attack.

## fortrabbit domain forwarding

The fortrabbit domain forwarding service redirects all incoming requests on the bare domain to the `www.` version of the domain using `301 Moved Permanently` headers. It also works for deeplinks, so `http://your-domain.com/page` will be forwarded to `http://www.your-domain.com/page`. A custom SSL cert for each bare domain will be issued, so that ALL communication can be secure (best combined with [.htaccess](/htaccess) rules on the `www.` side to force https). It needs to be set up as an `A`-record, you can not use `CNAME` on a bare domain, as that would possibly break your DNS settings (especially if you want to send e-mails). The service itself is independent from the App; it's the same IP for all Apps in one region.

### Recommendations using the redirect service

- Use `www.domain.tld` instead of just `domain.tld` in all links
- Configure your CMS to use the <www>. subdomain for all links (e.g. `site_url`)
- Send your external traffic (e.g. advertisement clicks) to the <www>. domain
- Configure your uptime checks with A URL to the the <www.domain.tld/foobar>
- Setup the redirect within CloudFlare if you are using it

In general you can expect our redirect service to work. However, in case of a redirect service outage if all or your links depend on it - by pointing to `https://naked.domain/foobar` instead of `https://www.naked.domain/foobarz` - your whole website will stop working.

Even more importantly, requesting a resource via the redirect service forces an additional http-redirect making your website function slower. For SEO purposes, keep in mind that all redirects on the redirect service are marked as 301 (moved permanently). That way search engines will pick up the <www>. subdomain as the primary address or URL for the website.

## Our opinion on APEX domains

Some think that the minimal look of an APEX domain is aesthetically more pleasing than their subdomain counterparts. But as described above, APEX domains don't play well with flexible host name routing. Big players like Google use a `www.` subdomain without you noticing, and most bigger sites do the same. Safari and Chrome don't show the `www.` prefix in the address bar anymore. Firefox greys out the protocol of this trivial domain. The `www.` prefix is so common, you hardly recognize it. Some people think, moving from bare to `www.` will impact SEO negatively. This should not be the case if done properly, as long as the APEX domain will forward all requests.

## Alternatives

You don't have to use our free domain forwarding service, here are some alternative options:

### ALIAS / ANAME routing

In the fortrabbit Dashboard you can add a bare domain. To make this work you need a domain provider that supports so called "ALIAS" or "ANAME" records. They allow you to have the functionality of CNAME routing (hostname target instead of IP). This is a list of domain / DNS providers who offer these special records:

- [AWS Route53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosing-alias-non-alias.html)
- [Cloudflare: CNAME flattening](https://developers.cloudflare.com/dns/cname-flattening/), also see [Cloudflare integration](/13.integrations/cloudflare.md)
- [DNS made easy: ANAME records](https://support.dnsmadeeasy.com/support/solutions/articles/47001001412-aname-records)
- [DNSimple: ALIAS records](https://support.dnsimple.com/articles/alias-record/)
- [Dreamhost: Custom DNS records](https://help.dreamhost.com/hc/en-us/articles/360035516812-Adding-custom-DNS-records)
- [Easy DNS: ANAME records](https://kb.easydns.com/knowledge/aname-records/)
- [Google domains: ALIAS records](https://cloud.google.com/dns/docs/records-overview#alias-records)
- [Namecheap: ALIAS records](https://www.namecheap.com/support/knowledgebase/article.aspx/10128/2237/how-to-create-an-alias-record/)
- [Porkbun: ALIAS records](https://kb.porkbun.com/article/68-how-to-edit-dns-records)

As far as we know, by the time of this writing, the following providers do not support ANAME records:

- GoDaddy - see [this SO question](https://webmasters.stackexchange.com/questions/141075/aname-record-not-accepted)

If your provider does not support CNAME flattening, but you would like to take advantage of it, we recommend switching to that does.

### Forwarding, using your domain provider

Almost all domain providers also support a simple HTTP redirect. Please see your domain provider's documentation.
