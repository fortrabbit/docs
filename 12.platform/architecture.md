---
reviewed: 2023-07-20
title: Architecture
naviTitle: Architecture
excerpt: App centric hosting, what is it?
lead: 
---


## Understand the architecture

```
# Universal App deployment architecture
                                                         ┌───────────────┐
                                                         │ website users │
                                                         └──────┬────────┘
                                                                │
                                                          http requests
                                                                │
                            ┌───────────────────────────────────┼─────────┐
                            │fortrabbit App                     │         │
                            │                                   │         │
┌────────────────┐          │┌─────────────────┐         ┌──────▼────────┐│
│ local Git repo ├─Git push─┼▶ remote Git repo ├──rsync──▶  web storage  ││
└────────────────┘          │└─────────────────┘         └──────▲────────┘│
                            │                                   │         │
                            │                                   │         │
                            └───────────────────────────────────┼─────────┘
                                                                │
                                                                │
                                                            SFTP/SSH
                                                                │
                                                          ┌─────┴─────┐
                                                          │ developer │
                                                          └───────────┘
```
