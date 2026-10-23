---
updated: 2026-10-23
reviewed: 2026-10-23
reviewer: fl
title: HTTPS troubleshooting
description: 'Certificate errors in the browser, explained: how to read the certificate details and fix TLS problems on domains hosted at fortrabbit.'
naviTitle: HTTPS troubleshooting
navigation.excerpt: Debugging SSL/TLS errors
figure:
  emoji: 🔒
  text: Debug SSL certificate issues.
  color: rgb(34, 197, 94)
  textColor: rgb(220, 252, 231)
lead: A certificate warning on fortrabbit usually means the domain does not point to fortrabbit yet. A mixed content warning means the page loads resources over http.
head:
  meta:
    - name: keywords
      content: 'HTTPS certificate error, SSL/TLS troubleshooting, certificate warning, mixed content, fortrabbit'
topics:
  - https
  - troubleshooting
---

## Check the certificate in the browser

Open the domain with `https://`, click the lock icon or the site settings icon in the address bar, and open the certificate details. They show which domains the certificate covers and when it expires. See [HTTPS](/1.platform/13.domains/06.https.md) for how certificates work on fortrabbit.

## Certificate warning

A warning such as `NET::ERR_CERT_COMMON_NAME_INVALID` means the certificate does not cover the domain, often because it shows `*.frbit.app` instead.

- **DNS not pointing to fortrabbit yet**: fortrabbit issues a certificate only for a domain routed to it. Check the [domain](/1.platform/10.objects/10.domain.md) in the dashboard and the DNS with [dig](/3.dev/15.learn/dig.md).
- **New domain**: the certificate follows shortly after the DNS points to fortrabbit.
- **CAA record**: a CAA record that does not allow Let's Encrypt blocks the certificate, see [HTTPS](/1.platform/13.domains/06.https.md#secure-your-domain-with-a-caa-record).

## Mixed content warning

The page loads over HTTPS but requests a script, style, image, font or API call over `http://`. Browsers block such requests:

> Mixed Content: The page at 'https://example.com' was loaded over HTTPS, but requested an insecure resource 'http://example.com/app.js'. This request has been blocked; the content must be served over HTTPS.

Search the templates, the CSS and the database content for `http://` and change the URLs to `https://`. In a CMS, check the site URL setting first, see the [Craft CMS domain setup](/2.guides/3.craft-cms/20.domain-setup.md) for an example.

## Redirect HTTP to HTTPS

Send all requests to HTTPS with a [redirect in .htaccess](/3.dev/21.htaccess/02.redirects.md).

## Certificate verify failed in PHP

An error like `SSL certificate problem: unable to get local issuer certificate` or `certificate verify failed` comes from an outgoing request of the app, such as cURL or Guzzle, not from the site itself. The remote server sends an incomplete or expired certificate chain, or the app passes its own outdated CA bundle. Check the remote host with `curl -v https://remote.example.com`, and never turn off verification to get rid of the error.
