---
reviewed: 2026-07-01
ai-author: co-authored
title: Apache error log codes
naviTitle: Apache error codes
navigation.excerpt: Decode the AHxxxxx codes in the Apache error log
lead: Apache tags each error-log line with a short AHxxxxx code. This page explains the ones seen most often on fortrabbit.
figure:
  emoji: 🔎
  text: Decode Apache log codes.
  color: rgb(70, 90, 120)
  textColor: rgb(220, 230, 240)
links:
  - title: Troubleshoot 500 errors
    route: /dev/http-status-codes/500
    property: docs
  - title: Troubleshoot 404 errors
    route: /dev/http-status-codes/404
    property: docs
  - title: Logs
    route: /platform/settings/logs
    property: docs
head:
  meta:
    - name: keywords
      content: 'apache error codes, AH01630, AH00128, AH01071, AH01075, AH01067, mod_proxy_fcgi, php-fpm, apache error log, fortrabbit'
---

## About Apache error codes

Every line in the Apache error log carries a unique `AHxxxxx` code — the letters `AH` plus five digits, like `AH01630`. Each marks one spot in the Apache source, so a code always points at the same condition.

### Relation to HTTP status codes

An Apache log code is not an HTTP status. Apache log codes live in the error log, statuses in the access log, the mapping is many-to-one — several codes share one status, many map to none. That is the value: a `500` only says something failed internally, while the code says whether a PHP-FPM process died, a rewrite loop ran away, or a rule denied the request.

On fortrabbit, Apache talks to PHP-FPM over FastCGI (`proxy_fcgi`). The codes below come from that path, from access control, or from Apache's core. Find them in the `apache` log source — see [logs](/1.platform/06.settings/25.logs.md).

| Code                                                                   | Meaning               | Module       | HTTP                                             |
| ---------------------------------------------------------------------- | --------------------- | ------------ | ------------------------------------------------ |
| [`AH01630`](#ah01630-client-denied-by-server-configuration)            | Client denied         | `authz_core` | [403](/3.dev/22.http-status-codes/others/403.md) |
| [`AH01631`](#ah01631-user-authorization-failure)                       | Authorization failure | `authz_core` | [403](/3.dev/22.http-status-codes/others/403.md) |
| [`AH00128`](#ah00128-file-does-not-exist)                              | File does not exist   | `core`       | [404](/3.dev/22.http-status-codes/404.md)        |
| [`AH00126`](#ah00126-invalid-uri-in-request)                           | Invalid URI           | `core`       | [400](/3.dev/22.http-status-codes/others/400.md) |
| [`AH00124`](#ah00124-request-exceeded-the-limit-of-internal-redirects) | Redirect loop         | `core`       | [500](/3.dev/22.http-status-codes/500.md)        |
| [`AH01071`](#ah01071-php-fpm-error-output)                             | PHP-FPM output        | `proxy_fcgi` | [500](/3.dev/22.http-status-codes/500.md)        |
| [`AH01075`](#ah01075-error-dispatching-request)                        | Dispatch failed       | `proxy_fcgi` | [503](/3.dev/22.http-status-codes/503.md)        |
| [`AH01067`](#ah01067-failed-to-read-fastcgi-header)                    | No FastCGI header     | `proxy_fcgi` | [503](/3.dev/22.http-status-codes/503.md)        |

## Access and authorization

### AH01630: client denied by server configuration

```raw
[authz_core:error] AH01630: client denied by server configuration: /srv/app/htdocs/.env
```

An access rule blocked the request before it reached the app. The path at the end of the message is what was requested — often a protected file like `.env` or a directory closed off by a `Require` directive. Maps to a `403`.

Check the `.htaccess` rules and any `Require` directives against the requested path. See the [.htaccess intro](/3.dev/21.htaccess/01.intro.md) for background. Requests for `.env`, `.git`, or dotfiles are usually scanners probing for secrets and can be ignored.

### AH01631: user authorization failure

```raw
[authz_core:error] AH01631: user jane: authorization failure for "/admin/":
```

Credentials were accepted but the authenticated user was not allowed into the requested area, or the authorization directives for that area are incomplete. Maps to a `403` — or a `401` when `AuthzSendForbiddenOnFailure` is off.

Review the `Require user` / `Require group` rules for the protected path and confirm the user belongs there.

## Missing files and bad requests

### AH00128: file does not exist

```raw
[core:info] AH00128: File does not exist: /srv/app/htdocs/public/favicon.ico
```

Apache could not find the requested file under the root path. Maps to a `404`. Most lines are harmless — browsers and bots probing for `favicon.ico`, `apple-touch-icon.png`, or stale source maps.

If a real page 404s, confirm the root path points at the framework's `public` directory and that the front-controller rewrite (`index.php`) is in place.

### AH00126: invalid URI in request

```raw
[core:error] AH00126: Invalid URI in request GET /%c0%ae/ HTTP/1.1
```

The request line held a malformed URI. Maps to a `400`. These almost always come from bots, malformed proxies, or scanners sending broken paths — rarely from the app itself.

## Redirect loops

### AH00124: request exceeded the limit of internal redirects

```raw
[core:error] AH00124: Request exceeded the limit of 10 internal redirects due to probable configuration error.
```

A rewrite rule kept redirecting the request to itself until Apache gave up. Maps to a `500`. The cause is nearly always a loop in `.htaccess` — a `RewriteRule` whose target matches its own pattern.

Review recent `.htaccess` changes and the `RewriteRule` targets. See the [.htaccess intro](/3.dev/21.htaccess/01.intro.md).

## PHP-FPM and FastCGI

### AH01071: PHP-FPM error output

```raw
[proxy_fcgi:error] AH01071: Got error 'PHP message: PHP Fatal error: Uncaught Error: Call to undefined function foo()'
```

PHP-FPM wrote to its error output and Apache surfaced it. The quoted text is the PHP message itself — a notice, warning, or fatal. A fatal pairs with a `500`; a warning may still return `200` while noise piles up in the log.

Read the quoted PHP message for the real cause, then open the `php` log source for the full stack trace. See [logs](/1.platform/06.settings/25.logs.md).

### AH01075: error dispatching request

```raw
[proxy_fcgi:error] AH01075: Error dispatching request to : (reading input brigade): Connection reset by peer
```

Apache started talking to PHP-FPM but the exchange broke off, commonly with `Connection reset by peer`. The PHP worker died mid-request — a fatal, a memory limit, a hard timeout, or a pool restart. Maps to a `503`.

Look for a matching `AH01071` fatal at the same time, and check `memory_limit` and execution time against what the request needs.

### AH01067: failed to read FastCGI header

```raw
[proxy_fcgi:error] AH01067: Failed to read FastCGI header
```

PHP-FPM returned no valid response header at all — the worker crashed, timed out, or was killed before it could answer. Maps to a `503`. Close cousin of `AH01075`; both point at a PHP process that never finished.

Check for out-of-memory kills and fatals in the `php` log, and confirm `memory_limit` and `max_execution_time` fit the workload.
