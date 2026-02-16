---
reviewed: 2026-02-13
title: rsync deployment
naviTitle: rsync
navigation.excerpt: Copy and sync like a boss
figure:
  emoji: rsync
  text: Sync only what changed, fast and safe.
  color: rgb(2, 132, 199)
  textColor: rgb(224, 242, 254)
lead: rsync is one of the best ways to deploy code fast and without hassle. It's also an often overlooked option. Let's change this! This article gives you some direction on how to use it in general and especially here on fortrabbit.
---

## About rsync

`rsync` is a shorthand for **r**emote **sync**hronization. It's a command line tool to synchronize files over the network. It's open source. It's old but really good and it's up to **10 times faster than FTP** as it uses compression and diffs to only transfer changes. rsync is a mighty sharp sword. Use it carefully. Please mind that providing the falsy parameters or the wrong order can result in data loss. rsync works on top of [SSH](/1.platform/04.code-access/03.ssh.md). Usually, like most deployment related tasks here, you will **use rsync from your local machine**, not on your fortrabbit environment directly.

## Installing rsync

Chances are that you already have it: **rsync is built-in with Linux and macOS**. Check if it is installed. Run this command in the Terminal of your local machine:

```shell
rsync --version
# If installed, it will output the version number.
```

For Windows 10 we recommend to install the Linux subsystem (WSL). For Windows 7 or even below you might use cwRsync which also requires Cygwin. There are some other clones and desktop GUI clients around as well. But don't be afraid of the Terminal, it's easier than you might think.

## Use cases

You can [deploy with Git](/1.platform/05.deployment/01.intro.md) or [upload files with SFTP](/1.platform/04.code-access/04.sftp.md) and/or [use SSH](/1.platform/04.code-access/03.ssh.md). Hook in rsync, either as an enhancement or as a replacement. These are your main options for using `rsync` to deploy code:

### rsync instead of SFTP

Consider `rsync` as a replacement for SFTP. With SFTP - unless your SFTP client has some kind of synchronization method (which still will be slower) - you will copy each file manually, one by one. This is mundane and can also be dangerous when forgetting to copy critical files. `rsync` can work as a two way street directly on the file system. Easily synchronize files up and down from your [local development](/4.integrations/01.local-development/01.intro.md) to the [environment](/1.platform/10.objects/02.environment.md).

### rsync in addition to Git

Consider `rsync` as an essential addition. Why? Your dependencies are managed with Composer and thus excluded from Git. They will be installed and managed with [Composer](/3.dev/15.learn/02.composer.md). So you are keeping your Git repo clean by just including the source files of your very own code. But there is more. Your project includes run time data and static assets:

## The rsync command structure

```shell
# sync all files UP
#
#      options
#       ─┴─
$ rsync -av ./ {{app-env-id}}@ssh.{{region}}.frbit.app:
#           ─┬─ ──────────────────┬────────────────────────
#          source           destination
```

