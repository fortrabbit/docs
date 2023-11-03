---
reviewed: 2023-08-30 18:19:13
title:    PHP version upgrade
navigation.excerpt:  Switch to a new version with confidence
lead:     Best practices upgrading the PHP version.
head:
  meta:
    - name: 'keywords'
      content: 'app-design, deprecation, migration, EOl, mcrypt'
---

## PHP versions at fortrabbit

* fortrabbit will provide new PHP versions some time after they became available
* New PHP versions are available to select per app environment in the dashboard
* There are usually multiple PHP version to choose from
* You need to update software you are using
* You can opt-out of automatic PHP version updates
* Outdated PHP versions will be removed, remaining app environments will be upgraded then

## Simple PHP version upgrade path

1. Make sure the software you are using is up-to-date
2. In the [dashboard](/11.concepts/dashboard.md)
3. Navigate to the app environment and then click on Settings > PHP version
4. Change to a newer PHP version and hit "save"
5. Check if your website is still working after a few minutes
6. You can safely switch back the version if it doesn't work

:DashboardLink{title="Change the PHP version for {{app-env-slug}}" path="/environments/{{app-env-slug}}/settings/php-version"}

This will update the PHP runtime on fortrabbit. You may also want to update your local development environment as well, read on.

## Sophisticated PHP version upgrade path

First update your local version, once that is working, deploy to fortrabbit and change the version. Here are the steps one by one:

### 1 - Update your local development environment

We recommend to have a local development environment, also see our [help article on that](/14.tips/local-development.md). First, make sure that your local PHP version is up-to-date. Depending on how your local development is set up, the path to upgrade is different.

If you are running PHP directly on your computer, then a simple `php -v` prints out the PHP version. Beware, if you are using [MAMP](https://www.mamp.info/en/) or [XAMPP](https://www.apachefriends.org/index.html), this is not the version of PHP your code runs on. With these tools you have to use their GUI to select the PHP version you want.

To upgrade your local PHP on macOS, [Homebrew](https://brew.sh/) is a popular package manager you can use. Homebrew also controls the PHP version used by [Laravel Valet](https://github.com/laravel/valet). When you are running a more complex setup with PHP virtualized, such as Vagrant, DDEV, Virtual Box or Docker, you have to dig in to your specific virtualization setup to see how to upgrade PHP.

### 2 - Update your software dependencies

Get your dependencies up-to-date:

#### 2.1 - Updating with Composer

Applications based on PHP frameworks like Laravel and Symfony are usually updated with [Composer](/14.tips/composer.md) which keeps track of all dependencies.

Issuing `composer outdated` in the Terminal will give you a list of outdated packages. Those in red need can easily be updated. Those in yellow also need to be updated but might cause trouble because they are major version upgrades.

You can also ask Composer why you currently can not upgrade to a PHP version:

```shell
composer why-not php 8
```

To update a dependency, simply change any required versions in your `composer.json` to a newer version and then issue a `composer update` to actually install the required updates. Keep in mind that the  `composer outdated` command does not care about PHP versions. It will only tell you about available updates for your dependencies, but hopefully newer packages should support newer PHP versions as well.

#### 2.2 - Updating a CMS

Many Content Management Systems, like WordPress and Craft CMS come with a built in update feature. So you can simply login to the admin area of the CMS and hit a button to update.

**Beware:** With fortrabbit, those changes only happen on the file system and are not reflected in Git. This is fine when you are using SFTP, otherwise read more in our [setup guide for WordPress](/5.guides/5.wordpress.md) or [update guide for Craft CMS](/3.craft/7.updating.md).

### 3 - Test it locally

When you have upgraded your local PHP version as well as your projects dependencies, it's time to make sure nothing is broken. Open your browser and try out as many views and actions as you can in your local development setup. If you are running a lot of custom code you have written yourself, we recommend that you run an automated code analysis. It checks your code and finds any deprecated functions that might break.

### 4 - Go live with the updated version

Now, as everything is up-to-date and tested in your **local** development environment, it's time to bring the updates to fortrabbit.

#### 4.1 - Change the PHP version on fortrabbit

Updating the PHP version for your fortrabbit App is as simple as pie:

1. Visit your app environment in the fortrabbit dashboard
2. Go to the PHP settings
3. Select a newer PHP version from the drop-down menu
4. Hit save

Changes can take two minutes to be applied. You can also test-run this. When your App is not running under the newer version of PHP you can switch back to the deprecated version for another while and find out why first.

:DashboardLink{title="Change the PHP version for {{app-env-slug}}" path="/environments/{{app-env-slug}}/settings/php-version"}

#### 4.2 - Deploy changes

Now, quickly after the new PHP version is in place, deploy your updated code from your local development, either with [Git](//6.deployment/1.intro.md or simply by [SFTP](/7.code-access/4.sftp.md) or by [rsync](/14.tips/rsync.md).

Don't forget that you might also have to run database migrations so that your database structure matches the latest code version. WordPress and Craft CMS automatically handle this in the web UI. For any other system, see their documentation on how to properly update the database.
