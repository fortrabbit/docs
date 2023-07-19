---

reviewed:      2023-07-08 14:42:47
title:         HTTPS
excerpt:       All about HTTPS and TLS on fortrabbit
lead:          Criminals and government agencies are trying to read your Apps communication. Better serve all requests over HTTPS for extended privacy. 
status:        todo

keywords:
  - ssl
  - TLS
  - domain
  - subdomain
  - CA
  - Certificate Authority
  - port 443
  - port 80

---

**TLDR;** Free and zero-config SSL certificates for all domains are provided, nothing you have to take care of. Read on if you want to learn about advanced options.

## About HTTPS, TLS & SSL

`HTTPS` is **H**yper **T**ext **T**ransfer **P**rotocol over Transport Layer **S**ecurity. It is used to secure the data transport between a client (browser) and a server. HTTPS is based on **TLS** (Transport Layer Security), which is the successor to the still better known **SSL** (Secure Sockets Layer).

Current browsers show a green lock in the address bar if the connection is over HTTPS, the certificate could be verified and if the certificate is still valid. Google is promoting "https everywhere" (snakeoil), your SEO pagerank might benefit from using HTTPS.

## HTTPS options on fortrabbit

As part of [security efforts](https://www.fortrabbit.com/security) our aim is to give you secure, still easy-to-use and affordable options. Available with all Apps on fortrabbit:

### 1. Piggyback HTTPS

That's the most easiest and most obvious way to quickly run your App on https. You can already access your [App URL](app#toc-app-url) using HTTPS. For example: `https://{{app-name}}.frb.io`. Use this URL for testing or if a custom domain is not important to you.

### 2. Automatic HTTPS

[Let's Encrypt](https://en.wikipedia.org/wiki/Let's_Encrypt) is a free certificate authority and can be used to generate free certificates for custom domains. The Automatic HTTPS feature is included for all fortrabbit Apps: All domains correctly added and routed will receive an SSL certificate by Let's Encrypt, no configuration or extra setup required. The certs will also be renewed automatically. This option does not work for wildcard domains (yet).

## Using TLS/HTTPS

The following practical tips on how to deal with HTTPS are applying to all TLS options on fortrabbit:

### Redirect all requests to HTTPS

It is recommended to forward all requests to the secure line, so no more "http://", only "http**s**://". See [an example here](/htaccess#toc-redirect-all-requests-to-https).

### Secure your domain with a CAA record

A Certification Authority Authorization (CAA) is a DNS record to specify which certificate authorities (CAs) are allowed to issue certificates for a domain. It's an extra security layer, so that now one else can intercept any certificates by wrong authorities. There is no integration here on fortrabbit needed. See if your DNS / domain provider supports CAA entries, set the according identifying domain name. When you are using our free Let's Encrypt certs, see [this article](https://letsencrypt.org/docs/caa/) on how to set it up. Mind that already existing CAA entries can also become a problem when trying to issue new certificates.

## Troubleshooting TLS

Sometimes it just doesn't work as supposed to. Don't panic. You can of course always ask us for support. [Here](/tls-errors) are some things you can do on your own.
