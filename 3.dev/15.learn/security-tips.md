---
reviewed: 2026-01-29
title: Security tips
naviTitle: Security tips
navigation.excerpt: 'Stay safe online'
figure:
  emoji: 🛡️
  text: Protect your account and code.
  color: rgba(200, 80, 30, 1)
  textColor: rgba(254, 243, 199, 1)
lead: 'Some basic tips to keep your fortrabbit account and your code base secure.'
---

## Dashboard and passwords security

- The password to login with the fortrabbit dashboard must be secure.
  - Use a password manager or a long pass-phrase.
  - Don't share your account password, use our collaboration features instead.
- Rotate internal passwords via the dashboard:
  - Object storage
  - When team members leave
- Go over the list of imported SSH public keys periodically and keep only those being used.

## PHP code security

- Make sure to follow common security guidelines - see [PHP the right way](http://www.phptherightway.com/#security).
- Mind the [OWASP Cheat Sheets](https://www.owasp.org/index.php/OWASP_Cheat_Sheet_Series) to negate attacks before they can start.
- Best practice for security and portability is to store secrets like database password not with code but with our App Secrets or ENV vars (as long as they are not exposed as well).
- Don't store sensitive information in plain text in the database, use ciphertext.
- Make sure you keep your software up-to-date
