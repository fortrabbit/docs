---
reviewed: 2024-08-01 11:58:26
title: CloudFlare
navigation.excerpt: DNS service and DDOS protection
lead: Use CloudFlare with fortrabbit.
sidebar: cloudflare
head:
  meta:
    - name: 'keywords'
      content: 'advanced, CDN, ddos, ssl'
---

## About Cloudflare

Cloudflare is a "magical" multi-purpose website performance & security service, which works at the DNS level. It can be used as a kind of Content Delivery Network and as a protection against Denial Of Service Attacks. It is also a popular choice to get SSL certificates for your domain without the costs and hassle.

## Pricing and signup

There is a free plan with basic features to get you started. [cloudflare.com/plans/](https://www.cloudflare.com/plans?utm_source=fortrabbit). Go to the [sign up page](https://www.cloudflare.com/a/sign-up), enter an email and choose a password.

## Integrating Cloudflare with fortrabbit

There is no technical connection between Cloudflare and fortrabbit. Cloudflare will sit in between your DNS provider and fortrabbit — think of it as a proxy. You will set your nameservers (NS records) to point to Cloudflare.

### Setup Cloudflare

In the following example you first register your domain with your domain provider, then point it to fortrabbit using our standard settings, then Cloudflare will scan the DNS records for you:

1. Make sure to have a domain registered with a domain provider
2. Make sure to have added the domain in the fortrabbit Dashboard
3. Route the domain using our instructions still with your old DNS provider
4. Set up the domain with Cloudflare
5. Cloudflare will scan and use the DNS settings already in place
6. DONE

You might also start with a fresh domain from scratch within Cloudflare. Then Cloudflare will act as your DNS provider. Enter the DNS settings from the fortrabbit Dashboard with Cloudflare.

### Crypto setting

Each domain on Cloudflare comes with a bunch of settings. One is called "Crypto" and is about SSL. Your goal is that the whole communication between the user of your website is encrypted of course. Now, Cloudflare, as described above, is a proxy between your user and fortrabbit. The first lap from the user to Cloudflare is secured by default, but what about the the next one, between Cloudflare and fortrabbit?

```
┌──────┐       ┌────────────┐             ┌────────────┐
│ User ├─HTTPS─▶ Cloudflare ├─ ? HTTPS ? ─▶ fortrabbit │
└──────┘       └────────────┘             └────────────┘
```

Cloudflare is the domain endpoint for the user. Cloudflare itself will actually talk to the App URL. The connection between the App and Cloudflare should also be encrypted.

The App URL has HTTPS, so you can and should set SSL to **full** to ensure end-to-end encryption. The default **flexible** setting is not enough (as we think). "Full (strict)" mode will not work but is not necessary.

## Advanced topics

### Cloudflare DNS and fortrabbit Dashboard Status

Cloudflare is a bit of black box, DNS-wise. When you visit a domain in the fortrabbit Dashboard that is routed via Cloudflare an accurate response is not possible. The Dashboard is aware of many Cloudflare IPs, so it will likely guess that the domain is routed via Cloudflare. But you might still see an error, even if the domain is in fact routed correctly.

### Cloudflare SSL VS Let's Encrypt

Many fortrabbit clients have used Cloudflare to get SSL for their own custom domain, without the need to book and set up a custom cert here. Now, fortrabbit also offers free SSL certificates via (free and zero-config) Let's Encrypt. So if that is your aim, you might not need Cloudflare.

### Cloudflare and 2nd level subdomains

If you see an `SSL_ERROR_NO_CYPHER_OVERLAP` error, but you think you have set up everything correctly, check the domain you are trying to route. Is it a second level of a subdomain like `dev.www.example.com`? If so, further actions might be required: please see the [Cloudflare help](https://support.cloudflare.com/hc/en-us/articles/200170566-Troubleshooting-SSL-errors#h_55e4d315-c60d-4798-9c4c-c75d9baed1b7).

### Other reasons to use Cloudflare

While free SSL has become a commodity, there are other reasons to use Cloudflare:

- Enhanced DDoS protection
- CNAME Flattening for [apex domains](/1.platform/11.concepts/apex-domains.md)
- Domain analytics

### Prevent direct access

You may want to ensure all traffic is routed through Cloudflare. This is important to secure 360 DDoS protection. You'll basically disable the App URL to be accessible. To block direct access and whitelist only Cloudflare's IPs, extend your `.htaccess` file with the following rules:

```
ErrorDocument 403 "Not Allowed"
Deny from all

### Cloudflare IPs ###

Allow from 103.21.244.0/22
Allow from 103.22.200.0/22
Allow from 103.31.4.0/22
Allow from 104.16.0.0/12
Allow from 108.162.192.0/18
Allow from 131.0.72.0/22
Allow from 141.101.64.0/18
Allow from 162.158.0.0/15
Allow from 172.64.0.0/13
Allow from 173.245.48.0/20
Allow from 188.114.96.0/20
Allow from 190.93.240.0/20
Allow from 197.234.240.0/22
Allow from 198.41.128.0/17
Allow from 2400:cb00::/32
Allow from 2405:8100::/32
Allow from 2405:b500::/32
Allow from 2606:4700::/32
Allow from 2803:f800::/32
Allow from 2c0f:f248::/32
Allow from 2a06:98c0::/29
```

As the IP ranges might change from time to time, you should update them on a regular basis.

## Alternatives to Cloudflare

Cloudflare is a magical package of different services all combined and streamlined in a single offering. Mind: by using Cloudflare, you make yourself dependent that this critical component (DNS/NS)) of your infrastructure is working correctly. It's another point of failure that makes your setup more complex. But overall, it's more likely that your website will stay up with Cloudflare enabled. Some of our clients prefer a separation of services. Instead of Cloudflare, they might use dedicated services for DNS/domain and CDN.
