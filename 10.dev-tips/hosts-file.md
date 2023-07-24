---
reviewed:      2023-07-08 15:00:38
title:         Hosts file 
excerpt:       Testing domain routing with your local hosts file
lead:          ''
---

Let's say you are developing a website soon to launch and want to test your custom domain before actually switching the DNS routing it to fortrabbit. Just add the domain to fortrabbit, as you would do with any actually routed domain, then modify your local hosts file, which lets your local machine know ahead of time that the domain is to be served from your fortrabbit e.

### hosts file location

The hosts file is a text file (without file type ending). It can be found here:

* MacOS & Linux: `/etc/hosts`
* Windows: `c:\windows\system32\drivers\etc\hosts`

### Editing your local hosts file

Your local file contains many entries: do not edit those. Just add a new line with the IP of your App and the domain you want to see routed there like so:

```bash
# pattern (how it works)
[your App's IP address] [your fully qualified domain name]

# example (what it looks like)
12.0.0.1 mydomain.com www.mydomain.com
```

### Undo changes to your hosts file

After your domain has been moved/propagated be sure to remove the entry from your hosts file.
