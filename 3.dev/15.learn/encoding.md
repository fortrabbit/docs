---
updated: 2026-10-23
reviewed: 2026-10-23
reviewer: fl
title: Encoding
description: 'UTF-8 is the default character encoding for fortrabbit apps. How to switch a PHP app, its headers and its MySQL tables to another charset.'
navigation.excerpt: UTF-8 alternatives
figure:
  emoji: 📝
  text: Configure character encoding properly.
  color: rgb(236, 72, 153)
  textColor: rgb(252, 231, 243)
lead: Use UTF-8 everywhere. PHP sends UTF-8 by default, static files and the MySQL connection need it set, with utf8mb4 in MySQL.
head:
  meta:
    - name: 'keywords'
      content: 'iso-8859-1, iso-8859-15, UTF-8, charset, encoding'
topics:
  - mysql
  - php
---

## Use UTF-8 everywhere

Mixed character encodings show up as broken umlauts or `�` characters. Use UTF-8 in PHP, in static files and in the database.

## PHP

PHP sends the charset in the `Content-Type` header, from the `default_charset` setting, `UTF-8` by default. Set another one per response:

```php
header('Content-Type: text/html; charset=UTF-8');
```

## Static files

Apache delivers static `.html` and `.txt` files directly. Set their charset in `.htaccess`:

```apache
AddDefaultCharset UTF-8
```

## MySQL

Use `utf8mb4` for tables and for the connection. The older `utf8` in MySQL stores only three bytes per character and breaks emoji. Set the connection charset in PHP:

```php
// PDO
$pdo = new PDO('mysql:host=…;dbname=…;charset=utf8mb4', $user, $password);

// mysqli
$mysqli->set_charset('utf8mb4');
```

Frameworks and CMS set the connection charset in their database configuration.
