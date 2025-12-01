---
reviewed: 2025-09-10 08:26:46
title: GitHub API limits and Composer
naviTitle: GitHub API limits
navigation.excerpt: Code collaboration and deployment.
figure:
  emoji: ⏱️
  text: Handle GitHub API rate limits.
  color: rgba(180, 68, 68, 1)
  textColor: rgba(254, 226, 226, 1)
lead: The reason why you can run into this issue temporarily is that GitHub limits it's API per IP.
wip: true
sidebar: github
---

The solution is to create a GitHub OAuth token and put it in your `composer.json` file. You can do so by visiting [https://github.com/settings/tokens](https://github.com/settings/tokens) or via terminal:

```bash
curl -u your-github-user -d '{"note": "Fortrabbit Auth"}' https://api.github.com/authorizations
```

If you are using multi factor authentication (OTP), then you need to provide a valid OTP token like so:

```bash
curl -u your-github-user -H 'X-GitHub-OTP: 123456' -d '{"note": "Fortrabbit Auth"}' https://api.github.com/authorizations
```

This will give you a response like the following:

```json
{
  "id": 123456,
  "url": "https://api.github.com/authorizations/123456",
  "app": {
    "name": "Fortrabbit Auth (API)",
    "url": "http://developer.github.com/v3/oauth/#oauth-authorizations-api",
    "client_id": "12345abc12345"
  },
  "token": "12345abc1234512345",
  "note": "Fortrabbit Auth",
  "note_url": null,
  "created_at": "2013-08-08T11:08:18Z",
  "updated_at": "2013-08-08T11:08:18Z",
  "scopes": []
}
```

What you need is the `token` value. In the above example it is `12345abc1234512345`. Open up your `composer.json` file and add the token under the `config` directive:

```json
{
  "require": {
    "awesome/package": "@dev"
  },
  "config": {
    "github-oauth": {
      "github.com": "12345abc1234512345"
    }
  }
}
```

That's it. Your API token will be used to give you a personal rate limit which is much more higher than the default one.
