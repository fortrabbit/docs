---
updated: 2026-10-23
reviewed: 2026-10-23
reviewer: fl
title: Backup files
description: 'What a fortrabbit backup archive contains — the full file system plus a database dump — and how to use it to restore a website.'
naviTitle: Backup files
navigation.excerpt: Files and database
figure:
  emoji: 📦
  text: Files and dumps, packed and ready.
  color: rgb(55, 65, 81)
  textColor: rgb(229, 231, 235)
lead: A fortrabbit backup is a downloadable archive with the files of the environment and, with MySQL booked, a database dump. Caches, logs, archives and Git folders are left out. Use it to restore single files, the database, or a local copy.
links:
  - title: Backup component
    route: /platform/components/backups
head:
  meta:
    - name: keywords
      content: 'backup files, restore backup, backup archive, database dump, file recovery, fortrabbit'
topics:
  - backups
---

The [backup component](/1.platform/09.components/05.backups.md) creates archives of an [environment](/1.platform/10.objects/02.environment.md), and its plan sets how many are kept. An archive holds:

- Files: the file system of the environment, without the [excludes](#excludes)
- Database: a dump, when the [MySQL component](/1.platform/09.components/02.mysql.md) is booked

## Use cases

- Get back a single deleted file
- Restore the database without the files
- Keep copies offsite for longer
- Set up a local development environment for a new developer
- Check a backup before [restoring](/1.platform/25.backups/restore.md) it

## Backups VS git deployment

With [Git deployment](/1.platform/06.deployment/01.intro.md), the repository holds the history of the code. A backup adds what Git does not have: the `vendor` folder, uploads and other runtime data.

## Backup file sizes

The size of a backup differs from the storage and MySQL usage of the environment: backups are compressed, and the excludes are left out.

The size in the dashboard also differs from the downloaded file. The dashboard counts in binary units (MiB), most operating systems in decimal units (MB), and file systems use different block sizes.

## Excludes

Caches, logs, archives and Git folders are left out of every backup:

```raw
# Craft
'storage/backups/',
'storage/logs/',
'storage/runtime/',
'web/cpresources/',

# Laravel
'storage/framework/',
'storage/logs/',

# Symfony
'var/cache/',
'var/log/',

# WordPress
'wp-content/cache/',

# Archives
'*.zip',
'*.tar',
'*.tar.gz',
'*.tgz',
'*.tar.bz2',
'*.tbz',

# Misc
'.git/',
'*.sql',
```

## Restore from backup files

Besides the [restore in the dashboard](/1.platform/25.backups/restore.md), parts of a backup can be restored by hand.

### Restore files

Unpack the archive locally, then upload the files with [SFTP](/1.platform/05.code-access/04.sftp.md) or [rsync](/3.dev/20.how-to/rsync.md). Include hidden files such as `.htaccess`, and remove files from the environment that the backup does not have.

### Restore database

The database file is a standard `mysqldump` dump. Import it like any other, see [database export and import](/1.platform/08.mysql/02.export-import/07.intro.md). Drop tables that the backup does not contain first.
