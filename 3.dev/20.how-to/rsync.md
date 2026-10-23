---
updated: 2026-10-23
reviewed: 2026-10-23
reviewer: fl
title: Sync files with rsync
description: 'Sync files between a local machine and fortrabbit with rsync over SSH: up, down, dry runs, excludes and deleting obsolete files.'
naviTitle: rsync
navigation.excerpt: Copy and sync like a boss
figure:
  emoji: rsync
  text: Sync only what changed, fast and safe.
  color: rgb(2, 132, 199)
  textColor: rgb(224, 242, 254)
lead: rsync copies only the files that changed, over SSH. Use it to sync uploads and content between the local machine and fortrabbit, next to git deployment or instead of SFTP.
head:
  meta:
    - name: keywords
      content: 'rsync, deployment, file sync, sftp alternative, git deployment, fortrabbit'
topics:
  - deployment
  - ssh
---

## About rsync

rsync is a command line tool that synchronizes folders. It compares source and destination and transfers only new and changed files, over [SSH](/1.platform/05.code-access/03.ssh.md) with the [SSH key](/3.dev/15.learn/01.ssh-key-setup.md) of the account. Run it on the local machine, not on the environment. Linux and macOS ship with it, check with `rsync --version`. On Windows, use it in [WSL](https://learn.microsoft.com/windows/wsl/).

A wrong option or a swapped source and destination can overwrite or delete files. Run a dry run first.

## Use cases

- **Next to [git deployment](/1.platform/06.deployment/01.intro.md)**: sync what git does not track, such as uploads, assets and CMS content. Add these folders to the [exclude patterns](/1.platform/06.deployment/10.exclude-patterns.md), or a deployment with the replace strategy deletes them.
- **Instead of [SFTP](/1.platform/05.code-access/04.sftp.md)**: upload a whole project and later only the changes, in one command.

## Commands

```shell
# UP: local folder to fortrabbit
rsync -av ./web/uploads/ {{app-env-id}}@ssh.{{region}}.frbit.app:web/uploads/

# DOWN: fortrabbit to local folder
rsync -av {{app-env-id}}@ssh.{{region}}.frbit.app:web/uploads/ ./web/uploads/
```

The first path is the source, the second the destination. A remote path is `user@host:folder`, relative to the home folder of the environment. A trailing `/` on the source copies the content of the folder, without it rsync copies the folder itself into the destination.

| Option | Effect |
| -- | -- |
| `-a` | Archive: recursive, keeps links, permissions and times |
| `-v` | Lists the transferred files |
| `-n` | Dry run, shows what would happen |
| `-z` | Compresses data during the transfer |
| `--exclude` | Skips matching files |
| `--delete` | Deletes files in the destination that are not in the source |

See the [rsync man page](https://download.samba.org/pub/rsync/rsync.1) for all options.

## Preview with a dry run

Add `-n` to any command. rsync lists what it would transfer or delete and changes nothing:

```shell
rsync -avn ./web/uploads/ {{app-env-id}}@ssh.{{region}}.frbit.app:web/uploads/
```

## Exclude files

```shell
rsync -av --exclude '*.jpg' --exclude '/cache' ./ {{app-env-id}}@ssh.{{region}}.frbit.app:
```

A pattern without a leading `/` matches anywhere in the path, with `/` only from the root of the source. Keep a longer list in a file and pass it with `--exclude-from=.rsyncignore`.

## Delete obsolete files

By default rsync never deletes. With `--delete`, files that are missing in the source are deleted in the destination. Always run it with `-n` first:

```shell
rsync -avn --delete ./web/uploads/ {{app-env-id}}@ssh.{{region}}.frbit.app:web/uploads/
```

`--delete-after` deletes only after all new files are in place, which keeps a live site complete during the sync.

## SSH options

Pass SSH options with `-e`, for example a specific key:

```shell
rsync -av -e 'ssh -i ~/.ssh/other_key' {{app-env-id}}@ssh.{{region}}.frbit.app:web/uploads/ ./web/uploads/
```

## Further reading

- [How rsync works](https://rsync.samba.org/how-rsync-works.html)
- [Deploying code with rsync](https://blog.fortrabbit.com/deploying-code-with-rsync), the older and longer blog post
