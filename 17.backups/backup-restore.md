---
reviewed: 2024-12-19 09:25:33
title: Backup restoration
naviTitle: Backup restoration
navigation.excerpt:
lead: How to use the backup restoration feature to rollback an environment to a prior state.
---

To use the backup restore feature the [backup component](/9.components/5.backups.md) needs to be booked and at least one backup already needs to be present to be chosen as backup source.

## How to trigger a restore

- Visit the backups section of an environment
- With the list of available backups choose the one you want to restore
- Click the restore button, confirm, wait until finished

The process can take a bit of time.

## What is happening during restore

## Use cases

- Something broke the site, you want to go back to a working state
- The site has been hacked

## Recommendations

- Make sure to have the current state backed up as well, either by manually triggering a backup or by [downloading a snapshot](/15.tips/download-a-website.md)
- Know about the state of the backup you are about to roll back to, see [backup files](/17.backups/backup-files.md)

## Gotchas

### No guarantees

It can not be guaranteed that the backup restoration will leave the environment in a working state. Their are plenty of documented edge cases where the environment returned an error after the restoration.

### Backup restore VS git deployment

Mind the backup excludes
