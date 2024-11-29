---
reviewed: 2023-08-13 19:16:25
title: Local development
navigation.excerpt: Websites running on your local computer
lead: Set up a local development environment on your local machine so that you can see your software while you are building it.
head:
  meta:
    - name: 'keywords'
      content: 'LAMP, vhosts, localhost, 127.0.0.1, ALM, application lifetime management'
---

A local PHP development environment is key for a successful application lifetime management and continuous deployment. Developing locally is by far the fastest way to see changes quickly in real time. Browse and test your code in the browser before deploying it. Also, this way, you always have an up-to-date backup of your code. There are multiple ways to get your local development stack up and running. Choose the one that best fits your skills and needs. Also, your Operating System (Windows, macOS or Linux) might affect your choice here:

## Local development in virtual boxes

Utilizing a virtualization for development allows you better replication of your local setup across your team. Also having everything stashed into a virtual machine very much nullifies any interference with your local host system. It keeps things clean. There are two primary virtualization approaches for development:

### Container virtualization

[Container virtualization](https://en.wikipedia.org/wiki/Operating-system-level_virtualization) is often harder to setup, but once done easier to use and is very economical in terms of resource usage. [Docker](http://www.docker.org/) is the goto tool. These days **we recommend to use [DDEV](https://ddev.com/)** as an abstraction layer on top of Docker to simplify local PHP development.

### Desktop virtualization

[Desktop virtualization](https://en.wikipedia.org/wiki/Desktop_virtualization) is the classic way, it's likely easier to setup for novice users, but eats up more resources. Example VM applications are: [VirtualBox](https://www.virtualbox.org/)(free by Oracle) or [VMware](http://www.vmware.com/)(paid). VirtualBox controlled by [Vagrant](https://www.vagrantup.com/) helps a lot when setting up reproducible development environments. [Homestead](https://laravel.com/docs/homestead#main-content), which builds upon Vagrant is popular with Laravel.

## Local development on your host machine

You can run a web server and PHP directly on your local machine. This is often quick and lightweight to get up and running. Your options:

### Laravel Herd

This is an even easier-to-use local solution not only for Laravel developers on macOS. You can download it. It bundles NGNIX, DnsMasq and some other magic to an easy to use statusbar app.

- [Offcial Herd website](https://herd.laravel.com/)

### Laravel Valet

This is an easy-to-use local solution not only for Laravel developers on macOS. You have to install it with the Terminal. It's best installed with Homebrew and it requires Composer. The setup is easier than you think and it aligns with best practices of modern development. It bundles NGNIX, DnsMasq and some other magic to an easy to use CLI.

- [Offcial docs to install Laravel Valet](https://laravel.com/docs/valet)

### Classical GUIs

These solution stacks are easy to handle through a graphical interface and they interfere with the rest of your system as little as possible. The most commonly used here are [MAMP](https://www.mamp.info/) (free and paid version) and [XAAMP](https://www.apachefriends.org/index.html). Please mind that those don't include Git and Composer.

### Manual setup

You can also install and manage the software to run your local web server yourself. You'll find lot's of tutorials searching the web. The following open source software should run in your local development environment to match on connect with the fortrabbit platform:

- **Apache** or NGNIX — a web server
- **MySQL** – the database if you make use of one
- **PHP** – the server side scripting language
- **Git** – the version control - [see article](/15.tips/git-intro.md)
- **Composer** – the dependency manager for PHP - [see article](/15.tips/composer.md)
- **Node.js** and NPM - for frontend build processes
