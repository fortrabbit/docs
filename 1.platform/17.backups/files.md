---
reviewed: 2025-07-09 14:38:11
title: Backup files
naviTitle: Backup files
navigation.excerpt: files and database
lead: What is included and excluded. How to use the files downloaded from the backup component to actually restore a website.
siblings: Backups
links:
  - title: Backup component
    route: /platform/components/backups
---

The fortrabbit [backup component](/1.platform/09.components/05.backups.md) provides you with a downloadable file archive of an [environment](/1.platform/10.objects/02.app-environment.md) at a given time, see [retention](/1.platform/17.backups/retention.md). This archive contains everything required to restore the state of that backup.

- Files: Everything present on the file system
- Database: a database dump file, if [database](/1.platform/09.components/2.mysql.md) is booked

## Use cases

- Grab a single file that was deleted
- Restore only the database but not the files
- Additional backups: store backups offsite for long time retention
- Boarding a new developer: Set up a local development
- Verifying the state of a backup before [restoring](/1.platform/17.backups/restore.md)

## Backups VS git deployment

Developers using [git deployment](/3.dev/03.deployment/01.intro.md) already have access to an archive with a complete history of the code base. The fortrabbit backups also contain runtime data such as the vendor folder contents and user uploads. Given the nature of most PHP based applications.

## Backup file sizes

The shown size of the backups is unlikely to match what is shown with actual usage for MySQL size and web storage. Mind that the backups are compressed, while the data in production is not.

The size of the backup shown in the dashboard likely will not match with the downloaded files. This is because the sizes with the dashboard are shown in binary (mebibyte) not decimal format (megabyte) like with most Operating Systems. Also the local file system may have a different block size.

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

While you can [restore from backup](/1.platform/17.backups/restore.md) using the dashboard, you also have the option to manually revert to a previous state by uploading the necessary files to the environment.

### Restore files

To recover files from a backup, first ensure to have the unpacked files from the backup archive on your local machine. Then upload these files to your environment at using SFTP or [rsync](//3.dev/20.how-to/rsync.md). Be sure to remove any unnecessary files from the remote environment and don't forget to include hidden files.

### Restore database

The database backup file is a standard dump created by the `mysqldump` tool. Restore it by importing the data into your MySQL database. For detailed instructions, refer to our [database export/import guide](/8.database/7.export-import.md). It may be necessary to drop the old tables before importing the new data.
