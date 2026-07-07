---
reviewed: 2026-07-07
reviewer: fl
title: Hosts file
navigation.excerpt: Testing domain routing with your local hosts file
figure:
  emoji: 🌐
  text: Test domains before DNS changes.
  color: rgb(6, 182, 212)
  textColor: rgb(207, 250, 254)
lead: Test a custom domain locally before switching DNS routing by adding an entry to your hosts file.
head:
  meta:
    - name: keywords
      content: 'hosts file, local testing, domain routing, DNS, development, fortrabbit'
---

To test a custom domain before actually routing DNS to fortrabbit, add the domain to your fortrabbit app, then modify your local hosts file to tell your local machine that the domain is served from your app on fortrabbit.

### hosts file location

The hosts file is a text file (without file type ending). It can be found here:

- MacOS & Linux: `/etc/hosts`
- Windows: `c:\windows\system32\drivers\etc\hosts`

### Editing your local hosts file

Your local file contains many entries: do not edit those. Just add a new line with the IP of your App and the domain you want to see routed there like so:

```shell
# pattern (how it works)
[your App's IP address] [your fully qualified domain name]

# example (what it looks like)
12.0.0.1 mydomain.com www.mydomain.com
```

### Undo changes to your hosts file

After your domain has been moved/propagated be sure to remove the entry from your hosts file.
