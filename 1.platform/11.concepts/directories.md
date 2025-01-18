---
reviewed: 2024-10-30 15:18:24
naviTitle: Directories
title: Directory structure
navigation.excerpt: Default folder organization
hideExamples: yes
head:
  meta:
    - name: 'keywords'
      content: 'folder, directory, directories, linux, unix, web root, doc root, document root'
---

When you login with [SFTP](/3.dev/7.code-access/4.sftp.md) or [SSH](/3.dev/7.code-access/3.ssh.md) to your [app environment](/1.platform/10.objects/2.app-environment.md) you can see the file directory structure. This is what you'll find:

```raw
srv
  data
    www
    home
```

## www

The default web root (aka document root) directory is the main tree 'visible' from the web. You can change the routing [root path](/1.platform/11.concepts/root-path.md), to any folder below the `htdocs` directory. The [git deployment](/6.deployment/1.intro.md) syncs to the `htdocs` folder as well. `htdocs` is also your 'login folder' - starting point for SSH/SFTP. The whole path looks something like this:

- `/srv/data/www`

<!-- ## tmp

Temporary folder; limited to 2GB of storage. Files older than 15 days will be automatically purged. Typical use cases are the default PHP session file folder or a temp destination for file uploads via PHP (before `move_uploaded_file()` is called). -->

## home

Like your `~` on your local machine. Contains bash history, private SSH keys.

- `/srv/data/home`

<!-- ## Other directories

The rest of the folders (and files which are not shown here) are part of the standard Linux distribution. All this stuff is handled by us for you. So you don't need to care about them. You can't change things outside the above outlined context. -->
