---
reviewed: 2025-09-22 09:20:31
title: Using Secure Copy
naviTitle: SCP
navigation.excerpt: Using secure copy for file transfers
figure:
  emoji: 🔐
  text: Copy files over SSH.
  color: rgba(91, 33, 182, 1)
  textColor: rgba(237, 233, 254, 1)
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
---

## About SCP

`scp` (Secure Copy Protocol) is a command-line utility for securely transferring files between a local host and a remote host over SSH. It provides the same authentication and security as SSH while enabling efficient file copying operations.

- Encrypted file transfers using SSH
- Preserves file permissions and timestamps
- Supports recursive directory copying
- Works with SSH key authentication
- Available on most Unix-like systems (Linux, macOS)

::CallOut{alert}
We suggest to use [rsync](/3.dev/20.how-to/rsync.md) instead of scp. It's more flexible with more features. It can upload directories.
::

## Get ready

Before using SCP with fortrabbit, ensure you have:

1. **SSH access configured** - See [SSH access guide](/1.platform/04.code-access/03.ssh.md)
2. **SSH key pair set up** - See [SSH key setup](/3.dev/15.learn/01.ssh-key-setup.md)
3. **SCP installed** - Usually pre-installed on Linux/macOS, via WSL on Windows

```shell
which scp
# If installed, it will show the path
```

:BlockLink{title="See SSH access for {{app-name}} / {{env-name}}" path="/environments/{{app-env-id}}/ssh/"}

## Examples

```bash
# Upload

## Upload a file to the web root
scp local-file.php {{app-env-id}}@ssh.{{region}}.frbit.app:

## Upload with verbose output
scp -v config.json {{app-env-id}}@ssh.{{region}}.frbit.app:

## Upload multiple files at once
scp file1.php file2.css file3.js {{app-env-id}}@ssh.{{region}}.frbit.app:

## Upload with wildcards
scp *.php {{app-env-id}}@ssh.{{region}}.frbit.app:


# Download

## Download a file from the web root
scp {{app-env-id}}@ssh.{{region}}.frbit.app:config.php ./

## Download to a specific local path
scp {{app-env-id}}@ssh.{{region}}.frbit.app:.env ./local-config/

## Download log files (Craft CMS)
scp -r {{app-env-id}}@ssh.{{region}}.frbit.app:storage/logs/ ./
```

### Common options

- `-r` - Recursive copy (for directories)
- `-p` - Preserve file permissions and timestamps
- `-v` - Verbose output for debugging

## Comparison with other tools

| Feature                 | SCP           | SFTP          | rsync         |
| ----------------------- | ------------- | ------------- | ------------- |
| **Security**            | SSH encrypted | SSH encrypted | SSH encrypted |
| **Resumable transfers** | No            | Yes           | Yes           |
| **Bandwidth limiting**  | Yes           | Limited       | Yes           |
| **Directory sync**      | Basic         | Manual        | Advanced      |
| **Progress indication** | Limited       | Yes           | Yes           |
| **File comparison**     | No            | Manual        | Automatic     |
