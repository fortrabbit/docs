---
reviewed:      2023-08-30 13:54:22
title:         Directories
lead:          The app environment directory structure on fortrabbit.
excerpt:       Default folder structure
hideExamples:  yes
head:
  meta:
    - name: 'keywords'
      content: 'folder, directory, directories, linux, unix, web root, doc root, document root' 
---

```raw
bin
dev
etc
lib64
proc
tmp
usr
srv
  app
    htdocs      < default root path
    home        < bash history …
```

When you login with [SFTP](/7.code-access/4.sftp.md) or [SSH](/7.code-access/3.ssh.md) to your [app environment](/10.objects/2.app-environment.md) you can see the file directory structure. In this article you can learn the predefined set of folders and what they are for.

## htdocs

The default web root (aka document root) directory is the main tree 'visible' from the web. You can change the routing root path, to any folder below the `htdocs` directory. The [git deployment](/6.deployment/1.intro.md) syncs to the `htdocs` folder as well. `htdocs` is also your 'login folder' - starting point for SSH/SFTP. The whole path looks something like this: `/srv/app/{{app-env-slug}}/htdocs/admin`.

## tmp

Temporary folder; limited to 2GB of storage. Files older than 15 days will be automatically purged. Typical use cases are the default PHP session file folder or a temp destination for file uploads via PHP (before `move_uploaded_file()` is called).

## home

Like your `~` on your local machine. Contains bash history, private SSH keys.

## Other folders

The rest of the folders (and files which are not shown here) are part of the standard Linux distribution. All this stuff is handled by us for you. So you don't need to care about them. You can't change things outside the above outlined context.
