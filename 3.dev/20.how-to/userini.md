---
reviewed: 2025-06-11 09:16:39
title: Configure .user.ini
naviTitle: Configure .user.ini
navigation.excerpt: Control advanced PHP settings
lead: How to use .user.ini files to configure PHP settings on fortrabbit
draft: true
links:
  - title: .htaccess intro
    route: /dev/how-to/htaccess/intro
    property: docs
  - title: PHP settings in dashboard
    route: /platform/settings/php
    property: docs
  - title: PHP component
    route: /platform/components/php
    property: docs
---

At fortrabbit, php-fpm is used for performance and security reasons. This means that adding `php_value` directives to `.htaccess` files has no effect. You can instead use `.user.ini` files to configure PHP settings that aren't available through the fortrabbit dashboard.

## When to use .user.ini

While the fortrabbit dashboard provides access to commonly needed PHP settings, there are cases where you might need `.user.ini`:

- Settings that cannot be changed at runtime (like `max_file_uploads`)
- Advanced configuration options not exposed in the dashboard
- Project-specific PHP configurations
- Settings that need to be version-controlled

## Creating a .user.ini file

The `.user.ini` file should be placed in the document root or in the sub-directories where settings should be applied. Common locations:

- `/public/` (for Laravel, Symfony)
- `/web/` (for Drupal, some Symfony setups)

### Example .user.ini file

```ini
; Set maximum file upload size
upload_max_filesize = 50M
post_max_size = 50M

; Configure file uploads
max_file_uploads = 50

; Set timezone
date.timezone = "Europe/Berlin"

; Session settings
session.cookie_lifetime = 7200
session.gc_maxlifetime = 7200
```

## File placement and inheritance

- Settings in `.user.ini` apply to the directory where the file is located and all subdirectories
- If multiple `.user.ini` files exist in the path hierarchy, settings are inherited and can be overridden
- Place the file as close to where it's needed as possible for better organization

## Security

- The `.user.ini` file should not be served by the web server
- By default, files starting with a dot are not served, but ensure your web server configuration doesn't expose them
- Never include sensitive information like database credentials in `.user.ini`

## Performance impact

- `.user.ini` files are parsed on every request by default
- Consider the performance impact when adding many settings
- Use the dashboard settings when possible for better performance

## Troubleshooting

Not seeing desired results?

### Settings not taking effect

1. **Check file location**: Ensure the `.user.ini` file is in the correct directory
2. **Verify syntax**: Invalid INI syntax will cause the entire file to be ignored
3. **Check permissions**: The file should be readable by the web server
4. **Test with phpinfo()**: Use `phpinfo()` to verify which settings are active

### Memory usage

You can use `.user.ini` to increase the `memory_limit` setting, but beware that we already set this to the same size as the booked [PHP plan](/1.platform/09.components/01.php.md). If you increase it further, the platform will start to randomly kill your PHP-FPM process any time it uses more memory than the booked plan. To safely get more PHP memory, book a larger plan using our dashboard.

### Debugging

Create a simple PHP file to check your configuration:

```php
<?php
// Show all PHP settings
phpinfo();

// Or check specific settings
echo "Memory limit: " . ini_get('memory_limit') . "\n";
echo "Upload max filesize: " . ini_get('upload_max_filesize') . "\n";
echo "Max file uploads: " . ini_get('max_file_uploads') . "\n";
?>
```

## Best practices

1. **Use dashboard first**: Always check if the setting is available in the fortrabbit dashboard before using `.user.ini`
2. **Document your changes**: Add comments to explain why specific settings are needed
3. **Version control**: Include `.user.ini` files in your repository for consistent deployments
4. **Environment-specific**: Consider different settings for development vs production
5. **Minimal configuration**: Only override settings that you actually need to change

## Related

- [.htaccess introduction](/3.dev/21.htaccess/01.intro.md)
- [php.net/configuration.file.per-user](https://www.php.net/configuration.file.per-user) - Official PHP documentation
