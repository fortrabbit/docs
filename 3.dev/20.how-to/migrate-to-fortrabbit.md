---
updated: 2026-10-18
reviewed: 2026-07-07
reviewer: fl
title: Migrate to fortrabbit
description: 'Move an existing website to fortrabbit, with the changes the application needs and the way code, database and assets get across.'
naviTitle: Migrate to fortrabbit
navigation.excerpt: Website transfer to fortrabbit
figure:
  emoji: 🚚
  text: Move your project here.
  color: rgb(146, 64, 14)
  textColor: rgb(254, 243, 199)
lead: How to transfer your website to fortrabbit.
head:
  meta:
    - name: keywords
      content: 'migrate, website migration, transfer hosting, DNS, domain migration, fortrabbit'
topics:
  - migration
  - deployment
faq:
  - question: Can I test my site on fortrabbit before switching DNS?
    answer: Yes. Every environment has a default domain with HTTPS that works right away. Deploy the code, copy uploads and database, and test there before changing any DNS records.
    links:
      - title: Default domain
        route: /platform/domains/default-domain
---

fortrabbit has no control panel and no root shell, so some apps need settings adjusted before the move. Read [project organization](/1.platform/02.get-started/01.project-organization.md) and the install guide for the framework or CMS first. Every project is different: adjust the order to it and ask support when something does not fit.

## 1. Create the app

Each website or web application is an [app](/1.platform/10.objects/01.app.md) with at least one [environment](/1.platform/10.objects/02.environment.md). Create the app in the dashboard. Its [default domain](/1.platform/13.domains/01.default-domain.md) works right away, with HTTPS, so the whole move can be tested before any DNS changes.

## 2. Lower the TTL

Resolvers cache DNS records for as long as their TTL says. Set the TTL of the domain's records to five minutes at the domain provider, and do it at least one old TTL ahead of the switch: with a TTL of one day, a day before. The switch then takes minutes instead of hours.

## 3. Deploy the code

Code reaches fortrabbit through Git, with the [GitHub integration](/1.platform/06.deployment/02.github-app.md). A project that is not in a Git repository yet needs one first. Composer and npm run in the [build commands](/1.platform/06.deployment/03.build-commands.md), database migrations and cache clearing in the [post-deploy commands](/1.platform/06.deployment/04.post-deploy-commands.md).

## 4. Copy the uploads

Files the app writes at runtime, such as user or CMS uploads, are not in Git. Copy them to the environment with [rsync](/3.dev/20.how-to/rsync.md). [Download a website](/3.dev/20.how-to/download-a-website.md) shows how to pull them off the old host.

## 5. Move the database

Book a MySQL component, export the database at the old host and import the dump. The [export and import](/1.platform/08.mysql/02.export-import/index.md) section covers the terminal and GUI routes.

## 6. Set up mail

`sendmail` and PHP `mail()` do not work on fortrabbit. Send mail through a transactional mail service or SMTP, as described under [mailing](/1.platform/03.concepts/09.limits.md#mailing).

## 7. Switch the DNS

Test the app on its default domain. Then add the domains to the environment and [point their DNS records to fortrabbit](/1.platform/13.domains/04.external-domain-setup.md). Each correctly routed domain gets a free [TLS certificate](/1.platform/13.domains/06.https.md), renewed automatically. With the lowered TTL, traffic moves within minutes. Raise the TTL again once everything runs.

## Moving from the old fortrabbit platform

Apps on the old fortrabbit platform move with their own guide, see [self-migration](/1.platform/01.new/8.self-migration.md).

## Moving away from fortrabbit

Apps can be canceled at any time. Code sits in Git, the database is a MySQL dump, uploads are plain files: the same steps work in reverse.
