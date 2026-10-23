---
created: 2024-12-19
updated: 2026-10-23
reviewed: 2026-10-23
reviewer: fl
title: Restore from backup
description: 'Restore a fortrabbit environment from a backup after a broken deploy or a hack: the requirements, the steps, and what the rollback touches.'
naviTitle: Restore from backup
navigation.excerpt: automated rollback
figure:
  emoji: ⏮️
  text: Roll back.
  color: rgb(153, 27, 27)
  textColor: rgb(254, 226, 226)
lead: Restore a fortrabbit environment from a backup in the dashboard after a broken update or a hack. The restore replaces files and database with the backup, and the current state is deleted.
links:
  - title: Backup component
    route: /platform/components/backups
head:
  meta:
    - name: keywords
      content: 'restore backup, rollback environment, database restore, file restore, backup recovery, fortrabbit'
topics:
  - backups
  - troubleshooting
---

## Requirements

The [environment](/1.platform/10.objects/02.environment.md) needs the [backup component](/1.platform/09.components/05.backups.md) and at least one backup.

## Use cases

- An update broke the site, and it should go back to a working state
- The site was hacked

## How to restore a backup

1. Open the backups of the environment in the dashboard.
2. Pick the backup to restore.
3. Click restore, confirm, and wait until it is finished.

A restore takes a few minutes for most projects, and hours for very large ones. The environment stays online for most of that time, slower than usual, with a short downtime at the switch.

## What happens during restore

The backup is unpacked and prepared, then the environment switches to it. **The previous state is deleted.**

## Recommendations

- Save the current state first, with a manual backup or by [downloading the website](/3.dev/20.how-to/download-a-website.md).
- Check what the backup holds, see [backup files](/1.platform/25.backups/files.md).
- Change nothing while the restore runs.

## No guarantees

A restored environment can still fail, for example because a dependency or setting changed since the backup. The error is often a [500](/3.dev/22.http-status-codes/500.md), and the [logs](/1.platform/07.settings/25.logs.md) name the cause.

## Backup restore VS git deployment

The backup holds the code of the time it was made. With [Git deployment](/1.platform/06.deployment/01.intro.md), the connected branch can be ahead, and the next push deploys that newer code again. Revert the branch to match the backup when the newer code caused the problem.

## Backup excludes

See [backup excludes](/1.platform/25.backups/files.md#excludes).
