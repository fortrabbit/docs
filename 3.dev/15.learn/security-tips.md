---
updated: 2026-10-23
reviewed: 2026-10-23
reviewer: fl
title: Security tips
description: 'Keep a fortrabbit account and its apps secure with strong passwords, a clean list of SSH keys and team members, and current software.'
naviTitle: Security tips
navigation.excerpt: 'Stay safe online'
figure:
  emoji: 🛡️
  text: Stay safe online.
  color: rgb(200, 80, 30)
  textColor: rgb(254, 243, 199)
lead: Use a password manager, share access through the team instead of logins, delete unused SSH keys, and keep secrets and software in order.
head:
  meta:
    - name: keywords
      content: 'security, password, SSH key, authentication, account protection, fortrabbit'
topics:
  - security
---

## Account security

- Use a password manager or a long passphrase for the dashboard login.
- Never share a login. Invite people to the [team](/1.platform/10.objects/04.team.md) instead, and remove them when they leave.
- Review the [SSH keys](/1.platform/10.objects/12.ssh-key.md) of the account and delete the ones nobody uses.

## Application security

- Keep the software up to date: framework, CMS, plugins and the [PHP version](/3.dev/20.how-to/upgrade-php.md).
- Keep secrets in [ENV vars](/3.dev/19.env-vars/20.security.md), not in code or git.
- Store personal data encrypted where possible, and passwords only as hashes with `password_hash()`.
- Follow the [security chapter of PHP The Right Way](https://phptherightway.com/#security) and the [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/).
- Never leave a [phpinfo](/3.dev/15.learn/10.php-info.md) file online.