- **options**: How to sync, see [below](#options).
- **source**: This is your local source directory.
- **destination**: The target URL, where the files should end up.

## Usage

Here are the most common rsync commands. Likely you will even come by using only the first two:

```shell
# DOWN: from remote to local
$ rsync -av {{app-env-id}}@ssh.{{region}}.frbit.app: ./

# UP: from local to remote
$ rsync -av ./ {{app-env-id}}@ssh.{{region}}.frbit.app:


# LOCAL: two local folders
$ rsync -av ~/projects/{{app-env-id}}/ ~/projects/{{app-env-id}}.copy/

# REMOTE TO REMOTE: from App to App
$ rsync -av {{app-env-id}}@ssh.{{region}}.frbit.app: {{app-name-2}}@ssh.{{region}}.frbit.app:
```

### Remote paths

Remote URLs consist of `{{user}}@{{host}}:{{folder}}`. In the examples here fortrabbit placeholders are used.

### Local paths

rsync accepts all ways to define local paths. `./` will translate to the current directory. You can also use absolute paths like `/home/your-user/projects/{{app-env-id}}` or relative paths like `../{{app-env-id}}`.

### Options

Here are some common options to alter the sync mode:

| Option      | Description                                                                                                                                       |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| `-a`        | Shorthand for `--archive`, like the set of options: `-rlptgoD`.                                                                                   |
| `-v`        | Verbose output shows all transmitted files and statistical data. Increase verbosity using `-vv` or `-vvv`                                         |
| `-n`        | Shorthand for `--dry-run`. See [below](#previewing-changes).                                                                                      |
| `-r`        | Recursive, so all files and directories below the source directory.                                                                               |
| `-l`        | Keep symbolic links.                                                                                                                              |
| `-p`        | Permissions will be synchronized.                                                                                                                 |
| `-t`        | Preserve modification times.                                                                                                                      |
| `-g`        | Set Unix group of file/folder on destination to group in source. Also: use group as check criteria                                                |
| `-o`        | Set Unix group of file/folder on destination to group in source. Also: use group as check criteria                                                |
| `-c`        | Instead of modification time and size, use checksum of the file contents. Use with caution when modification time on destination is not reliable. |
| `-C`        | Shorthand for `--cvs-exclude`. Exclude version control files like `.git`, `.hg`, `.svn`.                                                          |
| `-h`        | Human readable output: display byte sizes in MiB, GiB instead of plain bytes.                                                                     |
| `--delete`  | Remove unused files. See [below](#dealing-with-obsolete-files)                                                                                    |
| `--exclude` | Omit files from being synced. See [below](#excluding-files)                                                                                       |

For an exhaustive list of all the possible options and more in depth info on the above options, check out the official [rsync man page](https://linux.die.net/man/1/rsync). Mind that rsync options can be chained, `rsync -av` combines the two flags `-a` and `-v`.

### Previewing changes

The handy `--dry-run` option can be shortened to just `-n` and also be merged with other options to something like `-avn`. It will give you a preview of what will happen before doing anything:

```shell
$ rsync -avn ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/
sending incremental file list
./
index.php
wp-content/themes/your-theme/404.php
wp-content/themes/your-theme/archive.php
wp-content/themes/your-theme/content-link.php

sent 39,119 bytes  received 196 bytes  11,232.86 bytes/sec
total size is 23,325,044  speedup is 593.29 (DRY RUN)
```

Now, running this will print out everything that `rsync` **would** transfer - without doing anything. Better always execute a dry run before actually syncing. Once you're sure, that only files which you want to transfer are in the change set, you can just remove the `n` again from the options and execute it normally.

### Syncing single folders

This is a use-case for rsync as an additional step when primarily working with Git. In this case you only want to include a specific folder and its contents. You might want to "upload" your `dist` folder with your compiled CSS, JS and images. Or you want to "download" the assets folder, when an editor has uploaded new images to the CMS. This is the basic command:

```shell
rsync -av --include='/{{folder}}/***' --exclude='*' ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/
```

With the `--include` parameter you can specify the path to include, but you still need to exclude everything else. The include/exclude syntax is flexible as you can include patterns and multiple folders at once. Alternatively you can also just define the local folder and the remote folder.

### Excluding files

Sometimes you want to omit files from being synced. You can just add `--exclude=path/to/file`. Say we don't want the `404.php` from the previous example to be transferred, you would just do:

```shell
# use absolute path, as viewed from the source root
$ rsync -avC --exclude wp-content/themes/your-theme/404.php ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/
```

The value of `--exclude` is a pattern. It can be matched against the files to be transferred. In this case, the following patterns will have the same effect:

```shell
# use partial path
$ rsync -avC --exclude themes/your-theme/404.php ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/

# use smallest possible partial path
$ rsync -avC --exclude 404.php ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/
```

NOTE: The initial `/` character is important. `--exclude 404.php` and `--exclude /404.php` are _not_ the same. The former means: Any path which contains "404.php" is to be excluded. The latter means: Any path which starts with "/404.php" is to be excluded.

### Advanced exclude patterns

You can also use wildcard characters. For example:

```
$ rsync -av --exclude "*.jpg" --exclude "*.jpeg"` ...
#  exclude all JPEG files

$ rsync -av --exclude "/wp-content/themes/*/404.php" ...
# exclude all files, which start with `/wp-content/themes`, followed by an arbitrary name (no slashes! so only one level of sub directory!) and ending in `404.php`. So basically: All `404.php` files of all themes.

$ rsync -av --exclude "themes/**/*.css" ...
# exclude all files, which path name contains `themes/` then followed by anything (including any amount of sub directories) and ending in `.css`. So all `.css` files in all Themes.
```

Also, as you can see, in the JPEG example, you can add any amount of `--exclude` options to the command.

### Remembering excludes in a file

If you have a set of files which you always want to exclude, you can create an file containing all exclusions and then use it via `--exclude-from <file>`:

```shell
# add two excludes to a plain text file named ".rsyncignore"
$ echo 404.php >> .rsyncignore
$ echo something-else.php >> .rsyncignore

# run rsync, using the .rsyncignore file
$ rsync -av --exclude-from .rsyncignore ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/
```

NOTE: The file name `.rsyncignore` is just an example name, use any name you want for your excludes.

There is still a lot more you can do with exclude and filtering. Not only is there `--include`, which allows to granulate previous `--exclude` patterns, but there is also `--filter`. Here is a [very interesting blog post by Ira Cooke](http://blog.mudflatsoftware.com/blog/2012/10/31/tricks-with-rsync-filter-rules).

### Dealing with obsolete files

`rsync` will work in a non-destructive way by default, like our overwrite but not delete strategy. So new files will be written and replaced, but old files will not get deleted. Sometimes that's not what you want. Sometimes you want an exact copy - a mirror.

So, how to remove obsolete files on the remote? The short answer is: add the option `--delete` to your command line and you are done. To give you and example, using the WordPress setup from before: say you deleted this pesky `404.php` file locally. Now, if you run `rsync` without the `--delete` option (and no other added or modified files), `rsync` would tell you that it will do nothing:

```shell
$ rsync -av ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/
sending incremental file list
wp-content/themes/your-theme/

sent 39,037 bytes  received 162 bytes  15,679.60 bytes/sec
total size ...
```

Although it marks the folder `wp-content/themes/your-theme/`, as if there have been changes (the removal of `404.php`), rsync will not apply any changes. Now, if you run it with the `--delete` option, the file will be removed from the destination. **This is a feature, not a bug**, meaning: `rsync` won't let you down by deleting files without your say-so. Either way, on the first delete run, as always, use the condensed form `-n` of the `--dry-run` option, to show you exactly what would be deleted:

```shell
$ rsync -avn --delete ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/
sending incremental file list
deleting wp-content/themes/your-theme/404.php

sent 39,062 bytes  received 231 bytes  15,717.20 bytes/sec
total size ...
```

After you confirm that `rsync` will only delete what you want (otherwise: `--exclude` works also to exclude files which are not in your local file set but remote, and you don't want to remove them from remote), you can go ahead and remove the `-n` option and run again.

`rsync` even gives you four different ways to handle deletes: Besides the `--delete` flag, there is also `--delete-before`, `--delete-after`, `--delete-during` and `--delete-delay` (and `--delete-excluded`, but that's another special case of its own). Those four variants of `--delete` just let you control when files are removed. This is actually quite handy: When dealing with larger amounts of changed files to a live website, you might want to use `--delete-after` instead of `--delete-before`, so that first all new files are in place, then obsolete files are removed, which makes it more likely that your website is not "interrupted" when handling a request during the synchronization, which relies on files which would be removed.. I think you get the gist.

## Advanced topics

### SSH edge-cases

Should you need to set specific SSH options, for example, if you need to provide a specific private key, then you can use the `--rsh` option, which stands for "remote shell" and can be shortened to `-e`. Here an example:

```shell
# use specific private key
$ rsync -av -e 'ssh -i /path/to/your/key' {{app-env-id}}@ssh.{{region}}.frbit.app:~/ ./

# enforce password authentication
$ rsync -av -e 'ssh -o PreferredAuthentications=password' {{app-env-id}}@ssh.{{region}}.frbit.app:~/ ./
```

### How rsync transfers only changes

Say you have changed ten files in your local code set and want to deploy them now. `rsync` will first build a local set of files and directories and a remote set of files and directories. For each item in either set it will generate a check value. This check value, can be either the timestamp of the last change of a file, the size of a file, the current permissions or even a checksum (think MD5) of the file contents. Or any combination of those. Using the `-a` option rsync is gonna use timestamp + file size which is a good balance between performance and accuracy.

## Further reading

This article is loosely based on our still popular [blog post](https://blog.fortrabbit.com/deploying-code-with-rsync) which is even more complete and includes more details. Also of interest:

- [Manual page of rsync](https://linux.die.net/man/1/rsync)
- [How does rsync work](https://rsync.samba.org/how-rsync-works.html)
