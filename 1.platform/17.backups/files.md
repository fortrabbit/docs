---
reviewed: 2024-12-19 16:38:33
title: Backup files
naviTitle: Backup files
navigation.excerpt: files and database
lead: What is included and excluded. How to use the files downloaded from the backup component to actually restore a website.
siblings: Backups
links:
  - title: Backup component
    route: /components/backups
---

The fortrabbit [backup component](/9.components/5.backups.md) provides you with a downloadable file archive of an [environment](/1.platform/10.objects/2.app-environment.md) at a given time, see [retention](/17.backups/retention.md). This archive contains everything required to restore the state of that backup.

- Files: Everything present on the file system
- Database: a database dump file, if [database](/9.components/2.database.md) is booked

## Use cases

- Grab a single file that was deleted
- Restore only the database but not the files
- Additional backups: store backups offsite for long time retention
- Boarding a new developer: Set up a local development
- Verifying the state of a backup before [restoring](/17.backups/restore.md)

## Backups VS git deployment

Developers using [git deployment](/6.deployment/1.intro.md) already have access to an archive with a complete history of the code base. The fortrabbit backups also contain runtime data such as the vendor folder contents and user uploads. Given the nature of most PHP based applications.

## Backup file sizes differ to metrics

The size of the backups is unlikely to match what is shown with actual usage for MySQL size and web storage. The backups are compressed.

## Excludes

Some run-time and cache files are excluded from the backups.

```raw
# Craft
storage/backups
storage/logs
storage/runtime
web/cpresources

# Laravel
storage/framework
storage/logs

# Misc
.git
.idea
*.sql
```

## Restore from backup files

While you can [restore from backup](/17.backups/restore.md) using the dashboard, you also have the option to manually revert to a previous state by uploading the necessary files to the environment.

### Restore files

To recover files from a backup, first ensure to have the unpacked files from the backup archive on your local machine. Then upload these files to your environment at using SFTP or [rsync](/3.dev/rsync.md). Be sure to remove any unnecessary files from the remote environment and don't forget to include hidden files.

### Restore database

The database backup file is a standard dump created by the `mysqldump` tool. Restore it by importing the data into your MySQL database. For detailed instructions, refer to our [database export/import guide](/8.database/7.export-import.md). It may be necessary to drop the old tables before importing the new data.
