---
reviewed: 2024-10-30 15:18:24
naviTitle: Root path
title: Root path
navigation.excerpt: Landing directory for public access
lead: The root path refers to the directory that serves as the entry point for public requests from the world wide web.
hideExamples: yes
links:
  - title: Directory structure
    route: /concepts/directories
    property: docs
head:
  meta:
    - name: 'keywords'
      content: 'folder, directory, directories, linux, unix, web root, doc root, document root'
---

## Plain default

In a typical old school PHP project, the root path is on top level and contains the `index.php` file, which is the default script to be executed.

```raw
www <-- Root path
├── index.php  <-- file to be called
├── css/
├── js/
├── images/
├── includes/
```

- **`index.php`**: Main entry point
- **`includes/`**: PHP scripts included

## Modern root path settings

For a better file structure and increased security, it is recommended to keep most PHP files outside the publicly accessible directory and use a folder as the document root:

```raw
www
├── public/ <-- Root path
│   └── index.php <-- file to be called
├── src/
├── vendor/
└── composer.json
```

- **`public/`**: Public-facing files
- **`src/`**: PHP source code
- **`vendor/`**: Composer dependencies

By configuring the `public/` directory, you prevent direct web access to sensitive files in `src/` and `vendor/`. This pattern is standard for all modern PHP frameworks and CMS:

- `public` - Laravel, Statamic, October CMS …
- `web` - Craft CMS …

## Root path setting on fortrabbit

On fortrabbit you can set the root path for each app environment with the routing settings in the dashboard. When choosing a [software template](/11.concepts/software-templates.md) the correct root path will pre-configured.
