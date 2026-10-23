---
created: 2024-12-18
updated: 2026-10-23
reviewed: 2026-10-23
reviewer: fl
title: How to download a full website
description: 'Pull a complete website off a hosting provider — code, database and uploaded files — so it can run locally or move somewhere else.'
naviTitle: Download a website
navigation.excerpt: Get all data to have it running locally
figure:
  emoji: 🔻
  text: Pull files, data and dependencies.
  color: rgb(30, 64, 175)
  textColor: rgb(219, 234, 254)
lead: This guide explains how to download all necessary application data from a hosting provider to run a website elsewhere. Technical skills are required.
head:
  meta:
    - name: keywords
      content: 'download website, website backup, migrate hosting, database export, SFTP, fortrabbit'
topics:
  - migration
---

## When to download

Development happens in a [local development environment](/4.integrations/01.local-development/01.intro.md), so a working copy usually exists. A full download is needed when:

- a new developer joins and the old copy is gone
- a previous developer left without handing over the project
- the local copy is lost
- the project gets archived or moves to another host

A website consists of code, dependencies, files such as uploads, and the database. Each part comes from its own place.

## Code

After git deployments, clone the repository and run `composer install` to get the [Composer](/3.dev/15.learn/02.composer.md) dependencies. Check that the repository holds the deployed state.

After SFTP uploads, or when the repository may be behind, download the whole project like the files below.

## Uploads and other files

[Git only syncs up](/1.platform/06.deployment/01.intro.md#git-only-syncs-up): uploads and other files created on the environment are not in the repository. Download them with:

- [rsync](/3.dev/20.how-to/rsync.md), for a folder or the whole project
- [SFTP](/1.platform/05.code-access/04.sftp.md), in a GUI client

## Database

Export the database and import it locally, see [database down](/1.platform/08.mysql/02.export-import/07.intro.md).

## Backups

With the [backup component](/1.platform/09.components/05.backups.md) booked, download a backup of files and database from the dashboard, see [working with backup files](/1.platform/25.backups/files.md).

## Check the copy

Run the downloaded site locally and click through it. Compare file counts and the database size with the environment before deleting anything there.
