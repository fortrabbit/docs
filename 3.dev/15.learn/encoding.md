---
reviewed: 2026-07-07
reviewer: fl
title: Encoding
navigation.excerpt: UTF-8 alternatives
figure:
  emoji: 📝
  text: Configure character encoding properly.
  color: rgb(236, 72, 153)
  textColor: rgb(252, 231, 243)
lead: UTF-8 is the default encoding for fortrabbit apps. You can configure a different character encoding if needed. This guide explains how.
head:
  meta:
    - name: 'keywords'
      content: 'iso-8859-1, iso-8859-15, UTF-8, charset, encoding'
---

### PHP

PHP writes the encoding in the `Content-type` header. The default charset is `UTF-8` — `Content-type: text/html; charset=UTF-8`. You can change the charset via `ini_set`. Here is an example:

```php
ini_set('default_charset', 'iso-8859-15');
```

Make sure to write this in all your root PHP files. Alternatively, you can use the `header()` function to set the charset explicitly:

```php
header('Content-Type: text/html; charset=iso-8859-1');
```

### HTTP/Apache

Any static file — `.txt` or `.html` — is delivered directly via Apache. By default, Apache assumes the file is `utf-8`. You can change the charset via an `.htaccess` directive. Here is an example:

```apache
AddDefaultCharset iso-8859-1
```

### MySQL

When you store or fetch data from MySQL, you need to ensure the encoding matches the database when you connect to it. You can also set specific encoding for your columns. To set a different encoding than UTF-8 for your database sessions from PHP, you can use the `mysql_set_charset()` function. Here is an example:

```php
mysql_set_charset('iso-8859-15', $connection);
```
