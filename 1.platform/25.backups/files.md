---
reviewed: 2026-07-04
reviewer: fl
title: Backup files
naviTitle: Backup files
navigation.excerpt: Files and database
figure:
  emoji: 📦
  text: Files and dumps, packed and ready.
  color: rgb(55, 65, 81)
  textColor: rgb(229, 231, 235)
lead: What is included and excluded. How to use the files downloaded from the backup component to actually restore a website.
links:
  - title: Backup component
    route: /platform/components/backups
head:
  meta:
    - name: keywords
      content: 'backup files, restore backup, backup archive, database dump, file recovery, fortrabbit'
---

The fortrabbit [backup component](/1.platform/09.components/05.backups.md) provides you with a downloadable file archive of an [environment](/1.platform/10.objects/02.environment.md) at a given time, see [retention](/1.platform/25.backups/retention.md). This archive contains everything required to restore the state of that backup.

- Files: Everything present on the file system
- Database: a database dump file, if [database](/1.platform/09.components/02.mysql.md) is booked

## Use cases

- Grab a single file that was deleted
- Restore only the database but not the files
- Additional backups: store backups offsite for long time retention
- Boarding a new developer: Set up a local development
- Verifying the state of a backup before [restoring](/1.platform/25.backups/restore.md)

## Backups VS git deployment

Developers using [git deployment](/1.platform/05.deployment/01.intro.md) already have access to an archive with a complete history of the code base. The fortrabbit backups also contain runtime data such as vendor folder contents and user uploads, given the nature of most PHP-based applications.

## Backup file sizes

The shown size of the backups is unlikely to match actual usage for MySQL size and web storage. Note that backups are compressed, while production data is not.

The backup size shown in the dashboard likely will not match the downloaded files. Dashboard sizes use binary units (mebibyte), while most operating systems display decimal units (megabyte). Additionally, the local file system may have a different block size.

## Excludes

Some run-time and cache files are excluded from the backups.

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

While you can [restore from backup](/1.platform/25.backups/restore.md) using the dashboard, you also have the option to manually revert to a previous state by uploading the necessary files to the environment.

### Restore files

To recover files from a backup, first ensure to have the unpacked files from the backup archive on your local machine. Then upload these files to your environment using SFTP or [rsync](/3.dev/20.how-to/rsync.md). Be sure to remove any unnecessary files from the remote environment and don't forget to include hidden files.

### Restore database

The database backup file is a standard dump created by the `mysqldump` tool. Restore it by importing the data into your MySQL database. For detailed instructions, refer to our [database export/import guides](/1.platform/08.mysql/02.export-import/07.intro.md). It may be necessary to drop the old tables before importing the new data.
