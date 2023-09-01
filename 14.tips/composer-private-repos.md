---
reviewed: 2023-08-17 22:07:15
title:    Composer private repos
excerpt:  Access during git deployment
lead:     How to access private composer repositories during git deployment.
head:
  meta:
    - name: 'keywords'
      content: 'Composer, Git, ssh, GitHub, Bitbucket, auth.json, oAuth'
---

<!-- TODO: Review and finish. -->

<!--

2023-08-30 14:14:43 

-->

## What are private Composer packages?

Modern PHP app development utilizes [Composer](/14.tips/composer.md) as a dependency manager. There are many great open source packages [out there](http://packagist.org). But your company code is probably not intended to be released to the public or you rely on a third party package which is not open source. That's when you use private Composer repositories.

## A - Using SSH Keys

<!-- 2023-08-30 14:17:25 - TODO: there is a key installed with each app environment (and it could be visible with the dashboard as well.)  -->

Alternatively you can limit access to a specific SSH keys. To use your private Composer repo in [Git deployment](/6.deployment/1.intro.md) you need to set up authentication so your fortrabbit app can access your external repo (probably hosted on GitHub). For this you need a public and private SSH key-pair.

The private key will be stored in the deployment environment of your App that composer can use it but nobody else. The command shows the public key, in the example is starting with `ssh-rsa AAA...` and ending with `..odTimp`. You can now install the key in your private git repository. You can re-run this command at any time to view or change the current key of your app.

## B - Using oAuth or HTTP Basic Auth

In the script below we generate a global `auth.json` file that contains credentials to access a GitHub repo using oAuth, and another private repo which is protected with Basic HTTP auth, in our example Laravel Nova. This is just for the sake of demonstration, you will probably need to adjust it to your needs.

Since you don't want to keep secrets in your git history, you can store them in [ENV vars](/11.concepts/env-vars.md).

```php [add-auth.php]
// Github token example
if ($github_oauth =  getenv("GH_TOKEN")) {
    echo "Configure auth for github-oauth.github.com" . PHP_EOL;
    shell_exec("/usr/local/bin/composer config --global github-oauth.github.com {$github_oauth}");
}

// HTTP basic auth example
if (getenv("NOVA_USER") && getenv("NOVA_PASS")) {
    $nova_username = getenv("NOVA_USER");
    $nova_password = getenv("NOVA_PASS");
    echo "Configure auth for http-basic.nova.laravel.com" . PHP_EOL;
    shell_exec("/usr/local/bin/composer config --global http-basic.nova.laravel.com {$nova_username} {$nova_password}");
}
```

<!-- TODO: Below will be build step  -->

<!-- The script you created needs to be executed before Composer tries to install packages. Create a fortrabbit.yml file with the following structure:

```yaml
version: 2
pre: add-auth.php
``` -->

Additionally, you need to set the `COMPOSER_HOME` env var and the env vars you use in the script in the dashboard:

```yaml
COMPOSER_HOME=/tmp/.composer
GH_TOKEN= ...
```

After deploying the two files you are set to access your private repos.

### Link your private repo

Now you can add your private repositories to your `composer.json` file as usual:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url":  "git@github.com:my-company/my-package.git"
    }
  ],
  "require": {
    "my-company/my-package": "^1.2.3"
  }
}
```
