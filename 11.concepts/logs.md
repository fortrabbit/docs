---
reviewed: 2023-08-15 13:47:18
title: Logs
navigation.excerpt: Access and error logs
lead: 'Analyzing logs is an important part of maintaining a stable and secure website. Error logs often help to identify bugs and other issues. Here is how on fortrabbit.'
head:
  meta:
    - name: 'keywords'
      content: 'Logging, Logs, error logs, php logs, white screen of death'
---

## Log access

All logs are available through the [fortrabbit dashboard](/11.concepts/dashboard.md), individual per [app environment](/10.objects/2.app-environment.md). A live log stream as well as historical logs are available for `stdout` and `stderr`.

## PHP error logs

You see a [500 error](/15.tips/http-errors/500.md) and you need to know why. PHP error logs contain information about issues that occur while executing PHP code. Use these logs to identify bugs in the code or configuration. PHP error logs typically include information such as the time and date of the error, the type of error, and the file and line number where the error occurred.

## Deployment logs

You are using [Git deployment](/6.deployment/1.intro.md) with some [build steps](/6.deployment/3.build-commands.md) but for some reason nothing get's deployed or you are expecting a different result. Use the deployment logs to see what's happening during deployment.

## Apache access logs

You want to know about traffic patterns of your website. The Apache logs provide a detailed record of server activity, including requests for files, HTTP error codes, and other important information. These logs can be used to troubleshoot issues and monitor server performance.

## Worker and cron logs

Your [worker or cron job](/9.components/7.jobs.md) is crashing. You want to know why. Use the logs to see what your workers have been doing.

## Log files in your CMS or framework

Mind that your CMS or framework might pipe logs to a different location, other than `stderr` and `stdout`. If they do, you will not see the error output in the fortrabbit dashboard. You can still access the logs by [SSH](/7.code-access/3.ssh.md) or [SFTP](/7.code-access/4.sftp.md), please see your CMS / framework docs where the logs are stored.

Most CMS and frameworks also offer options to send these logs to the standard locations. With the [software template](/11.concepts/software-templates.md) the setting is getting pre-populated, if possible, by ENV var.

- [Craft CMS logging](/3.craft/3.tune.md#logging)
- [Laravel logging](/2.laravel/3.tune.md#logging)

### Verbose logging

Your CMS / framework might offer verbose logging, often this is connected to environment settings of the CMS / framework. Often more debugging information is printed with the error and sometimes errors are even send to the browser. Use that with care, since it can have a considerable performance impact. The general advice is to use it for development and staging environments, but not for production. If you happen to have an issue in production that requires verbose logging, turn it off, after you have finished.
