---
updated: 2026-10-23
reviewed: 2026-10-23
reviewer: fl
title: Upgrade the PHP version
description: 'Upgrade the PHP version of a fortrabbit environment: update dependencies locally, test, switch the version in the dashboard, deploy.'
naviTitle: Upgrade PHP
navigation.excerpt: Switch to a new version with confidence
figure:
  emoji: 🐘
  color: rgb(67, 56, 202)
  textColor: rgb(224, 231, 255)
lead: Upgrade PHP locally first, update the dependencies and test, then switch the version of the environment in the dashboard and deploy. Switching back works as long as the old version is available.
head:
  meta:
    - name: 'keywords'
      content: 'PHP upgrade, PHP version, migration, deployment, testing, fortrabbit'
topics:
  - php
  - updates
faq:
  - question: Can I switch back to the previous PHP version on fortrabbit?
    answer: Yes, select it again in the PHP settings of the environment, as long as that version is still available. Retired versions can no longer be selected.
  - question: What happens when my PHP version reaches end of life?
    answer: It stays available as is, without security fixes, and can cost a monthly fee on top of the PHP component. When fortrabbit retires the version, environments still on it are upgraded to the next newer version.
    links:
      - title: Legacy PHP versions
        route: /platform/settings/php#legacy-php-versions
      - title: Update policies
        route: /legal/policies/update-policies
        property: www
---

## PHP versions on fortrabbit

Each environment runs one PHP version, set in the PHP settings in the dashboard. It applies to the environment, the deployment service and [jobs](/1.platform/09.components/07.jobs.md).

- **Latest version** keeps the environment on the newest available PHP version.
- **A pinned version** stays as it is until fortrabbit retires it. Versions past their end of life can cost extra, see [legacy PHP versions](/1.platform/07.settings/06.php.md#legacy-php-versions).

New PHP versions arrive some time after their release, once the first patch release is out and the extensions are updated. See the [update policies](https://www.fortrabbit.com/legal/policies/update-policies).

## Upgrade step by step

1. **Upgrade PHP locally.** How depends on the [local development environment](/4.integrations/01.local-development/01.intro.md); in DDEV, `ddev config --php-version=8.4`.
2. **Update the dependencies.** `composer outdated` lists outdated packages, `composer why-not php 8.4` names the packages that block the new version. Update a CMS locally too, see the guides for [Craft CMS](/2.guides/3.craft-cms/12.updating.md) and [WordPress](/2.guides/6.wordpress/01.setup.md).
3. **Test locally.** Click through the site and run the tests. Static analysis, such as PHPStan or Rector, finds deprecated functions in own code.
4. **Switch the version on fortrabbit** and save:

   :BlockLink{title="Change the PHP version for {{app-env-id}}" path="/environments/{{app-env-id}}/php/php-version"}

5. **Deploy** the updated code with [git](/1.platform/06.deployment/01.intro.md), [SFTP](/1.platform/05.code-access/04.sftp.md) or [rsync](/3.dev/20.how-to/rsync.md), and run database migrations if the software needs them.
6. **Check** the site and the [logs](/1.platform/07.settings/25.logs.md). If it fails, switch back to the previous version and fix the problem locally.

To try the new version without touching production, create a second environment, switch its version and deploy there first.
