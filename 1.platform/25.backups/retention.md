---
reviewed: 2025-07-09 15:32:06
title: Backup retention
naviTitle: Backup retention
navigation.excerpt: monthly, weekly, daily
figure:
  emoji: 🗓️
  text: Keep the right backups for the right time.
  color: rgb(22, 101, 52)
  textColor: rgb(220, 252, 231)
# lead: The automatic backup retention model en detail.
draft: true
links:
  - title: Backup component
    route: /platform/components/backups
---

::CallOut{alert}
The backup retention feature is not implemented yet. So far only daily backups.
::

The [backup component](/1.platform/09.components/05.backups.md) is available in different plans. Larger ones include more backups. Backup retention determines how long backups are kept. This concept is crucial for ensuring data availability, compliance, and efficient storage management.

Depending on the plan chosen, multiple backups of the same type might be included. If the plan includes three monthly backups, then monthly backups are retained for three months.

## Daily backups

- kept for a short period
- created daily at randomized times

## Weekly backups

- retained for a longer period
- Sunday backups are kept

## Monthly backups

- kept for an extended period
- Backups from the start of the month are kept

## Manual backups

In addition to automatically scheduled backups, it's possible to trigger the immediate creation a backup from the dashboard. This backup will be treated like a new daily backup.

- If the currently booked [backup plan](/1.platform/09.components/05.backups.md) includes one daily backup, the new manual backup will replace the current backup.
- If the currently booked backup plan includes two daily backups, the oldest backup from two days ago will be deleted and the backup from yesterday will move down one slot.
