---
reviewed: 2026-07-07
reviewer: fl
title: Security tips
naviTitle: Security tips
navigation.excerpt: 'Stay safe online'
figure:
  emoji: 🛡️
  text: Stay safe online.
  color: rgb(200, 80, 30)
  textColor: rgb(254, 243, 199)
lead: 'Security tips to protect your fortrabbit account, SSH keys, and application code from unauthorized access.'
head:
  meta:
    - name: keywords
      content: 'security, password, SSH key, authentication, account protection, fortrabbit'
---

## Dashboard and passwords security

Protect your fortrabbit account by using a strong password and regularly reviewing which SSH keys and team members have access.

- The password to log in with the fortrabbit dashboard must be secure.
  - Use a password manager or a long pass-phrase.
  - Don't share your account password, use our collaboration features instead.
- Rotate internal passwords via the dashboard:
  - Object storage
  - When team members leave
- Go over the list of imported SSH public keys periodically and keep only those being used. See [SSH key setup](/3.dev/15.learn/01.ssh-key-setup.md) for more details.

## PHP code security

Follow established security practices to prevent common vulnerabilities in your application code and protect user data.

- Make sure to follow common security guidelines — see [PHP the right way](http://www.phptherightway.com/#security).
- Mind the [OWASP Cheat Sheets](https://www.owasp.org/index.php/OWASP_Cheat_Sheet_Series) to negate attacks before they can start.
- Best practice is to store secrets like database passwords not with code but with App Secrets or environment variables.
- Don't store sensitive information in plain text in the database, use ciphertext.
- Make sure you keep your software up-to-date.
