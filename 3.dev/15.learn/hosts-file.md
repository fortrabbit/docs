---
updated: 2026-10-23
reviewed: 2026-10-23
reviewer: fl
title: Hosts file
description: 'Test a custom domain against a fortrabbit app before moving DNS, by pointing the domain at the app in the local hosts file.'
navigation.excerpt: Testing domain routing with your local hosts file
figure:
  emoji: 🌐
  text: Test domains before DNS changes.
  color: rgb(6, 182, 212)
  textColor: rgb(207, 250, 254)
lead: Point a domain to the IP of a fortrabbit environment in the local hosts file to test it before switching the DNS.
head:
  meta:
    - name: keywords
      content: 'hosts file, local testing, domain routing, DNS, development, fortrabbit'
topics:
  - dns
  - local-development
---

## Test a domain before the DNS switch

The hosts file maps domain names to IP addresses on one computer only. Use it to see a site on fortrabbit under its own domain before changing the DNS for everyone:

1. Add the domain to the environment in the dashboard.
2. Get the IP of the environment with [dig](/3.dev/15.learn/dig.md): `dig +short {{app-env-id}}.frbit.app`
3. Add a line with that IP and the domain to the hosts file.

```shell
# IP of the environment, then the domains
203.0.113.10 example.com www.example.com
```

The hosts file has no file extension:

- macOS and Linux: `/etc/hosts`, edit with `sudo`
- Windows: `C:\Windows\System32\drivers\etc\hosts`, edit as administrator

Leave the existing lines as they are. The browser shows a certificate warning: fortrabbit issues the [TLS certificate](/1.platform/13.domains/06.https.md) only once the DNS points to fortrabbit.

## Remove the entry

Delete the line once the DNS switch is done. The IP of an environment can change, so a forgotten entry breaks the site on that computer later.
