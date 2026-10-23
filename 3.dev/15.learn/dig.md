---
updated: 2026-10-23
reviewed: 2026-10-23
reviewer: fl
title: Dig
description: 'Query public DNS records from the terminal with dig, to see which addresses a domain resolves to while pointing it at fortrabbit.'
navigation.excerpt: 'Query public DNS entries from the terminal'
figure:
  emoji: 🔍
  text: Query DNS records from terminal.
  color: rgb(99, 102, 241)
  textColor: rgb(224, 231, 255)
lead: dig +short example.com shows the IP a domain points to. Use dig to check DNS records from the terminal.
head:
  meta:
    - name: keywords
      content: 'dig, DNS, query, terminal, command, lookup, fortrabbit'
topics:
  - dns
  - troubleshooting
---

## Look up DNS records with dig

`dig` asks DNS for the records of a domain. Use it to check whether a domain points to fortrabbit, see [DNS troubleshooting](/1.platform/13.domains/08.dns-troubleshooting.md).

```shell
# A record, short answer
dig +short example.com

# CNAME record of a subdomain
dig +short CNAME www.example.com

# Ask a public resolver instead of the local one
dig +short www.example.com @1.1.1.1

# IP of the environment
dig +short {{app-env-id}}.frbit.app
```

Without `+short`, dig prints the full answer with TTL and the resolver it used. macOS and most Linux distributions ship with dig. On Windows, use `nslookup example.com` or dig in WSL.
