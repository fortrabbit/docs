---
reviewed: 2025-09-26 09:25:25
title: Restore from backup
naviTitle: Restore from backup
navigation.excerpt: automated rollback
figure:
  emoji: ⏮️
  text: Roll back.
  color: rgba(153, 27, 27, 1)
  textColor: rgba(254, 226, 226, 1)
lead: Rollback an environment to a prior state. Gotchas. Details.
links:
  - title: Backup component
    route: /platform/components/backups
---

## Requirements

To restore from a backup, the [backup component](/1.platform/09.components/05.backups.md) needs to be booked and at least one backup already needs to be present with the [environment](/1.platform/10.objects/02.environment.md) to be chosen as backup source.

## Use cases

- Something broke the site, you want to go back to a working state
- The site has been hacked

## How to restore a backup

- Visit the backups section of an environment
- With the list of available backups choose the one you want to restore
- Click the restore button, confirm, wait until finished

The process can take a while. The time it takes depends on the size of the project. It is usually finished within a couple a couple of minutes but can also take hours. While the backup restore is in progress, the environment will stay online for most of the time, but may have degraded performance. A short downtime is expected.

## What happens during restore

The chosen backup will be unpacked and prepared. Once ready, the state will be switched. The environment will serve the state of backup, the **previous state will be deleted**.

## Recommendations

- Back up the current state, by manual backup or by [downloading a snapshot](/3.dev/20.how-to/download-a-website.md)
- Know about the state of the backup you are about to roll back to, see [backup files](/1.platform/25.backups/files.md)
- Don't change anything while the backup rollback is in progress

## No guarantees

It can not be guaranteed that the backup restoration will leave the environment in a working state. It's possible that the environment returns an error after the restoration. In many cases that's a [500 error](/3.dev/22.http-errors/504.md), which is easy to debug, by looking at the logs.

## Backup restore VS git deployment

Mind that the backup includes the actual state of files present at the time when the backup was made. When [git deployment](/1.platform/05.deployment/01.intro.md) is used, the head of the connected branch might be ahead. So it's possible that the next git deployment will cause issues. One way to deal with that is to reset the connected Git repo to a state that matches the restored backup, but there is no general rule of thumb for that.

## Backup excludes

See [backup excludes](/1.platform/25.backups/files.md#excludes).
