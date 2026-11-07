---
created: 2024-12-19
updated: 2026-11-07
reviewed: 2026-11-07
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

## Slots per plan

| Plan | Daily | Weekly | Monthly | Total |
| -- | -- | -- | -- | -- |
| XS | 1 | 0 | 0 | 1 |
| SM | 1 | 1 | 1 | 3 |
| MD | 2 | 2 | 2 | 6 |
| LG | 4 | 4 | 4 | 12 |
| XL | 8 | 6 | 10 | 24 |
| 2XL | 14 | 10 | 24 | 48 |

## Which backups are kept

Once an hour, the backups that no slot needs are deleted. The slots are filled in this order, newest first:

1. Daily: the newest backup of each of the last days.
2. Weekly: the newest Monday backups that are not kept as daily.
3. Monthly: the newest backups from the 1st of a month that are not kept yet.
4. Spare: free slots hold the newest remaining backups.

All dates are UTC. A 1st that falls on a Monday counts as weekly first, and as monthly once newer Mondays take its weekly slot.

## Example: LG plan

An environment on the LG plan, 4 daily, 4 weekly and 4 monthly slots, on Friday 4 December 2026. The backups section of the dashboard lists:

| Date | Retention | Until |
| -- | -- | -- |
| 2026-12-04 | daily | 2026-12-08 |
| 2026-12-03 | daily | 2026-12-07 |
| 2026-12-02 | daily | 2026-12-06 |
| 2026-12-01 | daily | 2027-04-05 |
| 2026-11-30 | weekly | 2027-01-01 |
| 2026-11-23 | weekly | 2026-12-25 |
| 2026-11-16 | weekly | 2026-12-18 |
| 2026-11-09 | weekly | 2026-12-11 |
| 2026-11-01 | monthly | 2027-04-02 |
| 2026-10-01 | monthly | 2027-03-05 |
| 2026-09-01 | monthly | 2027-01-05 |
| 2026-08-01 | monthly | 2026-12-05 |

The next day, the backup from Saturday 5 December takes the first daily slot. The backup from 1 December leaves the daily slots and moves to the newest monthly slot, which pushes out the backup from 1 August. That is why the 1 December backup stays until April, while the 2 December backup is gone on 6 December.

"Until" is the day of the backup run that pushes a backup out, assuming nothing changes. A manual backup, a plan change or a failed backup moves it.

## New environments and plan changes

A new environment keeps every backup until the plan count is reached. Spare slots hold the newest backups, so the first weeks look like a row of daily backups. The same LG environment, created on 25 November:

| Date | Retention | Until |
| -- | -- | -- |
| 2026-12-04 | daily | 2026-12-14 |
| 2026-12-03 | daily | 2026-12-13 |
| 2026-12-02 | daily | 2026-12-12 |
| 2026-12-01 | daily | 2027-04-05 |
| 2026-11-30 | weekly | 2027-01-01 |
| 2026-11-29 | spare | 2026-12-11 |
| 2026-11-28 | spare | 2026-12-10 |
| 2026-11-27 | spare | 2026-12-09 |
| 2026-11-26 | spare | 2026-12-08 |
| 2026-11-25 | spare | 2026-12-07 |

Mondays and 1sts take over the spare slots as they come, so the weekly slots are complete after about a month and the monthly ones after a few months.

- Upgrade: nothing gets deleted, the new slots fill over time.
- Downgrade: the next run deletes the backups the smaller plan has no slot for. Deleted backups can't be brought back.

## Manual backups

"Backup now" in the dashboard creates a backup right away. It is marked as manual in the backup list and counts as the backup of its day: the newest backup of a day takes the daily slot. On the XS plan, right after a manual backup:

| Date | Retention | Until |
| -- | -- | -- |
| 2026-11-07 `manual` | daily | 2026-11-07 |
| 2026-11-06 | deleted soon | 2026-11-07 |

The backup from the day before has no slot left and is deleted within the hour. The scheduled backup later that day replaces the manual one the same way. To keep a copy from before a risky change, download the manual backup.
