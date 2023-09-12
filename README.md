---
navigation: false
---

# fortrabbit help pages

Welcome! This repo contains the contents of the (new) fortrabbit docs.

## Git repo

- <https://github.com/fortrabbit/help-new>

## Contributing

Found a typo or an error? Do you want to add something about your framework or service of choice? Do you run a 3rd party service or an open source project that can be integrated with fortrabbit? You are more than welcome to contribute.

### Pull requests

Please find a good balance in the number of commits contained with a pull request. For small typos, just use one commit and one PR. For larger text changes, consider combining commits for readability.

## Frontmatter tags

```yml
---
reviewed: 2023-06-12 # Last reviewed date (and time)
title:               # Long title with page
naviTitle:           # short title for list views
excerpt:             # additional details for list views
lead: blabla         # large text shown at the beginning
navigation: true     # lists this page with navigation
sidebar: craft       # shows meta data with 
nextNav: true        # will show
structureNav: true   # shows other pages in this folder
---
```

## Code blocks

Any code block should have a language defined. If applicable also define the file name like so ````php [info.php]`. The following languages are installed: 'apache', 'js', 'json', 'php', 'shell', 'sql', 'ts', 'twig', 'vue', 'yml'. Use apache for`.htaccess` & `.env` files. Use plain for anything else.

Use `shell` not `bash` as the language label for terminal stuff.

Indent with two spaces.

## Markdown editor setup

### VC Code

- Plugins: Markdownlint
- Settings: Auto update Markdown links

See the `.vscode` folder.

### Obsidian

- Plugins: Linter
- Templates: See templates folder

See the `.obsidian` folder.

## Internal links

Use relative links to local files including the full folder and file name. Example:

```md
…if not see [here](/3.craft/1.setup.md).
```

Your editor should offer autocomplete for this. Also such links can be automatically updated when the file name changes. Make use of that to avoid dead links.

## Navigation structure

The content get's rendered by Nuxt Content using Navigation to structure content based on the given folder structure. Please be aware of that. The numbers in front of the folder and files names are for sorting the navigation. The folders are creating a navigation structure.

## Local development

fortrabbit staff can run the fortrabbit docs locally to see documents rendered in the browser. See the instructions of the repo on how to integrate this.

## Deployment

There is currently no automatic deployment set up.

## Dynamic help TODO

Those values will be replaced by JS when users are logged in:

```plain
SSH user: {{ssh-user}}
Region:   {{region}}
Your app: {{app-env-slug}}
```

It will dynamically show the correct code examples and dashboard links.

## MDC components

There are some Markdown Components (powered by Nuxt Content) to use:

### DashboardLink

```md
:DashboardLink{title="" path=""}
```

This parses markdown inside the DIV. With the data-user attribute it checks if the user is logged in, links to the dashboard will be styled as buttons — use a verb to start them!

## Writing conventions

### Support driven documentation

These help pages are often used to point clients to answers on common questions. That's why some topics are covered im much detail. Clients are asking for it. So instead of writing an answer in client support, one might just update the help pages and point the client to the new section.

### Know the target audience

While some implicit technical details are obvious to you, they might not be for the client. Explaining one acronym only with another acronym might not help. Sometimes it needs some more words.

### Code examples

- Open and close code blocks with ````shell` where shell is the language for syntax highlighting
- Try to keep code examples together in one block, avoid mixing paragraphs and code blocks
- Code blocks follow standard markdown formatting
- Show output only when necessary
- Output should be a comment `#`
- Use comments in between commands to explain what's going on
- `$` to start a command
- Start code examples right away
  - PHP without `<?php`
  - Bash without `#!/bin/bash`

### Writing

- Use sentence case in headlines
- Don't use too many headlines to structure text
- Available headlines in text: h2, h3, h4, don't go deeper
- Avoid "eg", otherwise choose one style to write it
- Keep lists readable (no sublists, etc)
- Text structure is important, but readability is even more important
- Use ASCII art to illustrate topographies and such things
- Don't use italic > it looks ugly, it's rendered by the browser not the font
- Don't use a paragraph for every sentence
- Write speaking links, not like so: `[here](http://somewhere)` but so: `[GitHub project](http…)`
- Don't bullshit. Avoid the use of marketing buzzwords

### Maintainability

