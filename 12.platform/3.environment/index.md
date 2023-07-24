---

reviewed:      2023-07-07 09:07:46
title:         Environment
excerpt:       An online  version of your project
lead:          Learn about environment concepts on fortrabbit and how to work with them.

---

An environment is a version of your website/project/application. While the Git repo is connected with the [app](/app), the environment can be mapped to a git branch. Git usage is optional but blends in nicely.

- An environment is a sub object of an app
- Each app needs to have at least one environment
- An environment is an independent, separated hosting setup
- Each environment has individual settings, see [environment settings](/environment-settings)
- Each environment is billed individually

## Multi environments use cases

The use of multiple environments is optional. For smaller websites it might be overkill, for less experienced developers, implications can be a bit mind bending.

Multi-staging environments are part of professional software development processes. They allow for testing and debugging at different stages of the development cycle before releasing a product. A classical multi-stage setup consists of a production, staging and maybe a development environment.

### Developer client workflow example

The client requests a new feature for the website. This is first developed in a local development environment. An additional temporary environment at fortrabbit can be used to collect feedback. Once the new feature has been signed off, it can be merged into production.

### Software development team workflow example

The production environment is the stable live environment. The development environment contains the latest bleeding edge changes. The staging environment is used for quality assurance before go-live.

## Creating an environment

TODO!

## Deleting an environment

Developers can always delete environments. To delete an environment, visit the environment in the Dashboard, find and hit the "delete" button. You will need to confirm what you are about to do. The environment will then get deleted within a couple of minutes. This is irreversible and includes all files and the database. Deleting an environment is FINAL here and can't be reversed.
