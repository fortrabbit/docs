---
reviewed: 2024-12-18 19:51:23
title: How to download a full website
naviTitle: Download a website
navigation.excerpt: Get all data to have it running locally
lead: This guide explains how to download all necessary application data from a hosting provider to run a website elsewhere. Technical skills are required.
---

## Get ready

It's assumed that you have access to your hosting provider. We recommend maintaining a local development environment for your website. Development should occur locally first, and the local copy should be kept up-to-date. For more information, see our [local development article](/3.dev/20.how-to/1.local-development.md). That means, under normal situations the developer should always have a working copy of the website running locally already.

## Use cases

But there are some real world scenarios why downloading a website might still be required:

- A new developer is joining the project
- A previous developer has left without transferring the project
- Your hard disk crashed
- You have accidentally deleted your local setup somehow
- Archiving your project before shutting it down
- Moving away to a different hosting provider

## Downloading data directly

A hosting environment of a typical LAMP stack PHP setup consists of different parts that play together to display a functional website or application. The different parts need to be treated separately. The steps required are depending on your previous deployment workflows.

### Code by Git

When you deployed using Git, you can clone the existing Git repo. Most likely your Git repo is hosted on GitHub. The benefit is that the Git repo contains all the history of the project as well. Make sure that the Git repo is an up-to-date state.

### Composer dependencies

After cloning the Git repo, you might need to install the dependencies to make your local installation complete. The `composer.json` contains all the instructions. Run `composer install` locally in your root folder. See our [Composer article](/3.dev/15.learn/02.composer.md) for more details. This insures the installed dependencies are up-to-date and match you local development environment.

### Runtime data

Beside the code base which you might have received via Git, take care to grab assets and runtime data as well. This can be some compiled CSS/JS files that got deployed along with pipelining or uploads done by users of the application.

### Assets and other files

Remember Git works in [one direction only here](/1.platform/05.deployment/01.intro.md#git-works-only-one-way). So you might find files, like uploads, that are not covered with the Git repo, or files in the Git repo are not up-to-date. Options on your disposal:

- Login by SFTP and just download what is required - [see here](/3.dev/01.code-access/4.sftp.md)
- Login by SSH, zip the files and question and them from a public URL - [see here](/3.dev/01.code-access/3.ssh.md)
- Use rsync to download a folder or even the entire project - [see here](//3.dev/20.how-to/rsync.md)

You can use the methods above for the whole code base when you haven't been deploying with Git before or you are unsure if the Git repo contains the latest changes.

### Database backup

Last not least you likely will need the contents of your database. Use a local MySQL client to connect to your fortrabbit database and export a dump of it. Detailed instructions over [here](/8.database/2.access.md).

## Using our backups

When the above is not working for you for some reason and your website is hosted with fortrabbit, you might just use our [backups](/1.platform/09.components/05.backups.md) (when booked) as a source. With that you can download the latest state from the dashboard.

## Check for data consistency

We highly advice to double-check your new backup for completeness. You can run diffs on other copies. We also advice to run your App locally and see it with your eyes.