- Find the right balance between being general and being precise (aka Captain Obvious)
- Very detailed step-by-step articles are easy to follow but get outdated very quickly
- Don't use screenshots and images, use words and ASCII graphics
- Don't bury numbers (like prices and limits) in articles
- All those numbers must be managed in the "pricing" and the "specs" page
- Keep it DRY! Don't repeat yourself
- Have one SSOT, link to it
- Don't fully cover the same topic on different places, just link to the location

### File name conventions

When creating new files:

- use dashes instead of spaces or low dashes for file names
- use the short versions: `-uni`, `-pro` at the end for different stacks

### fortrabbit owned words and common casing

- **account** — ~~profile~~, ~~account~~
- **events** ~~history~~, ~~diary~~, ~~log~~, ~~activities~~
- **app URL**
- **app** — ~~app~~, ~~website~~, ~~application~~
- **payment method** ~~bc~~
- **cron job** — ~~cron~~, ~~cron job~~
- **dashboard** — ~~control panel~~, ~~console~~
- **fortrabbit**
- **docs** — ~~documentation~~, ~~handbook~~, ~~help~~
- **HTTP** — ~~http~~
- **HTTPS** — ~~https~~
- **root path** ~~document root~~, ~~doc root~~
- **terminal** ~~Terminal~~, ~~shell~~, ~~bash~~
- **URL** — ~~Url~~, ~~url~~

### Times & dates

- use the same time-zone E V E R Y W H E R E when communicating times
- the communicated time-zone is UTC
- use relative times (an hour ago, a few seconds ago)
- Markup example: `<time datetime="2016-01-01 08:22:10 UTC" title="2018-01-01 08:22:10 UTC">A few minutes ago</time>`
- **ms** — ~~MS~~
- **s** - ~~scds~~
- **m** - ~~mins~~, ~~min~~
- **h** - ~~hrs~~

### Metric units

- **16 MB** — ~~mb~~, capital letters, a space between value and unit
- **3 GB** ~~3078 MB~~ < prefer a readable unit
- **0 B**
- **16 KB**
- 10k — ~~10,000~~
- times a value: ×, `&times`; ~~x~~

### Other words

- €23 < without space char
- $23 < without space char
- **add-on** — add-ons, ~~Add-on~~, ~~Add-On~~, ~~AddOn~~
- **component** ~~plan~~
- **main domain**
- **e-mail** — ~~eMail~~, ~~email~~, ~~Email~~, ~~E-Mail~~
- **free trial** — ~~test flight~~, ~~test drive~~
- **host** — ~~server~~
- a space char belongs before the unit
- **MySQL** — ~~MySql~~
- **OPcache** — ~~OPCache~~ ~~Opcache~~
- **node** — ~~server~~
- **non-persistent storage** — ~~storageless~~
- **payment details** — ~~complete account~~, ~~payment credentials~~
- **PHP requests** — ~~requests~~
- **PHP response time** — ~~response time~~
- **PHP** — ~~Php~~
- **Scale** — ~~upgrade~~
- **session time**
- **SFTP**
- **SSH Key** — ~~pubkey~~, ~~public SSH key~~
- **SSH**
- **SSL cert** — ~~SSL certificate~~
- **web storage** — ~~webspace~~
- **Composer** — ~~composer~~
- **macOS** — ~~Mac OS X~~

## Avoid words list

Please do not use the following "bullshit" words:

- great
- awesome
- innovative
- game-changing
- empowering
- revolutionizing

### Gender-neutral language

When referencing a hypothetical person, such as "a user with a session cookie", use gender-neutral pronouns (they/their/them). For example, instead of:

- he or she, use they
- him or her, use them
- his or her, use their
- his or hers, use theirs
- himself or herself, use themselves

### Corporate identity

There is no fortrabbit logo as graphic file. To create the brand logo just type: "• fortrabbit" — bullet character, a normal space and then name of the company with a f. Use the [Georgia Typeface](http://en.wikipedia.org/wiki/Georgia_(typeface)) in bold and italic. Use lot's of whitespace around the logo, don't put other text nearby the logo. When using the company name within a paragraph of text, write "fortrabbit" with a f, even at the beginning of a sentence. Don't use the bullet or any other typeface here.

### Logos and brand assets

Place logos for external services and projects in the media folder. They ideally should be svg or either PNG with transparent background. Favor an "image mark" over a "word image mark".
