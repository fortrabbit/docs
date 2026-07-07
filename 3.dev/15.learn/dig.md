---
reviewed: 2026-07-07
reviewer: fl
title: Dig
navigation.excerpt: 'Query public DNS entries from the terminal'
figure:
  emoji: 🔍
  text: Query DNS records from terminal.
  color: rgb(99, 102, 241)
  textColor: rgb(224, 231, 255)
lead: 'Query public DNS entries from the terminal using the dig command.'
head:
  meta:
    - name: keywords
      content: 'dig, DNS, query, terminal, command, lookup, fortrabbit'
---

The `dig` command queries public DNS records to show which IP addresses a domain name resolves to. This example shows how to look up a domain.

```shell
$ dig fortrabbit.com

; <<>> DiG 9.10.6 <<>> fortrabbit.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 44565
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; QUESTION SECTION:
;fortrabbit.com.            IN  A

;; ANSWER SECTION:
fortrabbit.com.      600    IN  A       52.48.51.144

;; Query time: 24 msec
;; SERVER: 192.168.178.1#53(192.168.178.1)
;; MSG SIZE  rcvd: 59
```

### Dig an IP

```shell
# This prints the IP of the app
$ dig +short {{app-env-id}}.frbit.app
```
