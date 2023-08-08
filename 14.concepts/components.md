---
reviewed:  2023-08-01 18:38:06
title:     Components intro
naviTitle: Components
excerpt:   Individually scalable hosting resources
lead:      Individually scalable hosting resources for each app environment.
---

## Intro

With VPS hosting you pay for size of your box. Within that box you can run different services. fortrabbit on the other side has a micro service oriented architecture with services running in isolated containers. This architecture is reflected in the pricing. A component represents a service that can be booked and scaled individually per [app environment](/13.objects/2.app-environment.md).

PHP, MySQL, but also traffic and web storage are components. Most components are available in different sizes, those are called plans and are titled like t-shirt labels: XS, S, M, L …. Different resource attributes are associated with the plans as well.

| **Component** |  **Attribute**  | **Plan** | **Price** |
| ------------- | --------------- | -------: | --------: |
| PHP           |         XXX MB  |        S |       $X  |
| MySQL         |         XXX MB  |        M |       $X  |

See the [components list](/10.components/index.md) for all available components. The [pricing page](https://www.fortrabbit.com/pricing) gives you an overview. The [pricing intro](/15.billing/1.pricing.md) explains level billing concepts.

## Required and optional components

The components PHP, traffic and web storage are required, they can not be deselected. All other components are optional.

## Components during the free trial

All components are available with the [free trial](/13.concepts/2.free-trial.md). They are however limited to the smallest plan.
