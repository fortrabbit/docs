---
reviewed: 2024-08-15 13:29:46
title: Migrate to fortrabbit
naviTitle: Migrate to fortrabbit
navigation.excerpt: Website transfer to fortrabbit
lead: How to transfer your website to fortrabbit with confidence.
---

fortrabbit is not your traditional shared or VPS hosting. It may require some tinkering on your application and we recommend reading the [intro](/.1.get-started/1.intro.md) as well as our specific install guides for various frameworks & CMS to get the concepts and features.

This article covers the general basics as well as some deep links for moving your App from any hosting provider to fortrabbit. This will hopefully cover everything you need to realize a smooth transition. Each App is different, adjust your plan accordingly and don't hesitate to [contact us](/20.get-help/2.contact-us.md) with your specific questions.

## 1. Create your fortrabbit app

Each website or web application is represented by an [app](/1.platform/10.objects/1.app.md) with at least one [environment](/1.platform/10.objects/02.environment.md) on fortrabbit. You can have as many apps with as many environments as you want. So in order to move your project you need to create an app on fortrabbit first. Do so in the fortrabbit dashboard as a first step.

## 2. Prepare your domains

To minimize downtimes caused by DNS cache propagation you should change the Time to Live (TTL) of your domains to the lowest possible value. Something like five minutes would be just great. If you have some kind of web control panel with your domain provider, then you can most likely change it yourself. If not, just get in touch with the provider and ask them to reduce your TTL for you. You should do this 48-72 hours before you start with the migration.

After that's done make sure to add all the domains to your new fortrabbit App in the dashboard.

## 3. Migrate your code

If you already subscribe to a Git based workflow, then there is probably not much to do here. If not, then you should familiarize yourself with Git. We promise: You won't regret it. Once you've used it, you won't go back without being forced.

## 4. Migrate your runtime data

Runtime data means all kinds of data, which is created by your App at runtime. Usually these are user uploads or uploads from a CMS or some-such. When working with a clean Git workflow, the runtime data and the code should be separated.

## 5. Migrate your databases

If your App is using a MySQL database, you will need to migrate the database data as well. [Export the MySQL database from your old hosting and import](/1.platform/08.mysql/02.export-import/07.export-import-intro.md) it to the fortrabbit database.

## 6. Sending e-mails

Take care when you application needs to send mails. Simple `sendmail` won't work, see our [quirks article](/1.platform/03.concepts/04.limits.md#mailing) on how to send mails, either via SMTP or 3rd party provider.

## 7. HTTPS

All fortrabbit Apps can be accessed using a free HTTPS URL. There is also a free HTTPS Let's Encrypt certificate for [custom domains](/3.dev/dns-external-domains.md).

## 8 Final switch: DNS

Now that you have migrated your code, runtime data and database - and all the other stuff you needed - you are ready to push the button.

Now that your App is fully mirrored on fortrabbit and ready to handle traffic, you can [route your Domains DNS records to fortrabbit](/3.dev/dns-external-domains.md). If you waited the 48-72 hours for DNS caches to clear, downtime will be minimal as traffic is routed to your App on fortrabbit.

## Migrating away from fortrabbit

We don't lock you in. You can cancel at any time. Due to the distributed nature of services it's even easier to move somewhere else then. The steps are essentially the same as above.
