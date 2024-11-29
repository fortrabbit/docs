---
reviewed: 2023-02-15 08:20:37
title: SendGrid
navigation.excerpt: Transactional mail integration
section: Extending_fortrabbit
sidebar: sendgrid
---

## About SendGrid

SendGrid offers an e-mail delivery service that assists businesses with transactional e-mail management.

## Booking & signing up

Choose your desired plan to initiate the sign up. You'll first just need to choose a user name, tell them your email address and choose a password. Later on they want to know a little more about you. "Provisioning" your account includes human! checks.

## Setting it up

In order to get your mails through the SPAM filter of your users, you'll need to authorize the ownership of the domain you are using — think DNS modifications. fortrabbit is not involved here. You do this with your domain or DNS provider of choice. This is done with DKIM and SPF.

## Using SendGrid with fortrabbit

Once you have the setup done, you can finally start using SendGrid from your fortrabbit App. This is straight forward:

The **SendGrid PHP library** [here on GitHub](https://github.com/sendgrid/sendgrid-php) can be required like so:

```json [composer.json]
{
  "require": {
    "sendgrid/sendgrid": "~4.0"
  }
}
```

To send e-mails via the API, you'll need to specify your SendGrid API key. There is also an [PHP SendGrid example on GitHub](https://github.com/sendgrid/sendgrid-php-example) which makes use of both, the API and the SMTP gateway.
