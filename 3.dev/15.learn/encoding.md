---
reviewed: 2026-01-29
title: Encoding
navigation.excerpt: UTF-8 alternatives
figure:
  emoji: 📝
  text: Configure character encoding properly.
  color: rgb(236, 72, 153)
  textColor: rgb(252, 231, 243)
lead: UTF-8 is assumed as the default encoding. You can set a different encoding manually — if you really want. This is on how to change the character encodings with fortrabbit.
head:
  meta:
    - name: 'keywords'
      content: 'iso-8895-1, iso-8895-15, UTF8, charset'
---

### PHP

PHP writes the encoding in the `Content-type` header. The default charset is `UTF-8` — `Content-type: text/html; charset=UTF-8`. You can change the charset via `ini_set`. Here is an example:

```php
ini_set('default_charset', 'iso-8895-15');
```

Make sure to write this in all your "root" PHP files. Alternatively you can use the `header` method of PHP to set the charset explicitly:

```php
header('Content-type', 'text/html; charset=iso-8859-1');
```

### HTTP/Apache

Any static file — `.txt` or `.html` — is delivered directly via Apache. Per default, Apache assumes the file is `utf-8`. You can change the charset via an `.htaccess` directive. Following an example:

```apache
AddDefaultCharset iso-8859-1
```

### MySQL

When you store or fetch data from MySQL, you need to make sure to fit the encoding of the database when you connect to it. Further more, you can set specific encoding to your columns. To set a different encoding than UTF8 for your database sessions from PHP you can use the `mysql_set_charset` method. Here is an example:

```php
mysql_set_charset('ISO-8895-15', $connection);
```
