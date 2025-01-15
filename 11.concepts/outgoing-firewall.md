---
reviewed: 2024-08-29 20:32:51
title: Outgoing firewall
navigation.excerpt: Making requests to the outer world from the environment
lead: Learn how to make outgoing calls from your within your application hosted on fortrabbit.
---

<!-- TODO: Write it! -->
<!-- TODO: Review by infra. -->

By default, outgoing traffic is limited on most non-standard ports for security reasons. See our [specs](http://www.fortrabbit.com/specs#firewall). Please make sure to visit that page before making your request to open ports.

## Opening certain ports for outgoing calls

You can open ports with [App environment](/10.objects/2.app-environment.md) settings in the dashboard.

:DashboardLink{title="Outgoing firewall settings for {{app-env-slug}}" path="/environments/{{app-env-slug}}/settings/firewall-outgoing"}
