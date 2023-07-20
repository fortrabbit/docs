---

reviewed:      2023-07-07 09:07:46
title:         PHP info
excerpt:       Dump all configuration
lead:          Sometimes, you might be unsure on configuration settings, such as which extension in which version is exactly enabled or which ENV vars are actually available. phpinfo to the rescue!
status:        done

---

`phpinfo()` is a built-in PHP function that displays information about the current server settings, including:

- PHP version
- Loaded extensions
- Configuration settings
- Environment variables
- Server information
- and more

## Instructions

1. Create a `info.php` file anywhere in your publicly accessible path
2. Put `<?php phpinfo(); ?>` in that file
3. Call the URL with the browser to see a full config dump `domain.com/phpinfo.php`

Your CMS / framework might have its own dump of that. With Craft CMS for example you can visit a nicely formatted `phpinfo` in the control panel.

## Security advice regarding phpinfo

Don't use phpinfo in production or at least make sure to delete that file right away after you have finished your investigation, or put it behind a password. The output might contain sensitive information you don't want to share with the world. Keys and values of your ENV vars are visible, that can contain database access and API keys to external services.

## Related

- [offcial docs on php.net](https://www.php.net/manual/en/function.phpinfo.php)
