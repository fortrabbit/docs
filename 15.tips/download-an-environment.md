---
reviewed: 2023-08-25 16:20:40
title: Download an environment
navigation.excerpt: Get all data to have it running locally
lead: 'This article helps you downloading all the application data required directly from our services to run it elsewhere. Tech skills are required to do this.'
---

## Get ready

We highly advice to have your application or website in a local development environment running all the time. Your development setup should also be where development happens first and which is kept up-to-date in terms of contents. Please see [local development article](/15.tips/local-development.md) for more.

## Use cases

But there are some real world scenarios why downloading the remote App might still be required:

- A new developer is joining the project
- A previous developer has left without transferring the project
- Your hard disk crashed
- You have accidentally deleted your local setup somehow
- Archiving your project before shutting it down
- Moving away to a different hosting provider

## Downloading the fortrabbit environment data directly

Your environment on fortrabbit consists of different parts that play together to display a functional website or application. The different parts need to be treated separately. The steps required are depending on your previous deployment workflows. Choose what matches best for you:

### Code via Git

When you deployed by Git here before, you can clone the existing Git repo from fortrabbit. Please follow the steps in our [Git guides](/6.deployment/1.intro.md) to clone down the code. The benefit is that the Git repo contains all the history of the project as well. Make sure that the Git repo is an up-to-date state.

### Composer dependencies

After cloning the Git repo, you might need to install the dependencies to make your local installation complete. The `composer.json` contains all the instructions. Run `composer install` locally in your root folder. See our [Composer article](/15.tips/composer.md) for more details.

### Runtime data excluded by Git

Beside the code base which you might have received via Git, take care to grab assets and runtime data as well. This can be some compiled CSS/JS files that got deployed along with pipelining or uploads done by users of the application.

#### Receiving assets and other files

Remember Git works in [one direction only here](/6.deployment/1.intro.md#git-works-only-one-way). So you might find files, like uploads, that are not covered with the Git repo, or files in the Git repo are not up-to-date. Options on your disposal:

- Login by SFTP and just download what is required - [see here](/7.code-access/4.sftp.md)
- Login by SSH, zip the files and question and them from a public URL - [see here](/7.code-access/3.ssh.md)
- Use rsync to download a folder or even the entire project - [see here](/15.tips/rsync.md)

You can use the methods above for the whole code base when you haven't been deploying with Git before or you are unsure if the git repo contains the latest changes.

### MySQL

Last not least you likely will need the contents of your database. Use a local MySQL client to connect to your fortrabbit database and export a dump of it. Detailed instructions over [here](/8.mysql/2.access.md).

## Using our backups

When the above is not working for you for some reason, you might just use our backups (when booked) as a source. With that you can download the latest state (yesterday) as two files: code and MySQL database directly from the Dashboard. Please understand that this does not include the Git repo but just the files deployed and generated on the App itself. For Pro Apps backups are only optionally available for MySQL, since code is fully covered with Git.

## Check for data consistency

We highly advice to double-check your new backup for completeness. You can run diffs on other copies. We also advice to run your App locally and see it with your eyes.

## Contact us

If in doubt, don't hesitate to contact us. We are here to give technically guidance and help. Please mind fortrabbit is self service for developers. We might not be able to assist the non-technical business owner with this.
