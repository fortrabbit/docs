---
reviewed: 2025-09-15
title: Deployment overview
naviTitle: Deployment
navigation: false
lead: How code gets from your repository onto fortrabbit, what runs during a deploy, and what to do when it goes wrong.
---

Deployment on fortrabbit is a Git push. You connect a GitHub repository through the [fortrabbit GitHub app](/1.platform/05.deployment/02.github-app.md), pick a branch per environment, and every push runs your [build commands](/1.platform/05.deployment/03.build-commands.md), swaps the new release in, and runs any [post-deploy commands](/1.platform/05.deployment/04.post-deploy-commands.md).

The pages below cover the moving parts in detail: [trigger](/1.platform/05.deployment/05.trigger.md) and [deploy hooks](/1.platform/05.deployment/16.deploy-hook.md) for kicking off deploys from outside, [cached directories](/1.platform/05.deployment/07.cached-directories.md) and [exclude patterns](/1.platform/05.deployment/10.exclude-patterns.md) for shaping the build, and [troubleshooting](/1.platform/05.deployment/20.troubleshooting.md) when a deploy fails.
