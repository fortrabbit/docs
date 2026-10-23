---
created: 2025-09-22
updated: 2026-10-23
reviewed: 2026-10-23
reviewer: fl
title: Using Secure Copy
description: 'scp copies single files between a local machine and a fortrabbit environment over SSH, with the same keys and encryption as a shell session.'
naviTitle: SCP
navigation.excerpt: Using secure copy for file transfers
figure:
  emoji: 🔐
  text: Copy files over SSH.
  color: rgb(91, 33, 182)
  textColor: rgb(237, 233, 254)
lead: SCP (Secure Copy Protocol) enables secure file transfers between your local machine and remote servers using SSH encryption.
links:
  - title: SSH access
    route: /platform/code-access/ssh
    property: docs
  - title: SFTP access
    route: /platform/code-access/ssh
    property: docs
head:
  meta:
    - name: 'keywords'
      content: 'scp, secure copy, file transfer, ssh, command line, upload, download'
topics:
  - ssh
---

## About scp

`scp` copies files between the local machine and the environment over [SSH](/1.platform/05.code-access/03.ssh.md), with the same [SSH key](/3.dev/15.learn/01.ssh-key-setup.md). Linux and macOS ship with it, Windows has it in WSL and in the built-in OpenSSH client.

::CallOut{alert}
For folders and repeated uploads, use [rsync](/3.dev/20.how-to/rsync.md): it transfers only the changes.
::

:BlockLink{title="See SSH access for {{app-name}} / {{env-name}}" path="/environments/{{app-env-id}}/ssh/"}

## Examples

Paths on the environment are relative to its home folder, the project root.

```bash
# Upload a file to the project root
scp local-file.php {{app-env-id}}@ssh.{{region}}.frbit.app:

# Upload several files
scp file1.php file2.css {{app-env-id}}@ssh.{{region}}.frbit.app:

# Download a file to the current folder
scp {{app-env-id}}@ssh.{{region}}.frbit.app:composer.lock ./

# Download a folder
scp -r {{app-env-id}}@ssh.{{region}}.frbit.app:web/uploads ./
```

| Option | Effect |
| -- | -- |
| `-r` | Copies folders recursively |
| `-p` | Keeps modification times and permissions |
| `-v` | Verbose output for debugging the connection |

## scp, SFTP or rsync

| Tool | Use it for |
| -- | -- |
| scp | Single files, one command |
| [SFTP](/1.platform/05.code-access/04.sftp.md) | Browsing and copying in a GUI client |
| [rsync](/3.dev/20.how-to/rsync.md) | Folders, repeated syncs, only the changes |
