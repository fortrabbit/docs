---
updated: 2026-10-23
reviewed: 2026-10-23
reviewer: fl
title: Git intro
description: 'A short introduction to git, what version control does, how to install it and where to learn the commands for deploying to fortrabbit.'
naviTitle: Git intro
navigation.excerpt: Install, learn, enjoy
figure:
  emoji: 🌱
  text: Master version control.
  color: rgb(40, 100, 40)
  textColor: rgb(209, 250, 229)
lead: Git tracks every change to the code and, on fortrabbit, deploys it with a git push. Where to learn it, how to install it, and what stays out of the repository.
head:
  meta:
    - name: 'keywords'
      content: 'git, git basics, version control, ssh key, fortrabbit, learn git'
topics:
  - git
---

## About Git

Git is a distributed version control system. It records every change to the files of a project, so changes can be reviewed, undone and merged between people working in parallel on branches. Git is free and runs on the command line or in a [desktop GUI](/4.integrations/07.git-clients/01.intro.md).

On fortrabbit, Git also carries the code to the environment: a `git push` deploys, see the [git push deploy tutorial](/3.dev/15.learn/git-push-deploy.md).

## Learn Git

Know `commit`, `push`, `pull` and branches before deploying with Git. Good starting points:

- [GitHub quickstart](https://docs.github.com/en/get-started/quickstart)
- [Git documentation and the Pro Git book](https://git-scm.com/doc)
- [Learn Git Branching](https://learngitbranching.js.org/), interactive in the browser
- [Git Tower guides](https://www.git-tower.com/learn)
- [Atlassian Git tutorials](https://www.atlassian.com/git)

## Install Git

Check with `git --version` in a terminal. macOS asks to install the command line tools on first use, Linux distributions ship it or have it as a package. On Windows, install it from [git-scm.com](https://git-scm.com/downloads), which includes Git Bash.

## Git and GitHub

Git is the tool, [GitHub](https://github.com) is a service that hosts Git repositories and adds pull requests, issues and actions. fortrabbit deploys from GitHub, see the [GitHub integration](/4.integrations/03.git-providers/02.github.md) and [other Git providers](/4.integrations/03.git-providers/01.intro.md).

## Keep the repository small

Git keeps every version of every file in the hidden `.git` folder, deleted files included. Large binary files such as images, videos and uploads bloat the history for good and make cloning and deploying slow. Keep the repository to code and small layout assets like icons. Uploads and content stay out, see the [deployment intro](/1.platform/06.deployment/01.intro.md) on how code and content stay separate.
