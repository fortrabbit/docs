---
reviewed:      2023-02-15 08:20:13
title:         Dig
navigation.excerpt:       'Query public DNS entries from the terminal'
lead:          'Query public DNS entries from the terminal using the dig command.'
---

The `dig` command shows you if there are any DNS entries and where they are pointing to. Here we look up `help.fortrabbit.com`.

```shell
$ dig help.fortrabbit.com
;; Truncated, retrying in TCP mode.

; <<>> DiG 9.8.3-P1 <<>> ANY help.fortrabbit.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 44565
;; flags: qr rd ra; QUERY: 1, ANSWER: 3, AUTHORITY: 0, ADDITIONAL: 0

;; QUESTION SECTION:
;help.fortrabbit.com.       IN  ANY

;; ANSWER SECTION:
help.fortrabbit.com.      600    IN  CNAME   help-frbit.frb.io.
help-frbit.frb.io.        300    IN  CNAME   help-frbit.eu2.frbit.net.
help-frbit.eu2.frbit.net.  20    IN  A       52.48.51.144

;; Query time: 863 msec
;; SERVER: 192.168.178.1#53(192.168.178.1)
;; WHEN: Wed Jun  1 10:25:40 2016
;; MSG SIZE  rcvd: 122
```

### Dig an IP

```shell
# This will print out the IP of your App
$ dig +short {{app-env-slug}}.frb.io 
```
