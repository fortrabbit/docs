---
reviewed: 2026-02-13
title: Git intro
naviTitle: Git intro
navigation.excerpt: Install, learn, enjoy
figure:
  emoji: 🌱
  text: Master version control.
  color: rgb(40, 100, 40)
  textColor: rgb(209, 250, 229)
lead: This is a quick intro to Git, how to set it up and how to get started with it on fortrabbit.
head:
  meta:
    - name: 'keywords'
      content: 'ssh key, public key, git, ssh, Putty, msysGit, Cygwin, Windows, Git Bash'
---

## About Git

Git is a distributed version control system. It's quite popular to work with text files — hence in software development. It's fast, assures data integrity and supports non-linear workflows (branching). Git was developed by Linux kernel developers (including Linus Torvalds). It's free and can be used either from the command line or via graphical user interfaces.

Git can help you to collaborate on code projects, keep track of your code changes and rollback to points in time, if needed. It comes with:

- A history of all files included, so you can review or undo changes
- Powerful file merging which makes collaboration easy

On fortrabbit, Git also doubles as the deployment transport — the [git push deploy tutorial](/3.dev/15.learn/git-push-deploy.md) shows that workflow. Git should be part of the [local development setup](/4.integrations/01.local-development/01.intro.md).

## Learn Git

You should be familiar with Git standard operations and concepts — these are: `commit`, `push` and `pull`. If you don't know Git, yet, we recommend to go ahead and learn the basics. You will profit from it either way — whether you keep using fortrabbit or not. It's a cornerstone of todays software development. For developers not used to the shell it might not be very intuitive to start with, but once you got started it soon becomes very, very handy for all kinds of things besides deploying to fortrabbit. There are many good tutorials out there in the interwebs to get started. For example:

- [GitHub: Quickstart](https://docs.github.com/en/get-started/quickstart)
- [Official docs from Git SCM](https://git-scm.com/doc)
- [Try Git in your browser for free](https://try.github.io/levels/1/challenges/1)
- [Guides & ebook from Git Tower](https://www.git-tower.com/learn)
- [Get Git right from Atlassian](https://www.atlassian.com/git)
- and [many more](http://lmgtfy.com/?q=learn+git)

## Install Git

To use Git, you need to have it installed on your local machine. You might already have Git: open a terminal window and type `git --version`. Good news for macOS and Linux users: you most likely already have it installed.

### Git on Windows

You can work it out. The primary problem you have to solve is: which Git distribution are you going to use. There are multiple of those floating around, we recommend to download and install Git from the **[official Git website](https://git-scm.com/downloads)**. This one comes with the "Git Bash".

## The hidden .git folder

Git never forgets. It can bring back any content from any file, even deleted ones. To do so, it stores all the stuff in the hidden `.git` folder at the top level of the repo. Over time that file can get big too. It can also contain unreachable blobs and other stuff you are not aware of. Depending on the situation, there are many ways to clean this up: delete files of a certain type, delete the history before a certain date, or even start again from the current state.

## Git desktop GUIs

Most people probably use Git from the command line (aka bash, terminal, shell). But there are also GUIs (desktop Apps) to manage Git. Those help to get started and to see visually what's going on:

- [Git desktop GUIs](/4.integrations/07.git-clients/01.intro.md)

## About GitHub

You hopefully already know that [GitHub](https://github.com) is the most popular choice for versionized code hosting and collaborating. It is free to use with private and public projects. Sometimes people confuse Git with [GitHub](https://github.com). Git is the version control system established by Linus Torvalds. GitHub is the service, which offers Git remote hosting and additional extra magic collaboration features. GitHub has extended Git workflows with neat communication tools around the basic Git usage. Most notable is the "pull request" workflow.

See our [GitHub integration guide](/4.integrations/03.git-providers/02.github.md).

## Large Git repos

A bloated Git repository is slow to clone, push, and pull. In most cases the repo can and should be small.

## Large files in Git

Big binary files (> 2 MiB) do not belong in a Git repo. The same goes for most assets — images, videos, uploads. A small SVG that is part of the website layout is fine; a folder full of content images is not. Since Git never forgets, every large file bloats the history forever, even after deletion. Keep the repo to code; the [deployment intro](/1.platform/05.deployment/01.intro.md) explains how code and content stay separated on fortrabbit.
