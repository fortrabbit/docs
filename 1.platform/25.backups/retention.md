---
created: 2024-12-19
updated: 2026-11-06
reviewed: 2026-11-06
reviewer: fl
title: Backup retention
description: 'fortrabbit keeps the newest daily backups, Monday backups as weekly and backups from the 1st as monthly, up to the count of the backup plan.'
naviTitle: Backup retention
navigation.excerpt: See which backups are kept and for how long
figure:
  emoji: 🗓️
  text: Keep the right backups for the right time.
  color: rgb(22, 101, 52)
  textColor: rgb(220, 252, 231)
lead: Every environment gets one automatic backup a day. The backup plan sets how many backups are kept, split into daily, weekly and monthly ones. Weekly means the Monday backup, monthly the backup from the 1st.
draft: true
links:
  - title: Backup component
    route: /platform/components/backups
  - title: Restore from backup
    route: /platform/backups/restore
  - title: Backup files
    route: /platform/backups/files
topics:
  - backups
---

## About backup retention

The [backup component](/1.platform/09.components/05.backups.md) creates one backup per day, at a time set per environment. The dashboard shows the time of the next one. Every plan keeps a fixed number of backups. Retention decides which of the existing backups those are: a few recent days, a few weeks back, and a few months back.

## Which backups are kept

Once an hour, the oldest backups that no slot needs are deleted. The slots are filled in this order, newest first:

1. Daily: the newest backup of each of the last days.
2. Weekly: the newest Monday backups that are not kept as daily.
3. Monthly: the newest backups from the 1st of a month that are not kept yet.
4. Free slots: the newest remaining backups.

All dates are UTC. A 1st that falls on a Monday counts as weekly first, and as monthly once newer Mondays take its weekly slot.

An example with 4 daily, 4 weekly and 4 monthly slots, on Friday 4 December:

```raw
daily     Dec 4, Dec 3, Dec 2, Dec 1
weekly    Nov 30, Nov 23, Nov 16, Nov 9
monthly   Nov 1, Oct 1, Sep 1, Aug 1
```

## New environments and plan changes

A new environment keeps every backup until the plan count is reached. The free slots hold the newest backups, so the first weeks look like a row of daily backups. Mondays and 1sts take over the slots as they come, so the weekly ones are complete after about a month and the monthly ones after a few months.

- Upgrade: nothing gets deleted, the new slots fill over time.
- Downgrade: the next run deletes the backups the smaller plan has no slot for. Deleted backups can't be brought back.

## Manual backups

"Backup now" in the dashboard creates a backup right away. It is marked as manual in the backup list and counts as the backup of its day: the newest backup of a day takes the daily slot, and an earlier one from the same day is deleted with the next run. A scheduled backup later that day replaces a manual one the same way. To keep a copy from before a risky change, download the manual backup.

## Backup list in the dashboard

The backups section of an environment lists every backup with its role (daily, weekly, monthly or spare) and the date until which it stays. That date assumes nothing changes: a manual backup, a plan change or a failed backup moves it.
