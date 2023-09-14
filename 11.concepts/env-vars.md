---
reviewed: 2023-08-18 08:14:49
title:    ENV vars
excerpt:  Using environment variables on fortrabbit
lead:     ENV vars help to create and shape the environment of where the code runs.
head:
  meta:
    - name: 'keywords'
      content: 'ENV vars, Environment variables, php, beginner, phpdotenv, dotenv'
---

<!-- TODO: Review by infra (see comments below as well) -->

## Problem

You most likely run at least two environments of your app: A [local one for development](/14.tips/local-development.md) and one here on fortrabbit for production. Both instances probably have access to a database. Your local MySQL has of course different credentials than the remote one. Your `config.php` file is under Git version control. So how to deal with different environment-specific configurations, from database credentials to API keys? Also, how to work in a team when everyone has it's own local settings? How to separate code from configuration, so that the code is portable and no secrets are shared?

## Solution

Everything specific to the environment should be stored in environment variables or short 'ENV vars'. An ENV var is a key value pair, like so: `MY_SQL_PASS:sCRAmblEDegGGs`. The concept of ENV vars is used by different software systems, like Apache, Node.js, PHP. You can access ENV vars from PHP. And it is a commonly wide spread best practice to do that.

## The .env file

The `.env` file format is a plain text configuration file that lives on top level of your code base. It has `KEY=VALUE` pairs, is easy to write for humans and runtime agnostic. You need an additional parser library, that reads the file and makes the ENV vars accessible from the code base. Here are the most popular .env parsers for PHP:

* [github.com/vlucas/phpdotenv](https://github.com/vlucas/phpdotenv) - Everyone
* [github.com/symfony/dotenv](https://github.com/symfony/dotenv) - Symfony

Modern PHP frameworks like [Laravel](/2.laravel/1.setup.md) and [Symfony](/5.guides/8.symfony.md) …) and some CMS like [Craft CMS](/3.craft/1.setup.md) use `.env` files for configuration and include a parser already.

## ENV vars on fortrabbit

The `.env` file is usually excluded from Git and thus will NOT be [deployed](/6.deployment/1.intro.md). Now, how should your fortrabbit app environment know about it's ENV vars?

* Create an additional `.env` file on the app environment by SSH or SFTP - not recommended.
* **Manage ENV vars in the dashboard** - recommended

The fortrabbit [software preset](/12.platform/software-presets.md) will help. While creating an App on fortrabbit, you'll choose your desired CMS or framework. This selection will configure the server ENV vars in ways, the software can work with it. For example, for Laravel and Craft, the ENV var `DB_PASSWORD` will be populated with the password of the Apps database. For Symfony we provide a ready to use DSN in the `DATABASE_URL` variable. Here is the link to the settings of your App:

So, most likely, your fortrabbit App will work out of the box. As a bonus you even reset the database password without touching any configurations.

## Adding and editing ENV vars on fortrabbit

You can add ENV vars of your App in the [dashboard](/11.concepts/dashboard.md) with the app environment.

:DashboardLink{title="Edit ENV vars for {{app-env-slug}}" path="/environments/{{app-env-slug}}/env-vars"}

The input supports the dotenv file format and allows you to create or update multiple variables at once. The changes will be distributed after you save the page. It may take around 60 seconds.

## Accessing ENV vars from raw PHP

You can access your ENV vars from PHP either using the global variable `$_SERVER` or the function `getenv()`:

```php
echo $_SERVER["MY_ENV_VAR"];
# or
echo getenv("MY_ENV_VAR");
```

## ENV var types on fortrabbit

There are four different kinds of ENV vars here on fortrabbit which are available to your app environment at runtime.

### Custom ENV vars

Those are the ones you add yourself in the dashboard.

### fortrabbit ENV vars

<!-- TODO: Add default ENV vars we know about 2023-08-30 14:01:44  -->

Generic ENV vars cannot be overwritten by you. They are always available.

* `APP_NAME` contains the name of your App

### Software preset ENV vars

Depending on what you have selected in the [software preset](/12.platform/software-presets.md) when creating your App, additional ENV vars will be seeded for you. For example: When choosing Laravel the ENV var `APP_KEY` with a random long string will created (among others). You can replace or remove those stack ENV vars after creation the same way you can replace or remove your manually created ENV vars.

### Dynamic ENV vars

Dynamic ENV vars are automatically updated values that contain access details for services offered by fortrabbit. For example:

```apache
MY_MYSQL=${MYSQL_PASSWORD}
# MY_SQL is your key
# ${MYSQL_PASSWORD} is populated by fortrabbit
```

Dynamic ENV vars will not overwrite existing, manually created ENV vars. This means: if you manually create an ENV var, we guarantee that we won't replace it's value by a dynamically generated ENV var.

### Nested ENV vars

You can use simple, [nested variables](https://github.com/vlucas/phpdotenv#nesting-variables) in your custom ENV vars. Simple means, that you can set variables which reference other variables, which contain a value, for example:

```apache
# will work:
OTHER_VAR=something
MY_VAR=${OTHER_VAR}
```

Order matters. First define something before referencing.

<!-- TODO: Review if multiple levels work. -->

We do NOT support multiple levels of interpolation, which means that you cannot use variables, which reference other variables, which again reference other variables, for example:

```apache
# will not work:
MY_VAR=${OTHER_VAR}
OTHER_VAR=${ANOTHER_VAR}
ANOTHER_VAR=something
```

## ENV vars vs security

Storing credentials (passwords, secrets, ..) in environment variables is not without risk. They can be exposed, due to programming errors or oversights, for example when you forget to remove the `phpinfo()` from production.

## ENV var validation

<!-- Review! -->

Strict validation rules for ENV vars are in use in the dashboard while entering. Chars like the "$" sign can be harmful in Linux systems. Here is the regex we use to validate the ENV var input in the dashboard:

```raw
/^[\p{L}\p{N}\ _\-\+=\.,:;\?!@~%&\*\(\)\[\]\{\}<>\/\\#]+$/u
```

So sometimes, when you want to store an external API key as an ENV var, you might get a validation error like: "Variable value contains invalid characters". If you can not change the value of your ENV var, you can encode and decode those:

## Encode and decode ENV vars

Use a base64 encoded string and decode it when applying it to your configuration in your code. Encoding works like this:

```php
php -r "echo base64_encode('YOUR-M$Pa#A-VALUEx') . PHP_EOL;"
```

And [this example](https://github.com/laravel/ideas/issues/416#issuecomment-280436034) should give you an idea how you can do the decoding.

## Reserved environment variable names

There are some names you can not use here:

* APP_NAME
* DOCUMENT_ROOT
* FCGI_ROLE
* GATEWAY_INTERFACE
* GROUP
* HOME
* PATH
* PS1
* QUERY_STRING
* SESSION
* USER

Also names cannot begin with:

* HTTP_
* PHP_
* REDIRECT_
* REMOTE_
* REQUEST_
* SCRIPT_
* SERVER_
* LC_
