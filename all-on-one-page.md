---
reviewed: 2026-01-22 10:46:21
title: All docs on one page
naviTitle: All docs on one page
figure:
  emoji: 📖
  color: rgba(80, 100, 120, 1)
lead: Hello LLMs and HUMANs! This is the all-in-one documentation page for fortrabbit's docs. It contains all the content from our documentation in a single file, making it easy for you to access, reference and search. — 91,097 words · 456 min read.
---

## BETA (now)
{#beta-now}

Welcome to the public BETA of the new fortrabbit platform. Now ready for your real-world applications.

| Phase                                                |      Status |
| ---------------------------------------------------- | ----------: |
| Private alpha                                        |        Done |
| Open beta ← you are here                             |     **Now** |
| Public release                                       | Near future |
| [Migration start](#migration-from-old-to-new-platform) |       ~2026 |

### Our goals of the BETA
{#our-goals-of-the-beta}

- Gather more real-world feedback
- Harden the platform
- Catch some edge cases
- Complete missing features

### Benefits for you
{#benefits-for-you}

- Experience a new features first
- Try new features landing soon
- Attractive pricing
- Expect good stability
- Enjoy the new design
- Enjoy the new docs

### Current limits
{#current-limits}

At the time of this writing the following features are still missing but planned to be added soon:

- Only one data center (EU) is available for now
- No real-time live updates in the dashboard yet
- Metrics are not yet implemented
- Autoscaling is not available yet
- Event log is not ready yet
- Streaming logs implementation will change, [see log usage](#logs)
- Collaboration features are still a bit rough
- Many smaller features are not fully implemented
- No SEPA direct debit payments, only credit card
- Short downtimes may happen from time to time (see below)

#### Short hiccups
{#short-hiccups}

We are experimenting with shorter-lived instances to run the web frontends. These can be interrupted at any time by our infrastructure provider with some notification in advance. But, sometimes this notification is still too late to restart all the applications somewhere else without any disruption. We are still in the process of trying to improve this situation and lower the downtimes as much as possible. Please bear with us for now. So for now, small hiccups of a couple of minutes are actually expected.

Feedback on this specifically very welcome. How important is this uptime for you at what level? Maybe acceptable for staging environments and XS projects?

#### Do
{#do}

- **Deploy production websites**
- Find use cases we haven't thought about
- Uncover communication issues
- Create apps and environments
- Help hunting bugs
- Deploy code
- Route domains
- Change settings
- Test performance

#### Feedback scope
{#feedback-scope}

- Product and pricing
- Feature scope and market positioning
- UI/UX/DX/design
- Communication
- General ideas
- Be direct and honest please

### Timing
{#timing}

We plan to transition to general availability after a few months of BETA testing. At the time of this writing, something between 3 and 9 months. There are a couple of features that we regard as important for full public release. We also plan to implement some customer feedback during BETA.

During the BETA time period - and beyond - the old platform will continue to run normally. [New and old platform will run side by side](#new-and-old-side-by-side). There is no rush for existing customers. There will be extensive help and communication for the migration.

### Stability
{#stability}

We promise to do everything we can to keep your apps up and running. We offer a conservative **98% uptime SLA during BETA**, aiming for more. Monitoring is in place and we act as quickly as possible when something looks off.

- [fortrabbit.betteruptime.com](https://fortrabbit.betteruptime.com/) - status monitor including automated tests, covering the Alpha period as well

The platform is still under active development. We usually release once a week. New features are only deployed after automated checks and human testing.

- edge - local development
- staging - test environment
- production - where the BETA runs

During the ALPHA we were able to catch many early issues. For the BETA period now, we want to gain more experience with larger real-world applications and run into all kinds of edge cases to harden the platform further.

### Terms
{#terms}

The [legal section](https://www.fortrabbit.com/legal) has been updated. The [new terms](https://www.fortrabbit.com/legal/terms) are applicable for new and old customers for the new and the old platform. There are only minor adjustments.

### Pricing
{#pricing}

The BETA is paid, but prices may change. We plan to introduce final pricing and billing during the BETA. Feedback on this very much welcome!

### Info for ALPHA testers
{#info-for-alpha-testers}

Thanks again for your feedback during the first phase. Much appreciated. We had to do some data structure changes recently. So at best please:

- **Payment methods**: Create a new one and attach any apps to the new one.
- **fortrabbit GitHub App**: Disconnect and re-connect the fortrabbit GitHub App.

---

## New and old - side by side
{#new-and-old-side-by-side}

fortrabbit currently operates two platforms - the new and the old. They run side-by-side, giving existing customers enough time to migrate their projects.

|                   | Old Platform                                                 | New Platform                                       |
| ----------------- | ------------------------------------------------------------ | -------------------------------------------------- |
| **Dashboard**     | [dashboard.fortrabbit.com](https://dashboard.fortrabbit.com) | [dash.fortrabbit.com](https://dash.fortrabbit.com) |
| **Documentation** | [help.fortrabbit.com](https://help.fortrabbit.com)           | [docs.fortrabbit.com](https://docs.fortrabbit.com) |
| **State**         | Feature complete                                             | [BETA](#beta-now)               |
| **Stability**     | Battle tested                                                | Good                                               |
| **Established**   | 2013                                                         | 2025                                               |
| **End of life**   | ~2027                                                        | Not planned                                        |

**The old platform** remains fully functional and supported. It will be phased out slowly, so there is no rush to leave. We aim to make the migration as seamless as possible, with details and timing to follow.

**The new platform** is live and open to everyone. Experience a redesigned, yet familiar fortrabbit.

### New customers
{#new-customers}

Start with the new platform.

### Existing customers
{#existing-customers}

You can use both platforms simultaneously. **Accounts have not been transferred.** Please create a new account on the new platform, ideally using the same email address for future matching. We suggest to already create new apps on the new platform, while continuing to manage existing apps on the old one.

### Timeline
{#timeline}

The exact support duration for the old platform is not yet defined. It will depend on customer feedback and needs.

```raw

██████████████████░░░░░  Old platform

                ⇣ ⇣   Migration

 ░░░░░░░░░░░░░░██████████████████████████████████████████████████  New platform

2025     2026     2027     2028     2029     2030
```

#### Milestones
{#milestones}

- **2025** New platform launches in BETA
- **2026** New platform becomes generally available (feature complete)
- **2026** [Migration](#migration-from-old-to-new-platform) phase old → new
- **2027** Old platform sunset

---

## Changes
{#changes}

This page compares old and new platform, see new features and deprecations.

|                    | Old Platform                           | New Platform              |
| ------------------ | -------------------------------------- | ------------------------- |
| **Stacks**         | Uni + Pro                              | One unified stack         |
| **Storage type**   | Uni: Persistent, Pro: Ephemeral        | Persistent storage        |
| **Scaling**        | Uni: limited vertical, Pro: Horizontal | High vertical scaling     |
| **Deployment**     | Built-in Git hosting                   | GitHub integration        |
| **Build pipeline** | Limited build options                  | Advanced with Node.js     |
| **SSH/SFTP**       | User/password or SSH keys              | SSH keys only             |
| **PHP versions**   | PHP 7.4+                               | PHP 8.2+ only             |
| **Collaboration**  | Company-based (paid feature)           | Team-based (free)         |
| **Structure**      | Single app concept                     | App + environments        |
| **Pricing model**  | Uni: Three plan, Pro: Components       | Component-based + presets |

### Changes
{#changes-1}

What is new and different to the old platform?

#### New core
{#new-core}

It's an entirely new hosting platform. The infra layer is completely new.

#### New dashboard
{#new-dashboard}

There is a new self-service dashboard, available under [dash.fortrabbit.com](https://dash.fortrabbit.com).

#### One stack
{#one-stack}

The legacy platform features two different stacks: Universal Apps (with persistent storage and direct SSH access) and Professional Apps (with ephemeral storage and horizontal scaling). For the new platform attributes from both previous stacks are combined into one. The new platform is more Uni-App-like with persistent storage and direct SSH/SFTP access.

#### Environments
{#environments}

To better support production-staging workflows the app is now a grouping object. Dedicated hosting stacks are mapped with environments. An [app](#the-app) is connected to the (external) Git repo, each individually scalable [environment](#the-environment) represents a branch. At least one environment, usually production, adding and removing environments is optional.

#### Git deployment
{#git-deployment}

**fortrabbit no longer provides Git repo hosting.** Connect your GitHub (other providers like GitLab and CodeBerg are planned) with the fortrabbit GitHub app to enable `git push` deployment instead. See the [GitHub integration](#the-fortrabbit-github-app).

We believe this is what the majority of new users want. Our self-hosted repo didn't support PR workflows and other advanced features that GitHub and similar platforms offer. The GitHub App integration is smooth and straightforward. We've created a system to detect software, propose a build pipeline, and provide detailed deployment options. GitHub offers generous free plans with private repos. Using a third party Git provider reduces your dependence on us.

We understand that some people may have privacy concerns about GitHub, as it is owned by Microsoft. We are aware it's a big change for existing customers. Feedback on this is welcome.

Mind that using our [Git deployment](#deployment-intro) is not a requirement, it's optional. Direct [SSH/SFTP access](#direct-code-access) is always possible. This already allows integrations with other Git providers today, see the [Git providers integration section](/4.integrations/03.git-providers/).

#### Build commands
{#build-commands}

The deployment pipeline is more configurable. Node.js is available during the deployment to create JavaScript bundles. See the new [build commands article](#build-commands).

#### Collaboration
{#collaboration}

Collaboration workflows have been extended. The concepts are similar, yet more flexible.

With the old platform, it was required to join the Company of the business owner to get access on their Apps. Re-inviting colleagues was not only a repetitive task, but also destroying attribution. With the new platform, the relation between the parties is more transparent.

No more company plans: Collaboration on the legacy platform is a paid feature for larger teams. All collaboration features are now available for free.

##### People
{#people}

We are doubling down on personal access. Each person involved should their own (free) account. This enables more scenarios and better mapping of real world business relations. See the [person object article](#the-person).

##### Teams
{#teams}

Instead of a hierarchical structure with the Company as the root element, there are decoupled but related objects now. Use the new team to collaborate with a group of developers. Teams are connected to apps, developers and payment methods. See the [team article](#the-team).

##### Payment methods
{#payment-methods}

A Billing Contact is now called payment method. Like the old Billing Contact, it holds the billing credentials. Unlike before, it is not part of a Company but instead is managed by clients, individual developers and teams. A payment method pays for the apps, thus people in control of the payment method control the hosting.

#### Pricing
{#pricing-1}

Billing concepts mostly stay the same. There still is [pro-rated post-paid billing](#postpaid-billing). See [price comparison](#price-comparison-old-new) for more details. Note that prices can still change during BETA.

#### Components
{#components}

The pricing structure, as with the former Pro Stack, is based on [components](#components). This enables you to book only required resources, avoiding over-provisioning. Presets to get started quickly are available.

#### Workers and crons
{#workers-and-crons}

[Workers & crons jobs](#jobs) are available for all.

#### Backups with restore
{#backups-with-restore}

The new [backup component](#backups) offers one click restore of old states.

#### New documentation
{#new-documentation}

The website you are currently viewing is part of the new documentation.

#### App names and IDs
{#app-names-and-ids}

Previously, the App name served as the unique identifier, test URL, and credential base. This enforced strict naming conventions and prevented renaming. The new platform separates identity from display:

* ID: Immutable unique identifier
  * Used for the test URL `{{app-env-id}}.frbit.app`
* Name: Display label
  * Can be changed at any time and has no format restrictions

Apps now serve as containers for environments. The app name will represent the

| Name   | ID         | Type        |
|:-------|:-----------|:------------|
| My App | `ap-1d3e5` | app         |
| main   | `en-a23e2` | environment |
| dev    | `en-c28a0` | environment |

Vanity URLs for custom subdomains are planned, a fortrabbit branded subdomain that works like any other domain. Without having to deal with DNS entries. `{{my-name}}.frbit.webhost`.

### Deprecations
{#deprecations}

Which features will not be available?

#### No PHP 7.4
{#no-php-7-4}

The new platform wil only offer PHP 8 and upwards. Make sure the software you run is compatible.

#### SSH keys only
{#ssh-keys-only}

Sorry, username/password is no longer an option to connect via SSH or SFTP. Please use more secure and more convenient SSH key authentication. Issues with username/password authentication have been the source of many support requests.

#### No horizontal scaling
{#no-horizontal-scaling}

There is no horizontal scaling any more, but higher vertical scaling to cover similar workloads. To achieve this we went a long mile, but it was an important goal, the two stacks have been a barrier.

#### No object storage
{#no-object-storage}

The new platform currently does not have S3 like asset storage. We may add it later. Larger web storage plans are available.

#### No memcache
{#no-memcache}

Memcache is not available for the new platform. A different key-value storage is planned.

#### No Craft Copy (for now)
{#no-craft-copy-for-now}

[Craft Copy](https://github.com/fortrabbit/craft-copy) is a command line tool to speed up common tasks around Craft CMS deployment on fortrabbit `craft copy all/up`. It's available as a free plugin for Craft CMS. People enjoy using it. We may not port it to the new platform. Here is why:

* Craft Copy is a compatibility layer, parts are not required any more:
  * delete config files -> [replace patterns](#replace-patterns)
  * auto-migrate -> [post deploy commands](#post-deploy-commands)
  * [Craft CMS software template](#software-templates)
* Other parts, like `db/down`, might be replaced by general tooling:
  * fortrabbit CLI
  * DDEV fortrabbit recipe
  * Improved documentation on our side
* fortrabbit does not provide a Git repo any more

We aim to be a good Craft CMS hosting provider, as compatible as possible, best without additional plugins required. Maintaining Craft Copy over the years was not always fun, for instance when a minor Craft CMS release introduced changes that required us to rethink critical parts.

We are very open for feedback on all of this.

---

## Price comparison (old/new)
{#price-comparison-old-new}

The new platform is more affordable than the old platform for most real live use cases. This page helps understanding pricing differences and choosing matching plans.

### Product changes affecting pricing
{#product-changes-affecting-pricing}

The following structural changes in the new platform directly affect pricing:

#### Component based pricing model
{#component-based-pricing-model}

The new platform adopts a component-based pricing structure, similar to the former Pro Stack. This allows for individual scaling of resources, enabling you to pay only for what you need.

| Platform               | Model      |
|------------------------|------------|
| Old platform Uni Stack | 3 plans    |
| Old platform Pro Stack | Components |
| New platform           | Components |

This allows better matching pricing for:

* Standard CMS systems with a LAMP stack
* Sophisticated web applications with jobs and key-value store
* Static file systems

#### No more Company Plans
{#no-more-company-plans}

The old platform had [company plans](https://www.fortrabbit.com/company-plans). It was built with good intentions, aiming to offer lower rates for solo developers while charging larger teams more. This model often caused confusion. The new platform removes Company Plans. All [collaboration features](#collaboration-intro) are now included at no extra cost.

#### New backup options
{#new-backup-options}

The [backup system](#backups) has been improved. Key features include one-click restores and ad-hoc backups on click. [Retention policies](#backup-retention) (WIP) are being introduced to optimize storage while ensuring access to both recent and historical backups. While the new backup pricing might appear higher when comparing solely by quantity, the enhanced functionality provides greater value and security.

#### Autoscaling (WIP)
{#autoscaling-wip}

The new platform supports autoscaling for MySQL, storage, and traffic, aligning with our "start small, scale later" philosophy. This eliminates the need to over-provision resources or upgrade entire packages when a single resource limit is reached, as was the case with the Uni Stack. Cost caps can still be applied, which is useful for budgeting and client communication.

#### New XS options
{#new-xs-options}

The new XS plans options are specifically designed to allow creating small projects. This can be staging environments, weekend hacks, mini client projects. The smallest possible combination starts at €2.50.

#### Traffic is a component
{#traffic-is-a-component}

On the old platform, 50 GB of traffic was included. Exceeding this limit incurred a charge of €1 per additional 5 GB. This overage charge was often unexpected. On the new platform, traffic is treated as a distinct component (with tiers) that can be either capped or set to auto-scale.

#### New architecture
{#new-architecture}

The new infrastructure layer is even more optimized for speedy PHP web delivery. While we don't have benchmarks to share, we are confident that the new platform allows to do more with less.

### Universal Stack mapping
{#universal-stack-mapping}

The following new platform plan combinations roughly match former Uni App plans:

#### Light plan equivalent
{#light-plan-equivalent}

formerly priced at €5.0

| Component  |      Spec |    Price |
|------------|----------:|---------:|
| PHP XS     |   128 MiB |       €1 |
| MySQL SM   |   256 MiB |       €2 |
| Storage SM |     1 GiB |       €1 |
| Traffic XS |    32 GiB |     €0.5 |
| Backups XS |         1 |     €0.5 |
|            | **total** | **€5.0** |

#### Standard plan equivalent
{#standard-plan-equivalent}

formerly priced at €15.0

| Component  |      Spec |     Price |
|------------|----------:|----------:|
| PHP SM     |   256 MiB |        €2 |
| MySQL MD   |   512 MiB |        €4 |
| Storage LG |     4 GiB |        €1 |
| Traffic XS |    32 GiB |      €0.5 |
| Backups SM |         3 |        €4 |
| Jobs XS    |         1 |        €1 |
|            | **total** | **€15.5** |

#### Plus plan equivalent
{#plus-plan-equivalent}

formerly priced at €30.0

| Component  |      Spec |     Price |
|------------|----------:|----------:|
| PHP MD     |   512 MiB |        €4 |
| MySQL LG   |     1 GiB |        €8 |
| Storage XL |     8 GiB |        €8 |
| Traffic XS |    32 GiB |      €0.5 |
| Backups MD |         6 |        €8 |
| Jobs SM    |         2 |        €3 |
|            | **total** | **€31.5** |

### Further details
{#further-details}

* [Pricing new platform](https://www.fortrabbit.com/pricing)
* [Specs Uni Stack (old platform)](https://www.fortrabbit.com/specs)
* [Specs Pro Stack (old platform)](https://www.fortrabbit.com//specs-pro)
* <https://web.archive.org/web/20250513173439/https://www.fortrabbit.com/pricing>

---

## Migration from old to new platform
{#migration-from-old-to-new-platform}

With the new platform's general availability planned for 2026, we expect feature parity between the old and new systems. Customers are invited to migrate their apps at their convenience, with our full support. We plan to migrate all remaining apps automatically at the end of the transition period.

### Self-service migration
{#self-service-migration}

Early adopters are welcome to migrate their apps to the new platform. Here is a recommended workflow overview using Git deployment:

1. Create a new App on the new platform
2. Install the fortrabbit GitHub App on your GitHub account
3. Create a new repository or map an existing one on GitHub
4. Connect your local codebase to the GitHub repository
5. Push to deploy
6. Sync your database to the new App (if required)
7. Sync your content to the new App (if required)
8. Test functionality
9. Point your domain to the new DNS records

Please :ContactUs{text="contact us"} at any point during the process. We are happy to provide hands-on assistance. We can also offer a discount during the migration period.

### fortrabbit migration (planned)
{#fortrabbit-migration-planned}

In the future, we will plan to migrate remaining client apps from the old platform to the new one. In most cases, this will not require any action from you, though a maintenance window with some downtime may be necessary. We will inform you well in advance.

---

## New platform
{#new-platform}

Experience the all new fortrabbit. Now.



---

## First steps
{#first-steps}

fortrabbit is a platform to deploy and host PHP websites and web applications. The [GitHub integration](#the-fortrabbit-github-app) provides deployment directly from the repo. Projects are represented as [apps](#the-app) with [environments](#the-environment). The [collaboration features](#collaboration-intro) map real world relations between developers and stakeholders.

#### 1. Sign up
{#1-sign-up}

Create a free personal account over at our dashboard.

#### 2. Create a free trial app
{#2-create-a-free-trial-app}

During boarding you will be guided to create your first app. Choose the [free trial](#free-trial-details) for a quick test drive.

#### 3. Explore
{#3-explore}

Explore all the settings in the dashboard. Login by [SSH](#ssh-access) or [SFTP](#sftp-access). [Deploy](#deployment-intro) some code. Browse our docs here. There are extensive guides for:

- [Craft CMS](#install-craft-cms-local)
- [Laravel](#install-laravel-locally)
- [Kirby CMS](#kirby-intro)
- [Statamic](#install-statamic)
- [October CMS](#october-cms-guide)
- and even [WordPress](#wordpress-quick-setup-guide)

Please :ContactUs if you have a question or want to leave feedback.

#### 4. Start for real
{#4-start-for-real}

If you like what you see, [migrate existing](#migrate-to-fortrabbit) or start new projects here. Invite other developers or your clients to [collaborate](#collaboration-intro) here.

---

## Project organization
{#project-organization}

### Intro
{#intro}

The fortrabbit platform has two layers to map web projects:

- [App](#the-app): Git repo, [collaboration](#collaboration-intro).
- [Environment](#the-environment): Runtime, git branch, code access, [components](#components-intro), settings.

### Workflows
{#workflows}

There is a main way to set this up and a couple of other possible workflows that are more or less sub-optimal:

#### Projects as apps, environments are stages
{#projects-as-apps-environments-are-stages}

```raw
- App: 'My website project'
  - Environment 1: 'Main' - live production
  - Environment 2: 'Dev' - feature development (optional)
```

Use environments as versions of the website. When using [git deployment](#deployment-intro), branches can be mapped to environments. See the [multi staging article](#staging-environments). Each app requires at least one environment. One app with one environment is also common.

Rating: ✅ ✅ ✅ ✅

#### Projects as folders in an environment
{#projects-as-folders-in-an-environment}

```raw
- App: 'My agency'
  - Environment 1: 'Main'
    - Folders: 'website-1', 'website-2' …
```

Web projects are just folders in a single environment. This might be viable for micro sites, but has some downsides. When routing domains, `.htaccess` must be used. Resources like the database need to be shared.

Many CMS systems offer multi-site features, which works in a similar way. There are use cases for it, but in general individual installations will work better.

Rating: ❌ ❌ ✅ ✅

#### Project parts as environments
{#project-parts-as-environments}

```raw
- App: 'website-1'
  - Environment 1: 'frontend'
  - Environment 2: 'backend'
```

Environments map to parts of a web project. This may work for headless CMS systems, where frontend and backend are separated software.

Rating: ❌ ❌ ✅ ✅

#### Projects as environments
{#projects-as-environments}

```raw
- App: 'My agency'
  - Environment 1: 'website-1'
  - Environment 2: 'website-2'
  - Environment 3: 'website-3'
```

Web projects map to environments. This might be viable for tiny micro sites, but is sub-optimal. Resources and settings are shared. Individual web project access in collaboration is not possible.

Rating: ❌ ❌ ❌ ✅

#### Projects as apps, stages as folders
{#projects-as-apps-stages-as-folders}

```raw
- App: 'website-1'
  - Environment 1: 'Main'
    - Folders: 'prod', 'staging'
```

In this workflow, environments are ignored, instead stages are mapped as folders in one environment. This may not work as intended.

Rating: ❌ ❌ ❌ ✅

---

## Free trial details
{#free-trial-details}

Each new app at fortrabbit starts with a free trial that is limited in time. Use cases, options and limits.

### Starting a new trial
{#starting-a-new-trial}

Create a new app in to the dashboard.

### Use cases
{#use-cases}

The flexible free trial allows a variety of use cases and workflows. Fair usage of provided resources is expected.

- Exploring the platform
- Feature development
- Handover work to a client
- Weekend experiments

### Trial time limit
{#trial-time-limit}

There is a 72h time limit for the trial. A countdown timer in the dashboard with the app will show you the time left. We may experiment with different timing options.

<!-- ## Extend trial time

:ContactUs{text="Request more trial time"} with support to extend trial time. Write something about your goals and why you need more time. In most cases, we are happy to extend your trial time. This needs to be done ahead of trial end. -->

### Trial end
{#trial-end}

When setting an app in trial mode you can define what shall happen when the trial period ends:

#### Opt-in
{#opt-in}

- no credit card required
- the app will be **deleted** at the end of the trial time
- upgrade at any time before to keep it

#### Opt-out
{#opt-out}

- credit card required (no charges during trial)
- start paying after the trial ends
- cancel at any time before

The free trial is only limited by time. It's possible to book all components in all sizes. For larger plans opt-in is required.

---

## Get started
{#get-started}



---

## Account organization
{#account-organization}

Prefer one fortrabbit account per person. Create additional accounts only for strict separation or when using separate GitHub identities.

### Best use one account only
{#best-use-one-account-only}

A fortrabbit account maps to a person in real life. People manage [apps](#the-app), [teams](#the-team), and [payment methods](#the-payment-method).

| Person      | Team                  | App               | Payment method        |
| ----------- | --------------------- | ----------------- | --------------------- |
| human being | a group of developers | website / web app | object owning apps |
| active      | passive               | passive           | passive               |

#### How NOT to handle one account
{#how-not-to-handle-one-account}

* **No account sharing please** - No need to create an account and share credentials with colleagues or clients. Use [collaboration features](#collaboration-intro).
* **No generic accounts please** - Please sign up with `firstname.lastname@company.com` and not `accounts@company.com`.

### Why to have multiple fortrabbit accounts
{#why-to-have-multiple-fortrabbit-accounts}

In some scenarios it might be advisable to have multiple accounts at fortrabbit as one individual:

#### Strict separation
{#strict-separation}

Collaboration features are designed to be open and transparent. Collaborators can see your other apps, payment methods, and teams on your profile. They can see names and metadata, but cannot access them. Often that is desired; this way you can request access to an app that you need to work on as well.

If you don't want to expose any of your other projects to your co-workers, create a second private account at fortrabbit.

#### Multiple GitHub accounts
{#multiple-github-accounts}

At GitHub you can also use one Account to manage personal repos, contribute to other people's repos, and be part of multiple organizations. But when you have multiple accounts at GitHub, maybe one for work and a private one, you may also want to keep that separation with fortrabbit.

#### GitHub connection limits
{#github-connection-limits}

* You can't connect the same GitHub account to multiple accounts at fortrabbit
* You can't connect multiple GitHub accounts to one account at fortrabbit

#### How NOT to handle multiple accounts
{#how-not-to-handle-multiple-accounts}

* **New account for each app** - NO! You can have multiple apps
* **New account for new trial** - NO! Each new app starts as a new trial
* **New account for each client** - NO! Use [client collaboration](#billing-collaboration)
* **New account for organization** - NO! Use [developer collaboration](#developer-collaboration)

---

## Components intro
{#components-intro}

Individually scalable hosting resources for each environment.

### Intro
{#intro-1}

With VPS hosting you pay for size of your box. Within that box you can run different services. fortrabbit on the other side has a micro service oriented architecture with services running in isolated containers. This architecture is reflected in the pricing. A component represents a service that can be booked and scaled individually per [environment](#the-environment).

PHP, database, but also traffic and storage are components. Most components are available in different sizes, those are called plans and are titled like t-shirt labels: XS, S, M, L …. Different resource attributes are associated with the plans as well.

| **Component** | **Attribute** | **Plan** | **Price** |
| ------------- | ------------- | -------: | --------: |
| PHP           | XXX MB        |       XS |        $X |
| Database      | XXX MB        |       MD |        $X |

See the [components list](#components) for all available components. The [pricing page](https://www.fortrabbit.com/pricing) gives you an overview. The [pricing intro](#pricing-structure) explains level billing concepts.

### Required and optional components
{#required-and-optional-components}

The components PHP, traffic and storage are required, they can not be deselected. All other components are optional.

### Components during the free trial
{#components-during-the-free-trial}

All components are available with the [free trial](#free-trial-details). They are however limited to the smallest plan.

---

## Stack detector
{#stack-detector}

Automatic pre-configuration of hosting settings based on project requirements found with a Git repo.

When connecting a Git repo from GitHub while setting up an app for [git deployment](#deployment-intro), the code in the repo will be scanned using the stack detector:

- [github.com/fortrabbit/stack-detector](https://github.com/fortrabbit/stack-detector) - open source

It will discover the used software packages and versions. Matching settings from the [software templates](#software-templates) will be applied. In addition `composer.json` and `package.json` will be parsed to suggest custom [build commands](#build-commands):

- `npm run build` will be set when a `package.json` is present
- `composer install` will be set when a `composer.json` is present

---

## Software templates
{#software-templates}

We maintain a list of hosting settings for popular software to be pre-configured for smooth setup. When setting up an app with [Git deployment](#the-fortrabbit-github-app) the repos will be parsed by the [stack detector](#stack-detector) and the software will be detected automatically. If the software is not detected or setup without Git deployment is preferred, the software can be chosen by the user. Software templates are version aware (although just major versions).

- Book matching [components](/1.platform/09.components/)
- Enable PHP extensions
- Apply desired [root path](#root-path) — to serve from the right location
- Populate [ENV vars](#using-env-vars-on-fortrabbit) — to connect to the database automatically
- Suggest [post deploy commands](#post-deploy-commands)

This is especially handy with modern software that supports [ENV var](#env-vars-intro) configuration and environment detection — like [Laravel](/2.guides/2.laravel) or [Craft CMS](/2.guides/3.craft-cms) do.

### What it does not do
{#what-it-does-not-do}

The software template will **NOT install** the selected software on your behalf. Installing software with composer is easy. We expect you to have a local development running before. In many cases developers bring existing projects.

---

## Limitations
{#limitations}

Aren't there always some? Heads up so it doesn't cost you hours of researching in the wrong direction.

### This is not VPS hosting
{#this-is-not-vps-hosting}

The fortrabbit platform has a service oriented architecture with individually scalable as components. The [environment](#the-environment) are lightweight containers that are optimized for speedy web delivery of PHP applications. If you are shopping for as much hardware resources as possible for as little money as possible, you might look elsewhere.

### No 1-click installers
{#no-1-click-installers}

When creating an app we ask for the desired software you are about to use. This can be Laravel, Craft CMS, WordPress or alike. That will not install the software. Read more more about the [software templates here](#software-templates).

### No root shell
{#no-root-shell}

The SSH environment is "jailed". So you can use it for deployment and for common tasks around development. Therefore, it's NOT possible to install software like: FFmpeg, Node, NPM, Gulp, webpack, ruby, Rails or a mail server. We do this for security and performance and security design reasons.

### Need to call via php interpreter
{#need-to-call-via-php-interpreter}

To launch a PHP script you need to specify the PHP interpreter explicitly: for example, `php artisan` or `php craft`.

### No image optimization tools
{#no-image-optimization-tools}

Tools like `jpegoptim`, `optipng`, `pngquant`, `SVGO`, `gifsicle` and alike can help to reduce file size of your images. Using such tools are considered a best practice today. Unfortunately they consume a lot of CPU time and memory. fortrabbit apps are build for fast short running light processes, not heavy lifting. Consider using a third party service for this.

### No video compressing
{#no-video-compressing}

`ffmpeg` and `ffprobe` alike are also not available to avoid overuse of resources.

### wkhtmltopdf
{#wkhtmltopdf}

wkhtmltopdf is a popular library to convert HTML to PDF. It's NOT installed and you can not install it on your own for the reasons named above. Check out the following alternatives:

- [dompdf](https://github.com/dompdf/dompdf) is a PHP only PDF by CSS renderer
- Use PDF as a service
- Rethink if you really need PDF?
- Consider PDF creation on the client side with JS in the browser, with [jsPDF](https://parall.ax/products/jspdf) or similar

### Security responsibilities
{#security-responsibilities}

We believe in a clear division of security concerns. We - fortrabbit - take care of the Operating System level and the PHP runtime, you - the developer - are responsible for the software you write and use.

### Service location
{#service-location}

A data center can be chosen for each app individually, but can't be changed later on. The service is available in Euro (€) or US Dollars ($): This can be chosen with each [payment method](#the-payment-method). The fortrabbit headquarters is based in Berlin, time zone is: CET.

### Mailing
{#mailing}

Many applications and websites need to be able to send emails. The classical example is a password reset form for a CMS. Best use a third party service to achieve this. Here are the options:

#### Transactional mail provider
{#transactional-mail-provider}

**Recommended**: to use a "transactional mail service", those are built to ensure email delivery and will notify you when delivery fails — see [transactional mail](#transactional-email-services) for more details. These providers are easily integrated via an API and there are plugins for CMS and frameworks.

#### Direct SMTP
{#direct-smtp}

**Caution**: It's possible to use a mail script that uses SMTP (Simple Mail Transfer Protocol) via an email provider directly. There are countless possibilities how to use SMTP. Most frameworks and CMS have configuration options build in.

Although this is the standard approach, for example sending mails via Microsoft Exchange or Google for Work, but we can not recommend it any more. More mail providers are closing down this option.

To use this option anyhow, it's required to manually open the SMTP ports (25, 465, 587) with the [outgoing firewall rules](#outgoing-firewall).

#### No sendmail
{#no-sendmail}

**Not available**: It's not possible to use sendmail — the Mail Transfer Agent — on fortrabbit. The PHP `mail()` function uses Sendmail by default. Back in the good ol' days, this would simply call the shell command `sendmail` to send an email directly from your web server to the receiving email server. This is a bad practice nowadays and will rarely work. Most big email providers will simply ignore emails from unknown servers to avoid spam.

### PHP PATH_INFO
{#php-path-info}

Our runtime implements PHP via FastCGI + FPM. To utilize `PATH_INFO` you need to do a small hack-around in your `.htaccess` file:

```apache
RewriteCond %{REQUEST_URI} \.php/ [NC]
RewriteRule ^(.+)\.php/(.+)$    /$1.php [NC,L,QSA,E=PATH_INFO:/$2]
```

<!-- TODO:
### Authorization header
{#authorization-header}

If you need the `Authorization` header, for OAuth for example, you have to forward the header explicitly via an ENV variable:

```apache
RewriteCond %{HTTP:Authorization} .
RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]
```
Accurate still? -->

---

## Software support levels
{#software-support-levels}

We take pride in our software knowledge. This document outlines our technical competence levels and the support you can expect.

There are no one-click installers at fortrabbit. Our software guides are mostly about deploying and configuring an existing code base to fortrabbit. Our friendly support chat can help you with all general hosting questions as well as wth general PHP questions. Additionally we are good with certain frameworks and CMS. We have categorized our knowledge in levels.

#### A grade support
{#a-grade-support}

We have really solid hands-on experience with this. Ask us anything on [Craft CMS](/2.guides/3.craft-cms), [Laravel](/2.guides/2.laravel), [Symfony](#symfony-guide)

#### B grade support
{#b-grade-support}

We know how to install it here but have no hands-on experience here in-house: [WordPress](#wordpress-quick-setup-guide), [Statamic](/2.guides/5.statamic), [Kirby](/2.guides/4.kirby), [Grav](#grav-install-guide), October CMS, ExpressionEngine, Yii2, Drupal …

#### C grade support
{#c-grade-support}

You can install this software here. Some clients are using it here already. But we can not give you much specific support: Phalcon, CakePHP, Concrete5, Contao, Joomla!, Magento, ModX, MotoCMS, Neos, PhileCMS, Shopware, Silverstripe, Stacey, TYPO3, Zend, CodeIgniter.

---

## Live code examples
{#live-code-examples}

Literary copy/paste code examples here. Click on deep links to the dashboard directly from the docs here.

### Code example
{#code-example}

```raw
- {{app-name}} - name of the currently selected app.
- {{app-env-name}} - name of currently selected environment.
- {{app-env-id}} - ID of the currently selected environment.
```

- Logged can use the select on the right to change the values
- Unknown users will see the variables in curly braces `{{variable}}`

### Deep links
{#deep-links}

:BlockLink{title="Change plans for {{app-env-name}}" path="/environments/{{app-env-id}}/components"}

- Logged in users see a link
- Unknown users see on info to login to see the link

### How to use
{#how-to-use}

See a select on the left side of docs (desktop version). With that select, the most recently used environment is selected. Change the select to a different environment to show different examples.

### How it works
{#how-it-works}

The login state of the dashboard is stored in a functional cookie, along with a list of environments. It will change appropriate code examples on the current page according to the selected environment. Clearing browser cookie will reset the state.

---

## Concepts
{#concepts}

Nuts and bolts that make up the fortrabbit hosting platform.



---

## Direct code access
{#direct-code-access}

Access files, logs and runtime data in your environment directly.

### As alternative to Git deployment
{#as-alternative-to-git-deployment}

We usually recommend to use [Git deployment](#deployment-intro). But not every developer is used to [Git](#git-intro) yet and it has steep learning curve. Also not all software is ready to be used with Git and [Composer](#composer). Use [rsync](#rsync-deployment), to upload your website.

### SSH
{#ssh}

SSH (Secure Shell) is a network protocol to login to remote web servers. SSH is used in the terminal. It's pre-installed with most operating systems. With SSH you login to have an interactive session on the remote server - the [environment](#the-environment) in our case. SSH is not suited for transferring files from your computer to the server. See the [SSH guide](#ssh-access) for more details.

### SFTP
{#sftp}

SFTP (Secure File Transfer Protocol) is a network protocol to transfer files to and from web servers. It's build on top of SSH. You will usually use it with a graphical interface. See the [SFTP guide](#sftp-access).

### SSH key authentication
{#ssh-key-authentication}

To access code by either method, SSH keys are required. Upload your public SSH keys to your personal account with the dashboard. Read [more about SSH keys here](#ssh-key-setup).

:BlockLink{title="Your SSH keys" path="/you/keys"}

Your code access credentials are stored with your personal account on fortrabbit. This way you always have up-to-date code access on each environment you have access on. It also makes managing the team easy — add/remove collaborators and code access is handled "automagically".

---

## SSH access
{#ssh-access}

### Get ready
{#get-ready}

- You need to have setup [SSH keys](#ssh-key-setup) to authenticate.
- See the direct [code access intro](#direct-code-access) for uses cases and limits.

### Accessing SSH
{#accessing-ssh}

Each [environment](#the-environment) has it's own SSH access. Execute the following in your terminal to login:

:BlockLink{title="See SSH access for {{app-name}} / {{env-name}}" path="/environments/{{app-env-id}}/ssh/"}

```shell
## Connect to your environment via SSH
{#connect-to-your-environment-via-ssh}
$ ssh {{app-env-id}}@ssh.{{region}}.frbit.app
```

If the login went well, you will see a small welcome message:

```raw
–––––––––––––––––––––––  ∙ƒ  –––––––––––––––––––––––
```

### Executing PHP scripts
{#executing-php-scripts}

If you want to execute PHP scripts, including `artisan` and it's like, make sure to specify the PHP interpreter explicitly:

```shell
## will work
{#will-work}
$ php artisan some:command
$ php some-script.php

## will _not_ work:
{#will-not-work}
$ ./artisan some:command
$ ./some-script.php
```

### Using Composer
{#using-composer}

Using [Git deployment](#deployment-intro) will trigger [Composer](#composer) automatically. Therefore, it should not be necessary to run Composer from the environment. If you still need to run Composer manually on the App, you can. Please think twice before using `composer update`, because that will bring your local code out of sync which is likely to cause issues. Use `composer install` instead. Again, running Composer directly on the App is probably not what you want to do.

### Limitations
{#limitations-1}

- This is not a root shell, so you can't install or remove software packages
- Mind that you are using the same runtime as your web application: resource intensive operations will drain memory and CPU from the web execution
- [Worker and cron jobs](#jobs) are managed via the dashboard, not the shell

---

## SFTP access
{#sftp-access}

### Use cases
{#use-cases-1}

SFTP is commonly used by novice developers to upload code. It's not a good practice but get's the job done. We recommend to deploy code via Git or sync using rsync. Sometimes it's a helpful companion tool to look up something quickly.

* **Browse files**: Check what's actually on the server.
* **See logs**: Analyze access or error logs.
* **Upload assets**: If you have large binary files not suitable for Git (though Object Storage is usually better).
* **Troubleshooting**: Quick fixes or inspecting generated files.

### SFTP access details
{#sftp-access-details}

```raw
Host:       ssh.{{region}}.frbit.app
User name:  {{app-env-id}}
Password:   No password required, private SSH used
Protocol:   SFTP (not FTP)
Port:       22
```

### SFTP clients
{#sftp-clients}

There are various SFTP clients out there. Check our [SFTP clients section](#sftp-clients).

### SFTP is not FTP
{#sftp-is-not-ftp}

SFTP is short for SSH File Transfer Protocol. It is used for uploading and downloading files over a SSH connection. Despite the similar name, SFTP is very different than FTP or FTPS internally, but for most practical purposes they are very similar. SFTP is preferable to FTP because the the transferred data is encrypted and not visible to everyone on the network.

### SFTP command line interface
{#sftp-command-line-interface}

The `sftp` command line tool is available on most Unix-like systems, including macOS and Linux.

```bash
## Connect to your environment via SFTP
{#connect-to-your-environment-via-sftp}
sftp {{app-env-id}}@ssh.{{region}}.frbit.app

## Example: Upload a file
{#example-upload-a-file}
put /path/to/local/file.txt /path/to/remote/file.txt

## Example: Download a file
{#example-download-a-file}
get /path/to/remote/file.txt /path/to/local/file.txt
```

### Alternatives
{#alternatives}

Consider using more modern alternatives to SFTP, such as:

* [Git deployment](#deployment-intro) - advanced code deployment
* [SSH](#ssh-access) - interactive terminal access
* [rsync](#rsync-deployment) - repeatable file transfer

---

## Directory structure
{#directory-structure}

When you login with [SFTP](#sftp-access) or [SSH](#ssh-access) to your [environment](#the-environment) you can see the file directory structure. This is what you'll find:

```raw
srv
  data
    www
    home
```

### www
{#www}

The default web root (aka document root) directory is the main tree 'visible' from the web. You can change the routing [root path](#root-path), to any folder below the `htdocs` directory. The [git deployment](#deployment-intro) syncs to the `htdocs` folder as well. `htdocs` is also your 'login folder' - starting point for SSH/SFTP. The whole path looks something like this:

- `/srv/data/www`

<!-- ## tmp

Temporary folder; limited to 2GB of storage. Files older than 15 days will be automatically purged. Typical use cases are the default PHP session file folder or a temp destination for file uploads via PHP (before `move_uploaded_file()` is called). -->

### home
{#home}

Like your `~` on your local machine. Contains bash history, private SSH keys.

- `/srv/data/home`

<!-- ## Other directories

The rest of the folders (and files which are not shown here) are part of the standard Linux distribution. All this stuff is handled by us for you. So you don't need to care about them. You can't change things outside the above outlined context. -->

---

## Code access troubleshooting
{#code-access-troubleshooting}

Can't login by SSH or by SFTP or to your database? Most connectivity issues are related to local configuration. Test with SSH first. Here is what to look for.

### Are your SSH keys correctly set up?
{#are-your-ssh-keys-correctly-set-up}

- Have you setup SSH keys and uploaded the public part to fortrabbit?
- Have you been able to [access code](#direct-code-access) before?
- Is the same key you are using now here working elsewhere?

See our [SSH key setup](#ssh-key-setup) article if you are unsure about your SSH keys.

### Use verbose mode to see what's going on
{#use-verbose-mode-to-see-what-s-going-on}

Add the `-v` (verbose) flag to your login command. The output from this command is useful for troubleshooting issues.

```shell
$ ssh {{app-env-id}}@ssh.{{region}}.frbit.app -v

## OpenSSH_8.4p1, OpenSSL 1.1.1i  8 Dec 2022
{#openssh-8-4p1-openssl-1-1-1i-8-dec-2022}
## debug1: Reading configuration data /home/user/.ssh/config
{#debug1-reading-configuration-data-home-user-ssh-config}
## debug1: /home/user/.ssh/config line 6: Applying options for *
{#debug1-home-user-ssh-config-line-6-applying-options-for}
## debug1: Reading configuration data /etc/ssh/ssh_config
{#debug1-reading-configuration-data-etc-ssh-ssh-config}
## debug1: Authenticator provider $SSH_SK_PROVIDER did not resolve; disabling
{#debug1-authenticator-provider-ssh-sk-provider-did-not-resolve-disabling}
## … more lines here
{#more-lines-here}
```

### Check your local SSH configuration
{#check-your-local-ssh-configuration}

Open the files `~/.ssh/config` and `~/.ssh/known_hosts` and see if there is anything unusual. Delete all entries related to fortrabbit services to reset your local configuration.

### Access error for recently created environment
{#access-error-for-recently-created-environment}

If an environment was recently created, please wait about 5 minutes for it to become ready. Trying to connect before it is ready produces an error. If more than 10 minutes have passed and you still get a similar error (despite successful authentication), then please contact us.

### Access error with recently created SSH key
{#access-error-with-recently-created-ssh-key}

After importing a key in the dashboard, please allow up to 5 minutes for it to be activated.

### You are asked for a password
{#you-are-asked-for-a-password}

If you face a password prompt it can mean a few things:

- Your SSH key is protected by a local passphrase
- The keys in standard location `~/.ssh/` have been rejected
- Other issues on your side, check the verbose output, reset config

### If it takes forever
{#if-it-takes-forever}

If you can't establish a connection at all, or if it takes "forever" to connect and nothing actually happens a few things may be the cause.

- a firewall on your end blocking outgoing connections (not very likely)
- your IP has been quarantined by our service due to too many failed attempts (possible)

Try to figure out if you can connect to external services on port 22 from your network. Try disabling your (corporate) VPN connection, if any.

### Connecting from within a container
{#connecting-from-within-a-container}

When your local development environment is containerized with Docker, DDEV or alike and you want to deploy from within the container, make sure to have the SSH keys installed there as well.

### If it worked before and suddenly stops working
{#if-it-worked-before-and-suddenly-stops-working}

If you have deployed using SSH keys before and now it doesn't work any more:

1. Check if you have changed something, compare your local keys with the remote one
2. See if any change in collaboration happened, do you have access on the app still?

### Host authenticity warning
{#host-authenticity-warning}

The first time you are connecting to fortrabbit service via SSH, there will be a warning about connection to a new SSH server. Just type yes, which will record the fingerprint of the fortrabbit deploy service into the `~/.ssh/known_hosts` file. Say yes here:

```shell
The authenticity of host '…' can't be established
RSA key fingerprint is …
Are you sure you want to continue connecting (yes/no)?
```

If this fingerprint changes in the future, then you will se an error about that and will have to take further action depending on the situation.

---

## Code access overview
{#code-access-overview}

Get direct access on the deployed files on the environment.



---

## Deployment intro
{#deployment-intro}

Code deployment is a multi-step process to deliver code from your local computer to a web server in a reliable and automated fashion.

In regard of deployment, Git is not only used as a version control system, but also as a transport layer to copy over the latest code changes. A typical code deployment on fortrabbit consists of the following deployment pipeline:

### High level concept
{#high-level-concept}

```raw
1 Local   2 Git provider   3 fortrabbit       4 environment
┌─────┐   ┌────────────┐   ┌──────────────┐   ┌──────────────┐
│ Git ├───▶  Git repo  ├───▶  Deployment  ├───▶   web space  │
└─────┘   └────────────┘   └──────────────┘   └──────────────┘
```

1. You work on your local Git repo
2. You push code changes to the git provider (GitHub), to trigger a deployment
3. The deployment service is runs at fortrabbit
4. The build is getting distributed into the web space of the [environment](#the-environment)

### Code moves up, content moves down
{#code-moves-up-content-moves-down}

Development is usually happening in the [local development environment](#intro-to-local-development-with-php). Code changes are pushed up.

- Code tracked with git: templates,plugins, themes, CSS, JS …
- Content not tracked: images, uploads, database …
- Runtime data not tracked: logs, sessions, vendor folder, temporary files …

Content updates whoever are often created in the production environment directly, for instance when an editor is adding a new blog post. In many software systems, code and content are separated and do not interfere. A classical PHP project consists of these blocks:

| What                          | Git deployment | Alternative |
| ----------------------------- | -------------: | ----------: |
| Code and dependencies         |            Yes |           - |
| Database contents             |             No |        dump |
| Image uploads and other files |             No |       rsync |

In addition to git deployment, [direct code access](#direct-code-access) via [SSH](#ssh-access) and [SFTP](#sftp-access) is also available. This is useful to sync down contents.

### What the storage contains
{#what-the-storage-contains}

The Git repo is not a one to one representation of the storage. After you Git push, first the Git repo will be updated, then changes will be synchronized (overwrite but not delete) to the storage. So the storage contains:

1. The latest Git changes synced in
2. Artifacts from build steps
3. Changes done by [direct code access](#direct-code-access)
4. Runtime data like uploads, assets, logs, template fragments …

### Git only syncs up
{#git-only-syncs-up}

**Git is a one way street here and the only way is up.** You can not `pull` the changes, which are made via SSH or SFTP, from the storage back into your Git repo. So you can not upload something via SFTP and clone it down later via Git. While this might looks odd at first: this design keeps your Git repo clean of temporary, binary and other blob data. The diagram above visualizes this. Use Git only for code deployment, not to manage all of your Apps runtime data. Separate code - managed in Git - from content - managed via SSH/SFTP.

### Not all applications work well with Git
{#not-all-applications-work-well-with-git}

Git deployment is great when the skeleton has clean folder structure with exclude patterns and [Composer](#composer) support. [Laravel](#install-laravel-locally) and [Symfony](#symfony-guide) are poster-child-level for good Git support. [WordPress](#wordpress-quick-setup-guide) and other CMS are not Git compatible, out-of-the-box. [Craft](#install-craft-cms-local) works well with Git and Composer.

### Detailed run down
{#detailed-run-down}

```raw

               ┌ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ┐             ┌ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ┐

               │                        Deploy service                   │    ─ ─ ─ ▶  │          Environment          │

┌───────────┐  │  ┌──────────────┬────────────┬────────────────────┐   ┌─┴─────────────┴─┐  ┌──────────────────────┐   │
│           │     │              │            │                    │   │                 │  │                      │
│ 1 Queue   │  │  │ 2 Allocation │ 3 Code     │ 4 Build            │   │ 5 Deploy        │  │ 6 Post deploy        │   │
│           │     │              │ sync       │                    │   │                 │  │                      │
│ Waiting   │  │  │ Preparing    │            │ Build commands     │   │ Syncing deploy  │  │ Executing post       │   │
│ for free  │     │ deployment   │ Pull code  │                    │   │ package into    │  │ deploy commands      │
│ slot      │  │  │ containers   │ from git   │ composer install   │   │ web storage     │  │                      │   │
│           │     │              │ repo into  │ pnpm run prod      │   │                 │  │ artisan migrate:all  │
│           │  │  │              │ deploy     │                    │   │ merge           │  │                      │   │
│           │     │              │ container  │                    │   │ …               │  │                      │
│           │  │  │              │            │                    │   │                 │  │                      │   │
│           │     │              │            │                    │   │                 │  │                      │
│           │  │  │              │            │                    │   │                 │  │                      │   │
│           │     │              │            │                    │   │                 │  │                      │
└───────────┘  │  └──────────────┴────────────┴────────────────────┘   └─┬─────────────┬─┘  └──────────────────────┘   │
               └ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ┼ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ┘             └ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ┘
                                       ▲
                                       │
                                       │
                         ┌ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ┐

                         │          GitHub           │

                         └ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ┘
```

### Deployments and jobs
{#deployments-and-jobs}

After each deployment all running [jobs](#jobs) (workers and crons) will be restarted to make sure they'll be using the latest code.

---

## The fortrabbit GitHub App
{#the-fortrabbit-github-app}

Connect the most popular Git-as-a-service provider with your fortrabbit. Login with GitHub and use automatic git push to deploy.

### Get ready
{#get-ready-1}

- You are confident [using Git](#git-intro).
- You also have a good understanding of the fortrabbit [deployment options](#deployment-intro).
- Finally, you have an account here at fortrabbit as well as with GitHub already.

### Installation
{#installation}

To connect GitHub with fortrabbit you need to install the fortrabbit GitHub App with your account at GitHub:

- [github.com/apps/fortrabbit](https://github.com/apps/fortrabbit)

You can do this when signing up to fortrabbit by choosing GitHub or later with the account settings.

You will be prompted to give it access on your repos as well as to create repos on your behalf. You will also need to choose which context at GitHub you will want to give it access.

### Connect, create or change a repo
{#connect-create-or-change-a-repo}

The Git repo maps to the [app](#the-app) at fortrabbit. When creating an app you will be asked to either choose a repo from GitHub to be connected to the app or to create a new empty repo for the app. Later on you can change the repo of the app.

### Connect, create or change a branch
{#connect-create-or-change-a-branch}

The Git branch maps to the [environment](#the-environment) at fortrabbit. You can create environments for your branches.

### Repos from organizations at GitHub
{#repos-from-organizations-at-github}

You can choose repositories from organizations on GitHub if you have any, and you have given the fortrabbit GitHub app access to them.

### Only matching fortrabbit accounts can deploy
{#only-matching-fortrabbit-accounts-can-deploy}

Automatic deployment is limited to people who have an account at GitHub as well as on fortrabbit and the fortrabbit GitHub app installed. This is a security feature.

### GitHub Actions
{#github-actions}

GitHub is also offering [Github Actions](https://github.com/features/actions), an integrated continuous integration solution. You can use GitHub Actions in combination with our git deployment or with our [direct code access](#direct-code-access) as an alternative workflow to deploy. GitHub Actions give you more control control over the deployment pipeline.

### Removing access
{#removing-access}

You can at any time uninstall the fortrabbit GitHub app from your GitHub account. This will break
deployments. When deleting an app from fortrabbit, the connection over at GitHub will also be removed. Cancelling fortrabbit services will not automatically uninstall the fortrabbit GitHub app.

---

## Build commands
{#build-commands-1}

### Get ready
{#get-ready-2}

- Follow the [deployment section](#deployment-intro).
- Be ready to deploy code by git via the [GitHub integration](#the-fortrabbit-github-app).

### How build commands work
{#how-build-commands-work}

Build commands are a list of commands that will get executed after the [fortrabbit GitHub app](#github-app) has received the latest updates from Git and before those are getting deployed into the web space of the environment. The Git updates, together with the results from the build steps are forming the build package to be released with a [deployment](#deployment-intro).

### Automatic configuration
{#automatic-configuration}

When setting up an app or environment, the fortrabbit GitHub app will use the stack detector to detect and autoconfigure all deployment settings, including build commands. Predefined [software templates](#software-templates) and detection are combined. The most basic auto detected build commands are:

- When `composer.json` file is detected, `composer install` will run.
- When `package.json` is discovered `npm run prod` will run.

### Manually editing build commands
{#manually-editing-build-commands}

Build commands can be found with the git deployment settings in the fortrabbit dashboard. Define them for each [environment](#the-environment).

:BlockLink{title="Set build commands for {{app-name}} / {{environment-name}}" path="/environments/{{app-env-id}}/settings/git/build-commands"}

#### Composer
{#composer}

Most PHP development is done with the help of frameworks or content management systems. These are usually installed as a dependency and themselves using other dependencies. All that code is not part of Git, so when the code get's delivered, those dependencies need to be installed or updated for the given environment. Find more details with our [Composer article](#composer).

#### Node.js
{#node-js}

Most web development is done with the help of JavaScript build tooling. Specific production build steps create optimized build bundles to be served to clients from the web application.

---

## Post deploy commands
{#post-deploy-commands}

Run tasks such as migrations and cache clearing after deployment.

### Get ready
{#get-ready-3}

You have followed the [deployment section](#index) and are ready to deploy code via git using the GitHub integration.

### Architecture
{#architecture}

Post deploy commands are similar to [build commands](#build-commands), but they run after the build files have been copied into the live environment. Both build commands and post deploy commands are run in a separate deployment container.

### Use cases
{#use-cases-2}

- **Database migrations**: Apply schema changes after code deployment
- **Cache clearing**: Refresh application caches to reflect new code
- **Configuration updates**: Apply environment-specific settings
- **Search index rebuilding**: Update search indexes with new content structure

### Relation to deployments
{#relation-to-deployments}

Post deploy commands are done as part of the [deployment object](#the-deployment-object). This means that a deployment might show as failed, but new files were already deployed, if the failure happened in the post deploy commands.

### Setting up post deploy commands
{#setting-up-post-deploy-commands}

Post deploy commands are configured in the fortrabbit dashboard for each [environment](#the-environment). You can access these settings through the deployment configuration:

:BlockLink{title="Edit post deploy commands for {{app-env-id}}" path="/environments/{{app-env-id}}/git/post-deploy-commands"}

### Preset via software templates
{#preset-via-software-templates}

Many [software presets](#software-templates), such as those for Laravel, Symfony and Craft CMS, already include pre-configured post deploy commands.

#### Examples
{#examples}

```bash
## Laravel
{#laravel}
php artisan migrate --force
php artisan config:cache
php artisan route:cache

## Craft CMS
{#craft-cms}
php craft project-config/apply
php craft clear-caches/all

## Symfony
{#symfony}
php bin/console doctrine:migrations:migrate --no-interaction
php bin/console cache:clear --env=prod
```

<!--  TODO: Show examples by single source of truth! -->

### Limits
{#limits}

Post deploy commands are run in a separate deploy resource, which is separate from frontend web delivery resources. The deploy resources are still limited by your booked PHP plan.

### Timing and execution
{#timing-and-execution}

Post deploy commands run after the deployment has been marked as successful. This means:

- If a post deploy command fails, deployment is shown as failed, but new files have already been copied
- Commands execute in sequence, not parallel
- Each command must complete before the next one starts
- Total execution time should be kept reasonable to avoid timeouts

### Best practices
{#best-practices}

- **Cache management:** Consider the impact before clearing all caches every time, especially in production. Cache clearing not only consumes resources, but cache rebuilding can also significantly slow performance.
- **Error handling:** Design your commands to be idempotent (safe to run multiple times) and handle errors gracefully.
- **Monitoring:** Log important post deploy actions so you can troubleshoot issues later.
- **Performance:** Keep commands lightweight and avoid long-running processes that might timeout.

---

## Deployment trigger
{#deployment-trigger}

This settings define how deployment happens from GitHub to the environment.

### Push to deploy
{#push-to-deploy}

This is the default trigger. Deployment happens automatically on every push to the branch that is connected to the environment.

### Manual deployment
{#manual-deployment}

When manual deployment is selected, no automatic deployments will happen. Initiate a deployment from the dashboard.

### Deploy now button
{#deploy-now-button}

Trigger a new deployment for an environment, based on the latest commit. You will find a 'deploy now button' with the deployment settings of the environment and with the deployment that is based on the latest commit. This will use the latest commit as the source and apply all deployment related settings.

:BlockLink{title="Deploy {{app-env-id}} now" path="/confirm/environment-deploy?environment={{app-env-id}}"}

The deploy now action is shown with both deployment trigger settings. Deploying a commit again can be useful when a setting related to deployment has changed. To avoid inconstant states, it is not allowed to deploy an older commit again.

---

## Cached directories
{#cached-directories}

This settings controls whether and which folder are cached for deployment. This will speed deployment from the second time you deploy.

### How it works
{#how-it-works-1}

During most deployments the [build commands](#build-commands) will include something like `composer install` or `npm install`. These processes will download dependencies and populate the `vendor` and the `node_modules` folders. The cached directories defines folder to be preserved and re-used without downloading all dependencies with each deployment. Thus first deployment may take a couple of minutes, but successive deployments will be much faster.

Note that this is a setting that happens on the deploy service, not on the environment, see the [deployment intro](#deployment-intro).

### Default settings
{#default-settings}

```plain
vendor
node_modules
```

In most cases the default setting is what you want. To disable cached directories, save an empty value.

### Purging cached directories
{#purging-cached-directories}

It can be helpful to purge the cached directories. Purging the cached directories, as the title suggests, will delete all files and folders, so next time during deployment a new cache will be created.

There is a button with the dashboard to purge the cache. Saving the cached directories will also purge the cache.

---

## Deployment strategy
{#deployment-strategy}

This setting defines how the deployment result will be distributed to the web space of an environment.

The result of the changes received by git push and the build steps execution is called a deploy package - a temporary file set. This will be put into the storage of the environment somehow. You can change the deployment synchronization strategy setting with the dashboard. The strategy matches with the software and deployment flows to be used. With the [software template](#software-templates) defaults for the deployment strategy are set.

### Blend strategy
{#blend-strategy}

The save strategy for deployment package synchronization is overwrite but not delete:

- Newer files will replace older files on the storage
- New files will be created on the storage
- **Files not present in the deploy package but on the storage will not be touched**

With this no runtime data, like uploads, transforms, caches template fragments and other content will get deleted. It however can result in some weird edge case side effects. When blend strategy is enabled, [patterns to replace](#replace-patterns) certain files and folders can be defined.

### Replace strategy
{#replace-strategy}

Create an exact replica of the current deploy package within the web space. That means, all files in the web space will be deleted first and replaced by the contents of the deploy package. This is sometimes called an immutable deployment. It's related to 12-factor design and ephemeral storage where the web application should not write anything to disk. It allows to rollback to any previous state more easily. This may not play well with old school PHP based web applications.

In addition to the full replace strategy you can set certain [excluded files and folders](#exclude-patterns) that will be sustained from replacement.

---

## Git source directory
{#git-source-directory}

The Git source directory is a dashboard settings for environments that have git deployment enabled. Define which folder with the Git repo should be deployed. In most cases the root path of the repo will work fine. Leave the field empty for that.

### Use cases
{#use-cases-3}

The most common use case is when you have a mono repo that holds multiple websites on one Git repo. For this scenario you can choose to deploy only a sub folder of the root directory, for instance `/apps/website-1`.

---

## Exclude patterns
{#exclude-patterns}

A setting to define files and folders not be replaced during deployment with replace strategy.

This is essential to preserve user uploads, assets, and other user-generated content. This setting is only available when the [deployment strategy](#deployment-strategy) is set to 'replace'. Note that with the replace strategy, all files from the deployment build will replace the content of the actual web storage. Generally, you want to exclude runtime data (files and folder created by the website not with git). Usually this about user uploads, logs, sessions.

Sensible defaults based on [software templates](#software-templates) are provided.

Rsync syntax is supported, allowing regex like patterns. The asterisk `*` serves as a wildcard.

### Examples
{#examples-1}

```yml
### WordPress
{#wordpress}
/wp-content

### Laravel
{#laravel-1}
/storage

### Kirby CMS (if using git + rsync)
{#kirby-cms-if-using-git-rsync}
/content
/media

### Wildcard (rsync regex) syntax
{#wildcard-rsync-regex-syntax}
*/files

### Exclude things to show up in final build
{#exclude-things-to-show-up-in-final-build}
/node_modules
```

### One setting, two use cases
{#one-setting-two-use-cases}

- **Exclude from deployment**: Prevent files from being copied to the environment.
  - Useful for files that are only needed during deployment.
  - `node_modules` are often excluded to keep the runtime clean.
- **Preserve on environment**: Prevent files from being overwritten or deleted.
  - Essential for runtime data created by the application.
  - Example: User uploads, content files, and logs.

### Related
{#related}

When the [deployment strategy](#deployment-strategy) is set to blend, there is an opposite setting to define [replace patterns](#replace-patterns).

---

## Replace patterns
{#replace-patterns}

A setting to define files and folders to be replaced during deployment with blend strategy.

This is essential to avoid old files cluttering the system and confusing the software. This setting is only available when the [deployment strategy](#deployment-strategy) is set to 'merge'. Note that with the blend strategy, all files from the deployment build will synced into the content of the actual web storage. No old files will be deleted.

For certain folders, it's better to delete their content.

Sensible defaults based on [software templates](#software-templates) are provided. Rsync syntax is supported.

Rsync syntax is supported, allowing regex like patterns. The asterisk `*` serves as a wildcard.

### Examples
{#examples-2}

```yml
### Craft CMS
{#craft-cms-1}
/config/project

### Pattern to replace all JPGs
{#pattern-to-replace-all-jpgs}
*.jpg
```

### Related
{#related-1}

When the [deployment strategy](#deployment-strategy) is set to replace, there is an opposite setting to define [exclude patterns](#exclude-patterns).

---

## Deploy logs
{#deploy-logs}

Use deployment logs to understand why a deployment failed.

::CallOut{alert}
We plan to extend deployment logs functionality.
::

### Availability
{#availability}

- Deploy logs are available in the Dashboard; each deployment has its own log.
- Deploy logs appear shortly after the deployment ends.
- Deploy logs are only kept for 14 days after the deployment has finished.

### Common issues for failed deployments
{#common-issues-for-failed-deployments}

It's possible, but not very likely, that failed deployments are caused by a service issue. In most cases they are related to problems in your code and config — likely the with [build commands](#build-commands) or [post deploy commands](#post-deploy-commands).

It's also completely normal to see failing deployments while you are still setting things up.

### Build command errors
{#build-command-errors}

If the deployment is marked as failed and deploy log shows errors and no new code is deployed, most likely the build steps have failed. Read the error message carefully to understand what went wrong. Sometimes [build commands](#build-commands) are pre-configured by [software templates](#software-templates). In some cases these defaults don't match your project and need adjustment.

#### Composer errors
{#composer-errors}

Composer errors are usually caused by configuration issues in your project. Check your `composer.json` (and lock file) for:

- Invalid or conflicting version constraints
- Missing PHP extensions
- Repositories or packages that are no longer available

#### Node.js errors
{#node-js-errors}

Node task errors when running `npm run prod` or similar scripts are also common.

- Are all Node dependencies installed?
- Is the task defined in your `package.json`?
- Does the task succeed in your local development environment?

### Post deploy command errors
{#post-deploy-command-errors}

If the deployment is marked as succeeded, but the log shows errors and the code is actually deployed, the problem is most likely with the [post deploy commands](#post-deploy-commands). These run after the deployment and can fail even though the new code is already live.

### How to fix failing deployments
{#how-to-fix-failing-deployments}

Use the deploy logs to see where the process breaks and what the error message is. Many issues can be resolved just by carefully reading and following the hints from the log.

A frequent problem is a mismatch between local and remote environments: on fortrabbit the environment is usually set to production, while locally you might still be running a development build. Try running your production build locally (for example `npm run build` or `composer install --no-dev`) and fix any issues you see there first.

### Contacting support
{#contacting-support}

We're happy to help you figure out why your deployment fails. When you contact support, please include:

- Details about your project and environment
- What you changed before deploying
- The time of the failing deployment
- The specific error message or relevant excerpt from the deploy log

---

## Deployment troubleshooting
{#deployment-troubleshooting}

Can not deploy by Git? Let's start from scratch to make sure we don't miss anything.

### Get ready
{#get-ready-4}

Before starting to troubleshoot deployment issues, specifically if you are setting up things for the first time, make sure to have everything configured correctly:

- New to Git? Read the [git intro](#git-intro) first
- Read the [deployment intro](#deployment-intro)
- Have the [fortrabbit GitHub app](#the-fortrabbit-github-app) installed with GitHub
- Have an environment connected to a repo at GitHub

### GitHub connectivity errors
{#github-connectivity-errors}

You can NOT push to GitHub? You may see an error in the command line when trying to push or no changes arrive with the repo at GitHub.

- [GitHub: Troubleshooting SSH](https://docs.github.com/en/authentication/troubleshooting-ssh)
- [GitHub: Troubleshooting connectivity problems](https://docs.github.com/en/get-started/using-github/troubleshooting-connectivity-problems)

### Transit errors
{#transit-errors}

You can push to GitHub, the new deployment does not arrive with fortrabbit environment. There is no deployment at fortrabbit.

- Do you have an account at fortrabbit and one on GitHub?
- Make sure to have the [fortrabbit GitHub App](#github-app) installed and connected
- Are you deploying to the branch that is connected?
- How did you set up automatic deployment with fortrabbit?

### Deployment errors
{#deployment-errors}

Everything above is set up correctly, there are deployments with fortrabbit, but they fail.

- Check the [deploy logs](#deploy-logs) to see the error

---

---
title: Deployment overview
naviTitle: Deployment
navigation:  false
---

---

## Using ENV vars on fortrabbit
{#using-env-vars-on-fortrabbit}

Manage environment variables with the fortrabbit dashboard.

:BlockLink{title="Edit ENV vars for {{app-name}} / {{app-env-name}}" path="/environments/{{app-env-id}}/env-vars"}

The input supports the dotenv file format and allows you to create or update multiple variables at once. The changes will be distributed after you save the page. That may take around 60 seconds.

### ENV var types on fortrabbit
{#env-var-types-on-fortrabbit}

There are four different kinds of ENV vars here on fortrabbit which are available to your environment at runtime.

#### Software template ENV vars
{#software-template-env-vars}

Depending on the [detected](#stack-detector) or [chosen](#software-templates) software, additional ENV vars will be seeded for you. This selection will configure the server ENV vars in ways, the software can work with it. For example, for Laravel and Craft, an ENV var like `DB_PASSWORD` will be populated with the password of the database. So, most likely, your fortrabbit environment will work out of the box. As a bonus you even reset the database password without touching any configurations.

#### System ENV vars
{#system-env-vars}

System ENV vars are automatically updated values that contain access details for services offered by fortrabbit. For example:

```apache
MY_MYSQL=${FORTRABBIT_MYSQL_PASSWORD}
## MY_SQL is the key
{#my-sql-is-the-key}
## ${FORTRABBIT_MYSQL_PASSWORD} is an alias for a value populated by fortrabbit
{#fortrabbit-mysql-password-is-an-alias-for-a-value-populated-by-fortrabbit}
```

System ENV vars will not overwrite existing, manually created ENV vars. This means: if you manually create an ENV var, we guarantee that we won't replace it's value by a dynamically generated ENV var.

#### Custom ENV vars
{#custom-env-vars}

Those are the ones you add yourself in the dashboard.

#### Nested ENV vars
{#nested-env-vars}

You can use simple, [nested variables](https://github.com/vlucas/phpdotenv#nesting-variables) in your custom ENV vars. Simple means, that you can set variables which reference other variables, which contain a value, for example:

```apache
## will work:
{#will-work-1}
OTHER_VAR=something
MY_VAR=${OTHER_VAR}
```

Order matters. First define something before referencing. Multiple levels of interpolation are not supported. That means that you cannot use variables, which reference other variables, which again reference other variables, for example:

```apache
## will not work:
{#will-not-work-1}
MY_VAR=${OTHER_VAR}
OTHER_VAR=${ANOTHER_VAR}
ANOTHER_VAR=something
```

### ENV var validation
{#env-var-validation}

Strict validation rules for ENV vars are in use in the dashboard while entering. Chars like the "$" sign can be harmful in Linux systems. Here is the regex we use to validate the ENV var input in the dashboard:

```raw
/^[\p{L}\p{N}\ _\-\+=\.,:;\?!@~%&\*\(\)\[\]\{\}<>\/\\#]+$/u
```

So sometimes, when you want to store an external API key as an ENV var, you might get a validation error like: "Variable value contains invalid characters".

### Base64 encoding and decoding
{#base64-encoding-and-decoding}

Use the Base64 helper in the dashboard to handle special characters, multi-line values, or long strings.

```shell
## Can NOT save this due to special characters
{#can-not-save-this-due-to-special-characters}
MOTTO=$$$$ Rules Everything Around Me

## The tool converts it to Base64 with a prefix
{#the-tool-converts-it-to-base64-with-a-prefix}
MOTTO=fr+base64:JCQkJCBSdWxlcyBFdmVyeXRoaW5nIEFyb3VuZCBNZQ==

## The environment receives the original value
{#the-environment-receives-the-original-value}
MOTTO=$$$$ Rules Everything Around Me
```

The tool encodes your value to Base64 and adds the `fr+base64:` prefix. This encoded value is stored safely. At runtime, the platform automatically decodes it, so your application receives the original value without any extra work.

Laravel and Symfony have similar built-in functionality for variables prefixed with `base64:`. If you use that, the framework handles the decoding. The `fr+base64:` prefix is a platform-level feature that works for any application, regardless of the framework.

### Reserved environment variable names
{#reserved-environment-variable-names}

There are some names you can not use here:

_, \_\_FRBIT\_\_, argc, argv, AUTH*TYPE, CHARSET, CONTEXT_DOCUMENT_ROOT, CONTEXT_PREFIX, DOCUMENT_ROOT,
FCGI_ROLE, FORTRABBIT*_, GATEWAY*INTERFACE, GROUP, HOME, HTTP*\_, HTTPS, LANG, LC\_\_, LOGNAME, MAIL,
MUSL_LOCPATH, OLDPWD, ORIG_PATH_INFO, PAGER, PATH, PATH_INFO, PATH_TRANSLATED, PHP_AUTH_DIGEST, PHP_AUTH_PW,
PHP_AUTH_USER, PHP_SELF, PS0, PS1, PS2, PS3, PS4, PWD, QUERY_STRING, REDIRECT_REMOTE_USER, REMOTE_ADDR,
REMOTE_HOST, REMOTE_PORT, REMOTE_USER, REQUEST_METHOD, REQUEST_SCHEME, REQUEST_TIME, REQUEST_TIME_FLOAT,
REQUEST_URI, SCRIPT_FILENAME, SCRIPT_NAME, SCRIPT_URI, SCRIPT_URL, SERVER_ADDR, SERVER_ADMIN, SERVER_NAME,
SERVER_PORT, SERVER_PROTOCOL, SERVER_SIGNATURE, SERVER_SOFTWARE, SHELL, SHLVL, SSH_CLIENT, SSH_CONNECTION,
SSH_TTY, TERM, USER

---

## Password protection
{#password-protection}

Control public access to your environment with HTTP Basic Authentication for staging and development workflows.

:BlockLink{title="Edit password protection for {{app-name}} / {{app-env-name}}" path="/environments/{{app-env-id}}/settings/password-protection"}

When enabled, visitors must enter a username and password before accessing any page on your website. It applies to all domains routed to the environment.

### Use cases
{#use-cases-4}

- **Staging environments**: Protect environments from public access while allowing stakeholders and team members to review content before going live.
- **Development workflows**: Restrict access during development to prevent search engine indexing and public access to work-in-progress features.
- **Client previews**: Share protected environments with clients for review without public access.
- **Content preparation**: Protect environments during content updates, data imports, or major changes.

### Configuration
{#configuration}

- **Enable/disable**: Toggle protection without losing configured credentials.
- **Username and password**: Set custom credentials independent of your fortrabbit account.

Each environment has its own password protection settings, allowing different access controls across environments.

### How it works
{#how-it-works-2}

Password protection uses HTTP Basic Authentication (HTTP-auth) to restrict public access via HTTP to your environment. it:

- Shows a browser authentication dialog to visitors
- Persists authentication for the browser session
- Protects all pages, assets, and API endpoints
- Prevents search engine indexing

### Considerations
{#considerations}

- **Security level**: Provides basic access control suitable for preventing casual access, not high-security protection.
- **SEO impact**: Password-protected environments are not indexed by search engines.
- **Team access**: Share credentials securely with team members and stakeholders.
- **Production use**: Consider user experience impact before enabling on live websites.

### Technical details
{#technical-details}

Password protection is implemented at the web server level before your application code executes, ensuring consistent protection across all content. The authentication header is available to your application for additional logic if needed.

### Alternatives
{#alternatives-1}

Username/password can also be [configured through .htaccess](#http-auth) instead of the dashboard setting. Some software systems also offer settings or plugins for that.

---

## Routing options
{#routing-options}

How to configure public HTTP access for environments.

### Test domain
{#test-domain}

Each [environment](#the-environment) has a unique public test domain assigned that is constructed like `{{app-env-id}}.frbit.app`. Use it during development, testing or [multi staging](#staging-environments). Look up the actual name for your test domain with the dashboard under the environment overview.

### External domains
{#external-domains}

You can register your environment to accept requests from any external custom domain you route to fortrabbit — see also [the domain article](#the-domain). To set up a domain routing, you add a new custom domain within your App's domain settings in the dashboard.

### Main domain
{#main-domain}

Each environment has a main domain. It is exposed as a routing setting with the environment of the dashboard. The thumbnail preview shown with the dashboard uses the main domain as the source. It's also used for internal monitoring services. There is also a dynamic [ENV var](#env-vars-intro) that maps to the currently configured value.

:BlockLink{title="Change the main domain" path="/environments/{{app-env-id}}/settings/main-domain"}

---

## PHP settings
{#php-settings}

[Environments](#the-environment) ship with an opinionated (think optimized) pre-configuration of PHP settings. Those also depend on the [software template](#software-templates). The dashboard exposes the most important settings to configure the PHP version and certain PHP extensions.

:BlockLink{title="Edit root path vars for {{app-name}} / {{app-env-name}}" path="/environments/{{app-env-id}}/php"}

### Available settings
{#available-settings}

- PHP version
- PHP extensions
- PHP ini settings
  - `post_max_size`
  - `max_input_size`
  - `output_buffering`
  - `max_execution_time` ← Keep it low. [Why?](#php-processes)
  - `upload_execution_filesize`

### See all specific settings
{#see-all-specific-settings}

Use [phpinfo](#php-info) to dump all the PHP settings.

### Add additional settings
{#add-additional-settings}

Use [user.ini](#configure-user-ini) for more fine grained control over PHP settings.

---

## Root path
{#root-path}

The root path refers to the directory that serves as the entry point for public requests from the world wide web.

:BlockLink{title="Edit root path vars for {{app-name}} / {{app-env-name}}" path="/environments/{{app-env-id}}/settings/rootpath"}

Per default all the [domains](#the-domain) of the environment will route to the same root path (sometimes this is also called: document root, docroot or root folder): `htdocs`. This path is where the first `index.php` will be called, when people are visiting your App on any domain. This path setting can vary, depending on what the framework or CMS you have selected in the software chooser when creating the app.

You can however set the root path afterwards at any given time by tinkering with [.htaccess](#redirects) to enable per domain routing.

### Plain default
{#plain-default}

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

### Modern root path settings
{#modern-root-path-settings}

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

### Root path setting on fortrabbit
{#root-path-setting-on-fortrabbit}

On fortrabbit you can set the root path for each environment with the routing settings in the dashboard. When choosing a [software template](#software-templates) the correct root path will pre-configured.

---

## Incoming firewall (WAF)
{#incoming-firewall-waf}

Bots and crawlers scan your website for vulnerabilities and content. Keep out the bad actors.

::CallOut{alert}
This feature implementation is currently in testing.
::

Even unsuccessful requests do harm by consuming hosting resources and spamming logs. This can be bad for performance and consumes unnecessary energy. Specifically AI bots that ignore `robots.txt` can hammer websites considerably.

#### Implementation
{#implementation}

The current incoming firewall implementation is a 'poor mans WAF'. [nG Firewall](https://perishablepress.com/ng-firewall) by Perishable Press is used. It blocks out bad requests and most bad bots on the web server level by using a standard set of .htaccess rules.

### Usage
{#usage}

We provide an easy to use interface to turn on/off a WAF. Visit the PHP settings of the environment to enable or disable the setting.

:BlockLink{title="Set WAF for {{app-env-id}}" path="/environments/{{app-env-id}}/settings/firewall-incoming"}

### Quirks
{#quirks}

Bots are a major problem. The current solution provided is in testing while we are also exploring alternative approaches.

#### Possible performance impacts
{#possible-performance-impacts}

We are testing performance impacts. While this keeps the Apache more busy with each request, fewer requests will reach the PHP engine.

#### Chicken egg problems
{#chicken-egg-problems}

The firewall should only be activated after a software has been installed. An active WAF setting may prevent software to be installed.

### Alternatives
{#alternatives-2}

There are plenty of alternatives to using the WAF setting.

#### Create your own .htaccess
{#create-your-own-htaccess}

There are rules which may be specific to your use case but which are not necessarily required for everyone. Use an `.htaccess` file to write your own rules. See our [htaccess section](/3.dev/htaccess) for more.

#### Use an external service
{#use-an-external-service}

Some DNS infrastructure providers offer 'bot control' services where bad traffic will be filtered before it even reaches the web server.

- [Cloudflare bot management](https://www.cloudflare.com/application-services/products/bot-management)
- [AWS WAF Bot control](https://aws.amazon.com/waf/features/bot-control)

---

## Outgoing firewall
{#outgoing-firewall}

By default, outgoing (egress) traffic is limited on most non-standard ports for security reasons. Open ports from the dashboard to make outgoing calls from the app environment.

:BlockLink{title="Outgoing firewall settings for {{app-env-id}}" path="/environments/{{app-env-id}}/settings/firewall-outgoing"}

Open ports with [environment](#the-environment) settings in the dashboard. Outgoing firewall rules are environment specific.

### Outgoing IPs
{#outgoing-ips}

The outgoing firewall settings also show the outgoing IP for the environment.

---

## Logs
{#logs}

Analyzing logs is an important part of maintaining a stable and secure website. Error logs often help to identify bugs and other issues. Here is how on fortrabbit.

::CallOut{alert}
Log usage is subject to change. For now an intermediate solution is offered. The output format and kind of access will change.
::

### Tailing logs
{#tailing-logs}

1. Login by SSH to the environment
2. Run `frbit-tail-logs` to see live log streaming

This will provide you a stream of logs.

### Log files in your CMS or framework
{#log-files-in-your-cms-or-framework}

Mind that your CMS or framework might pipe logs to a different location, other than `stderr` and `stdout`. If they do, you will not see the error output in the fortrabbit dashboard. You can still access the logs by [SSH](#ssh-access) or [SFTP](#sftp-access), please see your CMS / framework docs where the logs are stored.

Most CMS and frameworks also offer options to send these logs to the standard locations. With the [software template](#software-templates) the setting is getting pre-populated, if possible, by ENV var.

- [Craft CMS logging](#logging)
- [Laravel logging](#logging)

#### Verbose logging
{#verbose-logging}

Your CMS / framework might offer verbose logging, often this is connected to environment settings of the CMS / framework. Often more debugging information is printed with the error and sometimes errors are even send to the browser. Use that with care, since it can have a considerable performance impact. The general advice is to use it for development and staging environments, but not for production. If you happen to have an issue in production that requires verbose logging, turn it off, after you have finished.

---

## Metrics
{#metrics}

Working with metrics in the dashboard.

::CallOut{alert}
This feature is not implemented yet.
::

### Usage metrics
{#usage-metrics}

Those show you the current status of the storage, MySQL storage in context.

### Performance metrics
{#performance-metrics}

Those show you how fast your App is and where you might need to improve. Performance metrics are: requests, PHP response time, traffic, errors and other useful stuff. You can set different time intervals to monitor performance over time.

---

## Hosting settings
{#hosting-settings}

These hosting settings are all exposed through the dashboard, individually for each environment.



---

## Database access intro
{#database-access-intro}

### Get ready
{#get-ready-5}

To connect to the remote MySQL database, it first need to be booked. The [MySQL component](/platform/components/mysql) is optional but pre-booked for database driven software systems.

To be able to connect to the remote database from your computer, also a [local development environment](#intro-to-local-development-with-php) with `mysql` and `mysqldump` is required for terminal usage. A database GUI such as Workbench or Sequel Ace is another option. Different local development environments come with different paradigms for working with a database. For containerized systems, the database service might not be directly exposed.

### Next steps
{#next-steps}

- [Connect from within the environment](#database-access-from-within-the-environment)
- [Database access via terminal from local](#database-access-via-terminal)
  - [Database up via terminal](#database-up-via-terminal)
  - [Database down via terminal](#database-down-via-terminal)
- [Database access via GUI from local](#database-access-via-gui)
  - [Database up via GUI](#mysql-database-upload-from-local-to-remote-by-gui)
  - [Database down via GUI](#mysql-database-download-from-remote-to-local-via-gui)

### Dashboard settings
{#dashboard-settings}

:BlockLink{title="See MySQL access dashboard settings for {{app-name}} / {{app-env-name}}" path="/environments/{{app-env-id}}/mysql#access"}

---

## Database access via terminal
{#database-access-via-terminal}

Connect to the remote database hosted on fortrabbit from your local machine by terminal commands.

The following commands are run on your local computer. The `mysql` command line client is required. Exact commands may differ depending on the kind of [local development environment](#intro-to-local-development-with-php).

```shell
## 1. Create a tunnel in a dedicated terminal window
{#1-create-a-tunnel-in-a-dedicated-terminal-window}
ssh -N -L 13306:mysql:3306 {{app-env-id}}@ssh.{{region}}.frbit.app
## This will have no output. That's Ok. Open a new window
{#this-will-have-no-output-that-s-ok-open-a-new-window}
```

```shell
## 2. In a new window connect to the database
{#2-in-a-new-window-connect-to-the-database}
$ mysql -u {{app-env-id}} -h127.0.0.1 -P13306 -p -D {{app-env-id}}
## In the next step you will be asked for your MySQL password.
{#in-the-next-step-you-will-be-asked-for-your-mysql-password}
```

<!-- :BlockLink{title="MySQL access for {{app-name}} / {{app-env-name}}" path="/environments/{{app-env-id}}/mysql#access"} -->

### Next
{#next}

- [Database upload via terminal](#database-up-via-terminal)
- [Database download via terminal](#database-down-via-terminal)

### Port setting
{#port-setting}

Port local 13306 is just an example, any port in the range 1025-65535 can be used. The remote port 3306 must be 3306.
This command is not supposed to print a confirmation message. If nothing shows up: you did it right!

### Troubleshooting
{#troubleshooting}

- The most common issue is to expect output with the tunnel command. No response is good. Open a new terminal window and continue.
- The second most common issue is to expect output with the tunnel command. No response is good. Open a new terminal window and continue.
- The third most common issue is to expect output with the tunnel command. No response is good. Open a new terminal window and continue.
- It's `127.0.0.1` not `localhost`.

---

## Database access via GUI
{#database-access-via-gui}

Connect to the remote database hosted on fortrabbit from your local machine using a GUI.

:BlockLink{title="See MySQL access for {{app-env-id}}" path="/environments/{{app-env-id}}/mysql#access"}

Using a database graphical user interface has many benefits: Visually browse and edit the database, get hints running queries, save connection details as bookmarks. It's also practical to have the client connect to the remote and to the local database. See our [database integration section](#database-clients) with specific guides for [Sequel Ace](#sequel-ace), [Workbench](#mysql-workbench) and others.

### General instructions
{#general-instructions}

fortrabbit requires database connections via SSH tunnel. All MySQL clients support this configuration, typically through a dedicated SSH tunnel tab.

- SSH part
  - **SSH Host**: `ssh.{{region}}.frbit.app`
  - **SSH User**: `{{app-env-id}}`
  - **SSH Keyfile**: Your local SSH private key
- MySQL part
  - **MySQL Host**: `mysql`
  - **MySQL Server Port**: `3306`
  - **Username**: `{{app-env-id}}`
  - **Password**: Look it up in the dashboard
  - **Default Schema**: `{{app-env-id}}`

### Next steps
{#next-steps-1}

- [Database up via GUI](#mysql-database-upload-from-local-to-remote-by-gui)
- [Database down via GUI](#mysql-database-download-from-remote-to-local-via-gui)

### Troubleshooting
{#troubleshooting-1}

The most common issues setting up the remote connection via database GUI are:

- Using no tunnel. Connect via SSH tunnel.
- Using localhost. Hostname is `mysql`.

---

## Database access from within the environment
{#database-access-from-within-the-environment}

How to configure code to connect to the database on fortrabbit.

### Automatic software configuration
{#automatic-software-configuration}

We recommend [ENV var](#env-vars-intro) configuration. Thanks to [software templates](#software-templates) ENV vars for connecting to the database are automatically mapped. Software like [Laravel](/2.guides/2.laravel), [Symfony](#symfony-guide), [Craft CMS](/2.guides/3.craft-cms) or [Statamic](/2.guides/5.statamic) will connect to the database without additional configuration.

```php
// Generic example for illustration purposes
$pdo = new \PDO(
  'mysql:host='. getenv('MYSQL_HOST'). ';dbname='. getenv('FORTRABBIT_DATABASE'),
  getenv('DATABASE_USER'),
  getenv('DATABASE_PASSWORD'),
);
$pdo->query("SELECT * FROM ...")
```

Environment variables for database connections that are automatically mapped to specific keys for various software systems:

- `FORTRABBIT_DATABASE`
- `FORTRABBIT_DATABASE_USER`
- `FORTRABBIT_DATABASE_PASSWORD`
- `FORTRABBIT_DATABASE_HOST`
- `FORTRABBIT_DATABASE_PORT`

### Manual software configuration
{#manual-software-configuration}

[WordPress](#wordpress-quick-setup-guide), for example, does not support ENV configuration. You will need to enter the database credentials during the install process or with the configuration files. Please look up the database credentials, such as database name, user and password with the dashboard.

:BlockLink{title="Database credentials for {{app-name}} / {{app-env-name}}" path="/environments/{{app-env-id}}/database#access"}

### Connecting via SSH session
{#connecting-via-ssh-session}

The command-line tools `mysql` and `mysqldump` are available via [SSH](#ssh-access). When you are logged just type `mysql` to login to the MySQL server.

---

## MySQL access
{#mysql-access}

All the ways to connect to the remote database.



---

## Database export/import
{#database-export-import}

Options to upload a database from local to remote and downloading a database from remote to local.

### Get ready
{#get-ready-6}

Database import/export is a crucial task. Sync the state of a remote environment with a local environment. For that it requires:

- Have a [local development environment](#intro-to-local-development-with-php) running.
- Be able to [access the remote fortrabbit database](#database-access-intro).

MySQL doesn't support incremental updates, so you'll always export the complete database structure and contents. This involves creating a `dump.sql` file from the source database and importing it to the destination database. The process works in both directions:

- **Upload**: Export from local and import to fortrabbit
- **Download**: Export from fortrabbit and import to local

During initial setup, you'll typically import your local database to fortrabbit at least once. Later, as content is added with the production environment, sync changes back to the local environment periodically.

Using `mysqldump` and `mysql` is the standard approach to migrate data between MySQL servers from the command line.

### Next
{#next-1}

Depending on your local development environment setup and preferences, certain commands may differ.

- [Database access via terminal from local](#database-access-via-terminal)
  - [Database up via terminal](#database-up-via-terminal)
  - [Database down via terminal](#database-down-via-terminal)
- [Database access via GUI from local](#database-access-via-gui)
  - [Database up via GUI](#mysql-database-upload-from-local-to-remote-by-gui)
  - [Database down via GUI](#mysql-database-download-from-remote-to-local-via-gui)

---

## Database up via terminal
{#database-up-via-terminal}

- [Database access intro](#database-access-intro)
- [Database export/import intro](#database-export-import)
- [How to connect to the remote database via terminal](#database-access-via-terminal)

The following commands are run in your local development environment. `mysql` and `mysqldump` are required.

```shell
## Terminal 1
{#terminal-1}
## Export database from your local machine
{#export-database-from-your-local-machine}
$ mysqldump --set-gtid-purged=OFF -u{{local-db-user}} -p {{local-db-name}} > dump.sql
## You'll be prompted for your local database password
{#you-ll-be-prompted-for-your-local-database-password}

## Open the SSH tunnel
{#open-the-ssh-tunnel}
ssh -N -L 13306:mysql:3306 {{app-env-id}}@ssh.{{region}}.frbit.app
## No output. Open a new terminal window!
{#no-output-open-a-new-terminal-window}
```

```shell
## Terminal 2 (new window)
{#terminal-2-new-window}
## Import Database
{#import-database}
mysql -h127.0.0.1 -P13306 -u{{app-env-id}} -p {{app-env-id}} < dump.sql
## You'll be prompted for your MySQL password (found in the dashboard).
{#you-ll-be-prompted-for-your-mysql-password-found-in-the-dashboard}
## The `dump.sql` file is from the first step.
{#the-dump-sql-file-is-from-the-first-step}
## Can take a while, depends on size.
{#can-take-a-while-depends-on-size}
```

### Development environments
{#development-environments}

Local developments based on containers may require some extra steps, like logging in to the MySQL container or executing commands on the container.

- Docker
  - `docker exec -i {container} …` - execute a command
- DDEV
  - `ddev export-db > dump.sql` command to export a database
  - `ddev auth` - login to the container (first)
  - `ddev exec …` - execute a command

---

## Database down via terminal
{#database-down-via-terminal}

- [Database access intro](#database-access-intro)
- [See database export/import intro](#database-export-import)
- [How to connect to the remote database via terminal](#database-access-via-terminal)

```shell
## Terminal window 1
{#terminal-window-1}
ssh -N -L 13306:mysql:3306 {{app-env-id}}@ssh.{{region}}.frbit.app
## This has no output. Open a new terminal window next.
{#this-has-no-output-open-a-new-terminal-window-next}
```

```shell
## Terminal window 2
{#terminal-window-2}
## 01. Create a dump from the remote database
{#01-create-a-dump-from-the-remote-database}
mysqldump --set-gtid-purged=OFF --no-tablespaces -h127.0.0.1 -P13306 -u{{app-env-id}} -p {{app-env-id}} > fortrabbit-backup.sql

## 02. Import to your local database
{#02-import-to-your-local-database}
mysql -u{{local-db-user}} -p {{local-db-name}} < fortrabbit-backup.sql
```

### Other development environments
{#other-development-environments}

Steps may differ on containerized development environments. It might be required to login to a container or specifically execute a command on the container.

- Docker
  - `docker exec -i {container} …` - execute a command
- DDEV
  - `ddev import-db < dump.sql` - import a database from host
  - `ddev auth` - login to the container (first)
  - `ddev exec …` - execute a command

---

## MySQL database upload from local to remote by GUI
{#mysql-database-upload-from-local-to-remote-by-gui}

Upload a local database to the fortrabbit remote via a graphical user interface.

### Get ready
{#get-ready-7}

- [Database access intro](#database-access-intro)
- [Database export/import intro](#database-export-import)
- [How to connect to the remote database through a MySQL GUI](#database-access-via-gui)

### Export from local
{#export-from-local}

1. Open your MySQL GUI
2. Open your local database connection
3. Choose: Server > Data Export from the menu
4. Select your local database name
5. Make sure to "Dump Structure and Data"
6. Choose a local destination file
7. Start the export

### Import to fortrabbit
{#import-to-fortrabbit}

1. Open your MySQL GUI
2. Open the remote database connection
3. Choose: Server > Data Import from the menu
4. Choose your previously generated dump file
5. Start the import

---

## MySQL database download from remote to local via GUI
{#mysql-database-download-from-remote-to-local-via-gui}

Upload a remote database to your local development environment.

### Get ready
{#get-ready-8}

- [Database access intro](#database-access-intro)
- [Database export/import intro](#database-export-import)
- [How to connect to the remote database through a MySQL GUI](#database-access-via-gui)

#### Export from fortrabbit
{#export-from-fortrabbit}

1. Open your MySQL GUI
2. Open the remote database connection
3. Choose: Server > Data Export from the menu
4. Select the remote database name
5. Make sure to "Dump Structure and Data"
6. Choose a local destination file
7. Start the export

#### Import to local
{#import-to-local}

1. Open your MySQL GUI
2. Choose: Server > Data Import from the menu
3. Choose your previously generated and downloaded dump file
4. Start the import

---

## MySQL export/import
{#mysql-export-import}

Syncing the database down and up.



---

## Advanced database tips
{#advanced-database-tips}

### Time zone
{#time-zone}

MySQL has [time zone support](http://dev.mysql.com/doc/refman/5.5/en/time-zone-support.html). Our Nodes are defaulting to the standard time zone UTC+00 (aka GMT). If you want to change this time zone, you can do so on a "per connection" basis.

There are two approaches to tackle this issue: handle the time zone on application level or handle the time zone on database level. Each has its merits and which one is better strongly depends on the use case.

### GTID flag for import/export
{#gtid-flag-for-import-export}

The `--set-gtid-purged=OFF` option prevents GTID-related permission errors during import. This is required when:

- Your source database has GTID enabled
- You're using MariaDB locally
- You encounter `#1227 - Access denied; you need SUPER privilege(s)` errors

#### Setting time zone in MySQL
{#setting-time-zone-in-mysql}

The syntax to change the time zone is:

```sql
-- set time zone to +3 hours
SET time_zone = '+03:00';

-- set time zone to -7 hours
SET time_zone = '-07:00';
```

You can query the current time zone like so:

```sql
SELECT @@session.time_zone;
```

#### Setting time zone with PDO
{#setting-time-zone-with-pdo}

`PDO` offers configurable options when setting up the connection. One of them allows you to issue commands right after initialization (connection).

```php
$pdo = new PDO(
    'mysql:host='. getenv('MYSQL_HOST'). ';dbname='. getenv('MYSQL_DATABASE'),
    getenv('MYSQL_USER'),
    getenv('MYSQL_PASSWORD'),
    array(
        PDO::MYSQL_ATTR_INIT_COMMAND => 'SET time_zone = \'+02:00\''
    )
);
```

### Resetting the MySQL password
{#resetting-the-mysql-password}

Instead of looking up the existing MySQL password, you can also reset it. Do so in the Dashboard > app > environment > MySQL. Please mind that this comes with consequences:

- Unless your are using [env vars](#env-vars-intro): You'll need to change the password in your code configuration files
- Your coworkers need to change their password in their locally configured remote access tools (see below)

### Accessing MySQL from a different environment
{#accessing-mysql-from-a-different-environment}

It is possible to access a MySQL from another environment within the same region (EU, US). The database from `environment-A` can be accessed from `environment-B`. This works since both environments are within the same network. You will only need to update the MySQL access credentials to do so. There are not many good use cases for this, but it might be good to know.

### Accessing the remote MySQL from your local environment
{#accessing-the-remote-mysql-from-your-local-environment}

It is also possible to access the fortrabbit database from the local installation. You will need to open a tunnel, as described above to do so. While possible we do not recommend that approach. You local App will feel slow, unless you have a very good internet connection. Further, you will run the risk of messing up the database if several apps are writing to it at the same time. The best practice here is separating the local development environment from production.

### MySQL limits
{#mysql-limits}

Each App has one database named like the App. The mysql-user you have received is not granted the privileges to `CREATE DATABASE`. Please mind that `CREATE SCHEMA` requires the same permission.

### Using MySQL functions, procedures and triggers
{#using-mysql-functions-procedures-and-triggers}

By default you don't have permissions to create MySQL functions, procedures and triggers as it requires SUPER privileges.

---

## Database troubleshooting
{#database-troubleshooting}

Common issues connecting to your database on fortrabbit.

### Can't connect from local
{#can-t-connect-from-local}

The most common misunderstanding when trying to connect from a local machine, is that people overlook to first open up the SSH tunnel and then connect to the database. Graphical MySQL clients support this connection method out of the box.

You'll need to **enter both: SSH access and MySQL access details**. Within the fortrabbit dashboard under your App > Access, there is a small link labeled: "Show SSH tunnel info" which will reveal everything you'll need to enter in a MySQL client to connect to the remote database.

:BlockLink{title="See MySQL access for {{app-env-id}}" path="/environments/{{app-env-id}}/mysqll#access"}

### max_user_connections error
{#max-user-connections-error}

You'll see a `max_user_connections` error when you've reached the max connection limit.

```sql
SQLSTATE[HY000] [1226] User 'xxxxxx' has exceeded the 'max_user_connections' resource (current value: 10)
```

The limit is defined by the [MySQL component](#mysql). Typical causes are:

- too many concurrent connections from the web
- every requests starts multiple connections to MySQL
- a background cron job or worker keeps connections open for a long time
- lingering queries that run for a long time
- MySQL GUI client opens too many connections (see below)

Figure out what's causing connections to linger → eliminate those causes.

#### GUI clients eating MySQL connections
{#gui-clients-eating-mysql-connections}

You are trying to connect to the database with a MySQL GUI, like Navicat, Workbench or Sequel Ace? Some those clients are "eating" MySQL connections like popcorn. With fortrabbit, the MySQL connections and the PHP processes are limited. If you use up all the allotted connections, it can take a little until the App recovers. If this turns out to be a problem for you, look into limiting the number of concurrent connections from your MySQL gui or the App itself.

### Access denied; missing SUPER privileges
{#access-denied-missing-super-privileges}

<!-- TODO: Review by infra. Maybe remove? -->

When importing a database dump you've created with a recent version of `mysqldump`, you may experience errors like this:

```raw
#1227 - Access denied; you need (at least one of) the SUPER privilege(s) for this operation
```

To prevent this error, create the dump again using the `--set-gtid-purged=OFF` option. If you don't use the `mysqldump` command line tool directly, but a GUI that relies on it, the chance is very high there is a checkbox to disable "GTID PURGED".

### Connection timeouts during large imports
{#connection-timeouts-during-large-imports}

- Split large dumps into smaller files
- Use `--single-transaction` flag for consistent snapshots

### Permission errors
{#permission-errors}

- Ensure you're using correct MySQL credentials from the dashboard
- Add `--set-gtid-purged=OFF` to the mysqldump command to maximize compatibility
- Add `--no-tablespaces` to the mysqldump command to maximize compatibility
- Check that you're running commands from your local machine, not via SSH

### Encoding issues
{#encoding-issues}

- Add `--default-character-set=utf8mb4` to both export and import commands
- Ensure your dump file is saved with UTF-8 encoding

---

## MySQL overview
{#mysql-overview}

Everything we know supporting our clients running MySQL.



---

## PHP
{#php}

The PHP component provides instantly scalable computing power for PHP.

### Booking
{#booking}

Choose the PHP component plan while creating a new [app](#the-app) or a new environment. For an existing environment you can visit the components page to change the PHP plan.

### Configuration
{#configuration-1}

Find PHP related setting pages with each of your [environments](#the-environment) in the dashboard. Here you can switch the PHP version and configure various PHP extensions and settings. There are also metrics and PHP related logs.

### Scaling
{#scaling}

PHP plans differ mostly in the available memory, as well as the number of PHP processes. Start small, scale later. Test and experiment with different scaling settings. Usually you will not need to change it over time. Keep an eye on memory and swap metrics in the dashboard.

#### Autoscaling
{#autoscaling}

Autoscaling for PHP is not available. This is because of the flaky nature of PHP processing time going up and down and different customer requirements.

#### Shared plans
{#shared-plans}

These are the most commonly used plans. Indeed the XS and the S plan are covering most normal website scenarios already. Some software systems have system requirements. The values below are good starting points from our experience:

| Software                         | PHP memory |
| -------------------------------- | ---------: |
| Craft CMS, October CMS           |     512 MB |
| WordPress, Kirby, Grav, Statamic |     256 MB |

The actual memory requirements are highly individual. It depends on the number of visitors, plugins and configuration and the custom code you write. See our [performance design section](#performance) for more.

### Dedicated plans
{#dedicated-plans}

Higher plans are available for heavy users and e-commerce systems.

### MySQL connections for PHP
{#mysql-connections-for-php}

The PHP plan also comes with matching MySQL connections, so that each PHP process can make one connection and there are some extra MySQL connections for connecting with a client from outside.

| PHP plan | PHP processes | MySQL connections |
|----------|--------------:|------------------:|
| XS       | 2             | 8                 |
| SM       | 2             | 8                 |
| MD       | 2             | 8                 |
| LG       | 4             | 12                |
| XL       | 6             | 16                |
| 2XL      | 8             | 24                |

---

## MySQL
{#mysql}

Scalable database resources, optional, on demand. MySQL is part why PHP is so popular. It's the M in the LAMP stack.

Most classical CMS systems, such as [WordPress](#wordpress-quick-setup-guide) and [Craft CMS](#install-craft-cms-local) are using it as the central data storage. Alternatives to MySQL are PostgreSQL and Redis derivatives like Valkey.

### Booking MySQL
{#booking-mysql}

A MySQL database is an optional component available in different plans. Each [environment](#the-environment) can have one database component containing one database booked. The database can have multiple tables of course. Currently, only MySQL databases are available.

### Configuration
{#configuration-2}

When the database is enabled, multiple settings and metrics become available in the dashboard. Please refer to the [MySQL usage section](/3.dev/08.mysql) to learn more.

### Scaling
{#scaling-1}

Database plans differ mostly in the available storage, as well as the associated computing power. Usually MySQL and [PHP](#php) are scaled alongside since they rely on each other. As a rule of thumb, match PHP XS with MySQL XS, PHP SM with MySQL SM etc.

When [autoscaling](#autoscaling) is enabled, smaller and larger plans are automatically booked, based on usage.

#### MySQL OFF
{#mysql-off}

The database is optional on fortrabbit. Your application may not require a database at all. [Kirby](#kirby-intro), [Statamic](#statamic-guides) and [Grav](#grav-install-guide) as static file systems are not requiring MySQL in the basic setup at all. Or maybe you run a [Laravel](#laravel) application that only consumes a third party API or uses [Redis](#key-value-store). Please refer to the software requirements of your CMS or framework.

#### Shared plans
{#shared-plans-1}

These are the most commonly used plans. Indeed the XS and the S plan are covering most normal website scenarios already. You can store a lot of text in 256 MB.

#### Dedicated plans
{#dedicated-plans-1}

Higher plans are available for heavy users and large databases.

#### Autoscaling
{#autoscaling-1}

MySQL has an autoscaling option. When turned on the next tier will be booked, once the storage limit is reached.

---

## Storage
{#storage}

Persistent local web space for code and files.

### Booking
{#booking-1}

Web storage is a required component available in different plans. Each environment needs to have storage booked.

### Configuration
{#configuration-3}

The storage is integrated as a persistent file system. You have direct [code access](#direct-code-access) by [SSH](#ssh-access) and [SFTP](#sftp-access). The storage contains the deployed code, as well as runtime data, such as uploads and temporary files. See the [directory structure article](#directory-structure) to learn about pre-configured folders. The dashboard shows metrics about the storage size.

### Scaling
{#scaling-2}

When [autoscaling](#autoscaling) is enabled, smaller and larger plans are automatically booked, based on usage. When autoscaling is disabled, the storage is capped at the chosen plan. Once the limit is reached, the environment can not write on the file system until space is cleaned. Web storage may grow over time as your website writes more files to the disk. Keep an eye on the metrics provided in the dashboard.

### Backups
{#backups}

Web storage backups are available through the additional [backup component](#backups).

---

## Traffic
{#traffic}

Outgoing bandwidth (egress) in bit and bytes.

::CallOut{alert}
Traffic capping and autoscaling not in place during BETA.
::

### Booking
{#booking-2}

Traffic measures the data transfer that is caused by visitors browsing around your website (environment). It is booked per [environment](#the-environment). Traffic is a passive component. It just happens. The max usage is billed over the month. It's designed in tiers and as most websites have predictable traffic patterns you can expect the same costs monthly. Most websites hosted here stay on the lowest tier.

### Scaling
{#scaling-3}

When [autoscaling](#autoscaling) is enabled, smaller and larger plans are automatically booked, based on usage. When autoscaling is disabled, the traffic will capped at the chosen level. Once the limit is reached, the environment will go offline until the next billing cycle (next month) or until the plan will be upgraded.

In many cases, increased traffic usage will correlate with more website visitors. This also can have an effect on other booked resources. Check the [website performance](/3.dev/02.performance/).

### Avoid website obesity
{#avoid-website-obesity}

Keep the footprint of your website slim. Send as few bytes over the wire as possible, so that you can serve more visitors with the same amount of traffic. Reducing your website weight will also make it load faster for your visitors and improve your SEO score. See also [topic performance](/3.dev/02.performance/).

---

## Backups
{#backups-1}

Offsite code and database copies of environments.

Backups are an optional scalable component available per environment in various plans. They include file and database backups, see [working with backup files](#backup-files). The encrypted backups are stored off-site on a block storage and do not count towards your [storage](#storage) usage. Backups can be downloaded from the dashboard, [backup restore](#restore-from-backup) is offered too.

The number of backups created depends on your plan size, see [backup retention](#backup-retention). The [backup schedule](#backup-retention) will start after booking. The first daily backup will become available the next day. On the next Monday, the weekly backup spot will be filled. On the first of the month the monthly backup will be stored.

---

## Jobs
{#jobs}

Offload long-running and compute-intensive worker tasks, and schedule cron scripts to run at specific times.

Jobs is an optional [component](#components-intro) that can be booked and scaled per [environment](#the-environment) in the dashboard. The scaling increases in available RAM and number of jobs.

```raw
┌─────────┐                        ┌───────────────────┐      ┌─────────────┐
│ visitor │ ◀─ Request/response ─▶ │  environment  │ ◀──▶ │ worker/cron │
└─────────┘                        └───────────────────┘      └─────────────┘
```

Jobs run in a separate runtime container with access to the environment's file system and [database](#mysql). They are deferred from the front-end web layer to a background process that operates outside the web request/response life-cycle. This ensures that web requests are delivered swiftly, even when heavy processing is happening in the background. Environment variables and settings are kept in sync.

### Job types
{#job-types}

Worker jobs and cron jobs are widely supported by modern PHP frameworks like [Laravel](/2.guides/2.laravel) and [Symfony](#symfony-guide), as well as CMS systems like [Craft CMS](/craft-cms) and [Statamic](/statamic).

- [Workers](#workers): Non-stop running in the background, event driven triggers
- [Crons](#crons): Scheduled at certain times

### Scaling
{#scaling-4}

The available job plans differ in available memory and the number of jobs, that can be booked. Use the dashboard metrics to understand usage to determine the right plan to choose. Experiment with different plans to find the optimal scaling the project requires.

### Performance
{#performance}

Beside scaling up the component to improve performance, consider code refactoring or adjusting usage patterns.

#### Sign of bad performance
{#sign-of-bad-performance}

- Overlapping jobs not finishing in decent time
- Increased 503 or 504 errors are

---

## Key-value store
{#key-value-store}

In-memory data store based on Valkey.

The key-value store is a Redis-compatible versatile open source software to be used as in-memory data structure store, key-value database, cache or even queue message broker.

:BlockLink{title="Book key-value store" path="/environments/{{app-env-id}}/settings/components#key-value-store"}

The key-value component is based on Valkey - a high-performance, open-source key-value data store that evolved from Redis. It supports various data structures including strings, hashes, lists, sets, and sorted sets. With sub-millisecond latency and the ability to handle millions of operations per second, it's perfect for modern web applications that need fast data access.

### Use cases
{#use-cases-5}

- **Caching**: Store frequently accessed data in memory to reduce database load and improve response times.
- **Session storage**: Keep user sessions in memory for fast access across multiple servers.
- **Real-time analytics**: Track page views, user interactions, and other metrics in real-time.
- **Message queuing**: Implement pub/sub patterns for real-time features like notifications or chat.
- **Rate limiting**: Track API usage and implement throttling mechanisms.
- **Temporary data**: Store short-lived data like shopping carts or form data.

### Booking
{#booking-3}

The key-value store is implemented as an optional component on fortrabbit with various plans differing the available memory. It can be booked and scaled per [environment](#the-environment). To book and scale the key-value store, navigate to the dashboard and select your environment. Find the components section. Choose the key-value store and select the desired plan based on your memory requirements. Confirm your selection to book the key-value store.

### Scaling
{#scaling-5}

Using a key-value store can contribute to better website performance. The component itself might also be scaled to further improve performance. As there are many different usage scenarios, there are no specific scaling recommendations. For most applications, the key-value store component will not hit critical limits. Thus autoscaling will not apply. When memory runs out, least recently used (LRU) keys are automatically removed to make space for new data.

- **Start small** and scale up based on your needs
- **Monitor memory usage** in the dashboard to understand your patterns
- **Test performance** at different scales to find the sweet spot
- **Scale up gradually** if you notice memory pressure
- **Consider usage patterns** - frequent writes need more memory than read-heavy workloads

### Using the key-value store
{#using-the-key-value-store}

Valkey is supported by many PHP frameworks and CMS's out of the box, it's popular among [Laravel](#install-laravel-locally) developers. For specific integrations check out the install guides and find out how to use it with your favorite framework or CMS.

#### Session handler
{#session-handler}

If you don't use a framework, configure `session.save_handler` and `session.save_path` in your php.ini to tell phpvalkey where to store the sessions. Make sure to do it very early in your application, before accessing session data.

```php
// Read the secrects you've set in the Dashboard
$secrets = json_decode(file_get_contents($_SERVER["APP_SECRETS"]), true);
$host    = $secrets['CUSTOM']['VALKEY_HOST'];
$port    = $secrets['CUSTOM']['VALKEY_PORT'];
$auth    = $secrets['CUSTOM']['VALKEY_PASSWORD'];

// Change the session handler
ini_set('session.save_handler', 'valkey');
ini_set("session.save_path", "tcp://{$host}:{$port}?persistent=1&timeout=2&auth={$auth}");
```

#### Persistent connections
{#persistent-connections}

We recommend using persistent connections. Most adapters are configurable with a setting like `persistent: 1`.

### Best practices
{#best-practices-1}

1. **Use meaningful key naming patterns** like `user:123:profile`
2. **Set appropriate expiration times** for temporary data
3. **Monitor memory usage** regularly
4. **Use persistent connections** to reduce overhead
5. **Implement proper error handling** for connection failures
6. **Test failover scenarios** in your application

### Related resources
{#related-resources}

- [Laravel Redis documentation](https://laravel.com/docs/redis)
- [Valkey documentation](https://valkey.io/docs/)
- [environments](#the-environment)
- [Component scaling strategies](/1.platform/09.components/)

---

## Components
{#components-1}

Individually scalable and billable hosting resources for environments AKA the service you buy here.



---

## The app
{#the-app}

Apps are grouping environments together and are the main subject of collaboration.

### Creating an app
{#creating-an-app}

Start a new app with the fortrabbit dashboard. The wizard will walk you through setting up the app, including plans and pricing, collaboration, software templates, data center location and git deployment.

:BlockLink{title="Create an app" path="/new/app/"}

### Apps and environments
{#apps-and-environments}

Each app represents one website or web application. Think about an app like a Git repo. In fact you can link a Git repo to an app. Each app has one ore more [environments](#the-environment). Think about environments as git branches containing all data and runtime settings.

### Collaboration
{#collaboration-1}

The app is the main [collaboration](#collaboration-intro) object. Developers can be added and removed from apps to manage settings, environments, deploy and access code.

### Billing
{#billing}

Apps are owned by [payment methods](#the-payment-method) and managed by developers in [teams](#the-team) or directly. The app can be moved from one payment method to another.

### Deleting an app
{#deleting-an-app}

You can always delete Apps you have access on. To delete an app, visit the app in the dashboard, find and hit the "delete" button. The app will then get deleted within a couple of minutes - this includes all files and the database and is irreversible.

### Preview image and links
{#preview-image-and-links}

In some lists, apps can show a preview image and a link to be visited in the browser. The image and the link will use the [environment](#the-environment) that is most likely production and it's [main domain](#main-domain).

### App name
{#app-name}

While creating an app, a name is suggested. When connecting a Git repo, the name of the repo is used. You can change that to anything you like. Choose a name that is easy for you to identify your project. The app name is only an identifier for the dashboard. It's not used anywhere else.

There is also an option to add a description to the app name.

### Changing the Git repo of an app
{#changing-the-git-repo-of-an-app}

You can change the repo of the app with the dashboard. It's a multi step process, as all environments will need to have branches mapped.

### Changing the payment method of an app
{#changing-the-payment-method-of-an-app}

You can move an app to a different payment method you have access to.

The app will be billed on the old payment method until that day of change and from the next day on to the new payment method. See [post paid billing](#postpaid-billing) for more.

### Technical contacts
{#technical-contacts}

You can set technical contacts with the app. A technical contact is a 'web master' person that can be contacted by fortrabbit.

Please [see the technical contact article](#technical-contact) for more details.

---

## The environment
{#the-environment}

An online version of your website including a full runtime.

### Intro
{#intro-2}

- An environment is a sub object of an [app](#the-app)
- Each app needs to have at least one environment
- Environments are managed in the dashboard
- Each environment is a separated hosting setup, with [individual settings](#hosting-settings)
- Each environment has individually billed [components](#components-intro)
- Create [multi staging workflows](#staging-environments) with multiple environments

We usually use 'environment', in some contexts maybe 'app environment' since this explicitly names the fortrabbit object and can not be confused with a development environment. In the dashboard, the environment title will constructed lie so: `{app name} / {environment id}`.

### Environment maps to git branch
{#environment-maps-to-git-branch}

While the Git repo is connected with the [app](#the-app), the environment can be mapped to a git branch. [Git deployment](#deployment-intro) is optional but blends in nicely.

### Environment workflows
{#environment-workflows}

Not all apps will have multiple environments. See the [project organization article](#project-organization) on how to work with apps and environments.

### Naming an environment
{#naming-an-environment}

The default name for environments is `main`. This does not imply if the environment is used for development or production. Many apps only have one environment that will first be used during development and later for production.

When connecting a git branch to an environment, the branch name will be used. The environment name can also be changed in the dashboard.

:BlockLink{title="Change environment name {{app-name}} / {{app-env-name}}" path="/environments/{{app-env-id}}/settings/name"}

### Creating an environment
{#creating-an-environment}

While creating a new app you will also create an environment along the way. You can also create new environments for any of your apps later on.

:BlockLink{title="Create an environment" path="/new/environment"}

### Restarting an environment
{#restarting-an-environment}

The restart button will restart all services. This can sometimes be helpful when processes are hanging.

In some edge cases, like hanging PHP processes with 504 errors or 408 errors, restarting an environment can be an option. Here is how you can do this:

1. visit the environment in the dashboard
2. find and click the "Restart" button
3. wait a minute until changes are applied

This will restart the Apache service and the PHP-FPM processes. Nothing more, the data will stay safe. There will be a short downtime. Use carefully, it should not be used on a regular basis. This button is not a silver bullet to fix all server issues. If performance is a constant issue, see [performance topic](/3.dev/02.performance).

### Deleting an environment
{#deleting-an-environment}

You can delete any environment you own or administer. To delete an environment, go to the environment in the dashboard and click the "delete" button. The environment will be removed within a few minutes, including all files and databases.

#### Recovering deleted environments
{#recovering-deleted-environments}

Environment deletion is permanent and cannot be reversed. We thoroughly remove data when requested by clients or when required due to legal or payment issues. This policy protects your privacy and security. We believe you have the right to be forgotten rather than having your data held hostage (for payment). In most cases, this complete deletion is actually beneficial. For more information, see [how we handle bounced payments](#late-payments).

### Environment settings
{#environment-settings}

The environment has a lot of settings exposed in the fortrabbit dashboard. See the [hosting settings topic](#hosting-settings).

---

## The person
{#the-person}

A person is an object within the fortrabbit dashboard that represents a human being. A person can actively manage things with the fortrabbit dashboard and access code and is free of charge.

### Understand individual access
{#understand-individual-access}

It's common in classical hosting to have one account shared with a group of developers. Don't do that here. An account on fortrabbit maps to a person in real life, not an entity. Learn more about [account organization](#account-organization).

### Developers and clients
{#developers-and-clients}

There are two types of people with the fortrabbit dashboard. You can choose your type when signing up and change it later on. A client is non technical person only managing to billing. A developer is a person with tech skills managing hosting, and maybe also billing. See [account types](#account-types) for more.

### Code access
{#code-access}

Developers can add their public SSH keys for direct private code access. See the [SSH keys](#ssh-key-setup) section for more.

### Account settings
{#account-settings}

The account settings are part of the person and refer to your user registration at fortrabbit. By signing up you create a personal account. This is how you login and use the services.

### GitHub app
{#github-app}

To enable git deployment from GitHub, developers need to install the [fortrabbit GitHub app](#the-fortrabbit-github-app) with their personal GitHub account.

---

## The team
{#the-team}

A group of developers collaborating on code and billing.

### Recap
{#recap}

Your [fortrabbit account](#the-person) is your personal access. The [payment method](#the-payment-method) represents the legal entity owning apps. The team object in the dashboard represents a group of developers collaborating on apps and payment methods. Check out the [collaboration intro](#collaboration-intro) for more of the basics.

### Use cases
{#use-cases-6}

A team may represent your real life connections with other developers, like:

- A whole organization - your small agency, startup, association
- An organizational unit - a smaller group within a business, team tokio
- Any other kind of group of developers

### Creating a team
{#creating-a-team}

You can create as many teams as you want with the dashboard. Teams are free of charge.

:BlockLink{title="Create a team" path="/new/team"}

### Inviting team members
{#inviting-team-members}

You can invite more team member through the dashboard. More details [here](#team-invite).

### Access levels
{#access-levels}

There are two roles with the team: limited and unlimited. See the [team roles article](#team-roles) for more.

### Payment method access
{#payment-method-access}

[Payment methods](#the-payment-method) can be attached to teams. Teams can own apps via payment methods created by their members. This also allows billing collaboration, when teams participate on payment methods by clients.

### Deleting a team
{#deleting-a-team}

When deleting a team, payment methods and apps that are only associated through this team will be deleted along the way. There is a warning screen when deleting the team, explaining what will happen and what not. Deleting a team will not cancel your personal account.

### Leaving a team
{#leaving-a-team}

Everyone, except the last full member, can leave a team. In that case the team will stay, but you will loose access to it and it's objects. When you cancel your account and you are part of a team with other members left, you will leave the team.

### Working with multiple teams
{#working-with-multiple-teams}

Just like in real life, you can create or join any number of teams with your account. So one account can be part of multiple teams in different roles.

### One person in different teams
{#one-person-in-different-teams}

If you have multiple teams and you want to collaborate with same person on all or a subset of them: Just invite them to each team. The same person then will have access to all teams while logged in with their account.

### When developers leave
{#when-developers-leave}

The developer who leaves a team will loose the ability to see and edit the apps in the dashboard and also will loose all personal code access. There are two directions of leaving a team:

#### Active: A developer leaves a team
{#active-a-developer-leaves-a-team}

You might want to leave the team when the project you have collaborated on has ended or you are actually leaving the team in real life as well.

1. Dashboard > team > Team overview
2. Click the "Leave" button

You can not leave a team when you are the last member remaining. A team must have at least one member.

#### Passive: Team access is revoked
{#passive-team-access-is-revoked}

Let's say a project phase has ended, so that developer does not need have access any more.

##### How to revoke developer access
{#how-to-revoke-developer-access}

1. Dashboard > teams > team overview > members
2. Click the action button to edit access
3. This will bring up a form in which you can edit and revoke access

---

## The invoice object
{#the-invoice-object}

The invoice object is a recording of booked component plans across environments per month and payment method.

### Invoice details
{#invoice-details}

Each [payment method](#the-payment-method) with attached apps will get an invoice for each service period (monthly) - after the service period ends. The invoice contains all the apps, their environments and booked components.

- Invoice number - An individual number.
- Invoice date - The day, the invoice was printed.
- Service period - The backdating month.
- Invoice address - Postal address from payment method.
- Invoice email - Email address from payment method.
- VAT - See [VAT article](#vat-rules).

### States
{#states}

Invoices have a lifetime, going through various phases:

#### Draft
{#draft}

During an ongoing service period, an invoice draft is kept and updated daily and with each booking. The invoice draft helps customers to keep track of current costs. During the DRAFT state the invoice will have a column to display current costs so far.

#### Paid
{#paid}

At the enf of the service period, the invoice will be finalized, send to customers. The payment credentials of the payment method will be used to automatically pay the invoice. When successful, the invoice is paid.

#### Bounced
{#bounced}

When the payment credentials on file fail, the invoice will be marked as bounced. If that will not resolved after various automatic retries, service cancellation is next. See [late payments](#late-payments).

### Invoice item rows
{#invoice-item-rows}

Each invoice contains a number of rows. They are grouped by environment as each has a set of booked components. Each invoice row contains the booked component and it's plan and how many days it is billed for by days. The table gives you an idea how components and plans appear on an invoice.

| Component plan | Days billed | Daily price |  Month |
| -------------- | ----------: | ----------: | -----: |
| PHP XS         |          10 |       $0.10 | $15.00 |
| PHP S          |          20 |       $0.16 | $15.00 |
| Traffic S      |          30 |       $0.03 |  $1.00 |

In this example PHP XS was booked for a couple of days and then replaced by PHP S. See the [postpaid billing article](#postpaid-billing) for more on that.

The printed invoice document may look a bit different.

---

## The payment method
{#the-payment-method}

A payment method owns apps, receives invoices and is managed by people.

### Overview
{#overview}

- A payment method has: payment type, invoice address, VAT settings …
- Each app - except [during trial](#free-trial-details) - is owned by a payment method
- Payment methods can own multiple [apps](#the-app)
- Payment methods are managed by people directly or in [teams](#the-team)
- Each team or person can have access on multiple payment methods
- Each payment method has its own [invoice](#the-invoice-object) archive
- Payment methods are free of charge, apps they own cost something
- People are connected to payment methods by a [billing connection](#billing-connection)

### Creating a payment method
{#creating-a-payment-method}

When creating your first paid app up or upgrading a trial app, you will create a payment method on the fly and link that app to it. You can also create a payment method from scratch to be used later on.

:BlockLink{ title="Create a new payment method" path="/new/payment-method" }

### Multiple payment methods
{#multiple-payment-methods}

You may need one app to be paid by one credit card and another app to be paid by another credit card. The payment method is not a part of your account but an individual object. You can create multiple payment methods and assign apps to them.

### Shared payment methods
{#shared-payment-methods}

You may be collaborating with other, in a team or in a client relation. Payment methods can also be shared. You can [invite someone to collaborate or to take over a payment method](#invite-someone-for-billing).

### Changing the invoice address
{#changing-the-invoice-address}

Your invoices contain the street address of your payment method. You will be asked for that while setting up a payment method. You can change this invoice address for future invoices at any time in the dashboard.

### Changing payment credentials
{#changing-payment-credentials}

You have a new credit card or the old one is about to expire? You can change the payment credentials of a payment credentials of the payment method in the dashboard. Changing the payment credentials will affect future payments and will also be used to balance possible open invoices. In order to change the payment method you will need to have a fortrabbit account with access to the payment method.

### Adding a VAT IN
{#adding-a-vat-in}

It is recommended to add your VAT IN to your payment method when your organization is registered in the European Union. This can save you (and us) upfront value added taxes. Please see our [VAT topic](#vat-rules).

We need to validate the VAT IN. So the number you enter needs to match the correct format. Please mind that your VAT IN is not the tax number. The correct number should start with your country code. Entering the VAT IN will change how VAT will be charged for future invoices, entering the VAT IN can not affect past invoices.

### Changing the payment method of an app
{#changing-the-payment-method-of-an-app-1}

In case you want an app to be billed from another credit card or bank account but still want to keep the team of the app the same. Either replace the payment credentials or create a new payment method.

### Deleting a payment method
{#deleting-a-payment-method}

Deleting a payment method is similar to a service cancellation, since all the apps owned will be deleted as well and the invoice archive will be removed.

### Troubleshooting setup issues
{#troubleshooting-setup-issues}

From time to time clients report issues with setting up new payment methods. Here are some common issues:

- Debit cards might not be accepted, use a full blown credit card please
- Sadly credit cards from certain countries like Nigeria seem to have less acceptance
- We are debiting the card with a test transaction with a small amount - that's not a payment, you'll get it back right after
- EU clients might need to solve strong authentication (redirect to bank website)
- US and other countries might need to authorize the test debit, in some cases that means calling up the bank

We can do little about this. We pass your data directly to the payment gateway. Thanks for your understanding.

---

## The domain
{#the-domain}

Each fortrabbit environment has a test domain. Additionally you can route external domains.

### External domain
{#external-domain}

An "external domain" is a domain registered with a third party domain name registrar. fortrabbit does not provide domain registration services. Proceed here:

- [Domain provider integration](#domain-registration-providers) - combine domain provider with fortrabbit
- [External domains intro](#external-domains) - options and limits
- [Point an external domain](#point-a-domain-to-fortrabbit) - step by step instructions

### Target settings
{#target-settings}

For most domains the target can be changed. Target settings can not be changed for:

- apex domains: will always forward to their www counterpart
- main domains: define a different main domain first

#### Environment setting
{#environment-setting}

Change the environment of an external domain with this setting. External domains can be moved across environments without DNS changes. This can be useful when switching the production domain to a new environment.

#### Root path setting
{#root-path-setting}

A root path is a folder in the [file system](#directory-structure) of the [environment](#the-environment) where a domain will end. The root path is saved with the environment for all it's domains. That means, no interface is offered to configure individual root paths per domain. You can however configure custom routing of domains in your code and config, either by `.htaccess` rules or by some routing options with your software.

#### Domain forwarding
{#domain-forwarding}

The dashboard allows you to forward domains with the same environment. Usually you will want to forward all domains to your main domain. See the [www domain forwarding article](#domain-forwarding).

---

## The deployment object
{#the-deployment-object}

After your git push, a deployment is happening, updating the web space with code changes from the Git repo. The deployment object makes that transparent with the dashboard.

The deployment object displays metadata, including deployment logs, the issuer, the environment, and a link to the deployed commit.

With the dashboard you can see a list of deployments that can be filtered down. Each list item links to an individual deployment which provides more insights and links. Older deployment events might be partially or fully pruned.

Deployments are recorded only for Git deployments using the [official fortrabbit GitHub app](#the-fortrabbit-github-app). Deployments via GitHub Actions are not recorded.

SSH/SFTP sessions are not considered deployments either. With the deployment settings of an environment you can control the rules for deployment.

Please proceed to the [deployment intro](#deployment-intro) to learn more about the steps and what happens during a deployment.

---

## The SSH key object
{#the-ssh-key-object}

Remember, on fortrabbit an account represents a [person](#the-person). SSH key authentication is used to securely identify you for your personal [code access](#direct-code-access). SSH keys are an object within the fortrabbit dashboard. [Personal SSH keys](#personal-keys) can be managed with your account settings, deploy keys with each environment.

Don't have local SSH keys already or don't know what that is? See the [SSH key setup and intro](#ssh-key-setup).

### Adding SSH keys to fortrabbit
{#adding-ssh-keys-to-fortrabbit}

:BlockLink{title="Add a new SSH key" path="/new/ssh-key"}

The public part of the key must be imported in the fortrabbit dashboard. Paste the PUBLIC part of the key and not the private part. The value to paste into the text field can be read into the clipboard.

```shell
## macOS
{#macos}
$ pbcopy < ~/.ssh/id_ed25519.pub

## Linux
{#linux}
$ xclip -i < ~/.ssh/id_ed25519.pub

## Windows
{#windows}
## Open the `id_ed25519.pub` file, select all, then copy.
{#open-the-id-ed25519-pub-file-select-all-then-copy}
```

### Personal keys
{#personal-keys}

:BlockLink{title="Manage your SSH keys" path="/you/ssh-keys"}

In most cases you want to add SSH keys to your personal developer account at fortrabbit to directly login to the environment and opening an SSH tunnel. Personal SSH keys will be automatically added to all the environments you have a [developer connection](#developer-connection) to.

Already using GitHub and our [deployment flows](#deployment-intro)? The fortrabbit dashboard may directly import public keys associated with your GitHub account so you don't need to setup additional keys for this.

### Deploy keys
{#deploy-keys}

In certain scenarios, you may want to grant a non-human service access to an environment. Use deploy keys for that. The deploy keys are managed via the dashboard with the environments. Adding and removing such keys follows the same concepts as described above. Use deploy keys to integrate with [Git hosting services](#git-providers) or deploy services.

---

## Dashboard objects
{#dashboard-objects}

Terminology, concepts, explanations.



---

## Pricing structure
{#pricing-structure}

Apps are grouping environments. Environments consist of components. Components are available in plans.

The example diagram below illustrates the billable structure of a [payment method](#the-payment-method) with two [apps](#the-app), one with one [environment](#the-environment), the other with two environments. The environments have different [plans](#plans) of [components](#components-intro) booked.

```raw
- App 1 (takas)
  - Environment (production)
    - Components
      - PHP S
      - Web storage XS
      - Traffic S
      - Database OFF
      - …
- App 2 (project-earth)
  - Environment (production)
    - Components
      - PHP M
      - Web storage M
      - Database L
  - Environment (staging)
    - Components
      - …
```

Most component plans are available as shared resources. Some higher plans of components are available as 'dedicated'.

---

## Postpaid billing
{#postpaid-billing}

First use, then pay: Service usage is measured throughout the billing period, with costs calculated and invoiced at completion.

### How prepaid works
{#how-prepaid-works}

In order to understand postpaid, it might be beneficial to describe the dominating model first: Most hosting providers offer prepaid pricing. That means you pay upfront for what you plan to use over the service period. Many hosting providers are requiring yearly subscriptions (with monthly payments). This in favor for the hosting provider, as it locks in the customers and guarantees long running contracts with fixed revenue.

### How postpaid works
{#how-postpaid-works}

With a postpaid model, also called in arrears, on the other side. Customers make use of the service and pay later after usage for the [monthly service period](#schedule).

- You don't pay on booking, only after the first month of usage
- After deletion, final charges appear on the next invoice

### Postpaid benefits
{#postpaid-benefits}

Postpaid enables [prorated billing with daily usage aggregation](#daily-aggregation). This again makes it easy to experiment with the hosting service as you'd aspect for agile workflows.

### No yearly payments
{#no-yearly-payments}

Postpaid usage is not compatible with yearly payment. As that would require to be able look into future usage or to only write yearly in arrears.

---

## Daily aggregation
{#daily-aggregation}

This is prorated billing where each day of service is billed at 1/30th of the monthly rate.

If you book a plan on the 16th day or create an app or environment, the invoice items will be calculated for 15 active usage days. The dollar signs indicate days that would be included in the invoice:

```plain
       April
Mo Tu We Th Fr Sa Su
     -  -  -  -  -
 -  -  -  -  -  -  -
 -  -  -  $  $  $  $
 $  $  $  $  $  $  $
 $  $  $  $
```

The above example gives you a clue that we are charging after usage, see [proration](#postpaid-billing). First you use the service, at the end of the service period, actual costs are calculated together and invoiced.

### Examples
{#examples-3}

```yml
## Adding a component mid-month:
{#adding-a-component-mid-month}
Monthly rate: €30
Start date: 15th
Days used: 16
Charge: €16 (€30 ÷ 30 × 16)

## Upgrading a plan:
{#upgrading-a-plan}
Old plan: €30/month (€1/day)
New plan: €60/month (€2/day)
Charge: €19 (19 days × €1) + €22 (11 days × €2)
```

### Benefits
{#benefits}

The daily cost usage aggregation promotes testing, tinkering and experimenting without much obligations and having to pay a fortune.

- Create a environment to test a feature branch for a couple of days
- Test best settings for scaling the production environment
- Scale up hosting resources for temporary events such as media coverage

### The largest plan counts
{#the-largest-plan-counts}

Let's say you want to find the best matching PHP plan size. For that you scale up and down the PHP plan while monitoring PHP response time and reloading the website to see effects in performance. On that day, PHP XS, PHP SM and PHP MD may have been in use. The invoice will show PHP MD for that day.

### Monthly prices for reference
{#monthly-prices-for-reference}

In our experience website projects most often run over months and even years. That's why monthly prices are most appropriate to show and reason about.

### 30 days monthly base
{#30-days-monthly-base}

Some months have 31 days, while February has either 28 or 29 days. To ensure consistency in monthly invoices, all months are normalized to 30 days. This means that when a component is booked for an entire month, it is always billed for 30 days.

The daily price is calculated as 1/30th of the monthly price. If a component is used for less than a full month, the cost is determined by multiplying the daily price (1/30th of the monthly price) by the number of days the component was active.

### No hourly prices
{#no-hourly-prices}

Some other hosting vendors offer hourly prices. We believe, that this is confusing and does not match the reality of most projects. To get an idea for the daily price you only need to divide the monthly price by 30. In most cases this about cents, costs one need not to worry much about anyways.

---

## Billing schedule
{#billing-schedule}

Within the first few days of every new month, you will get the invoice for the service period of the last month. After receiving the invoice, the payments are due and are charged automatically.

| Date            | Action                                  |
| --------------- | --------------------------------------- |
| End of month    | Invoice creation for monthly usage      |
| 1st             | Invoice distribution for previous month |
| 1st             | Credit card payment processing          |
| 1st             | SEPA direct debit execution             |
| Until month end | Review and retry of bounced invoices\*  |

\* See [late payments](#late-payments) for details

---

## Payment types
{#payment-types}

The fortrabbit service operates automatic monthly payments. This is how you can pay and under which conditions.

### Credit card
{#credit-card}

Visa, MasterCart and Amex are the supported credit cards. Many debit cards are not supported, some are, try it out. US clients might need to ask their bank to allow payments from us. When setting up the payment option we'll do a test charge. That's not a real charge. You may get a notification about this.

### SEPA direct debit (planned)
{#sepa-direct-debit-planned}

SEPA direct debit is accessible to clients in the European Union.

### Data sharing
{#data-sharing}

Billing data entered will directly be send to our payment provider.

---

## Autoscaling
{#autoscaling-2}

Scale components automatically when usage demands more resources.

::CallOut{alert}
This is not yet implemented.
::

Autoscaling is an option that can be toggled per environment with the component booking.

| Autoscaling | Fixed price | Availability   |
|-------------|-------------|----------------|
| **On**      | ❌ No        | Stays online   |
| **Off**     | ✅ Yes       | May go offline |

Autoscaling is available applies to the following components in the following ways:

| Component       | Autoscaling | Metric    |
| --------------- | ----------- | --------- |
| MySQL           | ✅ Yes      | Storage   |
| Traffic         | ✅ Yes      | Bandwidth |
| Web storage     | ✅ Yes      | Space     |
| PHP             | ❌ No       | -         |
| Key-value store | ❌ No       | -         |
| Jobs            | ❌ No       | -         |
| Backups         | ❌ No       | -         |

Components are grouped in tiers. Even with autoscaling on, price fluctuation is not likely.

### Details
{#details}

- Selected plan is the minimum when autoscaling is on
- For traffic, the largest plan reached applies for the month
- Monitor MySQL memory alongside database storage usage

---

## Plans
{#plans}

A plan defines the scaling of a booked component. Each plan has a price and a set of included resources.

### Plan resources
{#plan-resources}

Each plan includes specific hardware resources and performance limits. Detailed specifications are available with the pricing page. While most [components](#components-intro) represent single scalable resources (like traffic or storage), some plans combine multiple resources. For example, MySQL plans scale both storage capacity and computing power together.

### Tiers
{#tiers}

Plans are grouped in carefully designed buckets. That makes the costs predictable and unlikely to fluctuate often over time. In fact most standard websites and applications will work with small plans just fine.

### Changing plans
{#changing-plans}

Plans can be upgraded or downgraded at any time with immediate effect. Changes are prorated with daily aggregation. Common reasons to change plans include:

- Handling increased traffic
- Optimizing costs during quiet periods
- Preparing for marketing campaigns
- Scaling for seasonal peaks

:BlockLink{title="Change plans for {{app-env-name}}" path="/environments/{{app-env-id}}/components"}

### Finding the right plan
{#finding-the-right-plan}

Start small and scale up as needed. Each application has unique requirements that depend on:

- Traffic patterns
- Application architecture
- Caching strategy
- Database usage
- Storage needs

The monitoring tools help you track resource usage and determine when to scale. :ContactUs{text="Contact us"} if in doubt.

### Regional pricing
{#regional-pricing}

Plan prices vary by data center location due to local infrastructure costs. Consider this when choosing a region.

---

## Currency rules
{#currency-rules}

fortrabbit services are offered in (€) EUR and ($) USD. Different prices may apply based on the selected currency. It's also possible that prices differ by data center location.

### Ruleset
{#ruleset}

- All payment methods within the EU are required to pay in EUR.
- [Payment methods](#the-payment-method) from other countries can pay in USD or EUR.

### Changing the currency
{#changing-the-currency}

It is not possible to change the currency of a payment method later on. However, you can create a new payment method with a different currency and then move apps there.

---

## VAT rules
{#vat-rules}

fortrabbit is mainly a B2B service, clients are entrepreneurs or other businesses. It can also be used for B2C, clients are end consumers.

### Fiscal implications
{#fiscal-implications}

- Prices are shown as net prices, without Value Added Tax (VAT)
- No VAT is charged for customers outside EU
- No VAT is charged for registered business in EU (+ GB) with valid VATIN
- VAT is charged for VAT-registered business in Germany

### VATIN for EU clients
{#vatin-for-eu-clients}

It's recommended to enter your VATIN (Value Added Tax Identification Number), sometimes referenced as VAT TAX ID or similar. This way you save upfront costs for VAT — reverse charge makes this possible.

### EU VAT exemption
{#eu-vat-exemption}

We may not charge VAT, if article 151(1)(a) VAT Directive applies, e.g. for international bodies, embassies or other EU organizations with a valid VAT exemption certificate. Please get in touch if VAT exemption applies to your organization.

---

## Late payments
{#late-payments}

Sometimes payments don't go through. That happens. We understand it. Don't panic, but take care. This article guides you through the steps.

### Why payments bounce
{#why-payments-bounce}

There are various reasons why payments bounce:

- Insufficient funds - we will try to debit again after a few days
- Expired credit cards - [Update your payment method](#changing-payment-credentials)
- Something else - [Update your payment method](#changing-payment-credentials)

Please contact us if you are aware about open invoices with us and or if you have questions about an invoice. In any case, we will inform you by by e-mail about failed payments.

### Automatic retries
{#automatic-retries}

Over the course of the month we will retry to previously failed payments. This helps to resolve half on initial bounces.

### Service cancellation
{#service-cancellation}

At some point, after several unsuccessful attempts to charge the payment credentials on file, apps will be deleted. **Deleted apps can not be recovered.** Read why we do this in a [story from our blog](https://blog.fortrabbit.com/bounced-payment). Deleting apps for bounced payments is carefully considered with human review on a per customer basis.

### App deletion policy
{#app-deletion-policy}

If there are 3 consecutive unpaid invoices with no response, apps will be deleted.

- **New clients:** If the first or second invoice bounces and there is no response to our emails, apps will be deleted.
- **Clients with fewer than 6 invoices:** If an account has fewer than 6 invoices, or if the credit card processor flags potential fraud or the account appears suspicious, apps may be deleted.
- **Long-term clients** with more than 6 paid invoices: If there are at least 2 consecutive bounced invoices or a total of 4 unpaid invoices, we will attempt personal contact in addition to automated emails. If there is no response, apps may be deleted.
- **High-value invoices**: For clients with invoices exceeding €1k MRR, different rules may apply.

### Paying open invoices
{#paying-open-invoices}

Open invoices can be found in the Dashboard. Login to our Dashboard &gt; follow the instructions in the "open invoices" warning. Credit card payments are done immediately. SEPA direct payments are delayed. If your credit card has insufficient funds at the time of charging, we may try to charge it again during the month.

### Refund policy
{#refund-policy}

**We do not offer refunds** due to the complexities involved with our custom billing system and German accounting regulations. Issuing refunds would require generating negative invoices and additional manual bookkeeping steps.

If you believe there is an error in your invoice, please contact our support team. We may offer credits towards future invoices as a gesture of goodwill.

Please note that all booked apps and environments utilize hardware resources regardless of visitor traffic or usage patterns.

### Additional fees for bounced payments
{#additional-fees-for-bounced-payments}

Please note that our bank collects fees for failed charges or insufficient funds. We may pass those fees to you. Currently we usually don't.

---

## How to download previous invoices
{#how-to-download-previous-invoices}

Options to download previous invoices from fortrabbit.

### A - See your mailbox
{#a-see-your-mailbox}

Search your e-mail inbox for "fortrabbit invoice". Each invoice e-mail contains a secret link to the invoice. From there you can print or download the invoice.

### B - Download from the dashboard
{#b-download-from-the-dashboard}

Login to the fortrabbit dashboard. Navigate to the payment method and see the invoice archive. The payment method needs to be active and you need to have access on that payment method to do this.

Invoices are shown as HTML. Depending on support in your browser, a PDF can be generated using the "Print to File" feature from your Browser/OS.

---

## Invoice threshold
{#invoice-threshold}

Invoices for partial usage may be below a minimum required invoice amount.

The threshold value may change over time and may be differ depending on currency and payment type. Consider something like 50 cent. We use Stripe as our invoicing provider and their threshold functionality. Invoices below threshold will be nullified automatically, so nothing needs to be paid for that service period. The amount will be added to the payment methods balance and applied to the next invoice.

### Example
{#example}

```raw
€0.30 Invoice March -> Threshold applied
€4.50 Invoice April - Apply threshold from balance
€4.80 Amount due in April
```

---

## Billing
{#billing-1}

All stuff related to payments, invoices, VAT and what not.



---

## External domains
{#external-domains-1}

An "external domain" is a domain registered with a third-party domain name registrar. Connect an external domain with an environment to have it receive traffic for that address.

### Configure the external domain
{#configure-the-external-domain}

Please see [external domain configuration](#point-a-domain-to-fortrabbit).

### TLS certificates
{#tls-certificates}

Please see the [HTTPS article](#https) for information on secured connections.

### Choosing a domain provider
{#choosing-a-domain-provider}

Please see our [domain provider article](#domain-registration-providers) what you may want to look for when choosing a domain provider to be used in combination with fortrabbit.

### Wildcard domains
{#wildcard-domains}

Wildcard domains are currently not supported at fortrabbit. Please file a support ticket to describe your use case.

### Configuring a domain for e-mail
{#configuring-a-domain-for-e-mail}

To receive and send e-mails from your domain you will configure the MX record of your domain with your [domain provider](#domain-registration-providers). Please see your e-mail hosting provider for instructions, here is [more on e-mail hosting from us](#email-account-providers).

### Troubleshooting
{#troubleshooting-2}

See our [DNS troubleshooting guide](#dns-and-domain-troubleshooting) if it is stuck.

---

## Point a domain to fortrabbit
{#point-a-domain-to-fortrabbit}

How to add an external domain and configure the domain provider to receive traffic on an environment hosted on fortrabbit.

### 1. Tell fortrabbit about your domain
{#1-tell-fortrabbit-about-your-domain}

1. Click New > "Add a new domain" and follow the steps
2. Choose a domain name and an environment
3. Keep the overview tab open to copy the desired DNS settings

:BlockLink{title="Add a new domain" path="/new/domain"}

### 2. Point the domain to fortrabbit
{#2-point-the-domain-to-fortrabbit}

Use the provided DNS information from the fortrabbit dashboard to change the domain routing with your domain provider.

- For sub domains like www, use the CNAME record
- Apex domains get an A record for [forwarding](#domain-forwarding)
- Leave any other records untouched, especially MX
- Remove any AAAA records (IPV6)

Save the settings with your domain provider and wait a while. The while depends on the TTL settings of the DNS records, or usually up to 6h.

---

## Domain forwarding
{#domain-forwarding-1}

The fortrabbit domain forwarding service redirects incoming requests to another domain. It is mostly used to route an apex domain to 'www.'.

### Features
{#features}

- It uses '301 Moved Permanently' headers
- It works for `https`
- It also works for deep links like `https://your-domain.com/page`
- It works for `www.` and other subdomains

### General usage
{#general-usage}

[Domains](#the-domain) registered with the dashboard have a target setting. You can choose to route the domain directly to the root path of an environment or to be forwarded.

#### Limitations
{#limitations-2}

- The target of a forwarded domain needs to be routed directly
- It is not possible to forward a domain to a forwarded domain
- Deleting a domain will delete domains forwarded to this domain as well

### Forwarded apex domains
{#forwarded-apex-domains}

When adding a www domain to the dashboard you will be provided a CNAME record (host name) for the www prefix and another domain for the apex domain. Here the routing is via A record (IP address). The IP address is the forwarding service. You will add both records with your [domain provider](#domain-registration-providers).

#### Recommendations
{#recommendations}

- Use `www.domain.tld` instead of just `domain.tld` in all links
- Send your external traffic (e.g. advertisement clicks) to the `www.` domain
- Configure your uptime checks with a URL to the the `www.` domain

### Alternatives
{#alternatives-3}

You don't have to use the fortrabbit free domain forwarding service, other options:

- [ALIAS / ANAME routing](#aname-alias-records)
- Forwarding, using your domain provider
- Use `.htaccess` for more fine tuned control, see [htaccess redirects](#redirects)

---

## HTTPS
{#https}

Zero-config TLS certificates for all domains at no additional costs are provided. Read on if you want to learn about advanced options.

### HTTPS on fortrabbit
{#https-on-fortrabbit}

All external domains correctly routed will receive a TLS certificate, no configuration or extra setup required. The certs will also be renewed automatically.

### HTTPS options
{#https-options}

The following practical tips on how to deal with HTTPS are applying to all TLS options on fortrabbit:

#### Redirect all requests to HTTPS
{#redirect-all-requests-to-https}

It is recommended to forward all requests to the secure line, so no more "http://", only "http**s**://". You can do that with `.htaccess`, see [htaccess redirects](#redirects).

#### Secure your domain with a CAA record
{#secure-your-domain-with-a-caa-record}

A Certification Authority Authorization (CAA) is a DNS record to specify which certificate authorities (CAs) are allowed to issue certificates for a domain. It's an extra security layer, so that now one else can intercept any certificates by wrong authorities. There is no integration here on fortrabbit needed. See if your DNS / domain provider supports CAA entries, set the according identifying domain name. When you are using our free Let's Encrypt certs, see [this article](https://letsencrypt.org/docs/caa) on how to set it up. Mind that already existing CAA entries can also become a problem when trying to issue new certificates.

### About HTTPS, TLS & SSL
{#about-https-tls-ssl}

`HTTPS` is **H**yper **T**ext **T**ransfer **P**rotocol over Transport Layer **S**ecurity. It is used to secure the data transport between a client (browser) and a server. HTTPS is based on **TLS** (Transport Layer Security), which is the successor to the still better known **SSL** (Secure Sockets Layer). HTTPS is considered a standard must have for each website. Browsers show a lock in the address bar if the connection is over HTTPS.

### Troubleshooting HTTPS
{#troubleshooting-https}

[See the HTTPS troubleshooting guide](#https-troubleshooting) for some tips you can debug a secure connection on your own.

---

## Apex domains
{#apex-domains}

Apex domains, also called 'naked domain', 'root domain' or even 'bare domain', have no prefix and look like 'fortrabbit.com'.

### Apex routing at fortrabbit
{#apex-routing-at-fortrabbit}

Direct routing of apex domains to environments is not supported at fortrabbit. You can ese a www domain, the [www forwarding service](#domain-forwarding) will redirect all requests.

### No CNAME for apex domains
{#no-cname-for-apex-domains}

Although not impossible, apex domains should really not be routed using a CNAME record. Use an A-Record instead. This is because of [DNS specs](https://www.ietf.org/rfc/rfc1035.txt). Receiving e-mails like `info@fortrabbit.com` would not be possible when DNS entries have CNAME record at the same time. Modern DNS providers support ANAME/ALIAS records for this.

### No direct A-record routing here
{#no-direct-a-record-routing-here}

A host name is more flexible than an IP. Any domain routed to an IP is bound to that IP. This doesn't give us the flexibility to move environments around, in case of scaling or incidents, for example with a DDoS attack.

### Our opinion on apex domains
{#our-opinion-on-apex-domains}

Some think that the minimal look of an apex domain is aesthetically more pleasing than their subdomain counterparts. But as described above, apex domains don't play well with flexible host name routing. Big players like Google use a `www.` subdomain without you noticing, and most bigger sites do the same. Safari and Chrome don't show the `www.` prefix in the address bar anymore. Firefox greys out the protocol of this trivial domain. The `www.` prefix is so common, you hardly recognize it. Some people think, moving from bare to `www.` will impact SEO negatively. This should not be the case if done properly, as long as the apex domain will forward all requests.

---

## DNS and domain troubleshooting
{#dns-and-domain-troubleshooting}

Solving common DNS problems when connecting an external domain to fortrabbit.

### Common issues
{#common-issues}

Here are the most common reasons why domain routing is not working. Start with this list first.

#### Wrong DNS settings
{#wrong-dns-settings}

Most domain issues are related to wrong DNS settings. Carefully check if your actual target DNS settings match the desired DNS settings. It's possible that you have additional contradicting rules.

#### Time delays
{#time-delays}

Many domain providers default to a long TTL (Time To Live). The TTL value is in seconds. Often it's 3600 meaning one hour. The TTL caching itself is actually a good thing as it helps to reduce round trips. Most domain providers let you set down the TTL, which is very useful to do before moving domains. See below on how to query the current DNS settings.

#### Internal routing issues
{#internal-routing-issues}

When you see a 404 - file not found error after the domain is correctly via DNS and ending up at fortrabbit, then most likely your code configuration is not setup to receive traffic for the domain. This can be a wrong root path setting, or a siteUrl setting that is wrong. Also check our [404 tips](#troubleshoot-404-errors).

#### No DNS settings
{#no-dns-settings}

Depending on your browser you might see a _DNS_PROBE_FINISHED_NXDOMAIN_ or _This site can't be reached_ or _This webpage is not available_ error. In such cases, it is likely that the domain is not registered or there are no DNS settings for that domain. You need to fix that with your domain provider.

#### Certificate errors
{#certificate-errors}

Once a domain is correctly routed, the [TLS certificate](#https) needs to be installed. This takes some additional time in which requests to the https version of the website will display a certificate warning in the browser. This is actually not a DNS issue, see the [HTTPS troubleshooting guide](#https-troubleshooting).

#### No domain configured with fortrabbit
{#no-domain-configured-with-fortrabbit}

Sometimes people forget to register and configure the domain with fortrabbit. Check if the domain is correctly setup with fortrabbit as well.

### Debugging DNS issues
{#debugging-dns-issues}

The following tips can help you to verify DNS settings for your domain. This is useful especially with time delays and wrong DNS settings.

#### Use the dashboard as a guidance
{#use-the-dashboard-as-a-guidance}

When visiting your external domain within the dashboard, you'll see the desired and the currently active DNS values for the domain. Those two settings should match.

#### Use dig to verify current DNS values
{#use-dig-to-verify-current-dns-values}

You can verify DNS settings with the [dig command](#dig).

#### Use a DNS checker website
{#use-a-dns-checker-website}

You can also use DNS test websites to rule out caching, those can query your DNS entries from different locations at once.

---

## DNS and domains
{#dns-and-domains}



---

## Collaboration intro
{#collaboration-intro}

Collaborate on infrastructure just like you collaborate on code. Map real world business requirements related to your hosting. Work with other developers, billing managers and clients.

### Collaboration starts with you
{#collaboration-starts-with-you}

Sign up to fortrabbit as an individual person, not a company or entity. See [account organization](#account-organization) and the [person object](#the-person) for more details on why and how to use your personal account.

### Build for trust
{#build-for-trust}

The fortrabbit collaboration features are build to enable productive co-creation. The purpose is to connect people working together as developers and their business owners within the hosting platform. It's not about fine grained access control.

The collaboration features are a powerful sword aimed for professional usage. It's anticipated that you have trust and policies in place within the context of your real word relations and teams to avoid misusage and damage.

### Many to many relations
{#many-to-many-relations}

The fortrabbit collaboration features are designed without a lot of hierarchy. This enables to map many types of real world scenarios. You can have multiple apps, payment methods and teams connected to your personal account. Apps can be connected to multiple teams and solo developers. Payment methods also can be connected to multiple individuals and teams.

### Co-ownership
{#co-ownership}

Apps are paid and thus owned by [payment methods](#the-payment-method), not accounts. People with access on the payment method have billing control. Payment methods can be shared with developers, clients and teams. See the [billing collaboration article](#billing-collaboration) for more.

### Use cases
{#use-cases-7}

- Solo developers working for clients directly
- Solo developers working for organizations
- Smaller organizations with a fixed team
- Bigger organizations with multiple teams

### Example workflows
{#example-workflows}

- Invite clients and non-devs to take over billing
- Create teams to share apps with other developers
- Pass over app access from developer to developer

### Two levels of collaboration
{#two-levels-of-collaboration}

There are two types of collaboration on the fortrabbit hosting platform:

- [Developer collaboration](#developer-collaboration) - sharing technical aspects
- [Billing collaboration](#billing-collaboration) - sharing billing access

This enables to share developer access to an app without sharing billing access at the same time. It's also the foundation to work with non-technical business owners (clients).

With teams it's practical that the unlimited members have combined control on developer access and billing access.

---

## Team invite
{#team-invite}

Share access to a team with fellow developers by inviting them.

### Use cases
{#use-cases-8}

A [team](#the-team) is group of developers working together on multiple apps. Use this flow to invite a developer to collaborate on multiple (current and future) apps and take part in the team as well. Invite people you know well and trust.

### How it works
{#how-it-works-3}

This describes the team invite flow from both sides:

#### On the inviter side
{#on-the-inviter-side}

1. You need to have unlimited access on a [team](#the-team) already
2. In the dashboard, find the link.
3. Select the team you like to invite someone to
4. Select the role of the invited developer - see [team roles](#team-roles)
5. Select the apps they should have access on - see [developer connection](#developer-connection)
6. Enter the email address of your colleague

:BlockLink{title="invite to team" path="/new/invite/team"}

#### On the invited side
{#on-the-invited-side}

1. They receive an email with an invite link
2. They login to their fortrabbit account or create a new account for this
3. Then they need to accept the invite

#### Consequences
{#consequences}

- They will become part of your team with role you selected for them
- Their [team role](#team-roles) defines their access level

### Alternative app invite
{#alternative-app-invite}

You can also invite developers or teams to specific apps, see [the app invite flow](#invite-to-app).

---

## Invite to app
{#invite-to-app}

Share access to a single app. Use this flow to invite an external developer or team of developers to a specific app.

### Use cases
{#use-cases-9}

The app invite is a flow to share app access between developers who don't know each other so well or don't have to collaborate on a lot of apps.

- A solo developer invites a colleague
- A loosely connected group of developers collaborating per project
- A team works together with another team and shares one app
- A team invites a freelancer to a specific app but not to the whole team
- A client invites a developer

### How it works
{#how-it-works-4}

This describes the app invite flow from both sides:

#### On the inviter side
{#on-the-inviter-side-1}

1. You need to have an [app](#the-app) already
2. In the dashboard, find the link to invite to an app
3. Select the app you like to invite someone to
4. Enter the email address of your colleague

:BlockLink{title="invite to app" path="/new/invite/app"}

#### On the invited side
{#on-the-invited-side-1}

1. Receive an email with an invite link
2. Login to fortrabbit or create a new account for this
3. Accept the invite to gain a [developer connection](#developer-connection)

#### Consequences
{#consequences-1}

- Invited developers have a [developer connection](#developer-connection)
- They have the same access on the app as yourself
- They can change all settings, deploy code and delete the app
- They can also change collaboration of the app
- This does not change billing or access on the payment method of the app

### Alternative team invite
{#alternative-team-invite}

If you plan to collaborate with someone on a regular basis and on more than one app, consider using a [team](#the-team).

---

## Invite to a payment method
{#invite-to-a-payment-method}

Share access to a payment method. Use this to invite a developer or team to a payment method.

### Get ready
{#get-ready-9}

Understand that an account at fortrabbit represents a person. [Apps](#the-app) are owned by [payment methods](#the-payment-method), which are objects that are controlled by [people](#the-person). See [billing collaboration](#billing-collaboration) for the concepts.

### Use cases
{#use-cases-10}

Use the 'invite to payment method' flow to invite someone to access an existing payment method. The invited person can be a non technical business owner (client, see [account types](#account-types)) or a tech-savvy developer to connect a team. Use this flow to invite:

- A co-founder of a startup or agency
- Someone from the billing department
- Another team

Depending on the [account type](#account-types) people connected to a payment method can:

- Clients and developers: receive invoices, change the billing credentials
- Developers: attach the payment method to new apps or existing apps

### How it works
{#how-it-works-5}

This describes the app invite flow from both sides:

#### On the inviter side
{#on-the-inviter-side-2}

1. You need to have a [billing connection](#billing-connection) to a [payment method](#the-payment-method)
2. In the dashboard, find the link
3. Select the apps you like them to pay
4. Enter the email address of payee

:BlockLink{title="invite to payment method" path="/new/invite/payment-method"}

#### On the invited side
{#on-the-invited-side-2}

1. Receive an email with an invite link
2. Login to fortrabbit or create a new account for this
3. Accept the invite and follow the steps to create or choose a new payment method for the apps

#### Consequences
{#consequences-2}

- The inviter will loose their [billing connection](#developer-connection) to the app
- The inviter will keep the [developer connection](#developer-connection)
- The invited account is in power to delete the app or assign other developers
- It's also possible to connect a team to a payment method

### Alternatives
{#alternatives-4}

This flow is specifically made to share access on a payment method. You can also invite someone to a [take over billing](#invite-to-take-over-billing).

With team collaboration members with unlimited access - [see team roles](#team-roles) - automatically have access to payment methods that are connected to the team.

---

## Invite to take over billing
{#invite-to-take-over-billing}

Invite someone to take over billing and transfer the payment method of an app - works for trial apps too.

### Get ready
{#get-ready-10}

Understand that an account at fortrabbit represents a person. [Apps](#the-app) are owned by [payment methods](#the-payment-method), which are objects that are controlled by [people](#the-person). See [billing collaboration](#billing-collaboration) for the concepts.

### Use cases
{#use-cases-11}

Use the 'invite to pay' flow to invite your client or the new owner to pay for the apps.

- A freelancer developer invites his client
- The owner of a project is changing

In most cases the invited person is a non technical business owner and thus will choose to become a client, see [account types](#account-types), to not be bothered with developer topics.

#### Designed for freelancers and their clients
{#designed-for-freelancers-and-their-clients}

With the invite to pay flow you will pass on control of ownership. You will not have a [billing connection](#billing-connection) to the apps after any more. This is by design. The invite to pay flow specifically supports freelancers working with their clients. Freelancing developers should not be responsible for the hosting.

### How it works
{#how-it-works-6}

This describes the app invite flow from both sides:

#### On the inviter side
{#on-the-inviter-side-3}

1. You need to have an [app](#the-app) already, this can be a trial app
2. In the dashboard, find the link
3. Select the apps you like them to pay
4. Enter the email address of payee

:BlockLink{title="invite to pay" path="/new/invite/pay"}

#### On the invited side
{#on-the-invited-side-3}

1. Receive an email with an invite link
2. Login to fortrabbit or create a new account for this
3. Accept the invite and follow the steps to create or choose a new payment method for the apps

#### Consequences
{#consequences-3}

- The inviter will loose their [billing connection](#developer-connection) to the app
- The inviter will keep the [developer connection](#developer-connection)
- The invited account is in power to delete the app or assign other developers

### Alternatives
{#alternatives-5}

This flow is specifically made to transfer payment for apps. You can also invite someone to a [payment method](#invite-to-a-payment-method) that already exists.

---

## How to
{#how-to}

Git things done.



---

## Developer collaboration
{#developer-collaboration}

Concepts and workflows to share app access with other developers.

### Get ready
{#get-ready-11}

Have a look at the [collaboration intro](#collaboration-intro) to understand the basics of the fortrabbit collaboration features.

```raw
┌───────────┐    ┌───────────┐
│ developer │    │ developer │
└─────┬─────┘    └─────┬─────┘
  unlimited         limited
┌─────▼────────────────▼────┐
│           team            │
└───┬─────────┬─────────┬───┘
┌───▼───┐ ┌───▼───┐ ┌───▼───┐
│  app  │ │  app  │ │  app  │
└───────┘ └───▲───┘ └───────┘
        ┌─────┴─────┐
        │ developer │
        └───────────┘
```

The illustration above shows the different ways to connect developers to apps, directly or through teams.

### Direct app access and collaboration
{#direct-app-access-and-collaboration}

Suited for freelancers, solo developers and solopreneurs. By default apps are directly attached to your personal account. Use cases:

- Personal projects, portfolios, learning, weekend hacks
- Direct client work

It's possible to share developer access on an app by app basis. You can invite a colleague, or another freelancer to specific apps:

- [About app invites](#invite-to-app)

### Team collaboration
{#team-collaboration}

Work together on multiple apps in a team of developers with simple role based access. Instead of sharing app by app, share access to a group of apps with a group of people.

- [About teams](#the-team)
- [Team roles](#team-roles)
- [About team invites](#team-invite)

---

## Billing collaboration
{#billing-collaboration}

Share access to billing with clients, the boss, the billing department and fellow founders.

```raw
┌───────────┐    ┌───────────┐
│   team    │    │  person   │
└─────┬─────┘    └─────┬─────┘
    access           access
┌─────▼────────────────▼────┐
│       payment method      │
└───┬─────────┬─────────┬───┘
   owns      owns     owns
┌───▼───┐ ┌───▼───┐ ┌───▼───┐
│  app  │ │  app  │ │  app  │
└───────┘ └───────┘ └───────┘
```

The above illustrates how teams and individuals can share access on a payment method, which owns the apps.

### Non technical client access
{#non-technical-client-access}

Most parts of the fortrabbit platform are very technical. Often the business owners are not developers. That's why there are two type of accounts with the fortrabbit dashboard: developer and clients. See [account types](#account-types) for more.

### Direct billing access
{#direct-billing-access}

People can be connected to payment methods directly. This includes developers, as well as clients. When a connection between a payment method and a person is established by invitation, the person can control the payment method and it's apps.

### Billing access with teams
{#billing-access-with-teams}

Teams can also be connected to payment methods. In such cases the billing access is role based. All team members with unlimited team access have full access on the connected payment methods as well.

### Separation of concerns
{#separation-of-concerns}

Some of our agency and freelancer clients prefer to bill their clients a yearly maintenance fee for websites (retainer) which includes the fees for hosting. That's OK and you can continue doing that. But inviting clients to become fortrabbit themselves has some benefits:

Most importantly, responsibility gaps can be avoided. When end clients are becoming our clients are directly, we will have to deal with them. It includes an exist strategy for agencies and freelancers as well, they can simply leave the client apps alone.

We believe transparency is important for such business relations. So we don't offer a white label hosting solution or agency bonus programs.

### Two levels of collaboration
{#two-levels-of-collaboration-1}

---

## Technical contact
{#technical-contact}

Assign developers to be contacted by fortrabbit.

A technical contact is a [person](#the-person) with a [developer connection](#developer-connection) to the app - usually the responsible developer with good knowledge of the project and code base. Think 'web master'.

Each [app](#the-app) should have one or more technical contacts associated. There is a dashboard setting with the app to select technical contacts from a list of developers connected with the app. By default, the developer creating the app will be assigned.

fortrabbit staff may get in touch with the technical contacts by e-mail to inform about important updates related to specific apps. Examples are:

- Software vulnerabilities
- Important software updates or incompatibilities
- Targeted DDoS attacks
- Excessive resource over-usage
- Suspicious activities
- Website hacked

Pro-actively contacting customers about important issues is done by fortrabbit at a best effort basis. fortrabbit does not guarantee contact coverage for any potential problem. It remains the responsibility of the customer to keep the software up-dated, as well as the list of technical contacts.

---

## Billing connection
{#billing-connection}

A billing connection associates a person with an app through a payment method, either directly or through a team. A billing connection allows administrative tasks on an app, but has nothing to do with code access.

```plain
## Billing connection
{#billing-connection-1}
person → payment method → app
person → team → payment method → app 
```

### What you can do with a billing connection
{#what-you-can-do-with-a-billing-connection}

- Add/remove developers and teams
- Delete apps
- Create apps
- Change the [payment method](#the-payment-method)

### Who can have a billing connection?
{#who-can-have-a-billing-connection}

- Developers and clients, see [account types](#account-types)

### Billing connection types
{#billing-connection-types}

One can either have direct billing connection or through a team.

#### Direct billing connection
{#direct-billing-connection}

You can have your own personal payment method that can also be shared. You can also be invited or invite other developers to directly connect to an app you have access on.

#### Team billing connections
{#team-billing-connections}

Team members with unlimited access - see [team roles](#team-roles)- have access on all payment methods connected to the team.

### Relation to developer connection
{#relation-to-developer-connection}

A similar concept is the [developer connection](#developer-connection), which defines how a person has technical access on an app.

---

## Developer connection
{#developer-connection}

A developer connection defines how a developer is associated with an app.

```plain
## Developer connection
{#developer-connection-1}
person → app
person → team → app 
```

### What you can do with a developer connection
{#what-you-can-do-with-a-developer-connection}

- Change settings and deploy code to an app
- Delete apps
- Create apps

### Who can have a developer connection?
{#who-can-have-a-developer-connection}

- Developers only, see [account types](#account-types)

### Developer connection types
{#developer-connection-types}

A developer can have a direct developer connection or through a [team](#the-team):

#### Direct developer connection
{#direct-developer-connection}

You can have your own personal apps that can also be shared. You can also be invited or invite other developers to directly connect to an app you have access on. See [app invite](#invite-to-app).

#### Team developer connections
{#team-developer-connections}

When creating an app and you have access on teams, you will be asked about the context, which can either be personal or team.

Not all team members are automatically connected to all apps of the team. Instead you can subscribe to apps that you'd like to be connected to. Unlimited team members can subscribe themselves. Limited team members can request access on team apps. See [team roles](#team-roles).

### One developer connection per app
{#one-developer-connection-per-app}

Each developer can only have one active developer connection to an app. While it is possible that an app is connected to different teams and also a developer can be part of different teams, the developer still needs to decide how they want to be connected to the app.

### Relation to technical contacts
{#relation-to-technical-contacts}

Not all developers connected to the app need to be [technical contact](#technical-contact).

### Relation to billing connection
{#relation-to-billing-connection}

A similar concept is the [billing connection](#billing-connection), which defines how a person has billing access on an app.

---

## Account types
{#account-types}

### Understand individual access
{#understand-individual-access-1}

An account on fortrabbit represents a person, not an entity. Your account settings are part of your [personal access](#the-person) to the fortrabbit system, also see [account organization](#account-organization). You can choose your type of account when signing up and change it later on if you made mistake initially.

### Developer
{#developer}

As a developer you are exposed to all dashboard and platform features. You have technical access to apps and all collaboration features such as teams. Developers can:

- Create and delete teams
- Collaborate in teams
- Create, delete and change apps
- Create, delete and change environments
- Deploy code to environments
- Create, delete and change payment methods
- Change billing for apps

### Client
{#client}

As a client you have limited access on the dashboard. Most technical aspects are hidden to remove unnecessary complexity. A client account is also a personal login and should not be shared. A client can be the client of a freelancing developer or an agency. It can also be the boss or someone from the billing department. Clients have the power to manage billing aspects and certain parts of collaboration. This includes:

- Add and remove developers and teams to apps
- Delete apps
- Create, delete and change payment methods
- Change billing for apps

#### Convenience
{#convenience}

The client features are freeing you from babysitting the billing setup with your client. It's a more enjoyable experience for your client too. They are in control, yet not overwhelmed.

#### Responsibility
{#responsibility}

The most important part of the client feature is separation of concerns. When the website goes down because of service issues with us, we - not you the developer - need to face the client. For that, we have the service level agreement with your client directly. And when your client forgets to pay the hosting fees or to update the payment credentials, it's our job to run after the money.

#### Not limited
{#not-limited}

While the client feature is popular and recommended, we know that it will not fit all business workflows. More corporate clients might have restrictions on 3rd party providers, or you simply prefer to have a yearly retainer with your client. That's why there are additional workflows for consolidated billing using payment methods to be separated or shared by teams or projects.

---

## Team roles
{#team-roles}

Each team member has an associated role within a team. Developers with one role in one team can have a different role in a different team.

### Unlimited
{#unlimited}

This is the standard role and is often suitable for all members small teams or senior developers of large teams. It gives the person with thr role full access on the team, it's apps, it's members and billing.

- create, delete, configure & scale all apps with the tam
- create and delete environments
- access code of all apps of the team
- subscribe and unsubscribe from apps
- delete, create, change payment methods connected to the team
- manage all other member roles
- invite new member for any role to the team
- leave the team (if other members are present)
- delete the team

### Limited
{#limited}

Use this role to limit access for junior developers or developers that are not part of the core team.

- delete, configure & scale chosen apps of the team
- create and delete environments
- unsubscribe from team apps
- request access on team apps
- access code on chosen apps
- leave the team

---

## Collaboration
{#collaboration-2}

Sharing access infra resources with others.



---

## Backup files
{#backup-files}

What is included and excluded. How to use the files downloaded from the backup component to actually restore a website.

The fortrabbit [backup component](#backups) provides you with a downloadable file archive of an [environment](#the-environment) at a given time, see [retention](#backup-retention). This archive contains everything required to restore the state of that backup.

- Files: Everything present on the file system
- Database: a database dump file, if [database](#mysql) is booked

### Use cases
{#use-cases-12}

- Grab a single file that was deleted
- Restore only the database but not the files
- Additional backups: store backups offsite for long time retention
- Boarding a new developer: Set up a local development
- Verifying the state of a backup before [restoring](#restore-from-backup)

### Backups VS git deployment
{#backups-vs-git-deployment}

Developers using [git deployment](#deployment-intro) already have access to an archive with a complete history of the code base. The fortrabbit backups also contain runtime data such as the vendor folder contents and user uploads. Given the nature of most PHP based applications.

### Backup file sizes
{#backup-file-sizes}

The shown size of the backups is unlikely to match what is shown with actual usage for MySQL size and web storage. Mind that the backups are compressed, while the data in production is not.

The size of the backup shown in the dashboard likely will not match with the downloaded files. This is because the sizes with the dashboard are shown in binary (mebibyte) not decimal format (megabyte) like with most Operating Systems. Also the local file system may have a different block size.

### Excludes
{#excludes}

Some run-time and cache files are excluded from the backups.

```raw
## Craft
{#craft}
'storage/backups/',
'storage/logs/',
'storage/runtime/',
'web/cpresources/',

## Laravel
{#laravel-2}
'storage/framework/',
'storage/logs/',

## Symfony
{#symfony-1}
'var/cache/',
'var/log/',

## WordPress
{#wordpress-1}
'wp-content/cache/',

## Archives
{#archives}
'*.zip',
'*.tar',
'*.tar.gz',
'*.tgz',
'*.tar.bz2',
'*.tbz',

## Misc
{#misc}
'.git/',
'*.sql',
```

### Restore from backup files
{#restore-from-backup-files}

While you can [restore from backup](#restore-from-backup) using the dashboard, you also have the option to manually revert to a previous state by uploading the necessary files to the environment.

#### Restore files
{#restore-files}

To recover files from a backup, first ensure to have the unpacked files from the backup archive on your local machine. Then upload these files to your environment at using SFTP or [rsync](#rsync-deployment). Be sure to remove any unnecessary files from the remote environment and don't forget to include hidden files.

#### Restore database
{#restore-database}

The database backup file is a standard dump created by the `mysqldump` tool. Restore it by importing the data into your MySQL database. For detailed instructions, refer to our [database export/import guides](#database-export-import). It may be necessary to drop the old tables before importing the new data.

---

## Topic backups
{#topic-backups}



---

## Restore from backup
{#restore-from-backup}

Rollback an environment to a prior state.

### Requirements
{#requirements}

To restore from a backup, the [backup component](#backups) needs to be booked and at least one backup already needs to be present with the [environment](#the-environment) to be chosen as backup source.

### Use cases
{#use-cases-13}

- Something broke the site, you want to go back to a working state
- The site has been hacked

### How to restore a backup
{#how-to-restore-a-backup}

- Visit the backups section of an environment
- With the list of available backups choose the one you want to restore
- Click the restore button, confirm, wait until finished

The process can take a while. The time it takes depends on the size of the project. It is usually finished within a couple a couple of minutes but can also take hours. While the backup restore is in progress, the environment will stay online for most of the time, but may have degraded performance. A short downtime is expected.

### What happens during restore
{#what-happens-during-restore}

The chosen backup will be unpacked and prepared. Once ready, the state will be switched. The environment will serve the state of backup, the **previous state will be deleted**.

### Recommendations
{#recommendations-1}

- Back up the current state, by manual backup or by [downloading a snapshot](#how-to-download-a-full-website)
- Know about the state of the backup you are about to roll back to, see [backup files](#backup-files)
- Don't change anything while the backup rollback is in progress

### No guarantees
{#no-guarantees}

It can not be guaranteed that the backup restoration will leave the environment in a working state. It's possible that the environment returns an error after the restoration. In many cases that's a [500 error](#504), which is easy to debug, by looking at the logs.

### Backup restore VS git deployment
{#backup-restore-vs-git-deployment}

Mind that the backup includes the actual state of files present at the time when the backup was made. When [git deployment](#deployment-intro) is used, the head of the connected branch might be ahead. So it's possible that the next git deployment will cause issues. One way to deal with that is to reset the connected Git repo to a state that matches the restored backup, but there is no general rule of thumb for that.

### Backup excludes
{#backup-excludes}

See [backup excludes](#excludes).

---

## Backup retention
{#backup-retention}

::CallOut{alert}
The backup retention feature is not implemented yet. So far only daily backups.
::

The [backup component](#backups) is available in different plans. Larger ones include more backups. Backup retention determines how long backups are kept. This concept is crucial for ensuring data availability, compliance, and efficient storage management.

Depending on the plan chosen, multiple backups of the same type might be included. If the plan includes three monthly backups, then monthly backups are retained for three months.

### Daily backups
{#daily-backups}

- kept for a short period
- created daily at randomized times

### Weekly backups
{#weekly-backups}

- retained for a longer period
- Sunday backups are kept

### Monthly backups
{#monthly-backups}

- kept for an extended period
- Backups from the start of the month are kept

### Manual backups
{#manual-backups}

In addition to automatically scheduled backups, it's possible to trigger the immediate creation a backup from the dashboard. This backup will be treated like a new daily backup.

- If the currently booked [backup plan](#backups) includes one daily backup, the new manual backup will replace the current backup.
- If the currently booked backup plan includes two daily backups, the oldest backup from two days ago will be deleted and the backup from yesterday will move down one slot.

---

## Jobs usage
{#jobs-usage}

Jobs are an optional component, see [booking and scaling jobs](#jobs). After booking a new settings page will become available with the environment in the dashboard. Here you can add, remove, start, stop and edit jobs.

### Job settings
{#job-settings}

- **Status**: active/disabled
- **Job name**: A unique name, identifier
- **Command**: The command to run, [see below](#command-settings)
- **Job type**: Cron or worker
- **Exit signal**: Graceful shutdown - default is usually fine
- **Exit timeout**: Time to forceful kill when graceful shutdown is not responding

When choosing the type cron these additional settings become available:

- **Interval**: How and when the job should run, see [crontab help](#crontab-schedule-reference)
- **Max runtime**: How long the job is allowed to run

#### Command settings
{#command-settings}

You need to call a command or script via the runtime. To call a PHP task you need to prefix it with `php`. To call a shell script you need to prefix it with `bash`:

- `php artisan queue:listen -v`
- `bash path/to/my-script.sh`

### Job types
{#job-types-1}

- [Workers](#workers): Non-stop running in the background, event driven triggers
- [Crons](#crons): Scheduled at certain times

---

## Crons
{#crons}

Cron basics, crontab syntax.

### About crons
{#about-crons}

A cron job is a scheduled task in Linux that automates executing software, typically shell scripts or executables. They allow you to schedule tasks, such as running scripts or commands, to occur automatically at specific times or intervals. The fortrabbit platform offers some additional abstraction. Crons are available with the [jobs component](#jobs) and managed through the dashboard, see [job usage](#jobs-usage). The job component runs in an isolated container, so that frontend and backend processes are separated.

#### Cron use cases
{#cron-use-cases}

- Publish a scheduled story
- Periodic email sending
- Read and parse RSS feeds
- Collect and analyze data
- Generate reports
- Run database optimizations
- Update contents
- Clear caches

Cron jobs are entries in the cron table (crontab), each containing a schedule and a command to execute. The cron daemon (crond) reads the crontab to determine which jobs to run and when to run them.

### Crontab schedule reference
{#crontab-schedule-reference}

```plain
* * * * *
| | | | |
| | | | Day of week (0-6 | Sun-Sat)
| | | |
| | | Month (1-12)
| | |
| | Day of Month (1-31)
| |
| Hour (0-23)
|
Min (0-59)
```

Online tools like [crontab.guru](https://crontab.guru) can help you with configuration.

### Crons in PHP today
{#crons-in-php-today}

Crons are common and have been around for a long time in the PHP world. You can call any PHP script as a cron at a specified time or interval. Having the cron script in PHP gives you the benefit of version controlling the logic of the job to run. Modern PHP frameworks, such as [Laravel](#laravel) and [Symfony](#symfony-guide) have added their own scheduling components and logic with advanced features. They offer additional abstraction so developers don't need to deal with nitty gritty.

- Laravel: `artisan schedule:run`, see [Laravel queuing](#queueing)

### Crons on fortrabbit
{#crons-on-fortrabbit}

The fortrabbit platform offers additional abstraction. Crons are part of the [jobs component](#jobs). See [job tuning](#jobs-tuning).

### Crons and deployments
{#crons-and-deployments}

Each successful [deployment](#deployment-intro) will restart all running crons. This assures the jobs are running on the latest code base.

---

## Workers
{#workers}

Long running scripts, isolated in the background.

### About workers
{#about-workers}

A worker job is a long running task that is executing software, scripts or executables. The fortrabbit platform offers some additional abstraction. Workers are available with the [jobs component](#jobs) and managed through the dashboard, see [job usage](#jobs-usage). The job component runs in an isolated container, so that frontend and backend processes are separated.

Unlike crons, which offer scheduled execution of scripts, worker jobs can run non-stop in the background.

### Worker jobs use cases
{#worker-jobs-use-cases}

- Image processing
- API communication
- Meta data aggregation

### Workers and deployments
{#workers-and-deployments}

Each successful [deployment](#deployment-intro) will restart all running workers. This assures the jobs are running on the latest code base.

---

## Jobs tuning
{#jobs-tuning}

### Logging
{#logging}

Both STDOUT and STDERR generated by any job are logged by our platform, but aren't accessible right now. They will eventually be shown in the dashboard.

### Restart after code update
{#restart-after-code-update}

This happens automatically. Whenever you push a new code update via [git deployment](#deployment-intro), jobs will be shutdown and started anew.

### Considerations
{#considerations-1}

- The total (max) memory amount of all jobs should be below the memory limit of the plan.
- Exits of jobs should be looked into. Usually nonstop worker jobs should run continuously and not exit often.

The memory limit is for all jobs combined. Resources needed for each application can vary largely, depending on what each particular job is doing.

### Graceful shutdown
{#graceful-shutdown}

If your job does really long running processing, it's likely running at all times. Any code push or manual deployment forces a restart of all jobs.

To avoid losing valuable state when our system kills the job, you can use Unix signal handling to write a graceful shutdown handler. For this you can use the automatically available [PCNTL](http://php.net/manual/en/book.pcntl.php) extension.

The most simplistic PHP script for a job is a while loop:

```php
while (true) {
  do_something();
  sleep(5);
}
```

To make sure that `do_something()` is never aborted, you can extend the script like so:

```php
declare(ticks=1);

$shutdown = false;
pcntl_signal(SIGTERM, function($signo) use (&$shutdown) {
    error_log("Received shutdown signal");
    $shutdown = true;
});

while (true) {
  do_something();
  foreach (range(1, 5) as $num) {
    if ($shutdown) {
      error_log("Shutting down safely");
      exit(0);
    }
    sleep(1);
  }
}
```

### Do not detach
{#do-not-detach}

If you don't know what that is: never mind. If you do know: don't detach. To guarantee that we can monitor jobs correctly they need to run with-under the parent processes which started them. All detached processes will be killed.

### Overlapping jobs
{#overlapping-jobs}

Sometimes a cron job may be called quickly multiple times and thus end up with multiple instances of the same job running. At best you should design your application so that this does not happen or happens in a controlled manner. We have reasonable limits in place to control how many instances of the same job are allowed to run in parallel.

---

## Jobs
{#jobs-1}

Working with crons and workers.



---

## Platform
{#platform}

Familiarize yourself with the building blocks of fortrabbit.



---

## Install Laravel locally
{#install-laravel-locally}

### Get ready
{#get-ready-12}

Have a [local development environment](#intro-to-local-development-with-php) up and running.

### Install Laravel on your local machine
{#install-laravel-on-your-local-machine}

**Recommended**: Use the detailed [official Laravel install guide](https://laravel.com/docs/installation) as your guideline to install Laravel on your local machine first. Here is the gist:

```shell
## Install the Laravel installer
{#install-the-laravel-installer}
composer global require laravel/installer

## Create a Laravel project
{#create-a-laravel-project}
laravel new {project_folder_name}
```

In some cases Laravel is the framework for the actual software that runs on top - like with [Statamic](#install-statamic) or [October CMS](#october-cms-guide).

### Install Laravel on the server
{#install-laravel-on-the-server}

Another option is to install Laravel directly on the environment like so:

1. Login to an environment by [SSH](#ssh-access)
2. Run the above steps to install a Laravel project
3. Move all files in `{project_folder_name}` one level up again

We believe it's better to start with a local development environment first. A local first approach is easier for Git deployments too.

### Add your magic
{#add-your-magic}

Installing a plain Laravel will not do much. Now add your templates, design and content to make it shine. You probably don't need hosting right away. Most development can happen locally. Start thinking about deployment, once it's ready.

### Setup GitHub
{#setup-github}

**Optional but recommended**: To enable git deployments later on, init git and add GitHub as remote repo, either as a public or private.

- [Deployment intro](#deployment-intro) - concepts on fortrabbit
- [Git intro](#git-intro) - new to Git?

---

## Laravel setup
{#laravel-setup}

Prepare your local Laravel installation for fortrabbit.

### Get ready
{#get-ready-13}

- [Local development environment](#intro-to-local-development-with-php) up and running.
- [Laravel installed locally](#install-laravel-locally) best with attached Git repo.
- Install the [fortrabbit GitHub App](#the-fortrabbit-github-app) for automatic deployments.

### Create an app at fortrabbit
{#create-an-app-at-fortrabbit}

Create a new app in the fortrabbit dashboard. The wizard will guide you through the steps. You can connect the repo from GitHub.

:BlockLink{title="Create a new app" path="/new/app"}

### Software template
{#software-template}

If Laravel is detected or you have chosen it in the software list, the Laravel [software template](#software-templates) will be applied. This will pre-configure common ENV vars, build and post-deploy commands and set the root path to `public`.

### MySQL configuration
{#mysql-configuration}

Not all Laravel projects require a database connection. Some do. Just keep `config/database.php` as it is when you have chosen Laravel with the software template. The all CAPITAL configs in the `config/database.php` file will be replaced by the contents of the environment variables. For your local development setup you can populate the `.env` file with your local database credentials. See the [ENV var topic](#env-vars-intro) as well.

This will enable the environment to connect to the database.

---

## Laravel deployment
{#laravel-deployment}

Setup automatic git deployment for your Laravel application hosted on fortrabbit.

### Get ready
{#get-ready-14}

1. Have a [local development environment](#intro-to-local-development-with-php) running
2. Local [Laravel installation](#install-laravel-locally)
3. Know about [deployment features](#deployment-intro)
4. Install the [fortrabbit GitHub app](#the-fortrabbit-github-app) with your GitHub account
5. Completed [Laravel setup steps](#laravel-setup)

### Initialize Git and add GitHub
{#initialize-git-and-add-github}

Here's an example using Git and [GitHub CLI](#github-cli) to set up a local repository and connect it to GitHub:

```shell
## Setup local git repo
{#setup-local-git-repo}
$ git init
$ git add -A
$ git commit -m 'Init'

## GitHub CLI to create/connect remote Git repo
{#github-cli-to-create-connect-remote-git-repo}
$ gh repo new
## Follow the steps
{#follow-the-steps}
## Push an existing local repository to github.com
{#push-an-existing-local-repository-to-github-com}
## Add as remote and assign current branch as 'origin'
{#add-as-remote-and-assign-current-branch-as-origin}
```

At the end, the Git repo at GitHub is created and content already pushed. From now on you only need to run `git add`, `git commit`, and `git push` to send code changes to GitHub.

See the [git deployment intro](#deployment-intro) for more details on how to connect a local repo to a GitHub remote and enable automatic deployment using the [fortrabbit GitHub App](#the-fortrabbit-github-app).

### Connect your GitHub repo with fortrabbit
{#connect-your-github-repo-with-fortrabbit}

If you already created an app on fortrabbit, connect the repository through the app settings. If not, create a new app on fortrabbit and set up the deployment:

:BlockLink{title="Create a new (free trial) app" path="/new/app"}

Choose Laravel as the software preset. Use Git deployment and select the Git repository you created previously.

---

## Laravel deploymentbuild settings
{#laravel-deploymentbuild-settings}

Configure git deployment for your Laravel application hosted on fortrabbit.

### Get ready
{#get-ready-15}

1. Have a [local development environment](#intro-to-local-development-with-php) running
2. Local [Laravel installation](#install-laravel-locally)
3. Know about [deployment features](#deployment-intro)
4. Install the [fortrabbit GitHub app](#the-fortrabbit-github-app) with your GitHub account
5. Completed [Laravel setup steps](#laravel-setup)
6. Ready for [Git deployment](#laravel-deployment).

### Recommended Laravel build steps
{#recommended-laravel-build-steps}

If you import an already existing app from GitHub, we detect what is needed for deployment and you should have sensible defaults already.

But Laravel is versatile. It can act as a backend to exchange with a frontend or it can be used as a monolith. It might be extended with additional software. Therefore [deployment build step pipeline](#build-commands) options differ.

Laravel Livewire and Laravel Inertia (without Server Side Rendering) should work out of the box.

Because Inertia with SSR (Server Side Rendering) requires a node runtime, this is not currently supported by our platform.

Configure the build steps in the fortrabbit dashboard. These are commonly used:

#### Composer build step
{#composer-build-step}

In almost all cases you will want to run Composer during deployment for Laravel based applications, see also [Composer on fortrabbit](#composer).

```shell
composer install --no-dev --prefer-dist --no-interaction --no-ansi --no-progress
```

#### NPM build step
{#npm-build-step}

[Vite](https://vitejs.dev) is the default asset bundler for Laravel. For more details on using Vite, see [Laravel's docs](https://laravel.com/docs/vite).

```shell
npm install
npm run build
```

This will first install node dependencies. It will then compile the assets and place them in a `build` folder in the `public` directory. This folder is by default excluded from the repo in `.gitignore`.

#### Post-deploy commands
{#post-deploy-commands-1}

Laravel requires a few directories to run correctly.

If you are using a database, you likely will want to run database migrations after you have deployed. We advice to run these post-deploy commands:

```shell
mkdir -p storage/framework/{sessions,views,cache}
php artisan migrate --force
```

### Mostly done
{#mostly-done}

Now you should have setup an automatic deployment pipeline that will listen to changes on your GitHub repo branch and deploy these automatically, running the configured build steps.

### Database syncing
{#database-syncing}

Laravel applications with databases may require content syncing from your local development to the environment or the other way around. Please see [MySQl import/export guides](#database-export-import).

### Additional workflows
{#additional-workflows}

The fortrabbit platform is not limited to GitHub deployment. Your application might has runtime data such as uploaded assets that require syncing. Have a look at our [deployment features in 'Code VS Content'](#code-vs-content) for options and concepts.

#### Laravel installer
{#laravel-installer}

Beside the `artisan` CLI, there is also a `laravel` installer CLI. It adds a convenience layer installing Laravel and some a lot of commands using the Laravel Cloud solution (bloatware). It can be installed as a global composer dependency.

- [Laravel docs install](https://laravel.com/docs/installation#creating-a-laravel-project)

It's possible, but not recommended, to install and use the laravel installer CLI on the remote environment with fortrabbit. Better use it in your local development environment.

---

## Laravel tuning
{#laravel-tuning}

Configure Laravel and run on fortrabbit.

### Get ready
{#get-ready-16}

You have already started your Laravel on fortrabbit journey with the [setup](#laravel-setup) and continued over [deployment](#laravel-deployment). This is the final article to address most common configuration options to successfully run Laravel based applications on fortrabbit.

### Emoji support
{#emoji-support}

<!-- TODO: Review by infra! -->

Laravel uses the `utf8mb4` character set by default, which includes support for storing "emojis 🔥" in the database. You need to manually configure the default string length generated by migrations in order for MySQL to create indexes for them in your `AppServiceProvider`:

```php
use Illuminate\Support\Facades\Schema;

/**
 * Bootstrap any application services.
 *
 * @return void
 */
public function boot()
{
  Schema::defaultStringLength(191);
}
```

### Manually running artisan migrate
{#manually-running-artisan-migrate}

While it's recommended to [run database migrations automated](#migration-build-step) each time you deploy, you can also do that manually. Log in by [SSH](#ssh-access) and execute `artisan`:

```shell
## login and execute
{#login-and-execute}
$ ssh {{app-env-id}}@ssh.{{region}}.frbit.app
$ php artisan migrate --force
```

**Note**: If `APP_ENV` is set to `production` - which is the default - the `--force` flag for migrate commands will override the confirmation prompt. You can also add this command to your `composer.json` to have it run automatically every time you push changes.

```json [composer.json]
"scripts": {
  "post-install-cmd": [
    "php artisan migrate --no-interaction --force",
  ],
}
```

With that in place, any time you deploy your code, database changes will be applied immediately. If no database changes are required, nothing happens, so it is safe to run all the time. Just make sure to test your upgrades and migrations locally first.

### Logging
{#logging-1}

<!-- TODO: Review this with care! Is it really possible to alter an ENV var to output this? Otherwise provide exact settings -->

Logs for Laravel are stored in `storage/logs` per default. Our [software preset](#software-templates) for Laravel however pre-configures log output to `stderr` and `stdout` so the logs become available in the dashboard - see the [logging article](#logs).

If for some reason you can not access the logs in the dashboard, see if you can access these via [SSH](#ssh-access) or [SFTP](#sftp-access).

See [Laravel logging help](https://laravel.com/docs/logging) for more.

### User sessions
{#user-sessions}

There are various session drivers available in Laravel. Whichever driver you end up using, will need to be specified in the environment variables. Add a new ENV var `SESSION_DRIVER` in the dashboard and give it the appropriate value. Since fortrabbit environments have persistent storage, you are able to use the default `file` driver for sessions.

To use the `database` driver, follow these steps:

```shell
## Create a migration for the session table  - locally
{#create-a-migration-for-the-session-table-locally}
$ php artisan session:table

## Apply the migration - locally
{#apply-the-migration-locally}
$ php artisan migrate

## Add, commit and push the migration file
{#add-commit-and-push-the-migration-file}
$ git add .
$ git commit -m "session migration"
$ git push

## Run the migration on the App via SSH remote execution
{#run-the-migration-on-the-app-via-ssh-remote-execution}
$ ssh {{app-env-id}}@ssh.{{region}}.frbit.app php artisan migrate --force
```

### Queueing
{#queueing}

Laravel supports multiple queue drivers. One which can be used with fortrabbit out of the box is `database`, which simply uses your database connection as a queue:

```shell
## Create a migration for the jobs table locally
{#create-a-migration-for-the-jobs-table-locally}
php artisan queue:table

## Apply the migration locally
{#apply-the-migration-locally-1}
$ php artisan migrate

## Add, commit and push the migration file
{#add-commit-and-push-the-migration-file-1}
$ git add .
$ git commit -m "queue migration"
$ git push

## Run the migration on the App via SSH remote execution
{#run-the-migration-on-the-app-via-ssh-remote-execution-1}
$ ssh {{app-env-id}}@ssh.{{region}}.frbit.app php artisan migrate --force
```

That's great for small use-cases and tinkering, but if your application handles very many queue messages you should consider using the [key-value store](#key-value-store).

Once you've decided the queue you want to use, just open `config/queue.php` and set `default` to either `redis`, `database`, `sqs` - or even better: set the `QUEUE_CONNECTION` environment variable accordingly in the dashboard.

To run `php artisan queue:work` in the background, spin up a new [worker job](#jobs) and define the artisan command as a job.

Laravel offers two commands to process queues: `queue:work` and `queue:listen`. We recommend using `queue:work`, and _not_ using `queue:listen`. This is because the `queue:listen` command boots the Laravel framework for each iteration, whereas `queue:work` boots the framework once and runs as a daemon. Using `queue:work` offers high memory and performance gains in comparison with `queue:listen`.

<!-- ## Working with Redis

Redis can be used in Laravel as a cache or a queue or both. fortrabbit does not offer a Redis service of its own. To use Redis, you will need to book an externally-hosted Redis service.

1. On the fortrabbit side, turn on the Redis extension
2. Then setup an account with a Redis provider.
3. Then configure the redis database connection in `config/database.php`:

```php
$redis = [
  'host'     => env('REDIS_HOST', 'localhost'),
  'password' => env('REDIS_PASSWORD', null),
  'port'     => env('REDIS_PORT', 6379),
  'database' => 0,
];

return [
  // other code …
  'redis' => [
    'cluster' => false,
    'default' => $redis
  ],
  // other code …
];
```

If you plan on using Redis as a cache, then open `config/cache.php` and set the `CACHE_DRIVER` environment variable to `redis`. -->

<!--

TODO: Write something about scheduling, Cron?

### Scheduling
{#scheduling}

-->

### Using artisan down
{#using-artisan-down}

`artisan down` generates the file `storage/framework/down`, which is then checked from your App's HTTP kernel with the `CheckForMaintenanceMode` middleware. You can run the command run the command via [SSH](#ssh-access) or during deployment.

### Using Laravel Envoy
{#using-laravel-envoy}

Easy. Here is an `Envoy.blade.php` example:

```php
@servers(['fr' => '{{app-env-id}}@ssh.{{region}}.frbit.app'])

@task('ls', ['on' => 'fr'])
  ls -lha
@endtask

@task('migrate', ['on' => 'fr'])
  php artisan migrate
@endtask
```

Then execute locally:

```shell
envoy run ls
envoy run migrate
```

### Sending mail
{#sending-mail}

You can not use [sendmail](#limitations) on fortrabbit but Laravel provides an API over the popular SwiftMailer library. The mail configuration file is `app/config/mail.php`, and contains options allowing you to change your SMTP host, port, and credentials, as well as set a global form address for all messages delivered by the library.

---

## Laravel
{#laravel-3}

Setup, deploy and tune Laravel based web applications on fortrabbit.



---

## Install Craft CMS local
{#install-craft-cms-local}

### Install and deploy run down
{#install-and-deploy-run-down}

1. **Install Craft CMS locally** *← you are here*
2. [Setup an app at fortrabbit](#craft-cms-setup-at-fortrabbit)
3. [Deploy code via Git](#deploy-craft-cms-to-fortrabbit)
4. [Database syncing](#database-syncing-with-craft-cms)
5. [Assets syncing](#craft-cms-assets-handling)

### Get ready
{#get-ready-17}

- Have a [local development environment](#intro-to-local-development-with-php) running. [DDEV](#local-development-with-ddev) is recommended.
- Use the [official Craft CMS install guide](https://craftcms.com/docs/5.x/install.html) as your guideline.
- Skip this step when you have a Craft project running locally and a GitHub repo connected [see below](#a---git-deployment-recommended).

### Choose your install workflow
{#choose-your-install-workflow}

The way you will install Craft will set the course on how you will deploy Craft CMS here on fortrabbit:

#### A - Create with Composer (recommended)
{#a-create-with-composer-recommended}

This is the recommended - more sophisticated - way. You will use [Git](#deployment-intro) and [Composer](#composer) in the Terminal. Run this command **on you local machine** to create a Craft CMS project to get started:

```shell
composer create-project craftcms/craft my-project
```

See an error? Check your [local development](#intro-to-local-development-with-php). Later on you can deploy Craft with Git on fortrabbit.

#### B - Download zip file
{#b-download-zip-file}

Are you more "designer" and less "developer"? Just download Craft directly from the Craft website: [craftcms.com/latest-v3.zip](https://craftcms.com/latest-v3.zip). Unpack that zip file to get to the actual project files.

### Install Craft CMS locally
{#install-craft-cms-locally}

Configure it to work on your local machine now. You have two options to install Craft:

#### A - Terminal setup (recommended)
{#a-terminal-setup-recommended}

```shell [content/index.md]
## 1. go into your local Craft folder
{#1-go-into-your-local-craft-folder}
$ cd my-project

## 2. run the terminal installer
{#2-run-the-terminal-installer}
$ ./craft setup
```

This will ask you some questions, the defaults will work mostly, you can change these settings later.

#### B - Browser setup
{#b-browser-setup}

You can also run the installer in the browser by visiting this address: `http://{{host}}/index.php?p=admin/install` in your browser. Substitute `{{host}}` with the [host name of your local development environment](#intro-to-local-development-with-php).

### Add your magic
{#add-your-magic-1}

Installing a plain Craft CMS will not do much. Now add your templates, database structure, design, plugins and content to make it shine. We recommend to do this work mostly in your local development environment.

- - -

### Choose a code deployment workflow
{#choose-a-code-deployment-workflow}

Now is a good time to think ahead a bit. How do you plan to keep your local project and the remote app environment at fortrabbit in sync? Understand that Craft CMS basically consists of three parts that needs special treatment for deployment:

- **Code** - Craft CMS (vendor) + templates/config *← decide now*
- [Database](#database-syncing-with-craft-cms) - Content tables
- [Assets](#craft-cms-assets-handling) - Volumes

#### A - Git deployment (recommended)
{#a-git-deployment-recommended}

To connect your app environment to a GitHub repo set up one now. Init git and add GitHub as remote repo - either as a public or private. Here is an example using the GitHub CLI.

```bash
## Initialize a new git repository
{#initialize-a-new-git-repository}
git init

## Add files and commit
{#add-files-and-commit}
git add .
git commit -m "Init"

## Create a new public repository on GitHub from the current directory
{#create-a-new-public-repository-on-github-from-the-current-directory}
gh repo create --public --source=. --push
```

We recommend to exclude asset volumes from Git to [sync them up and down](#craft-cms-assets-handling). In most cases this is already the case.

Skip this step if your code is already at GitHub, see [Git provider integration](#git-providers) for other providers with CI/pipeline/actions flows. If this fuzzy to you see:

- [Deployment intro](#deployment-intro)
- [GitHub CLI guide](#github-cli)
- [Git intro](#git-intro)

#### B - SFTP / rsync deployment
{#b-sftp-rsync-deployment}

Later on you can upload Craft with [SFTP](#sftp-access).

---

## Craft CMS setup at fortrabbit
{#craft-cms-setup-at-fortrabbit}

### Install and deploy run down
{#install-and-deploy-run-down-1}

1. [Install Craft CMS locally](#install-craft-cms-local)
2. **Setup an app at fortrabbit** *← you are here*
3. [Deploy code via Git](#deploy-craft-cms-to-fortrabbit)
4. [Database syncing](#database-syncing-with-craft-cms)
5. [Assets syncing](#craft-cms-assets-handling)

### Install the fortrabbit GitHub App (recommended)
{#install-the-fortrabbit-github-app-recommended}

To enable [automatic git deployments](#deployment-intro) the [fortrabbit GitHub App](#the-fortrabbit-github-app) needs to be installed with your personal account. You can do and verify this with your account settings:

:BlockLink{title="Check GitHub app" path="/you/settings"}

You can also do that later or skip it all together if you don't plan to use automatic git deployment, but SFTP upload.

### Create an app at fortrabbit
{#create-an-app-at-fortrabbit-1}

Create a new app in the fortrabbit dashboard. The wizard will guide you through the steps.

:BlockLink{title="Create a new app" path="/new/app"}

If you have the GitHub app connected and already a Git repo for your project you can connect the repo now. It will detect the software. If not, choose Craft CMS as software.

### Configuration
{#configuration-4}

If Craft CMS is detected or you have chosen it in the software list, the Craft CMS [software template](#software-templates) will be applied. This will pre-configure common [ENV vars](#env-vars-intro), build commands, post deploy commands and set the root path to `web`.

---

## Deploy Craft CMS to fortrabbit
{#deploy-craft-cms-to-fortrabbit}

### Install and deploy run down
{#install-and-deploy-run-down-2}

1. [Install Craft CMS locally](#install-craft-cms-local)
2. [Setup an app at fortrabbit](#craft-cms-setup-at-fortrabbit)
3. **Deploy code via Git** *← you are here*
4. [Database syncing](#database-syncing-with-craft-cms)
5. [Assets syncing](#craft-cms-assets-handling)

### Git deployment
{#git-deployment-1}

You are mostly set when you have followed our Craft CMS guides so far. Your local Craft CMS project is connected with a Git repo at GitHub and you have created an app and connected it to your GitHub repo.

You can now trigger a code deployment by issuing `git push` or clicking the deploy button with the dashboard. This will update the GitHub repo and deploy the latest commit to fortrabbit. See the [Git deployment intro](#deployment-intro) on how this works. The fortrabbit platform is not limited to [GitHub based deployment](#deployment-intro). See [code access](#direct-code-access) for available options.

### Deployment configuration
{#deployment-configuration}

**Likely nothing to do here.** Craft CMS is a pretty standardized application. In most cases the [build commands](#build-commands) are pre-configured through [stack detection](#stack-detector) (scanning the repo) or [software template](#software-templates).

#### Deployment strategy
{#deployment-strategy-1}

Craft CMS projects are set to [blend deployment strategy](#blend-strategy) with [replace patterns](#replace-patterns) for all project config YML files in the config folder by default. This is because the [Craft asset volumes](#craft-cms-assets-handling) can be placed anywhere in the file structure.

Consider using the [replace strategy](#replace-strategy) with [exclude patterns](#exclude-patterns) for each asset volume. It works either way.

#### Build commands
{#build-commands-2}

This setting is most likely pre-configured.

```shell
composer install # Always
npm run prod # If detected
```

#### Post deploy commands
{#post-deploy-commands-2}

This setting is most likely pre-configured. In most cases it's useful to run database migrations after deployment to apply changes from project config and migrate all changes.

```shell
php craft project-config/apply
php craft migrate/all
```

---

## Database syncing with Craft CMS
{#database-syncing-with-craft-cms}

### Install and deploy run down
{#install-and-deploy-run-down-3}

1. [Install Craft CMS locally](#install-craft-cms-local)
2. [Setup an app at fortrabbit](#craft-cms-setup-at-fortrabbit)
3. [Deploy code via Git](#deploy-craft-cms-to-fortrabbit)
4. **Database syncing** *← you are here*
5. [Assets syncing](#craft-cms-assets-handling)

### Database configuration setup
{#database-configuration-setup}

In most cases, the Craft CMS installation on fortrabbit can already connect to the remote [MySQL database](#mysql) through pre-populated [environment variables](#using-env-vars-on-fortrabbit).

But when initially installing Craft CMS on your fortrabbit environment, after [Git deployment](#deploy-craft-cms-to-fortrabbit) or [SFTP upload](#sftp-access) your database is still missing. In most cases you want to import your local database now, to have database content and structure up.

Visit the [MySQL import/export guides](#database-export-import) to learn how to sync the database up and down using different techniques.

#### Database up
{#database-up}

1. Export the local database
2. Upload the the dumped `.sql` file
3. Import the database dump into the app environment database

* [Database up via terminal](#database-up-via-terminal)
* [Database up via MySQL GUI](#mysql-database-upload-from-local-to-remote-by-gui)

#### Database down
{#database-down}

In later live cycle stages of your project you more often likely would like to download the database.

1. Export the remote database
2. Download the dumped `.sql` file
3. Import the database in your local development

* [Database down via terminal](#database-down-via-terminal)
* [Database down via MySQL GUI](#mysql-database-download-from-remote-to-local-via-gui)

---

## Craft CMS assets handling
{#craft-cms-assets-handling}

### Install and deploy run down
{#install-and-deploy-run-down-4}

1. [Install Craft CMS locally](#install-craft-cms-local)
2. [Setup an app at fortrabbit](#craft-cms-setup-at-fortrabbit)
3. [Deploy code via Git](#deploy-craft-cms-to-fortrabbit)
4. [Database syncing](#database-syncing-with-craft-cms)
5. **Assets syncing** *← you are here*

### About Craft assets
{#about-craft-assets}

Craft CMS "assets" are user generated stuff: uploaded files, mostly images that lives in "volumes" — also see [the official Craft docs](https://craftcms.com/docs/5.x/reference/element-types/assets.html) on that.

#### Assets and Git
{#assets-and-git}

When creating asset volumes in the Craft CMS control panel, their contents are by default excluded from Git, so that code and content are separated. However, if you've already created a directory in your `web` folder and you now reference that directory as the webroot of a volume you're creating, you will need to manually configure Git to ignore the files in it. To do this, add a file `.gitignore` in the volume's directory, with the following contents:

```gitignore
*
!.gitignore
```

Another reason that assets should be managed and deployed independently from Git deployment, is that files uploaded to the environment would not be represented in Git, as [Git deployment is a one way street](#git-only-syncs-up).

### Options to sync assets
{#options-to-sync-assets}

There are two directions you want your assets to flow:

- UP — When you first developed Craft locally, you may want to upload all the images you already have locally to the environment;
- DOWN — When the environment is running in production for some time and the clients or editors have created content on the environment you want to download that, so your local version is in sync.

#### 1 — Manage assets with rsync
{#1-manage-assets-with-rsync}

Give the good old `rsync` command line tool a try. It's easier than you think:

```shell
## Sync UP local assets with remote
{#sync-up-local-assets-with-remote}
$ rsync -av ./web/{your-asset-folder} {{app-env-id}}@ssh.{{region}}.frbit.app:web/
```

Replace the path and your individual folder name with your own settings. Our [rsync tutorial](#rsync-deployment) covers many useful rsync options, like excludes, `--dry-run` and `--delete`.

#### 2 — Manage assets with SFTP
{#2-manage-assets-with-sftp}

Good old [SFTP access](#sftp-access) is another valid way to to do it. Just fire up your SFTP client, log in to the App and manage the assets manually. Many SFTP clients are offering sync options, to keep local and remote files up-to-date.

#### 3 — Outsource assets to a cloud storage
{#3-outsource-assets-to-a-cloud-storage}

The assets are not stored on the file system of the App any more; once the user uploads files, they get uploaded to external cloud storage like S3 (or the Object Storage here). Then, within the templates you hot-link all the files to the external storage. This more professional design helps to reduce load on the App. Look out for S3 Craft plugins to get started with this. Only use this if you really need it. Don't over-engineer.

---

## Craft CMS tuning
{#craft-cms-tuning}

Tips, tricks, best practices and advanced topics on how to run Craft CMS successfully on fortrabbit.

### ENV var configuration
{#env-var-configuration}

Craft CMS uses modern `.env` style configuration, see [topic ENV vars](#env-vars-intro). This means you can run your Craft locally and remotely without code or configuration file changes. Locally, your `.env` file will be modified and read. That file is not part of Git, you don't need it on fortrabbit.

#### Manually setting ENV vars
{#manually-setting-env-vars}

The [software templates](#software-templates) will populate required ENV vars. If you didn't choose the Craft preset when creating the app or the ENV vars have been deleted, this is likely what needs to be set.

#### Craft ENV vars for fortrabbit
{#craft-env-vars-for-fortrabbit}

```apache [.env]
CRAFT_DB_DRIVER=mysql
CRAFT_DB_PASSWORD=${FORTRABBIT_MYSQL_PASSWORD}
CRAFT_DB_DSN=mysql:host=${FORTRABBIT_MYSQL_HOST};port=3306;dbname=${FORTRABBIT_MYSQL_DATABASE}
CRAFT_ENVIRONMENT=production
CRAFT_SECURITY_KEY=LongRandomString
```

The syntax of the keys may differ by Craft CMS version. See [ENV var usage](#env-vars-intro) for more details on aliases.

### Software template
{#software-template-1}

If Craft CMS is detected or you have chosen it in the software list, the Craft CMS [software template](#software-templates) will be applied. This will pre-configure common ENV vars, build and post-deploy commands and set the root path to `web`.

### Database setup
{#database-setup}

On fortrabbit the [environment variables](#env-vars-intro) are seeded from the ones set in the fortrabbit dashboard (not from the .env file). If you chose Craft in the [software preset](#software-templates) when creating the app, all ENV vars at fortrabbit will already be pre-populated.

### Multi-environment configuration
{#multi-environment-configuration}

Craft embraces the idea of storing environment specific configurations in ENV vars. You can create groups in every config file. The top level array key maps with the `CRAFT_ENVIRONMENT` constant, which defaults to the `CRAFT_ENVIRONMENT` ENV var. With this flexible approach you decide which configurations are under version control to share with your team and which are not. We assume fortrabbit to be your production environment, so the `CRAFT_ENVIRONMENT` ENV var is set to `production` on remote and locally to `dev`.

```shell
## Local environment ENV
{#local-environment-env}
CRAFT_ENVIRONMENT=dev
```

### Using .htaccess for redirects and to force https
{#using-htaccess-for-redirects-and-to-force-https}

Craft CMS comes with a predefined `.htaccess` file that lives inside the `web` folder. You can extend that with your own rules, like forwarding all requests to https or disabling access on the App URL. Please see our [.htaccess articles](#htaccess-intro) for examples.

### X-Powered-By headers
{#x-powered-by-headers}

<!-- TODO: Are we still using x-powered by headers? -->

You probably think it's a good idea to disable headers that expose which PHP version and CMS you use. And we think so too!

However, internally we analyze this header to determine if it is a static or dynamic PHP response. With this information we generate two different metrics for the dashboard: PHP requests and Static requests.
In `config/general.php` you can disable the header with `'sendPoweredByHeader' => false,` (default: true). This is not required, since we strip all `X-Powered-By` headers eventually.

### Enabling dev mode
{#enabling-dev-mode}

Sometime while developing you might want to see some error output directly on your browser screen. That's what the `devMode` flag is for. See the [Craft docs](https://craftcms.com/knowledge-base/what-dev-mode-does) for more details.

DevMode is disabled by default via [software template](#software-templates) on fortrabbit as the installation is public. You can change that setting with by [ENV vars](#using-env-vars-on-fortrabbit) in the fortrabbit dashboard:

:BlockLink{title="Edit ENV vars for {{app-name}} / {{app-env-name}}" path="/environments/{{app-env-id}}/env-vars"}

### Don't allow updates in production
{#don-t-allow-updates-in-production}

Craft CMS has the option to run updates directly from the Craft Control Panel. A client or editor might be tempted to use that update button in production. This is not a good idea. On fortrabbit Git is a one-way street, so any changes on the App itself can not easily be ported back to the local development environment. Also `composer update` might be triggered on the App and that can lead to performance problems.

So it's better to prevent the shiny "update" button from showing up at all. You can do that in your Craft configuration in the general settings with the `allowUpdates` flag.

`allowUpdates` is disabled by default via software template too. Change by ENV var.

### Don't allow admin changes in production
{#don-t-allow-admin-changes-in-production}

We highly recommend not making any admin changes to your production environment (fortrabbit) at all. Only do editorial changes. Have one single source of truth and only one direction (up). Please also see the official [Craft CMS docs](https://craftcms.com/docs/5.x/reference/config/general.html#allowadminchanges) on that.

Otherwise you can run into trouble: Imagine you make changes to the database structure, by adding tables for example, changing the field layout in production. Now you don't have the changes locally. But you deploy other new changes from local to production. This might overwrite the `project.yml` in production and therefore will roll back your changes. Your local development should be your master in applying design and functional changes.

`allowAdminChanges` is disabled by default via software template too. Change by ENV var.

### Change the control panel URL
{#change-the-control-panel-url}

"Security through obscurity" is a widely discussed concept. We suggest to obscure the control panel URL of your Craft installation, just because you can. Do so with the `cpTrigger` setting. If you don't set this value it defaults to `admin`.

```php
return [
  'cpTrigger' => 'godmode'
];
```

### MySQL table prefixes
{#mysql-table-prefixes}

If your local Craft installation contains a table prefix, the one on the fortrabbit app should be the same. You can set the table prefix, locally in your `.env` file, and on fortrabbit with the App's [ENV vars](/#craft-config-example) like so:

```apache [.env]
## Example Table prefix
{#example-table-prefix}
CRAFT_DB_TABLE_PREFIX=craft_
```

### Craft CLI
{#craft-cli}

Craft CMS comes with a built in command line interface which can be called from the console. You can also run it one the environment itself like so:

```shell
## Call Craft CLI via php
{#call-craft-cli-via-php}
php craft
```

Not all Craft CLI commands are safe to run in production. Our recommendations:

- `setup/*` — Don't, intended to run locally only
- `update/*` — Don't, if you deploy using git or using project config
- `clear-caches/*` — Don't, unless you have a good reason
- `resave/*` — Sometimes needed
- `project-config/sync` — Only needed if it's not part of your deployment
- `migrate/all` — Only needed if it's not part of your deployment
- `backup/db` — Useful to make a database backup. Can harm performance
- `restore/db` — Useful if you need to revert the DB to a previous state

### Logging
{#logging-2}

Without configuration, Craft CMS will pipe PHP errors to `storage/logs/web.log`.

The Craft CMS stream log location can be set to `stderr` and `stdout` by setting the [environment variable](#env-vars-intro) `CRAFT_STREAM_LOG=true`. This is pre-populated when choosing Craft CMS in the [software chooser](#software-templates) while creating the app. When the ENV var is present and true, Craft CMS error logs can be accessed through the fortrabbit dashboard.

### Sending mail
{#sending-mail-1}

Use an external third party transactional mail provider to send emails. Pixel & Tonic (Craft CMS creators) maintain a [plugin for Postmark](https://plugins.craftcms.com/postmark). With that plugin installed you can easily set it up.

See our [quirks article](#limitations) on limits sending emails. Also see [transactional mail provider integration](#transactional-email-services).

### Licensing Craft CMS
{#licensing-craft-cms}

Craft CMS is not all free. To enable the good parts you need to obtain a license from Pixel & Tonic (the folks building Craft CMS). A Craft CMS license is limited to a single domain, which means you can only access the Craft CP with one domain - otherwise you'll see a warning. You might have used the fortrabbit App URL for development and you might have used that to connect your Craft CMS licence with. You can change the domain of a Craft licence as well, if for instance you started with our App URL but now want to use your own domain with your Craft ID — over at <https://console.craftcms.com/>.

### Craft storage folder
{#craft-storage-folder}

We found a couple of Craft CMS installations blowing up the storage folder. This is often related to plugins and configuration. Some search engine bot might try to crawl all pages, causing a faceted search plugin to create gigabytes of template fragments. Some other plugin may just write very verbose logs. Best, make sure to configure your website to not cause such issues, beside the storage, such issues have impact on performance.

---

## Craft CMS performance tips
{#craft-cms-performance-tips}

All about performance problems with Craft CMS and how to run Craft CMS fast on not only on fortrabbit.

### Get ready
{#get-ready-18}

Please check out our general [PHP performance section](/3.dev/02.performance) article as well before looking at specific Craft CMS related performance issues.

### MySQL related issues
{#mysql-related-issues}

The amount and complexity of database queries, as well as the size of your dataset, have a direct impact on the performance of your site. While the queries you create in your templates are more or less your responsibility, there are other queries that you can't directly control. We have analyzed hundreds of Craft sites to understand common query patterns. Especially sites with large amounts of data (Entries, Fields, etc) and frequent content updates suffer from these "hidden" queries.

#### How Craft CMS makes use of the database
{#how-craft-cms-makes-use-of-the-database}

The beauty about Craft CMS is that you can get by with just writing TWIG templates — you don't need to write a single MySQL query yourself. Within the TWIG templates there is an abstraction layer to create a query to the database. That's a dangerous tool at your proposal since there a couple of important not so well known things about it.

- Craft is running database queries all the time, completely blocking
- Craft is joining all the time, since everything is an element, that can get slow quickly

There is much more to know, exceeding the scope of this post. Here are the most important parts:

#### How the MySQL dataset size matters
{#how-the-mysql-dataset-size-matters}

The flexible content model in Craft CMS makes it easy to write code that makes either too many database queries and/or slow queries in MySQL. Most commonly poorly performing MySQL queries are easy to miss during development, since with local development you commonly **only have a small dummy dataset**.

Also mind your local machine has a different hardware than your hosted website. In production later on, when all the pages are published and a couple of blog posts have been written, the underlying issues will become more visible. MySQL query runtime is not just adding up, it's multiplying.

#### General tips on MySQL performance with Craft CMS
{#general-tips-on-mysql-performance-with-craft-cms}

**Prevention is better than cure!** If you're reading this, the odds are you may already have run into performance issues on a Craft CMS project. But if you're just starting out with a new project, being aware of how Craft models content behind the scenes can spare you a lot of time-consuming debugging later on.

Look out for code smell: Common Craft performance anti-patterns include:

- `where` conditions on custom fields
- Queries in nested loops (N+1)
- Order on custom fields `orderBy`

**Optimizing database queries**

- [Official Craft documentation on Eager loading](https://craftcms.com/docs/3.x/dev/eager-loading-elements.html)

**Database indexes**

- [How does database indexing work? on StackOverflow](https://stackoverflow.com/questions/1108/how-does-database-indexing-work)
- [What columns are indexed in Craft (source code link)](https://github.com/craftcms/cms/blob/d4be41dae683f1f06d42c300620b556c9c057ad3/src/migrations/Install.php#L754-L935)

#### Use the Craft Debug Toolbar
{#use-the-craft-debug-toolbar}

The YII toolbar is integrated with Craft CMS. It ([see article by NYS+107](https://nystudio107.com/blog/profiling-your-website-with-craft-cms-3s-debug-toolbar)) provides useful information about which queries you run and how long it takes to execute them. Rule of thumb: if you run more 50 queries you should do something about it. It's easy to use and can help you to find slow queries with low efforts while developing.

- [Yii debug toolbar documentation](https://www.yiiframework.com/extension/yii-debug-toolbar)

#### Use the Relax plugin
{#use-the-relax-plugin}

Fortunately, there is a plugin called [Relax](https://plugins.craftcms.com/relax) that takes care it. We have released it for free to help our clients and the broader craft community.

s## Issues related to blocking PHP requests

Like described above, a PHP process is busy as long as it is executing. No one will pick up the phone (return a web page) when all the PHP processes are busy. There are various reasons why PHP requests are busy or are running for too long.

Examples from support:

- A plugin is querying an external service in a blocking way and the answer is taking too long
- The database is overwhelmed by too many or too expensive queries

### Memory/CPU related issues
{#memory-cpu-related-issues}

Sometimes there is just not enough memory or computing power to perform a calculation. This is often the case when image transformations are involved or when a lot of concurrent requests hit your App.

Examples from our support:

- Image transformations are used extensively to create too many versions of a certain image in too many sizes and formats
- Thousands of queue messages need to be processed, often caused by bulk-updates
- Bots crawl the entire site including non-existing pages which are not cacheable

### Craft queue related issues
{#craft-queue-related-issues}

Craft has its own queue implementation. You can see and control it from the Craft CMS Control Panel. The [craft-async-queue plugin](https://github.com/ostark/craft-async-queue) helps to improve the performance of the Craft queue. Hanging queues are a bad sign.

To see if performance problems are related to the Craft queue, check if one is running and delete it from the Craft Control Panel. This of course is only possible when the website is still responding.

Look for errors in the Craft queue.

### Disk I/O related issues
{#disk-i-o-related-issues}

Sometimes the file system disk operations are slowing down a website. This can be when your website is accessing the disk a lot.

Examples from support:

- Using Craft's Twig `{% cache %}` tag missing the key attribute can lead to thousands of cache files with the same data and a terrible cache-hit-rate
- The website is configured to write verbose log files

### Static files in /templates
{#static-files-in-templates}

We've seen this many times. Developers put static assets like `.css` and `.js` in the `/templates` folder next to the twig templates. Craft delivers those files, but it creates massive overhead. Instead you should always put static files in `/web/some-dir/` to prevent any PHP execution when delivering those files.

### Twig cache tag
{#twig-cache-tag}

Craft's `{% cache %}` tag is a good thing to prevent execution of expensive queries over and over again, however it's **very important** to use it wisely. Make sure to use a specific cache key, otherwise you risk an inefficient Cache-Hit-Rate and lots of cache items filling up the disk or Memcache.

### General configuration related issues
{#general-configuration-related-issues}

Performance problems are also often caused by general misconfiguration. Examples from support:

- Not having set the environment to `production` - this can contribute to bad performance since in development mode more things are getting logged
- A plugin is (mis)configured to blow up the database

### Fixing and mitigation
{#fixing-and-mitigation}

In our experience, problems are often unique to individual projects. So there is no silver bullet to make things fast. There are however some general things you can do:

#### Check and maybe block certain requests
{#check-and-maybe-block-certain-requests}

Depending on your configuration, checking the source of requests might help you to understand where resources are getting spent.

Examples from support:

- A deep content structure, creating an endless amount of possible pages that are getting crawled by web crawlers. Block certain bots or rethink your content structure.
- Common bot attacks targeting WordPress requesting a `wp-login` page which results in a 404 page, but that page is not cached or creating an expensive database query, so that the requests are generating a lot of load.
- The Blitz plugin is configured to flush the cache every hour, which triggers cache warming. [See this Twitter thread](https://twitter.com/o_stark/status/1189626958713368578).

#### Caching to the rescue
{#caching-to-the-rescue}

Caching can be highly beneficial, particularly in providing the fastest possible end user experience but shouldn't be a crutch. Instead, it's usually better to find and remediate the **root cause** of the issue where possible.

Doing caching wrong can also be the problem itself.

You want repeating parts of the website or full pages to be cached and rendered without hitting PHP or a database query touching the server. A "mega menu" is a perfect example and an opportunity for fragment caching. It creates the same database queries (sometimes 50+) for every page.

There are multiple approaches for caching in Craft CMS including:

- [**Native Twig cache tag**](https://craftcms.com/docs/3.x/dev/tags.html#cache) - the out of the box tool for fragment caching, be careful when using for side effects, more above.
- **[Blitz](https://github.com/putyourlightson/craft-blitz)** Craft CMS plugin - a popular full cache plugin with tons of options
- **[Upper](https://github.com/ostark/upper)** Craft CMS plugin (by fortrabbit co-founder Oliver Stark) - integrates reverse proxies (Cloudflare, Vanish, KeyCDN) with Craft

Please be careful about caching. In our experience, this is probably causing more problems than it is solving.

### Further reading
{#further-reading}

Ryan has some good educational video content (some paid, some free) on related topics:

- [About the Yii debug toolbar](https://mijingo.com/lessons/yii-debug-toolbar-craft-cms)
- [Debugging in Twig and Craft](https://craftquest.io/lessons/debugging-in-twig-and-craft)
- [Profiling with Xdebug live stream](https://craftquest.io/livestreams/profiling-in-xdebug)
- [Debugging with Xdebug course](https://craftquest.io/courses/debugging-with-xdebug)

---

## Updating Craft CMS
{#updating-craft-cms}

Always use the latest software version for security reasons. Here are some strategies to best keep Craft CMS up-to-date.

### Update your local development environment first
{#update-your-local-development-environment-first}

Your [local development environment](#intro-to-local-development-with-php) is where changes are applied and tested first. Please update your local Craft CMS installation first and apply updates by deploying as a second step. That way you make sure that your environments are in sync.

The `config/general.php` file we use in [our setup guide](#install-craft-cms-local) sets `allowUpdates` to `false`: this prevents plugin and Craft core updates from the Craft Control Panel in the `production` environment.

It's a common mistake we see. Make sure your environments are in sync and you don't mess with updates and installing plugins on the environment itself.

Here are the options to update Craft CMS and Craft plugins. Make sure to also check out the [official guides on the topic](https://craftcms.com/docs/5.x/update.html).

#### A) Update Craft using the Control Panel - simple
{#a-update-craft-using-the-control-panel-simple}

1. Login to the Craft CMS Control Panel of your local Craft installation
2. Go to Utilities > Updates
3. Click the "Update all" button

This will update your **local** development environment to the latest versions of Craft CMS as well as all plugins. After testing changes, deploy updates to your production App (see below).

#### B) Update Craft using the Craft CLI - advanced
{#b-update-craft-using-the-craft-cli-advanced}

Run the following command in the terminal on your computer **locally** in the root folder of the Craft project:

```shell
./craft update all
```

This will update Craft, as well as all dependencies. For a dry run just type `./craft update`, that will list the available updates.

### Deploying Craft updates
{#deploying-craft-updates}

After you have tested the updates locally you can deploy them to your environment at fortrabbit. Here are your options:

#### A) Deploying updates with Git
{#a-deploying-updates-with-git}

1. Add and commit the local changes (`composer.json`, `composer.lock`, `project.yaml` …)
2. Deploy the changes by `git push` to trigger deployment

During the [Git deployment](#build-commands) `composer install` will likely run automatically. This way your local Composer changes get applied on the remote.

#### B) Uploading updates with SSH/SFTP based workflows
{#b-uploading-updates-with-ssh-sftp-based-workflows}

Continuous development with an SFTP workflow is a hassle. One strategy is to upload the changed files from local to the App. Another strategy is to re-run the very same steps that have been done locally on the App itself.

### Database migrations
{#database-migrations}

In most cases when updating a database migration is required. This will upgrade the database table structure to match the latest updates. It will be carried out when running the updates locally. But it's an extra step required to be done with your fortrabbit environment. All essential Craft CMS settings are stored in the `project.yaml` files.

Here are your options to run migrations:

#### A) Database migrations as a build step (recommended)
{#a-database-migrations-as-a-build-step-recommended}

<!-- TODO: Test and review this section!! -->

When you have chosen Craft CMS in the [software preset](#software-templates) while creating the environment, the following two commands are part of your [deployment build steps](#build-commands).

```shell
php craft project-config/sync
php craft migrate/all
```

#### B) Craft Copy and Craft auto-migrate
{#b-craft-copy-and-craft-auto-migrate}

<!--
TODO:
Review if we still want to recommend the plugin here and if it still works. We can add the two auto-migrate commands as a standard deploy step if Craft CMS is chosen.
-->

We have also created a little auto-migrate package - [see it on GitHub](https://github.com/fortrabbit/craft-auto-migrate) - which triggers `migrate/all` and `project-config/sync` every time `composer install` runs, which means it runs every time you deploy using git.

```shell
## Install the package (locally)
{#install-the-package-locally}
$ composer require fortrabbit/craft-auto-migrate
```

With that in place, every time you deploy your code, database and project config changes will be applied. If no changes are required, nothing happens, so it is safe to run all the time. Just make sure to test your upgrades and migrations locally first. The package is also dependency of our [Craft Copy](https://github.com/fortrabbit/craft-copy) deployment tool plugin. So when you have that installed, it will always run on `git push` which is the equivalent to `./craft copy/code/up` - one of the commands the plugin provides.

#### C) Trigger a database migration by visiting the Control Panel URL
{#c-trigger-a-database-migration-by-visiting-the-control-panel-url}

After applying updates on your fortrabbit Craft App, you might see a "Service unavailable" message. Visit the control panel URL `{{app-env-id}}.frbit.app/admin` or whatever you have set) and you might see a message saying that database changes need to applied. Click the "apply" button to run the migration manually.

#### D) Manually run database migrations on the App via Craft CLI
{#d-manually-run-database-migrations-on-the-app-via-craft-cli}

You can trigger the changes via the Craft CLI in the terminal via [SSH](#ssh-access):

```shell
## After being logged in to the environment
{#after-being-logged-in-to-the-environment}
php craft migrate/all
php craft project-config/apply
```

---

## Running a headless Craft CMS on fortrabbit
{#running-a-headless-craft-cms-on-fortrabbit}

Craft can be used as a headless CMS. Here is how to on fortrabbit.

### Intro
{#intro-3}

With Craft CMS headless mode you have a Craft CMS installation that consists only of the backend without any server-side Twig templates. In addition you create another application, usually with a JavaScript framework (Next, Nuxt, React, Vue …) that will fetch content using the built-in GraphQL API and render it on the client-side in the browser.

### Headers
{#headers}

By default HTTP responses with content type `text/html`, `text/css` and `text/javascript` are gzipped. When you use Craft in headless mode as a GraphQL or REST API, the content type is application/json. In the article about [GZIP compression](#gzip-with-htaccess) you learn how to enable it for other content types.

### Related
{#related-2}

- [Headless considerations](#headless-hosting-workflows)
- [Craft CMS help on headless mode](https://craftcms.com/docs/getting-started-tutorial/more/graphql.html)

---

## Using Craft CMS plugins
{#using-craft-cms-plugins}

We highly recommend to not install plugins directly on your production environment. Instead install plugins locally first, then deploy that state to get them installed on the environment as well.

### Install Craft plugins from the control panel
{#install-craft-plugins-from-the-control-panel}

This method let's you conveniently discover, install and also "activate" (pay for) the plugins right in place.

1. Visit the control panel of your local Craft installation
2. Visit the plugin store
3. Search, install and activate plugins

Plugins installed via the plugin store are "pinned" with `composer.json` and must also be updated through the same mechanisms. Please also see our [updating instructions](#updating-craft-cms).

### Install Craft plugins via command line
{#install-craft-plugins-via-command-line}

This is a more advanced method to install plugins directly from the command line:

```shell
## 1. Add the plugin to Composer:
{#1-add-the-plugin-to-composer}
$ composer require {vendor/package-name}

## 2. Install the plugin via Craft CLI
{#2-install-the-plugin-via-craft-cli}
$ ./craft plugin/install {plugin-handle}
```

Plugins installed that way can be updated with `composer update` later on. Please also see our updating instructions.

### Using image tuning plugins
{#using-image-tuning-plugins}

Image uploads to Craft are usually getting processed by ImageMagick. Image transformations happen when original images are sized down into several delivery formats. That happens during upload for display in the Craft Control Panel but also in your templates when you want to show those images to the users. Nowadays with image media queries like `srcset` one needs not only two sizes (thumbnail and large) but all kind of different sizes for different device resolutions. Please keep in mind that image transforms are "expensive" in terms of CPU utilization. Best don't overdo it. Use only as much as you'll need. Maybe four sizes per image are enough, for the imager plugin that can be four steps. The image format `webp` is supported with fortrabbit's imageMagick version.

#### jpegoptim and company
{#jpegoptim-and-company}

[Some people suggest](https://nystudio107.com/blog/creating-optimized-images-in-craft-cms) further optimizing images with jpegoptim or optipng. These tools are not available here on fortrabbit. We advise using dedicated specialized third party image optimization services, like imgix, tinypng, kraken to do the job best.

### Plugins VS performance
{#plugins-vs-performance}

In our experience, some plugins are over-engineered, bloated. That can result in considerable performance degradation. Consider using light weight plugins that are easy to combine and manage. Consider not using too many plugins.

### Plugins VS updates
{#plugins-vs-updates}

Craft CMS changes. Not plugin developers will follow the Craft CMS update path. It might well be that you can not update your Craft CMS installation because of plugins missing updates. Yet again, consider using only required plugins.

---

## Craft CMS queue jobs
{#craft-cms-queue-jobs}

Craft CMS uses queue jobs for long-running tasks. By default these jobs are processed by a web based ajax call which blocks PHP processes that are meant for site delivery. In the worst case scenario the queue runner consumes all PHP resources. Luckily there are more robust solutions available.

The most common use case is image transformations.

### Worker jobs
{#worker-jobs}

Run long running processes in a isolated environment without hurting site delivery. The [jobs component](#jobs) allows you to create a [worker job](#workers) to run in the background.

1. Make sure the jobs component is booked
2. Set up a job with this Craft command: `php craft queue/listen -v`
3. Remove `runQueueAutomatically` from `config/general.php` to disable the standard queue

### Alternatives
{#alternatives-6}

Another approach is to use a **poor mans worker**: The Async Queue plugin from our co-founder Oliver is just that. For many queue workloads the `ostark/craft-async-queue` plugin can mitigate performance problems without the need of an extra component and further configuration.

- [github.com/ostark/craft-async-queue](https://github.com/ostark/craft-async-queue)
- [plugins.craftcms.com/async-queue](https://plugins.craftcms.com/async-queue)

---

## Craft CMS domain setup
{#craft-cms-domain-setup}

fortrabbit environments come with a testing URL. At some point you will very likely add your own domains.

For general information on how to add domains to your fortrabbit App, please see our [domains article](#the-domain). For Craft CMS be sure to have set your domain's root path to the `/web` folder.

When installing Craft locally, it will ask you which domain you want to use. This local domain differs form the one you want to use in production. That's why it is stored in the `PRIMARY_SITE_URL` ENV var. The installer creates this ENV var in the .env file. In your fortrabbit production environment you may need to set `PRIMARY_SITE_URL` using the ENV var settings of your App.

Craft CMS uses `@web` alias internally when it deals with HTTP requests. Unless you define it, Craft will try to figure it out based on HTTP headers - which is not always possible. It's good practice to define it explicitly using `PRIMARY_SITE_URL` ENV var.

```php
return [
  // Recommended aliases in config/general.php
  'aliases' => [
    '@web' => \craft\helpers\App::env('PRIMARY_SITE_URL') ?: '/',
    '@webroot' => dirname(__DIR__) . '/web'
  ],
];
```

You can also add multiple domains. From the fortrabbit side, just point them to the App's root path, configure routing and display of contents within Craft CMS and/or use additional [htaccess rules](/3.dev/htaccess).

### Multi site domain settings
{#multi-site-domain-settings}

For multi-site setups, you may need to hard-code the domains for each environment. Here is an example of that:

```php
return [
  // fortrabbit (multi site)
  'production' => [
    'siteUrl' => [
      'en' => '//www.site.com',
      'nl' => '//www.site.nl',
    ],
  ],
  // local (multi site)
  'dev' => [
    'siteUrl' => [
      'en' => '//en.site.dev',
      'nl' => '//nl.site.dev',
    ],
  ],
];
```

---

## Craft CMS troubleshooting
{#craft-cms-troubleshooting}

Tips, tricks, best practices and advanced topics on how to run Craft CMS successfully on fortrabbit.

### Common errors with initial setup
{#common-errors-with-initial-setup}

Here are some common errors, the cause of 90% of failing Craft CMS installations here:

- **Mismatching Security Key** — Make sure to have the same key with your local development environment and on your fortrabbit environment.
- **Wrong database configuration** - Make sure your fortrabbit database is using the ENV vars provided by the fortrabbit Dashboard to connect to the fortrabbit database in production. Leave your `.env` file at home as it will be ignored anyway. See our [ENV vars](#env-vars-intro).
- **Missing table prefix** - You might have a table prefix locally, some users do this locally to have multiple installations in one big database. To distinguish between them you can set up a table prefix. You can do this with an environment variable: locally you set that with your `.env` file, in fortrabbit via the Dashboard.
- **Missing .htaccess file** — Commonly happens with SFTP upload. The `.htaccess` file is hidden, make sure to copy it over as well.

### Temporarily turning on/off dev mode
{#temporarily-turning-on-off-dev-mode}

The production environment will not print errors. When a runtime exception occurs, you will presented with the very basic "Service Unavailable" error screen. This is to prevent visitors of your website from seeing any information about the system and the errors. One thing you can do, is temporarily setting DevMode to true, so that you can see the error output printed on screen. We advise against doing it, unless it is a non-production environment.

### Large assets upload problems
{#large-assets-upload-problems}

Most likely this is a setting within Craft CMS itself. The setting you are looking for is `maxuploadfilesize` and its default is 16MB, please see the official Craft Docs on that. This can also be caused by the `post_max_size`, `memory_limit`, `upload_max_filesize` or `max_execution_time` settings, which you can configure in the dashboard, but by default those are OK. If that still doesn't help, check the [logs](#logs) to see if you can find some meaningful errors.

---

## Craft CMS guides
{#craft-cms-guides}

Install, deploy, develop and tune Craft CMS on fortrabbit.



---

## Kirby intro
{#kirby-intro}

Kirby CMS is a flat file content management system from Germany. Learn about deployment options and workflows.

### Understand flat file systems
{#understand-flat-file-systems}

Unlike [WordPress](#wordpress-quick-setup-guide) or [Craft CMS](#install-craft-cms-local) Kirby is a file based CMS. So there is no database, the actual contents are markdown text files written on the file system. Other flat file systems are [Grav](#grav-install-guide) and [Statamic](#install-statamic). In general, this design approach makes things more easy, but also has some gotchas.

### License model
{#license-model}

Kirby CMS is open source, but not free software. You can test it for free. Support the authors and the longevity of the project by obtaining a license for production.

### Deployment options
{#deployment-options}

Special consideration should be taken when deploying Kirby CMS. We assume you have a [local development environment](#intro-to-local-development-with-php) running. Now from time

- [Git + rsync deployment](#deploy-kirby-with-git-and-rsync) - advanced, sophisticated, recommended
- [rsync sync](#sync-kirby-with-rsync) - advanced, quick
- SFTP upload - easy peasy, see [general SFTP article](#sftp-access)

---

## Sync Kirby with rsync
{#sync-kirby-with-rsync}

Deploy Kirby CMS on fortrabbit using rsync.

### Get ready
{#get-ready-19}

Our recommendation is to use a [combination of Git and rsync](#deploy-kirby-with-git-and-rsync) where code is deployed via Git and the content folder is synced down (and up) by rsync. But you can also deploy the whole project using rsync as well. Upload code changes and download content changes.

### Local installation
{#local-installation}

It is recommended to have a [local development environment](#intro-to-local-development-with-php). Here is a quick guide on how quickly get the Kirby plainkit running locally without Git from your terminal:

```shell
## Make a directory and move into it
{#make-a-directory-and-move-into-it}
$ mkdir {{app-env-id}} && cd {{app-env-id}}

## Get the plainkit
{#get-the-plainkit}
$ wget https://github.com/getkirby/plainkit/archive/main.zip

## Unzip the plainkit
{#unzip-the-plainkit}
$ unzip main.zip

## Move all contents from the folder one level up
{#move-all-contents-from-the-folder-one-level-up}
$ mv plainkit-main/* .

## Remove artifacts
{#remove-artifacts}
$ rm -rf main.zip plainkit-main

## Make the site locally available
{#make-the-site-locally-available}
## This uses valet, there are other tools too
{#this-uses-valet-there-are-other-tools-too}
$ valet link

## After that you can see the page locally
{#after-that-you-can-see-the-page-locally}
## http://{{app-env-id}}.test
{#http-app-env-id-test}
```

See the [official Kirby docs quick start installation](https://getkirby.com/docs/guide/quickstart#installing-kirby). There are many more ways to do it.

### Deployment
{#deployment}

```shell
## UP: from local to remote
{#up-from-local-to-remote}
$ rsync -av ./ {{app-env-id}}@ssh.{{region}}.frbit.app:

## DOWN: from remote to local
{#down-from-remote-to-local}
$ rsync -av {{app-env-id}}@ssh.{{region}}.frbit.app: ./
```

See the [rsync article](#rsync-deployment) for more details.

### The vendor folder
{#the-vendor-folder}

When syncing the whole project folder, the vendor folder will be synced along. In most cases this works surprisingly well. Keep in mind that the local development environment and the software versions of the local PHP environment and the fortrabbit remote should roughly match for that to work. It's possible to run `composer install` with the fortrabbit environment. A better alternative is to use Git deployment and automate composer with [build commands](#build-commands).

---

## Deploy Kirby with git and rsync
{#deploy-kirby-with-git-and-rsync}

This is yje recommended workflow to deploy Kirby using Git. It's a bit more advanced, but worth the mile when maintaining a project.

### Get ready
{#get-ready-20}

- Read the [Kirby Composer guide](https://getkirby.com/docs/guide/install-guide/composer) from the official Kirby docs.
- Have a [local development environment](#intro-to-local-development-with-php) including PHP and Composer running.
- Have an Account with fortrabbit and GitHub.
- Install the [fortrabbit GitHub app](#the-fortrabbit-github-app) at GitHub.

### Rundown
{#rundown}

1. Install Kirby locally
2. Start Git and integrate with GitHub
3. Connect your GitHub repo with fortrabbit
4. Synchronize contents with rsync

- - -

### Install Kirby locally with Composer
{#install-kirby-locally-with-composer}

```shell
## 1. Create a local (on your computer) Kirby project folder with Composer:
{#1-create-a-local-on-your-computer-kirby-project-folder-with-composer}
$ composer create-project getkirby/plainkit {{app-env-id}}
```

Kirby offers a "starterkit" (with some demo contents and a theme with some templates) and a "plainkit" with no contents at all (which is used here). There is also the "composerkit" which has a different folder structure.

Maybe you also have a project running locally and are just looking for ways to deploy that. Continue with the next steps.

#### Configure Kirby for git deployment with rsync
{#configure-kirby-for-git-deployment-with-rsync}

Open your local Kirby project folder with your text editor or IDE. Open the (hidden) `.gitignore` file at the top level to tell Git to ignore some folders. Add these three ignore rules if not already present:

```shell
## .gitignore
{#gitignore}

## Kirby itself
{#kirby-itself}
/kirby

## Composer dependencies
{#composer-dependencies}
/vendor

## Stuff you are creating
{#stuff-you-are-creating}
/content
```

The setting above will also keep the `/content` folder out of Git. This is our opinionated way of doing it for this workflow. It will help keeping your repo tidy by separating code from content. But you will need to run dedicated rsync commands to deploy and update the "contents" (see below). You can also decide to not touch the `.gitignore` so that you can deploy everything with Git all together.

At this point you should be able to run the project in your local development environment already. We highly recommend to develop the site locally, use fortrabbit for staging and production.

### Init Git and add GitHub
{#init-git-and-add-github}

See the [git deployment intro](#deployment-intro) to get an idea how to connect a local repo to the GitHub remote and enable automatic deployment by installing the [fortrabbit GitHub App](#the-fortrabbit-github-app) with GitHub account.

Here is an example creating a repo from your local code base and using git command line and [GitHub CLI](#github-cli) to setup a local repo, and connect it to .

```shell
## Setup local git repo
{#setup-local-git-repo-1}
$ git init
$ git add -A
$ git commit -am 'Init'

## GitHub CLI to create/connect remote Git repo
{#github-cli-to-create-connect-remote-git-repo-1}
$ gh repo new
## Follow the steps
{#follow-the-steps-1}
## Push an existing local repository to github.com
{#push-an-existing-local-repository-to-github-com-1}
## Add as remote and assign current branch as 'origin'
{#add-as-remote-and-assign-current-branch-as-origin-1}
```

At the end, the Git repo at GitHub is created and content already pushed. From now on you only need to run add, commit and `git push` to send code changes to GitHub.

### Connect your GitHub repo with fortrabbit
{#connect-your-github-repo-with-fortrabbit-1}

Now, the last step is to setup and connect an app on fortrabbit. Start the process in the fortrabbit dashboard:

:BlockLink{title="Create a new (free trial) app" path="/new/app"}

Choose Kirby as software preset. Use Git deployment and select the Git repo that you have created previously. At the end the end of the process, start the first deployment and lean back. At this stage you have deployed a semi broken Kirby installation. That's because the content is missing. Let's fix this with the next step.

If you already created an (new empty) app at fortrabbit, connect the repo branch through settings.

### Synchronize contents
{#synchronize-contents}

As mentioned, deployment of code (templates and configuration) and dependencies (Kirby and Composer) is done via Git deployment. Deploying the content is a separate step. We recommend to use rsync to upload or download new contents to and from your remote fortrabbit environment. See also our [rsync article](#rsync-deployment). On your local computer in the Terminal in the kirby project folder execute:

```shell
## SYNC UP: from local content folder and it's files to remote
{#sync-up-from-local-content-folder-and-it-s-files-to-remote}
$ rsync -av ./content/ {{app-env-id}}@ssh.{{region}}.frbit.app:content/
```

It works also the other way around. For example in a case, where you have done some edits online and want those changes to be reflected in your local development environment:

```bash
## SYNC DOWN: from files from remote content folder to local folder
{#sync-down-from-files-from-remote-content-folder-to-local-folder}
$ rsync -av {{app-env-id}}@ssh.{{region}}.frbit.app:content/ ./content/
```

You can also use [SFTP](#sftp-access) to synchronize the `content` folder.

### Going forward
{#going-forward}

From now on you can `git push` to trigger a [deployment](#the-deployment-object) to fortrabbit via GitHub.

---

## Tune Kirby
{#tune-kirby}

Tune the popular blogging and CMS engine WordPress on fortrabbit.

### Working with the panel
{#working-with-the-panel}

Kirby - like other CMS - has a "Panel". It enables you - or maybe the client/editor - to create and edit the contents easily in the browser. You can create different users (admins) for the Panel. When first visiting the Panel, locally, you are greeted to set up the first admin user.

The panel users are by default NOT stored with Git. So your local users will not available on the fortrabbit App. You can now either include the users with Git by removing the relevant lines from `.gitignore` or - maybe better - set up the users locally and on the remote environment.

#### Setup panel
{#setup-panel}

Kirby does not let you set up the Panel by default on public-facing servers, see [create your Kirby first account](https://getkirby.com/docs/guide/quickstart#create-your-first-account). If you upload your contents before setting up the panel and want to use the panel on the server, rather than locally, you need to [enable the `panel.install` option](https://getkirby.com/docs/reference/system/options/panel#allow-the-panel-to-be-installed-on-a-remote-server).

### Updating Kirby
{#updating-kirby}

We recommend updating your local development environment first. On your local computer enter `composer update` in the terminal at the root level of the project folder to trigger the update. When you have confirmed that everything works, `git push` to push the latest updates to fortrabbit.

### Caching
{#caching}

We highly recommend to turn on Kirby's native page caching. This is how you can enable it with the config file:

```php
// /site/config/config.php
return [
  'cache' => [
    'pages' => [
      'active' => true,
    ]
  ]
];
```

If the config file does not exist, create it. Check the [official Kirby caching guides](https://getkirby.com/docs/guide/cache) for more options and a video.

### Sending mails
{#sending-mails}

fortrabbit does not support `sendmail`, so sending mails out of the box might not work. Kirby provides config for transactional mail providers, or you can use a plugin to send e-mail over your own SMTP account.

---

## Kirby guides
{#kirby-guides}

Install, deploy, run and tune Kirby CMS on fortrabbit.



---

## Install Statamic
{#install-statamic}

Learn here how to install Statamic locally and prepare it to be deployed to fortrabbit.

### Get ready
{#get-ready-21}

Have a [local development environment](#intro-to-local-development-with-php) with PHP and a web server ready.

### Install Statamic locally
{#install-statamic-locally}

**Recommended approach**: Before you deploy anything to fortrabbit, get your Statamic project running on your local computer. Please see the [official Statamic install guide](https://statamic.dev/installing/local) for up-to-date instructions. It boils down to something like this:

```shell
## Install the Statamic CLI
{#install-the-statamic-cli}
composer global require statamic/cli

## Create a new Statamic project
{#create-a-new-statamic-project}
statamic new {project_folder_name}
```

It would also be good to already have your first admin user set up.

### Install Statamic on the server
{#install-statamic-on-the-server}

Another option is to install Statamic directly on the environment like so:

1. Login to an environment by [SSH](#ssh-access)
2. Run the above steps to install a Statamic project
3. Move all files in `{project_folder_name}` one level up again

We believe it's better to start with a local development environment first. A local first approach is easier for Git + rsync deployments too.

### Add your magic
{#add-your-magic-2}

Installing a plain Statamic will not do much. Now add your templates, design and content to make it shine.

### Setup GitHub
{#setup-github-1}

**Optional**: To enable git deployments later on, init git and add GitHub as remote repo - either as a public or private.

- [Deployment intro](#deployment-intro)
- [Git intro](#git-intro)

---

## Statamic deployment options
{#statamic-deployment-options}

Learn here how to install Statamic on fortrabbit.

### Get ready
{#get-ready-22}

- Have a [local development environment](#intro-to-local-development-with-php) with PHP and a web server ready.
- Have [Statamic installed locally](#install-statamic).

### Deployment workflow introduction
{#deployment-workflow-introduction}

There are two "main" ways to deploy code here on fortrabbit: [Git](#deployment-intro) and [SFTP](#sftp-access). The general rule of thumb is, that content driven legacy applications, like [WordPress](#wordpress-quick-setup-guide), are better uploaded in classical manner with SFTP. Modern PHP web frameworks that are based on [Composer](#composer) are mostly deployed with Git.

Now, Statamic is a bit in between and is - like [Grav](#grav-install-guide) and [Kirby](#kirby-intro) - file based. So there is usually no database, the actual contents are text files written on the file system.

Files you can access via SFTP or SSH are not the exact ones that are in Git. The Git repo is a separate thing. This means that deploying with [Git is a one way street](#git-works-only-one-way) that only goes up. In other words: You can NOT `git pull` any changes you have made on the environment's file system. In an ideal world, code and content are maybe separated. With a file based CMS this is all together.

### Deployment options
{#deployment-options-1}

Here are three ways to get your code up (and down):

#### 1 - SFTP upload
{#1-sftp-upload}

There is not much to say on that topic. Just make sure to upload all contents of your local Statamic folder, including the hidden `.htaccess` file into the `htdocs` folder within your environment. Consider using [rsync](#rsync-deployment) to sync all contents all up and down.

#### 2 - Git + rsync workflow (recommended)
{#2-git-rsync-workflow-recommended}

Manage template code with Git and content with rsync. Instructions [over here](#deploy-statamic-with-git-and-rsync).

#### 3 - Git experimental workflow
{#3-git-experimental-workflow}

Feeling adventurous? Use Git on the App to be able to push/pull contents. Instructions [over here](#statamic-git-experimental-deployment-workflow).

---

## Deploy Statamic with Git and rsync
{#deploy-statamic-with-git-and-rsync}

Learn here our recommended way to deploy Statamic with Git and rsync on fortrabbit. You'll deploy to fortrabbit using Git (and Composer) and (optionally) synchronize contents with rsync.

### Get ready
{#get-ready-23}

You should have Statamic running on your local machine, have a good understanding of Git and rsync, have an App on fortrabbit ready. Read our [Statamic intro](#install-statamic) first.

### Configure Statamic for Git with rsync
{#configure-statamic-for-git-with-rsync}

Open your local Statamic project folder with your text editor or IDE. Within it open the `.gitignore` file at the root level to tell Git to ignore all content. We need to add any folders to `.gitignore` which contain user-generated content:

```shell
…
## Exclude stuff you are creating from Git
{#exclude-stuff-you-are-creating-from-git}
/content
/users
/resources/blueprints
/resources/fieldsets
/resources/forms
/resources/users
/storage/forms
/public/assets
```

PLEASE NOTE: This is our recommended way of doing it. It separates code from content. You will need to run dedicated rsync commands to deploy and update this user-generated content (see below). You can also decide to not touch the `.gitignore` file so that you can deploy everything with Git all together. Keep in mind that you can not pull in new contents from the fortrabbit App this way (see on work-flows above).

At that point you should be able to run the project in your local development environment already. We highly recommend developing the site locally, using fortrabbit for staging and production.

### Deploy Statamic with Git
{#deploy-statamic-with-git}

In case you haven't already, set up Git, configure a Git repo as a remote and push the code. See our [deployment intro article](#deployment-intro) for more details on Git here on fortrabbit.

### Synchronize content with rsync
{#synchronize-content-with-rsync}

As mentioned above, deployment of your code base (templates and configuration) and dependencies (Statamic and Composer) is done via Git deployment. Deploying the content is a separate step. We recommend using rsync to up- or down-load new contents to and from your remote fortrabbit App (see also our [rsync article](#rsync-deployment)). On your local computer in the terminal in the Statamic project folder execute:

```shell
## SYNC UP: from local to remote
{#sync-up-from-local-to-remote}
$ rsync -avR ./content ./users ./resources/blueprints ./resources/fieldsets ./resources/forms ./resources/users ./storage/forms ./public/assets {{app-env-id}}@ssh.{{region}}.frbit.app:/
```

(You may not have all these folders on your local system: Only include folders which you do have.)

It works also the other way around. For example, if you have some edits done online and want them to be reflected in your local development environment:

```shell
## SYNC DOWN: from remote to local
{#sync-down-from-remote-to-local}
$ rsync -av '{{app-env-id}}@ssh.{{region}}.frbit.app:/content ./
$ rsync -av '{{app-env-id}}@ssh.{{region}}.frbit.app:/users ./
$ rsync -av '{{app-env-id}}@ssh.{{region}}.frbit.app:/resources/blueprints ./
$ rsync -av '{{app-env-id}}@ssh.{{region}}.frbit.app:/resources/fieldsets ./
$ rsync -av '{{app-env-id}}@ssh.{{region}}.frbit.app:/resources/forms ./
$ rsync -av '{{app-env-id}}@ssh.{{region}}.frbit.app:/resources/users ./
$ rsync -av '{{app-env-id}}@ssh.{{region}}.frbit.app:/storage/forms ./
$ rsync -av '{{app-env-id}}@ssh.{{region}}.frbit.app:/public/assets' ./
```

---

## Statamic tuning
{#statamic-tuning}

By now, you hopefully have a Statamic installation running on your local machine and you can easily deploy it to your fortrabbit App. You can deploy code changes with Git and/or rsync. Let's dig deeper!

### Adding domains
{#adding-domains}

At the beginning you have probably been using the App URL as your domain. You can also add any number of domains to your App. Please see our [domain articles](#the-domain) for more.

### Environment variables
{#environment-variables}

Statamic comes with a predefined `.env` file. It includes what you'll need to run Statamic locally. Bear in mind that the `.env` is ignored in Git.

If you have not chosen Statamic as the [software preset](#software-templates) for the app, you may need to set some environment variables. Go to your environment in the dashboard, and under settings find "ENV vars". You will be presented with a textarea to put in your "Custom ENV vars". Have the same APP_KEY locally and on the App (copy from your local installation).

```shell
APP_KEY=(copy what you have locally)
APP_ENV=production
APP_DEBUG=false
APP_URL=https://{{app-env-id}}.frbit.app
```

Please also see the [ENV vars topic](#env-vars-intro) to learn more about this kind of configuration and implementation at fortrabbit.

### ENV vars for Statamic MySQL setup
{#env-vars-for-statamic-mysql-setup}

MySQL access will be configured via ENV vars as well. Copy/paste this additional setup into the environment variables form in the fortrabbit Dashboard:

```env
DB_CONNECTION=mysql
DB_DATABASE=${MYSQL_DATABASE}
DB_HOST=${MYSQL_HOST}
DB_PASSWORD=${MYSQL_PASSWORD}
DB_PORT=3306
DB_USERNAME=${MYSQL_USER}
```

It maps the keys Statamic is expecting to dynamic ENV vars provided by fortrabbit.

### Root path
{#root-path-1}

This setting again is only required if you have not chosen Statamic with the software preset. Statamic is a Laravel application. So the root path needs to be set to `public`. This should be set already if you have chosen the Laravel software preset.

:BlockLink{title="Set the root path" path="/environemnts/{{app-env-id}}/settings/root-path" text="dashboard.com/environments/{{app-env-id}}/settings/root-path"}

### Working with the Control Panel
{#working-with-the-control-panel}

Statamic - like other CMS's - has a control panel. That dashboard enables you - or maybe the client/editor - to create and edit the contents easily in the browser. You can create different users (admins) for the control panel.

- `{{app-env-id}}.frbit.app/cp`

For this, please consider how you are dealing with the content created:

- You should really not use the control panel on the App if you have all content stored in Git: you should only change things locally.
- When using rsync (or SFTP) you can sync changes you have made on the App directly back down or the other way around.
- When using MySQL as a data store, you might want to dump the production database and bring it back locally from time to time

### Using the Statamic CLI
{#using-the-statamic-cli}

Statamic has an installer CLI, which can be installed as a global composer package. You can use that on the environment, but it is not recommended to do so. Install Statamic locally, then deploy.

- [statamic.dev/installing/local](https://statamic.dev/installing/local)

### Continuous development
{#continuous-development}

We recommend to always develop locally first — it's just the most convenient way. Deploy when you have reached a certain state of development. In many cases the "real" content will be created on the fortrabbit App. You can easily sync down changes from production into development with rsync or sftp unless you have the content in MySQL.

### Backups
{#backups-2}

[Backups](#backups) are available as an optional component. You can also spin your own solution. With Git you can already easily roll back changes.

### Updating Statamic
{#updating-statamic}

We recommend updating your local development environment first. On your local computer execute `composer update` in the terminal at the root level of your project folder to trigger the update. When you have confirmed that everything works, `git push` to bring the latest updates to your fortrabbit App.

### Sending mails
{#sending-mails-1}

fortrabbit does not support `sendmail`, so sending e-mails out of the box might not work. Statamic provides config for transactional mail providers, or you can use a plugin to send e-mail over your own SMTP account.

### Getting a license
{#getting-a-license}

Remember that Statamic is free for personal use. For a client project, get a license, support the authors!

---

## Statamic Git experimental deployment workflow
{#statamic-git-experimental-deployment-workflow}

Here is an adventurous Statamic Git deployment workflow.

<!-- TODO: review again, or maybe drop for now.  -->

This is an advanced, opinionated and VERY experimental (not well tested) workflow for experienced developers to deploy Statamic, where all content is stored as files and managed with Git using the Statamic Git Automation. See the [Git Automation Statamic docs article](https://statamic.dev/git-automation) (Pro feature) to get the idea and as reference.

### Concepts
{#concepts-1}

It's kinda like a two way git binding. Usually git works as a one way street at fortrabbit.

Create a repo on the environment, which has the same upstream as your local repo. We create a new branch because we do not want to push changes to the main branch to avoid a deployment loop and to keep code and content separated. Then, any changes we make to content on the environment can be pulled into your local repo, where it can be merged back into main.

```raw
┌───────────────────────┐
│  fortrabbit app env   │
└──────▲─────────┬──────┘
       │         │
     main     content
       │         │
┌──────┴─────────▼──────┐
│        GitHub         │
└──────▲─────────┬──────┘
       │         │
     main     content
       │         │
┌──────┴─────────▼──────┐
│   local development   │
└───────────────────────┘
```

### Get ready
{#get-ready-24}

- Statamic running on your local machine
- a good understanding of Git and rsync
- an app with environment on fortrabbit, see [Statamic topic](/2.guides/5.statamic/) too

### 1 - Local preparation
{#1-local-preparation}

1. Install Statamic on your local computer as described above.
2. Follow our [GitHub guides](#the-fortrabbit-github-app) to connect to GitHub and enable automatic deployment

Once finished you `git push` to deploy, so that Statamic will be installed with the environment on fortrabbit.

### 2 - Get Statamic Pro
{#2-get-statamic-pro}

The Git Automation is part of the commercial Statamic version. You need to enable the Pro version and obtain a Statamic license to use that feature on fortrabbit. See the [official guide](https://statamic.dev/licensing) on how to do that. As usual, do this with your local installation first and then push the latest state to fortrabbit. After this, you should be able to find Git with the utilities under the Statamic control panel.

### 3 - Set ENV vars in the fortrabbit dashboard
{#3-set-env-vars-in-the-fortrabbit-dashboard}

Add the environment variables listed below to the environment with the fortrabbit dashboard.

```shell
STATAMIC_LICENSE_KEY=your-site-license-key
STATAMIC_GIT_ENABLED=true
STATAMIC_GIT_AUTOMATIC=true
```

### 4 - Prepare Git on the environment
{#4-prepare-git-on-the-environment}

Login to your fortrabbit environment by SSH and:

1. Set up an SSH key with SSH keygen (no passphrase), see our [SSH keys setup guide](#ssh-key-setup)
2. Copy the content of the public key (likely `.ssh/id_ed25519_fortrabbit.pub`) to a buffer
3. Add the public key to GitHub so you can push from the environment

### 5 - Init Git on the environment
{#5-init-git-on-the-environment}

We create a separate branch to deployment loops when pushing and to separate code from content. SStill logged in by SSH on the fortrabbit environment.

First add a `.gitignore` file. Its contents should be the same as the `.gitignore` file on your local project. Then:

1. Initialise a new Git repo: `git init`.
2. Create a Git user (see example below)
3. `git add .` & `git commit -m 'initial commit'`
4. Create an `editorial` branch and check it out (`git checkout -b 'editorial'`)
5. Add the GitHub repo as remote

```shell
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

See the [Statamic Git guide](https://statamic.dev/git-automation#remote-setup) and the [fortrabbit git guide](#deployment-intro) as reference.

### 6 - Try it out
{#6-try-it-out}

Still logged in by SSH you should be now able to add and commit files with Git to the App and push changes to the deploy service remote from the `editorial` branch.

When pushing for the first time, set the remote as an upstream. To get this new branch locally fetch new branches from the GitHub remote.

With the Git repo on your local computer you can fetch and checkout the `editorial` remote branch. Pull changes from there and merge them back into your `main` branch that you are using for development.

### 7 - Git in the Statamic Control Panel
{#7-git-in-the-statamic-control-panel}

Now you can also use the Statamic Git Automation, depending on the setup, pending editorial changes are visible with the online Git editor in the Statamic control panel or get committed and pushed automatically (we advise using the recommended delay).

---

## Statamic guides
{#statamic-guides}

Install, deploy, run and tune Statamic on fortrabbit.



---

## WordPress quick setup guide
{#wordpress-quick-setup-guide}

Install the popular blogging and CMS engine WordPress on fortrabbit.

We assume you've already created an [app](#the-app) and chose WordPress in the [software template](#software-templates). In the following, you will install WordPress directly on the environment. We do not recommend to use [git deployment](#deployment-intro) since, WordPress is not ready for it yet.

### Install WordPress
{#install-wordpress}

Open your terminal app of choice, login to the environment by SSH, directly download WordPress like so:

```shell
## 1. Login to your environment via SSH
{#1-login-to-your-environment-via-ssh}
$ ssh {{app-env-id}}@ssh.{{region}}.frbit.app

## Once you are logged in:
{#once-you-are-logged-in}

## 2. Download latest WordPress
{#2-download-latest-wordpress}
$ wget https://wordpress.org/latest.tar.gz

## 3. Unpack wordpress
{#3-unpack-wordpress}
$ tar zxf latest.tar.gz

## 4. Move unpackged files to top level
{#4-move-unpackged-files-to-top-level}
$ mv wordpress/* .

## 5. Remove the downloaded container
{#5-remove-the-downloaded-container}
$ rm -r wordpress latest.tar.gz
```

### Run the installer
{#run-the-installer}

Once the upload is finished:

:BlockLink{title="Visit test domain" path="https://{{app-env-id}}.frbit.app" property="none"}

Commence with the guided web installation to finish the setup. See the dashboard to look up your database credentials. The installer will also ask you for your WordPress site's Site title, User name, Password, Your email and so on. After the guided web setup is done, you will be automatically redirected to the WordPress admin login form. Use the previously chosen credentials to login.

### Installing themes & plugins
{#installing-themes-plugins}

These are pretty standard operations. You can download and update themes directly from the WordPress admin. Or you can create your own, test them locally, then upload them to your remote themes folder. The same applies to plugins.

---

## Tune WordPress
{#tune-wordpress}

Tune the popular blogging and CMS engine WordPress on fortrabbit.

### Adding a custom domain
{#adding-a-custom-domain}

Your test domain `{{app-env-id}}.frbit.app` is the first address your WordPress can be reached from. Later on, when you go live, you will add your own custom external domains. Here is the basic setup:

1. Register and route the domain to the environment < see [domain article](#the-domain)
2. Connect the domain to your fortrabbit environment, so that requests for a new domain will be delegated
3. Once the domain is routed, tell WordPress to use the new domain as well:

#### Changing the site_url domain in the wp-admin
{#changing-the-site-url-domain-in-the-wp-admin}

In the WordPress admin change the Site URL from your App URL to that new domain. Find this setting in wp-admin under Settings > General: "WordPress Address (URL)" and "Site Address (URL)". Change this to your new domain. More advanced help regarding domains and the vars `home_url` and `site_url` can be found in the Wordpress codex article on [changing the Site URL](https://wordpress.org/support/article/changing-the-site-url).

### Database migration
{#database-migration}

WordPress consists of code files, the user generated uploads and of course the [MySQL database](#mysql), in which most of the contents are stored. There are various use cases to export and import the database:

1. Export the database from your old web hosting
2. Export your local database to import it to the fortrabbit database
3. Export the remote database from fortrabbit to bring your local installation up-to-date

Read the [MySQL export / import guides](#database-export-import).

### Deploying WordPress changes with rsync
{#deploying-wordpress-changes-with-rsync}

Sophisticated developers might have a look at rsync. It's many times faster than SFTP. See our [rsync article](#rsync-deployment).

### Using the WP-CLI
{#using-the-wp-cli}

<!-- TODO: Review by infra. Will we have wp-cli? -->

You can also use the popular and handy WordPress Command Line Interface on your fortrabbit App. When logged in to your fortrabbit App via SSH, you can just issue this command:

```shell
wp
```

The first time you call this will install it, next time you can just use it. See a [list of commands here](https://developer.wordpress.org/cli/commands).

### Running WordPress in a sub folder
{#running-wordpress-in-a-sub-folder}

There are two reasons to install WordPress in a sub directory instead of in `htdocs`:

1. WordPress is just the blog-part of the website: `mydomain.com/blog`
2. You want to run multiple WordPress sites in one environment. Please don't.

You can achieve the first option by putting WordPress in a folder and by changing the "Site Address URL" parameter (see above). Also see the official WordPress codex on how to [give WordPress it's own directory](https://wordpress.org/support/article/giving-wordpress-its-own-directory).

---

## Update WordPress
{#update-wordpress}

Update popular blogging and CMS engine WordPress on fortrabbit.

There are many ways to deploy and develop WordPress. Depending on your work-flow, the way you'll update WordPress and deploy the update might be different. Minor patch versions of WordPress might be updated automatically.

With WordPress, except when using [Bedrock](https://roots.io/bedrock) or the like, most likely you will just use the update functionality provided by the WordPress admin. Log in to `wp-admin`: when an update is available, it will inform you and display an "update" button you can click. That will trigger the update. See also the [official WordPress docs on updating](https://wordpress.org/support/article/updating-wordpress).

### Update locally first
{#update-locally-first}

We recommend to have a [local development environment](#intro-to-local-development-with-php) and do the updates locally first and then deploy the changes to fortrabbit. That way you can make sure that everything works in development before doing something in production. While updating the WordPress core, it's likely that the database design will change. The update script will do a migration, converting the tables to the new design while keeping their contents. When you run the installer in your local development and then deploy the new files only, the database version and the file versions do not match. Most likely you will see a warning in "wp-admin" to run the migration from there.

### Parallel updates
{#parallel-updates}

To avoid migration struggles you can also keep your local and your remote version of WordPress in sync by running the updates in both environments, one by one. You might start with the local version and when successful, run the installer again on the environment itself.

### Updating plugins and themes
{#updating-plugins-and-themes}

So far we have covered updating the WordPress core, but WordPress wouldn't be WordPress without the eco-system of themes and plugins. Those can and have to be updated as well. The same mechanisms as above apply.

### Keeping your environments in sync
{#keeping-your-environments-in-sync}

WordPress is a **C**ontent can be **M**anaged in that **S**ystem. So in consequence that means that content is likely to be added and edited on the system — the environment — itself. This content could be blog posts, pages and also media like images. Maybe you are adding them, maybe the client, maybe the editors. Now, if you have been following our recommendation to have a local development environment. WordPress stores the text content of posts and pages in the MySQL database, uploads are stored on the file system. So you need to sync two things:

1. For the **database**, check our [MySQL article for import/export](#database-export-import).
2. For the **files** you can either use [SFTP](#sftp-access) or have a look at [rsync](#rsync-deployment) to synchronize certain folders.

The techniques described work in both directions. Most likely you want to get the newest contents from the environment into your local development environment, but maybe have you local changes that you would like to see on the environment as well.

---

## Secure WordPress
{#secure-wordpress}

Urgent security advice: WordPress is popular with hackers. You are responsible to keep the software you install up-to-date.

The good news is that WordPress has automatic background updates and they are enabled by default. Please check the article from the official WordPress codex on how to [configure automatic background updates](https://wordpress.org/support/article/configuring-automatic-background-updates) and take care that your WordPress core, plugins and even themes are always [up-to-date](#updating-wordpress).

### Protect against bots
{#protect-against-bots}

WordPress often gets targeted by bots, trying to access `wp-login.php` and `xmlrpc.php`. Blocking access to these files will increase stability and security.

### Sending e-mails
{#sending-e-mails}

You cannot use [sendmail](#mailing) on fortrabbit but you can use a SMTP plugin like [WP SMTP](http://wordpress.org/plugins/wp-smtp) or [MAIL SMTP](http://wordpress.org/plugins/wp-mail-smtp) to enable SMTP support for the `wp_mail()` function.

### Resetting your password for wp-admin
{#resetting-your-password-for-wp-admin}

Some users might be too lazy to configure the mail delivery for WordPress via SMTP (see above). Now imagine they also forget the password for `wp-admin`. Without email, the forgot password function from WordPress will not work. The user can still set a new password in the database. Like so:

1. Connect to the remote MySQL database from local
2. Browse the MySQL tables to find the right admin user
3. Choose a safe password
4. Convert that password to a MD5 hash
5. Update the table with the new password
6. Go back to wp-admin and login using the new password

### Running WordPress in a sub folder
{#running-wordpress-in-a-sub-folder-1}

There are two reasons to install WordPress in a sub directory instead of in `htdocs`:

1. WordPress is just the blog-part of the website: `mydomain.com/blog`
2. You want to run multiple WordPress sites in one environment. Please don't.

You can achieve the first option by putting WordPress in a folder and by changing the "Site Address URL" parameter (see above). Also see the official WordPress codex on how to [give WordPress it's own directory](https://wordpress.org/support/article/giving-wordpress-its-own-directory).

---

## WordPress guides
{#wordpress-guides}

Install and run WordPress on fortrabbit.



---

## Drupal guide
{#drupal-guide}

Drupal is a free and open-source content management system. Learn how to install and run Drupal on fortrabbit.

::CallOut{alert}
This is work in progress. We are still learning about Drupal. Let us know if something is odd.
::

### Get ready
{#get-ready-25}

It's assumed you've already created a new app and chose Drupal in the [software template](#software-templates). If not: You can do so in the fortrabbit dashboard. You should have a [local PHP development environment](#intro-to-local-development-with-php) running on your local machine. Drupal has good backward compatibility and this guide should work for Drupal 9, 10, and 11. We recommend following the [official Drupal installation guide](https://www.drupal.org/docs/installing-drupal) to install Drupal locally first. Here is an idea how to do it with Composer:

```shell
## Create a new Drupal project with Composer
{#create-a-new-drupal-project-with-composer}
composer create-project drupal/recommended-project my-drupal-site

## Navigate to the project directory
{#navigate-to-the-project-directory}
cd my-drupal-site

## Install Drupal via Composer (alternative method)
{#install-drupal-via-composer-alternative-method}
composer install
```

We recommend to use DDEV for local development. See their [Drupal quick start](https://docs.ddev.com/en/stable/users/quickstart/#drupal-drupal-11).

### Root path
{#root-path-2}

If Drupal was chosen or detected when creating the environment in the dashboard, 'web' was pre-selected as the root path. You can configure the [root path](#root-path) in the dashboard.

:BlockLink{title="Change the root path for {{app-env-id}}" path="/environments/{{app-env-id}}/settings/rootpath"}

### MySQL configuration
{#mysql-configuration-1}

If Drupal was chosen or detected, required environment variables for the MySQL connection will be pre-populated.

:BlockLink{title="Change the ENV vars for {{app-env-id}}" path="/environments/{{app-env-id}}/env-vars"}

### Deployment
{#deployment-1}

Drupal supports Git and Composer workflows. Deploy via GitHub using our [GitHub integration](#the-fortrabbit-github-app) via `git push`. SSH/SFTP code access is also available too.

#### Git ignores
{#git-ignores}

By the time of this writing, it appears that Drupal does not ship with a standard `.gitignore` file. It's suggested to create such a file on the root directory of the project, matching your requirements.

- [drupal.org/project/drupal_cms/issues/3500134](https://www.drupal.org/project/drupal_cms/issues/3500134) - Issue
- [github.com/github/gitignore/blob/main/Drupal.gitignore](https://github.com/github/gitignore/blob/main/Drupal.gitignore) - Example

#### Git deployment workflow
{#git-deployment-workflow}

1. Set up your local Drupal project with Git
2. Deploy to GitHub
3. Install the [fortrabbit GitHub App](#the-fortrabbit-github-app)
4. Connect your GitHub repository to your fortrabbit app environment
5. Push to deploy automatically

The [build commands](#build-commands) will automatically run `composer install` during deployment when using our Drupal software template.

#### Initial deployment steps
{#initial-deployment-steps}

1. Create your Drupal project locally
2. Initialize Git and make your initial commit
3. Push your code to your GitHub repository
4. Deploy to fortrabbit via GitHub integration
5. Import your database (see MySQL section below)
6. Run Drupal installation via SSH or upload your database

### Files and uploads
{#files-and-uploads}

Drupal stores uploaded files in the `sites/default/files` directory by default. For production sites, consider:

#### Using rsync for file management
{#using-rsync-for-file-management}

You can use [rsync](#rsync-deployment) to sync files between your local development and fortrabbit:

```shell
## Download files from fortrabbit to local
{#download-files-from-fortrabbit-to-local}
rsync -av {{app-env-id}}@ssh.{{region}}.frbit.app:web/sites/default/files/ ./web/sites/default/files/

## Upload files from local to fortrabbit
{#upload-files-from-local-to-fortrabbit}
rsync -av ./web/sites/default/files/ {{app-env-id}}@ssh.{{region}}.frbit.app:web/sites/default/files/
```

### Environment variables
{#environment-variables-1}

When Drupal is detected or chosen, important environment variables for connecting to the database should be pre-configured. Set these environment variables in your fortrabbit dashboard:

:BlockLink{title="Edit ENV vars for {{app-env-id}}" path="/environments/{{app-env-id}}/env-vars/edit"}

#### Additional ENV vars
{#additional-env-vars}

- `DRUPAL_HASH_SALT`: A unique hash salt for your Drupal installation
- `APP_URL_HOST`: Your domain name (automatically set)
- Other custom variables as needed for your modules

### Logs
{#logs-1}

Check your Drupal logs via the admin interface at `/admin/reports/dblog` or access system logs in the [fortrabbit dashboard](#logs).

### Manual database settings
{#manual-database-settings}

Drupal uses a `settings.php` file to configure database connections. When using our software template, the database configuration is automatically handled via environment variables. Your `web/sites/default/settings.php` should include:

```php
// Database configuration using fortrabbit environment variables
$databases['default']['default'] = [
  'database' => $_ENV['MYSQL_DATABASE'],
  'username' => $_ENV['MYSQL_USER'],
  'password' => $_ENV['MYSQL_PASSWORD'],
  'host' => $_ENV['MYSQL_HOST'],
  'port' => $_ENV['MYSQL_PORT'] ?? '3306',
  'driver' => 'mysql',
  'prefix' => '',
  'collation' => 'utf8mb4_general_ci',
];
```

For your local development setup, you can create a `settings.local.php` file with your local database credentials.

---

## October CMS guide
{#october-cms-guide}

### Get ready
{#get-ready-26}

Make sure to have a [local development environment](#intro-to-local-development-with-php) up and running. Use the detailed [official October install guide](https://docs.octobercms.com/3.x/setup/installation.html) as your guideline to install October CMS on your local machine first. October CMS is based on Laravel, please have a look at our [Laravel guides](#install-laravel-locally) as well.

#### MySQL configuration
{#mysql-configuration-2}

If you have chosen October or Laravel in the [software preset](#software-templates) when creating your app, we will automatically populate the "right" environment variables for the MySQL connection. So **you don't need to set anything**! Just keep `config/database.php` as it is. The all CAPITAL configs in the `config/database.php` file will be replaced by the contents of the environment variables. For your local development setup you can populate the `.env` file with your local database credentials. See the [ENV var topic](#env-vars-intro).

### User sessions
{#user-sessions-1}

There are various session drivers available in Laravel: see a [full list here](https://laravel.com/docs/session#configuration). Read further to see which ones are most suitable for your App. Whichever driver you end up using, you will need to specify it in the environment variables. Add a new ENV var `SESSION_DRIVER` in the Dashboard and give it the appropriate value.

Since environments have persistent storage, you are able to use the default `file` driver for sessions. You can of course also use the other options specified in the [Laravel session docs](https://laravel.com/docs/session#configuration).

To use the `database` driver, follow these steps:

```shell
## Create a migration for the session table  - locally
{#create-a-migration-for-the-session-table-locally-1}
$ php artisan session:table

## Apply the migration - locally
{#apply-the-migration-locally-2}
$ php artisan migrate

## Add, commit and push the migration file
{#add-commit-and-push-the-migration-file-2}
$ git add .
$ git commit -m "session migration"
$ git push

## Run the migration on the App via SSH remote execution
{#run-the-migration-on-the-app-via-ssh-remote-execution-2}
$ ssh {{app-env-id}}@ssh.{{region}}.frbit.app php artisan migrate --force
```

### Sending mail
{#sending-mail-2}

You can not use [sendmail](#mailing) on fortrabbit but Laravel provides an API over the popular SwiftMailer library. The mail configuration file is `app/config/mail.php`, and contains options allowing you to change your SMTP host, port, and credentials, as well as set a global form address for all messages delivered by the library.

---

## Grav install guide
{#grav-install-guide}

Grav is a popular, free, file based CMS based on Twig & Markdown. Learn here how to install and tune Grav on fortrabbit.

### Quick start
{#quick-start}

We usually advice to run [your project locally](#intro-to-local-development-with-php) and use [Git deployment](#deployment-intro). Since Grav CMS is a static file content management system where files may change on the environment, we can not advice to use git deployment, since it is designed to work as a one way street.

### SFTP installation guide
{#sftp-installation-guide}

1. Download the "latest Grav Core + Admin plugin" from the [Grav website](https://getgrav.org/downloads) from the Grav website and unpack it locally.
2. Copy all **contents** of the local `grav-admin` folder (not the folder itself) via [SFTP](#sftp-access) to the `htdocs` folder of your environment.

<!-- When the upload is finished, visit [\{\{app-env-id\}\}.frbit.app](https://{{app-env-id}}.frbit.app) in your browser and commence with the guided web installation to finish the setup. -->

Once upload is done, commence with the guided web installation to finish the setup.

:BlockLink{title="Visit test domain" path="https://{{app-env-id}}.frbit.app" property="none"}

Consider to use [rsync](#rsync-deployment) to sync changes up and down.

### Environment configuration
{#environment-configuration}

Grav allows you to [configure different settings based on the domain](https://learn.getgrav.org/advanced/environment-config) it is served from. For example, if you are developing your Grav site locally, you probably want the debugging enabled while you want it to be disabled, when serving the environment from fortrabbit. To that end, you can create domain specific configurations. All you need to do is create a new `system.yaml` configuration file for you custom domain. Say the domain you are using is `www.my-grav.tld`, you would create the file `user/www.my-grav.tld/config/system.yaml`, in which you then set:

```yaml
debugger:
  enabled: false
```

An even better approach is set your `user/config/system.yaml` as restrictive as possible while using a special localhost configuration in `user/localhost/config/system.yaml`, which enables debugging and so on:

```yaml
debugger:
  enabled: true
```

---

## Symfony guide
{#symfony-guide}

Symfony has been around for some while — but it doesn't look old. Install and tune Symfony on fortrabbit.

### Get ready
{#get-ready-27}

You should have a [local PHP development environment](#intro-to-local-development-with-php) running on your local machine.

### Install Symfony locally
{#install-symfony-locally}

Follow the [official Symfony guides](https://symfony.com/doc/current/setup.html) to create a local installation of Symfony if you not already have one.

Symfony has good backward compatibility, usually not introducing break changes, this guide most likely works for older versions as well. This can be an existing project or a new one, see the [official download page](https://symfony.com/download) for instructions for your local Operating System.

Given that fortrabbit uses Apache as a web server, consider fetching the default `.htaccess` file for Symfony. This can easily be done through (confirm the installation of the flex recipe by pressing `y`):

```shell
composer require symfony/apache-pack
```

### Setup GitHub
{#setup-github-2}

**Optional but recommended**: To enable git deployments later on, init git and add GitHub as remote repo, either as a public or private.

- [Deployment intro](#deployment-intro) - concepts on fortrabbit
- [Git intro](#git-intro) - new to Git?

### Create an app at fortrabbit
{#create-an-app-at-fortrabbit-2}

Create a new app in the fortrabbit dashboard. The wizard will guide you through the steps. You can connect the repo from GitHub.

:BlockLink{title="Create a new app" path="/new/app"}

### Root path
{#root-path-3}

If you did not choose Symfony when creating the environment in the dashboard at first, please set the following: Go to the dashboard and set the [root path](#root-path) to 'public'.

:BlockLink{title="Change the root path for {{app-env-id}}" path="/environments/{{app-env-id}}/settings/rootpath"}

### ENV vars
{#env-vars}

Symfony [environments](https://symfony.com/doc/current/configuration.html#configuration-based-on-environment-variables) are controlled by the `APP_ENV` ENV var. You can even use ENV vars in the .yml configurations now. To get you started quickly, we provide you with the following ENV vars by default when you have chosen the Symfony from when creating the App:

```shell
APP_ENV=prod
APP_DEBUG=0
APP_SECRET=SECRET
DATABASE_URL=mysql:host=${FORTRABBIT_MYSQL_HOST};port=3306;dbname=${FORTRABBIT_MYSQL_DATABASE}
```

[ENV vars](#env-vars-intro) can be changed with the dashboard. Modify `APP_DEBUG` or `APP_ENV` to change the behavior of your application.

:BlockLink{title="Edit ENV vars for {{app-env-id}}" path="/environments/{{app-env-id}}/env-vars/edit"}

### Git deployment
{#git-deployment-2}

See the [GitHub app](#the-fortrabbit-github-app) guide on how to connect fortrabbit to your Git repo.

### MySQL
{#mysql-1}

The database should be configured out of the box.

### Doctrine & symfony console
{#doctrine-symfony-console}

#### Deployments through GitHub
{#deployments-through-github}

The build and post-deploy commands should be detected by fortrabbit and provide sensible defaults.

Here is what we automatically set up for you:

- Build commands:

```
composer install --no-dev --prefer-dist --no-interaction --no-ansi --no-progress
```

We also add node dependencies installation and build if detected:

```
npm install
npm run build
```

- Post-deploy commands:

- 'php bin/console cache:clear'
- 'php bin/console assets:install public'
- 'php bin/console doctrine:migrations:migrate'

#### Non-git deployment
{#non-git-deployment}

You may want to run migrations and maybe load fixtures on the instance. You can login via [ssh](#ssh-access) in to your environment, or instead just fire single commands like so:

```shell
## doctrine
{#doctrine}
$ ssh {{app-env-id}}@ssh.{{region}}.frbit.app 'php bin/console doctrine:migrations:migrate'
$ ssh {{app-env-id}}@ssh.{{region}}.frbit.app 'php bin/console doctrine:fixtures:load'

## cache clear
{#cache-clear}
$ ssh {{app-env-id}}@ssh.{{region}}.frbit.app 'php bin/console cache:clear'
```

You can also add this migrate command to your `composer.json` to have it run automatically every time you push changes.

```json
"scripts": {
  "post-install-cmd": [
    "php bin/console doctrine:migrations:migrate --no-interaction",
  ],
}
```

With that in place, any time you deploy your code, database changes will be applied immediately. If no database changes are required, nothing happens, so it is safe to run all the time. Just make sure to test your upgrades and migrations locally first.

### Tailwind usage
{#tailwind-usage}

Unfortunately [TailwindBundle](https://symfony.com/bundles/TailwindBundle/current/index.html) uses [Tailwind CLI](https://tailwindcss.com/docs/installation/tailwind-cli) which is not currently compatible with our service.

You can instead use [Symfony Encore](https://symfony.com/doc/current/frontend/encore/installation.html) to install Tailwind.

```
composer require symfony/webpack-encore-bundle
npm install && npm install -D tailwindcss postcss postcss-loader autoprefixer @tailwindcss/postcss
```

Add this part in `webpack.config.js`:

```js
    // enable PostCSS loader
    .enablePostCssLoader()
```

Create the following `postcss.config.js` file in the root directory:

```js
module.exports = {
  plugins: {
    '@tailwindcss/postcss': {},
    autoprefixer: {},
  },
};
```

And finally add these lines to your `app.css` file:

```css
@import 'tailwindcss';
@source "../../templates";
```

Since we detect node configuration this should then be deployed without any change of your configuration.

### Symfony installer
{#symfony-installer}

The symfony docs suggest to download a Symfony installer CLI. You can not do that on the remote environment. Do that in your local development environment.

- [symfony.com/download](https://symfony.com/download)

### Logging
{#logging-3}

You can access all log files with the dashboard.

### Sending emails
{#sending-emails}

You can not use [sendmail](#mailing) on fortrabbit but you can use the `Swiftmailer`. Symfony provides a Mailer component that makes things easy. To configure the way your emails are sent, mind setting a `MAILER_DSN` environment variable. More on this in the [official documentation](https://symfony.com/doc/current/mailer.html).

---

## Typo3 guide
{#typo3-guide}

Typo3 has been around for some while. Here are some details running Typo3 on fortrabbit.

### Get ready
{#get-ready-28}

We assume you've already created a new app and chose Typo3 in the [software template](#software-templates). If not: You can do so in the fortrabbit dashboard.

You should also have a [local PHP development environment](#intro-to-local-development-with-php) running on your local machine. Typo3 has good backward compatibility, usually not introducing break changes, this guide most likely works for older versions as well.

We recommend following the [official Typo3 install guides](https://docs.typo3.org/m/typo3/reference-coreapi/main/en-us/Administration/Installation/Install.html) to install Typo3 locally first. You can start with composer like so:

```shell
composer create-project typo3/cms-base-distribution example-project-directory "^13"
```

### Root path
{#root-path-4}

If you have chosen Typo3 when creating the environment in the dashboard at first, 'public' was pre-selected as the root path. If you have a different root path, go to the dashboard and set the [root path](#root-path) to .

:BlockLink{title="Change the root path for {{app-env-id}}" path="/environments/{{app-env-id}}/settings/rootpath"}

### MySQL
{#mysql-2}

Typo3 does not support ENV var based MySQL connection out of the box. We recommend to extend your Typo3 installation to use ENV vars for database access. [ENV vars](#env-vars-intro) can be changed with the dashboard.

:BlockLink{title="Edit ENV vars for {{app-env-id}}" path="/environments/{{app-env-id}}/env-vars/edit"}

The other solution is to run the web installer after the Typo3 code base has been deployed. This will alter configuration files directly.

### Deployment
{#deployment-2}

Typo3 supports git driven applications and composer driven workflows. So you can deploy it via GitHub. See the [GitHub app](#the-fortrabbit-github-app) guide on how to connect fortrabbit to your Git repo. Do yourself a favor and use ENV vars for database access when using Git deployment. SSH and SFTP are also available.

---

## Other CMS & frameworks
{#other-cms-frameworks}

What else you may want to install here.

- [Pyro CMS](https://pyrocms.com)
- [CakePHP](https://cakephp.org)
- [Typo3](https://typo3.org)
  - [Neos](https://www.neos.io)
- [Slim](http://www.slimframework.com)
- [CodeIgniter](https://www.codeigniter.com)
- [Laminas](https://getlaminas.org)
- [Phalcon](https://phalcon.io) - beginning with version 6
- [Drupal](https://www.drupal.org)

---

## Software guides overview
{#software-guides-overview}

We pride ourselves to know a bit about the software you are running here. Check out our intensive installation and usage guides.



---

## Guides
{#guides}

How to run popular PHP software on fortrabbit.



---

## Intro to website performance
{#intro-to-website-performance}

Slow websites suck but are a reality. Website speed matters for your users, for SEO and your budget.

### No silver bullets
{#no-silver-bullets}

A common misconception is that a powerful web server alone will make a website run fast. 'Buy a fast server' is naive and wrong advice, we think.

<!-- :ContentQuote{text="Throwing more money at a problem will rarely fix problems."} -->

While we provide scalable hosting services, it's important to understand that simply adding more hosting power won't necessarily improve performance. Effective performance requires understanding and coding skills. You, the web developer, have most responsibility when it comes to website performance. Good code can fly.

### Not all websites are alike
{#not-all-websites-are-alike}

Your milage may vary. For some websites or individual pages, an execution time of 500 ms might be acceptable, while for others it might not be. Individually built websites have unique performance patterns as well. We support a wide range of different applications using software systems such as Laravel, Symfony, Craft CMS, WordPress and many more.

---

## People problems
{#people-problems}

Most performance problems are people problems. Developers often overlook performance design until real issues appear.

### Daily drama
{#daily-drama}

Support requests from customers complaining about server errors asking us to fix it (immediately) are our daily reality.

<!-- :ContentQuote{text="My site has crashed. Please fix ASAP!"} -->

We get it. The website may suddenly return a [504 server error](#504). That looks like something is odd with the hosting. Maybe nobody touched the code for months, it has been running like this for months. Now suddenly an issue pops up. Then suddenly an issue appears, causing confusion, shame and strong emotions.

Our job is to explain that this is typically not an infrastructure problem, but an application issue. In most cases, we can help clients identify what's causing their problems. This can be a delicate situation. Sometimes business owners contact us after their web developer told them to do so. We then ask them to contact their developer again so the developer can work with us directly.

### Responsibility
{#responsibility-1}

We run the infrastructure. You are responsible for the code you write and deploy. That's essentially what our terms of service state. We believe it's important to separate responsibilities clearly – there need to be clear, distinctive rules.

This separation can be challenging. We often work with freelancers and website creators who excel at creating good designs, managing clients, and configuring content management systems. However, performance optimization requires deeper insights into underlying technical processes. Performance should never be treated as an afterthought.

We aim to help us much as we can. Case by case.

---

## Common performance issues
{#common-performance-issues}

The following performance issues are happening often. Compare with your project setup and issues.

### Misconfiguration
{#misconfiguration}

Configuration errors are among the most common causes of performance issues. These problems often stem from development settings being used in production, improper caching configurations, or conflicting plugins and extensions. What works fine during development can become a major bottleneck when deployed to a live environment with real traffic and data volumes.

- All assets are re-generated with each deployment or even page load
- The production environment is set to development
- A plugin creates a ton of load or conflicts with other config
- Slow MySQL queries

### External sources
{#external-sources}

Modern applications rarely exist in isolation - they depend on external APIs, CDNs, payment processors, and other third-party services. When these external dependencies experience issues, your application's performance suffers as a direct consequence. A single slow external service can create cascading delays throughout your entire application.

- A third party service is down or slow

### Data threshold reached
{#data-threshold-reached}

Applications that perform beautifully during development and testing can hit performance walls when they encounter real-world data volumes. What seems fast with a few hundred test records can become painfully slow with thousands of production records. This is one of the most surprising issues for developers.

- A MySQL query that is fast locally with little testing data, is slow in production

### Usage patterns changed
{#usage-patterns-changed}

Maybe the number of visitors has increased, or how people and even bots are interacting with a project. User behavior and traffic patterns are constantly evolving, and applications that were designed for certain usage assumptions can struggle when those patterns change. Sudden traffic spikes, different user workflows, or unexpected bot activity can expose performance weaknesses that weren't apparent under normal conditions. These changes often happen gradually until they cross a critical threshold, making the performance degradation seem sudden.

- A website was linked from a popular blog and get's more visits
- A new user is uploading images of a larger size
- Bots are aggressively curling all pages

---

## Monitoring & metrics
{#monitoring-metrics}

Identify common slow website culprits. How to uncover performance related problems, at best before issues appear.

### Experience website speed yourself
{#experience-website-speed-yourself}

Your website is slow? Feel it! Common signs of performance issues are:

- Pages are slow to load - the browser loading icon spins
- You see timeout errors - a [504 error](#504) printed on screen

### Check the browser dev tools
{#check-the-browser-dev-tools}

Open the dev tools of your browser and use the performance related tools provided to measure and identify the source of the problems. The network tab is a good starting point. You can do a performance test like Lighthouse too. The dev tools can help to distinguish between frontend and backend related performance issues.

### Check the hosting metrics
{#check-the-hosting-metrics}

The fortrabbit dashboard offers a metric section (your hosting provider likely will have something similar) including the following vital data points:

- **PHP response time**: Aim for less than 250ms on average. In our experience, it's more likely that a website with an average high response time will have problems. Slow websites that are getting some more visits than usual are tending to break down (504) faster.
- **5xx error metric**: See if there are any peaks in 5xx errors. If there are, see if at the same time, the PHP response time went up, in that case those 5xx errors are likely 504 time out errors.
- **Memory usage**: The memory used should not come to close to the hosting resources you have booked on average, 80% average usage and single peaks are Ok.
- **Memory swap usage**: Swap is when there is no (fast) RAM available anymore and data needs to be accessed from disc (slow). This should be within bounds, which depends on your website.
- **OpCache**: This should usually not max out. Aim for 80% or less. Higher values are usually not a problem.

---

## Backend performance best practices
{#backend-performance-best-practices}

Performance design makes websites run fast - from development to production, from backend to frontend. Do it for your wallet, your users and the environment.

We want you to encourage to **design for performance** and scalability. And that is all about thinking a bit ahead. Speed matters for your users and for SEO. You - the responsible PHP developer - may have more responsibility than you think.

### Time to first byte
{#time-to-first-byte}

The TTFB depends on how fast the service can compute. Your code plays a major role. Also see the [PHP processes article](#php-processes) to learn about limits when executing PHP. See our [understand performance article](#monitoring-metrics) on how to analyze backed performance problems.

#### Prepare to cache
{#prepare-to-cache}

If you begin developing, you might not instantly utilize a pair of multi gigabyte Redis servers. Still: make sure to implement caching early on and to use abstraction, so you can later on switch to those caching machines when you need them. Available caching solutions on fortrabbit:

- File: Disk storage is not very fast.
- Database: Faster than disk. Use if you need to cache data for a long time.
- APC: Aside from opcode caching which happens automatically, you can use APC as an object cache very similar to Memcache or Redis.
- Valkey: Modern key value im memory caching service

#### Reduce I/O
{#reduce-i-o}

It's always a good idea to reduce file input/output operations on the disk to the minimum. In PHP this means:

- **PHP includes**: Reduce amount of includes as much as possible. Always use absolute path names, which reduces the amount of lookups.
- **Avert files**: Don't use file-sessions, file-caches or anything `file-*`, if you can replace it with an in-memory cache or even the database.
- **Outsource static files**: Put your static files on an object storage. Sure, they could be delivered very fast from local, but still, they will create I/O which your (PHP) App will be missing.
- **Shrink your loader chain**: Make sure you load only the classes (files) you need. For a production App (in which code changes do not occur often) you can set `apc.stat` or `pcache.validate_timestamps` to `0`, which reduces I/O on `.php` files even further, but requires an APC/OPcache flush for changed files to apply.

#### Decouple, but loosely
{#decouple-but-loosely}

Leverage the power of the cloud: Span your App across multiple services. If you need image or video encoding: use an external service for this. If you want to send mass mails: use an external service for this. Why? Because it balances the load of your App and thereby gives it more resources for each individual task it has to perform.

However, if one of those external service (temporarily) breaks, make sure you can switch it off in seconds! You still want your shopping basket to run, if your image transformation has a problem.

#### Prepare for CDN
{#prepare-for-cdn}

If you're planning on growing large and expect a lot of traffic, you will end up putting your static files (images, videos, css and js files, ...) behind a Content Delivery Network. Nowadays, you can do this pretty effortless with specialized services. Some services work best with a dedicated (sub)domain for your static contents, such as _img.yourdomain.com_. If you expect to use them in the future, you should implement the required structure from the start. Also a good precaution is to setup your cache headers properly from the start.

#### Database considerations
{#database-considerations}

Very common: check your JOIN queries! If they ran fast when your dataset was small, it doesn't mean they still do with a bigger dataset. Utilize caches to buffer costly databases results. Database optimization could easily fill a whole book — or books. Read our [dedicated MySQL performance tips](#database-performance-tips).

#### Static file separation
{#static-file-separation}

Sure, a request to a static file can be delivered faster than a request handled by a dynamic script - nonetheless, the more static requests are performed by your App, the more it has to do overall. More is more in the end. If you split up the traffic in dynamic and static requests, by utilizing a cloud hosting service, all the requests for static files are not handled by your App anymore but by another server somewhere else. Resulting, your App on fortrabbit acts as the motor for your PHP scripts, while a host dedicated to delivering static files takes care of the rest.

#### Profile your code
{#profile-your-code}

Web applications are usually fast after the launch, but degrade over time. They receive more requests and process more data. You add more features and at some point everything or some parts of your app become slow. Profilers give you deep insights of your code and all dependencies that are involved to handle requests. XDEBUG profiler and XHPROF are the defacto open source standard, but you need additional tools to visualize the data. The [blackfire profiler](#blackfire) makes it really easy to start profiling in minutes.

#### Use load testing
{#use-load-testing}

We advise to put your website under some controlled stress to see when it will break. There are tools you can use from your computer to fire up a couple of simultaneous requests. This way you can see how the website will behave before your first unlucky visitors will find the bottleneck for you.

#### Reduce max execution time
{#reduce-max-execution-time}

This is an opinionated topic. If you come from searching 504 time out errors, you will often read to increase the `max_execution_time` setting to allow a certain process to finish it's task.

By the way: You can adjust this setting with your environment under "PHP settings" in the dashboard.

In some cases that makes sense, but it's often a poor design decision. Image transformations with imageMagick are often long running, therefore you might want to increase the execution time to avoid time outs. But, as stated here often: long running tasks should best be separated from the frontend tasks into the background. With the [jobs](#jobs) component you can outsource jobs.

Frontend requests should always return a swift answer. The number of PHP processes is limited. When all PHP processes are occupied with long running tasks, new requests need to wait. That can easily pile up. A lower max execution time limit often results in faster errors. And that's often what you want. When making an API call to an external service, usually that reply should be there within a second, how long should you wait for it max? Maybe 10 seconds is reasonable. It's not likely that there will be an answer when you wait longer.

So for most cases, short is better.

#### Block and limit bots
{#block-and-limit-bots}

A lot of web traffic is generated by crawling bots. There are bad ones and good ones. Did you know: A wrongly configured navigation plugin can cause a bot to get stuck in a loop visiting an endless number of pages within your website. This can cause high load, traffic and ultimately spam your template caching folder.

Enable our [WAF feature](#incoming-firewall-waf).

Set a crawl delay to limit unnecessary crawling of your website if it is not updated very frequently. The craw-delay directives in `robots.txt` are supported by good bots such as search engines, commercial bots, SEO bots.

### Swap issues
{#swap-issues}

In some cases swap usage by the application is not possible. In these cases you might see dreaded white-pages and along going error messages in the log: "Allowed memory size of 1234.. bytes exhausted (tried to allocate 234 bytes)." This should be understand as an urgent reminder to scale up the [PHP plan](#php).

---

## PHP processes
{#php-processes}

This is a deep dive into PHP processes and response time, how it correlates with perceived page speed.

### PHP processes
{#php-processes-1}

Unlike frontend JavaScript, which is usually running in the web browser, PHP scripts are executed on the web server, and the output is then usually delivered to the web page as HTML. A PHP FPM process is a reserved computing resource - think CPU. Each PHP process can respond to one concurrent PHP request at a time.

fortrabbit utilizes FPM (FastCGI Process Manager). Unlike with php-cgi the PHP FPM process stays alive. Besides the allocated PHP memory, a number of persistent FPM PHP processes is spawned with each plan. See the [PHP component article](#php).

### PHP memory requirements
{#php-memory-requirements}

How much memory your website will require depends on multiple factors. Let's start with the theory:

- Extensions: Each enabled PHP extension must be loaded into memory.
- PHP libraries: You most likely are using Composer to manage your dependencies. This implies a set of PHP files which need to be interpreted and loaded into memory - specifically into the OPcache.
- PHP code: The code you write yourself consumes memory in the OPcache as well. The more code you have, i.e. the more functions and complexity, the more memory is required.
- Runtime variables: In each request your App fills variables (`$foo = "bar"`), which consumes memory. How much it will use depends on the amount of data used in variables. You can measure how much you are by calling [memory_get_peak_usage()](http://php.net/manual/en/function.memory-get-peak-usage.php).

Now, the memory used by extensions and OPcache is shared. This means: If you run an app on a single process and use 10 MB OPcache, then you will also only use 10 MB of OPcache with two processes. The memory consumed by runtime variables is not shared. It's hard to pre-calculate the expected memory usage.

The tricky part is the data size. Say you have a blog with comments using a database. Now rendering a small blog entry with no comments will utilize less memory than rendering a large blog entry with thousands of comments. Or does it? Well, it really strongly depends on your design and actual code. For example, you could load all of the thousands of comments into a PHP array and then render the site or you could load them one by one and print them out immediately - both would have a different impact on memory. In general the memory usage will change over the lifetime of your App - expect it to increase with growing data size.

### PHP processes, PHP requests, PHP response time
{#php-processes-php-requests-php-response-time}

- By design PHP requests should only take a very short time to execute.
  - If it takes longer, it's likely your code is slow. Refactor it for performance!
- Aim for 250 ms or less on average.
  - Our dashboard shows you PHP response time metrics.
- A new incoming PHP request will have to wait if all PHP processes are busy.

#### A simple example
{#a-simple-example}

- Your App has 2 PHP processes
- 1 PHP request takes 500 ms to execute (PHP response time)
- So each PHP process can handle 2 PHP requests per second
- Since there are 2 PHP processes, the App can deliver 4 PHP requests in 1 second

#### A bad example
{#a-bad-example}

- Your environment has booked 4 PHP processes
- 1 PHP request commonly takes 1000 ms (1 second) - which is too long
- 1 page view of your website creates 3 PHP requests
- 3 website visitors at the exact same time can bring the website down

### PHP processes VS page views
{#php-processes-vs-page-views}

Page views refer to a single request made by a user to view a page on a website. This request will likely involve a number of HTTP requests, such as images, HTML, CSS, and JavaScript files, all of which must be downloaded from the Apache web server.

A page view will likely also require the server to execute any PHP scripts associated with the page, which translates into one PHP process for each PHP script.

For many websites the ratio between page view and PHP request is one to one. But often one page view will generate multiple PHP requests, for instance by making different AJAX calls to the backend to query the database, returning API requests, or transforming images.

### PHP processes VS max execution time
{#php-processes-vs-max-execution-time}

Sometimes clients ask us in support to increase the `max_execution_time`. While this might help to execute long-running tasks, this also blocks PHP processes for a longer time. See the examples above. That's why we usually recommend lowering the time it takes to execute PHP to be able to serve your website to your visitors simultaneously.

### TTFB and PHP response time
{#ttfb-and-php-response-time}

For web server performance "PHP response time" is an important metric. It can be roughly translated to the Time To First Byte, which also includes network latency effects. Most websites should be able to attain a "PHP response time" of 250ms or even less. This is possible with attention to best practices.

---

## Frontend performance best practices
{#frontend-performance-best-practices}

Are you a full-stack developer? A lot of delivery can be optimized in the front facing side of your application. Let's have a look what can be done on the last meters and how to optimize content efficiency.

### JS & CSS
{#js-css}

Assets are static files, such as JS, CSS, SVG and some images. It's common to have two versions of your asset files:

- the original files, that you can edit, probably SASS, POSTCSS, TS … (included in Git)
- the optimized files that are served in production (usually not included in Git)

Minifying JS/CSS files removes unnecessary extra spaces, line breaks and indentations. Modern tools support tree shaking as well. Another technique is to combine — concating — different JS or CSS files into one file. This brings you: less requests and probably better GZIP compression ratios. Finally, there are specific techniques to further reduce size: For JS, variable names can be changed automatically for shorter ones, in CSS you can use shorthands and short notations of colors and values.

You can hook in Node.js pipelining tasks during [deployment build steps](#build-commands).

### Images
{#images}

Images (JPG, PNG, SVG, WebP …) represent around 70% of the total footprint of an average website. Most images are user generated content, for example when an editor uploads a photo to a CMS. Invest some time to tune your image transformations. Deliver only required sizes to the website visitor. Try different compression settings and even image formats. Consider using a third party service to host images, if your website needs a lot or if it has many visitors or you need to serve large versions og images.

### Videos
{#videos}

Our [traffic tiers](#traffic) are not designed to host local videos. It's recommended to outsource video hosting to a 3rd party. That will also help with compression and delivery.

### Web fonts
{#web-fonts}

Web fonts are nice but they also come with a footprint. The file size is determined by the number of glyphs, metadata and compression. On top of that, there are four different formats and you probably need to include all to have the best coverage. External services can help to optimize font size and delivery.

### Caching assets
{#caching-assets}

Don't serve the same content to the same client twice. Cache it with their browser. While modern browsers are already doing great work here. You can further control the caching by altering the Cache-Control with the HTTP headers.

GZIP provides lossless compression for
text files such as HTML, CSS or JS. It's implemented on the web server — Apache in our case otherwise nginx — as a module. You can enable and configure it in your `.htaccess` file (see also our [htaccess GZIP article](#gzip-with-htaccess).

It works like this: after all the HTML is rendered on the server side it gets compressed and send to the browser in such a minified format. The browser then has to decompress everything on the fly. So as you can imagine: that of course saves bandwidth but also costs a little bit of CPU on both sides. It is in general recommended to use it but can cause strange effects when combined with other techniques, like caching.

### Cookies
{#cookies}

Eat diet Cookies! Cookies are sent in the HTTP headers in every single request, always. Use a different domain for serving static assets can help to reduce the cookie traffic.

### DNS lookups
{#dns-lookups}

You might parallelize downloads across host names. This may help speed up delivery, but if the number of host names is too long the time that the client spends to resolve the domain can affect negatively. The concurrent connections of web browsers is limited.

### Check your speed
{#check-your-speed}

Faster websites and apps are more fun to use and are better ranked in search engines. Measure the performance of your App. Master the web developer tools of your browser and use external services such as Google PageSpeed (Lighthouse), YSlow and GTmetrix.

### External data sources
{#external-data-sources}

If you are integrating external services, for example for any kind of REST API, make sure it does not slow you down. Set proper but very small timeouts and log response times once they exceed the threshold.

Congrats. You came all the way to the bottom.

---

## Database performance tips
{#database-performance-tips}

Website performance problems are often caused by misusage of the MySQL database resources provided. Those not only consist of an available storage size, but also computing power - think CPU cycles.

Many [504 errors](#504) and slow PHP response times are related to slow MySQL queries. It's your job as the responsible developer to make sure no insane MySQL queries are executed with your [environment](#the-environment). When using a framework or CMS you might not write MySQL queries directly. Still you need to take that the requests to the database are executed without waste.

### Consider real usage scenarios
{#consider-real-usage-scenarios}

Most commonly database problems are not becoming visible in development when there are just a couple of rows in the tables. Also consider that a local machine might have more memory and CPU available, than the app here hosted on fortrabbit. In addition, consider that there might be more parallel requests to the app ongoing.

### Use profiling
{#use-profiling}

There are a couple of tools you cna use to identify and debug slow queries:

#### Framework and CMS plugins
{#framework-and-cms-plugins}

- Laravel Debugbar
- Yii Debug Toolbar

#### External services
{#external-services}

APM (Application Performance Monitoring) is a whole industry of it's own. In professional environments, deep insights into code performance is crucial. Such tools will also provide stack tracing and issue spotting for database queries. Not all of them are supported with fortrabbit.

- Blackfire - [integration guide](#blackfire)
- New Relic - [integration guide](#new-relic)
- Tideways
- Laravel Nightwatch
- Flare by Spatie
- Datadog

Here are some ideas how you can help yourself without fancy tooling:

### Monitor live load with `SHOW PROCESSLIST`
{#monitor-live-load-with-show-processlist}

Sometimes you need a snapshot of what the database is doing right now. Inside the MySQL shell you can run:

```sql
SHOW FULL PROCESSLIST;
```

This lists currently executing threads including the user, host, database, command type, runtime, and the full query text. Look for rows where `Command` is `Query` and `Time` keeps climbing, or where `State` mentions "Waiting for table lock" or "Copying to tmp table". Those usually point to problematic statements.

1. Connect to the MySQL shell of your environment.
2. Run `SHOW FULL PROCESSLIST;` a few times in succession to see patterns.
3. Copy suspicious queries and run them through `EXPLAIN` to find missing indexes or bad joins.
4. If zombie threads stay around, consider killing them with `KILL <Id>;` (but always fix the underlying query afterwards).

The command requires the `PROCESS` privilege; managed fortrabbit environments include it for the application user. If you do not see full text results, use `SHOW PROCESSLIST;` together with `SET GLOBAL log_output = 'TABLE';` or a slow query log for additional insight.

### Use `EXPLAIN` to inspect query plans
{#use-explain-to-inspect-query-plans}

EXPLAIN shows you which columns and which of their indices (if any) are used. It also points out if inefficient strategies, such as "temporary tables" or "filesort" are applied.

`EXPLAIN SELECT ...` shows how MySQL intends to execute a statement. The output highlights which indexes will be used, how many rows are inspected, join order, and whether temporary tables or filesorts are involved. Running an `EXPLAIN` before optimizing a query gives you a baseline; running it afterwards lets you confirm improvements.

#### Basic example
{#basic-example}

```sql
EXPLAIN SELECT id, email
FROM customers
WHERE country = 'DE'
ORDER BY created_at DESC
LIMIT 25;
```

- `type`: The access method. `ref` or `range` is usually good; `ALL` signals a full scan.
- `key`: Index chosen for this table. `NULL` means no index is used.
- `rows`: Estimated rows to inspect. Large numbers hint at inefficient filters.
- `Extra`: Notes such as `Using filesort` or `Using temporary` that point to extra work.

#### Highlighting join issues
{#highlighting-join-issues}

```sql
EXPLAIN SELECT o.id, c.email
FROM orders o
JOIN customers c ON c.id = o.customer_id
WHERE o.status = 'open'
  AND o.created_at >= NOW() - INTERVAL 30 DAY;
```

Watch the `rows` column for each table. If the joined table `customers` shows `ALL`, MySQL scans every customer regardless of the join condition—time to add an index on `customers.id` or rewrite the join.

##### Re-running after index changes
{#re-running-after-index-changes}

After adding or adjusting an index, rerun `EXPLAIN`. You should observe:

- `key` now referencing your new index
- lower `rows` estimates
- `Extra` dropping `Using temporary` or `Using filesort`

If the improvements do not show up, ensure statistics are current (`ANALYZE TABLE`) and that the query matches the index column order.

### Split write-tables & read-tables
{#split-write-tables-read-tables}

Try to use separate write-intensive and read-intensive tables. Whenever you write on a table, you invalidate the query cache. For instance: if you have a read-intensive user table, and want to log their latest activity, use an additional table for this.

### Use Smart indexing
{#use-smart-indexing}

**First off: Use indexes.** But which? Look at your queries. Log your queries, run them through EXPLAIN and build your (multi-column) indexes based on the EXPLAIN results. Most importantly: repeat this from time to time, because things change and different data-size proportions might benefit from different indexes.

### Avoid JOINs
{#avoid-joins}

JOINs are easily used with modern ORMs and look like a good idea at first glance (and in certain situations they are!). However, when your App grows, they are many times the reason why your database performance decreases hugely. Why? Because there is a major difference between a join between 100 x 100 rows and 10,000 x 100,000 rows: the former fits in the memory, the latter not.

### Avoid full table scans
{#avoid-full-table-scans}

The output from EXPLAIN shows ALL in the type column when MySQL uses a full table scan to resolve a query. This usually happens under the following conditions:

- tables with few rows (index lookup not worth it)
- there is no ON or WHERE conditions for indexed columns
- constant values in columns spanning large portion of rows
- low cardinality index (many similar values in column)

For small tables, a table scan often is appropriate and the performance impact is negligible. For large tables, try the following techniques to avoid having the optimizer incorrectly choose a table scan:

- Use ANALYZE TABLE tbl_name to update the key distributions for the scanned table. See Section 13.7.3.1, "ANALYZE TABLE" Statement.
- Use FORCE INDEX for the scanned table to tell MySQL that table scans are very expensive compared to using the given index:

```sql
SELECT * FROM t1, t2 FORCE INDEX (index_for_column)
WHERE t1.col_name=t2.col_name;
See Section 8.9.4, "Index Hints".
```

---

## Scaling ideas
{#scaling-ideas}

When to upgrade or downgrade a component plan.

The fortrabbit platform offers a high grade of abstraction for booking required hosting resources, aiming to make booking more resources an almost seamless experience. The product catalog is designed in [components](#components) that can be booked and scaled individually.

Finding the optimal plan for an website depends on many factors and is the responsibility of the web developer. There are quite a few factors that come into play.

### Scaling and performance
{#scaling-and-performance}

- Components like Jobs and Key-value store can reduce load on other components
- Increasing traffic can affect resource requirements of other components
- Code and config has a huge impact on performance

### Tips
{#tips}

- Turn on [autoscaling](#autoscaling)
- Start small, scale later
- Monitor performance
- Review and refactor code before scaling resources
- Book smaller plans for staging environments
- Book higher plans for production environments

### Related
{#related-3}

ach component has unique scaling considerations:

- **[PHP scaling](#scaling)** - Memory, CPU, and concurrency
- **[MySQL scaling](#scaling)** - Storage, memory, and query performance
- **[Traffic scaling](#scaling)** - Bandwidth and request limits
- **[Web storage scaling](#scaling)** - Disk space and I/O performance
- **[Jobs scaling](#scaling)** - Background processing capacity
- **[Key-value store](#key-value-store)** - Memory-based caching and sessions
- **[Backup scaling](#backups)** - Independent of performance needs

---

## Performance
{#performance-1}

Understand and optimize your websites's performance.



---

## SSH key setup
{#ssh-key-setup}

All about SSH keys and how to create an SSH key pair on your local machine.

### About SSH keys
{#about-ssh-keys}

SSH keys are a secure and convenient alternative to passwords. A key pair consists of a public key (shared with the server) and a private key (kept secret). Authentication happens automatically when the server verifies you hold the matching private key.

```shell
~/.ssh/
│
├── id_ed25519        # Private Key (The Key) KEEP SECRET!
├── id_ed25519.pub    # Public Key (The Lock) SHARE
├── id_rsa            # Legacy Private Key
└── id_rsa.pub        # Legacy Public Key
```

### Do you already have a SSH key?
{#do-you-already-have-a-ssh-key}

To see any existing keys, open a terminal to list the `~/.ssh` folder:

```shell
$ find ~/.ssh
#/…/.ssh/config
#/…/.ssh/id_ed25519      
#/…/.ssh/id_ed25519.pub  
#/…/.ssh/known_hosts
```

Proceed to the next section if you don't have any key pairs or get an error about a missing folder. If you do see key pairs like above, then you can [upload the public SSH key](#importing-ssh-keys-to-fortrabbit).

### Generate a SSH key pair
{#generate-a-ssh-key-pair}

```shell
## NOTE: me@fortrabbit is just an identifier, use what suits you
{#note-me-fortrabbit-is-just-an-identifier-use-what-suits-you}
$ ssh-keygen -t ed25519 -C me@fortrabbit
## Generating public/private ed25519 key pair.
{#generating-public-private-ed25519-key-pair}
## Enter file in which to save the key (/home/user/.ssh/id_ed25519):
{#enter-file-in-which-to-save-the-key-home-user-ssh-id-ed25519}
## Enter passphrase (empty for no passphrase):
{#enter-passphrase-empty-for-no-passphrase}
## Enter same passphrase again:
{#enter-same-passphrase-again}
```

We suggest to use `me@fortrabbit` so that you can identify the key as being associated with your fortrabbit account later on. Use anything you like.
It's just a comment.

### Specify a different key than the default
{#specify-a-different-key-than-the-default}

If you use an unprotected key (no passphrase) and still get asked about a password, it may be the case that the key in the default location is not imported into fortrabbit. To use a specific key run SSH like this:

```shell
$ ssh -i ~/.ssh/CUSTOM_KEY {{app-env-id}}@ssh.{{region}}.frbit.app
## Replace CUSTOM_KEY with a key on your machine
{#replace-custom-key-with-a-key-on-your-machine}
```

### SSH keys generation on Windows
{#ssh-keys-generation-on-windows}

The procedure to create SSH keys is slightly different on macOS and Linux compared to Windows. There are different ways to set up and use Git with Windows and also different ways set up and store the keys. We recommend using the official installer from the Git website, together with Git Bash.

#### SSH keys under Windows with PuTTY
{#ssh-keys-under-windows-with-putty}

If you generated an SSH key with PuTTY, you will need to make sure that the private key is saved in the location where `git.exe` or `ssh.exe` are looking for it or take steps to specify where the key is. Additionally, PuTTY uses a special format to store the private key, which also requires additional steps to use with other tools. Because of these reasons and previous experience with clients, we advise against using PuTTY.

---

## Composer
{#composer-1}

Composer is the defacto standard to handle PHP application dependencies, as well as providing mechanisms to keep them up-2-date. Integrate Composer into your development workflow with fortrabbit.

### Get ready
{#get-ready-29}

It's recommended that you have a [local development environment](#intro-to-local-development-with-php) running including Composer and that you are making use of it already. Have a good understanding of [deployment in general](#deployment-intro) and on fortrabbit.

### Composer as part of deployment
{#composer-as-part-of-deployment}

We recommend to run `composer install` as part of the build pipeline. When you deploy code with Git and Composer is defined as a [build command](#build-commands), it will run automatically with each deployment. New and updated dependencies will be synced into the web space.

### Composer and Git
{#composer-and-git}

The `vendor` folder should NOT be in Git: Make sure that folder is included in your `.gitignore` file. This directory is created by Composer within your project locally and contains all the packages you are using locally. Make sure that both the `composer.lock` file and the `composer.json` file are present and part of Git.

### Alternative locations
{#alternative-locations}

Your `composer.json` and `composer.lock` files need to be stored in the root folder of your application.

### Private repositories in Composer
{#private-repositories-in-composer}

You need to add the private repositories into your `composer.json` file? Read on with [composer private repos](#composer-private-repos).

### Composer from SSH
{#composer-from-ssh}

While we highly recommend leveraging Composer via the Git deployment (see above), you can also execute Composer when logged in via [SSH](#ssh-access). Please note that this should only be done in certain edge cases.

```shell
ssh {{app-env-id}}@ssh.{{region}}.frbit.app
composer install
```

This way Composer will be executed within the web delivery environment, which is not optimized for such tasks. **Don't use `composer update` as this might cause Composer to hit the App's memory limits.** The most common Composer issue is, when users are running into memory problems when trying to execute composer while logged in via SSH here. The general answer on that is: Please don't. Use Composer together with Git deployment as described above.

---

## Staging environments
{#staging-environments}

An app on fortrabbit represents a project or website. It can be connected to a Git repo at GitHub. An environment can be linked to a branch of a Git repo. Each app has at least one environment.

### Use cases
{#use-cases-14}

- **Feature development**: Build a new version while still being able to fix bugs in the running version without uploading all the new feature code.
- **Purpose separation**: The backend team can break things while the frontend team can still work uninterrupted.
- **Continuous integration**: Code needs to be tested and monitored before being deployed live.

The use of multiple environments is optional. For smaller websites it might be overkill, for less experienced developers, implications can be a bit mind bending.

Multi-staging environments are part of professional software development processes. They allow for testing and debugging at different stages of the development cycle before releasing a product. A classical multi-stage setup consists of a production, staging and maybe a development environment.

#### Developer client workflow example
{#developer-client-workflow-example}

The client requests a new feature for the website. This is first developed in a local development environment. An additional temporary environment at fortrabbit can be used to collect feedback. Once the new feature has been signed off, it can be merged into production.

#### Software development team workflow example
{#software-development-team-workflow-example}

The production environment is the stable live environment. The development environment contains the latest bleeding edge changes. The staging environment is used for quality assurance before go-live.

### Common multi-staging set ups
{#common-multi-staging-set-ups}

- **staging + production**: "Staging" is where you do your development. "Production" runs the live code. From time to time you migrate all the (stable) changes from staging into production.
- **temporary + production**: Same as above, it's more of a one-time-developed project. Maybe once a year there is an upgrade, a re-brush or alike. For this you utilize an additional, temporary environment, in which you do the upgrades.
- **testing + staging + production**: Code changes are made to the testing environment. Once they seem stable, they get published to the staging where they are monitored and further tested. Finally they get published to production.

#### Multi-staging and local development
{#multi-staging-and-local-development}

Most likely you are developing with a [local PHP development environment](#intro-to-local-development-with-php) on your machine. So your laptop is already a of kind of **staging** while the actual part at fortrabbit is usually **production**.

### Multi-staging on fortrabbit
{#multi-staging-on-fortrabbit}

All you need to utilize multi-staging on fortrabbit is an [app](#the-app) with multiple [environments](#the-environment). environments are made to support multi staging setups.

### Multi-staging with framework or CMS
{#multi-staging-with-framework-or-cms}

Most modern CMS and frameworks anticipate and support multi-staging workflows. The concepts are similar, implementation differs in detail. In most cases, the stage is defined by an [ENV var](#env-vars-intro).

### Multi-staging and Git
{#multi-staging-and-git}

Multi-staging is mostly associated with [Git deployment](#deployment-intro). Git supports multiple, named branches of your code. On fortrabbit, each branch can be mapped to an [environment](#the-environment).

### Caveat runtime data
{#caveat-runtime-data}

The biggest problem introduced with multi stage environments is runtime data: databases, user uploads and anything else that is being generated by the App. Sure you need to separate those as well. If all environments require the latest data to run properly or for testing, you need to figure out a way to synchronize the production data downwards, to the other environments. These problems are highly individual and cannot be solved in a general manner. We are experienced with these kind of things and we love to help you.

---

## Monorepos
{#monorepos}

It's a trend to organize multiple projects into one Git repo. What to consider when it comes to deployment and hosting monorepos.

### About monorepos
{#about-monorepos}

A monorepo (monolithic repository) stores multiple related projects in a single Git repository, potentially enabling shared dependencies and coordinated releases:

```raw
mono-repo
 - dependencies (shared)
 - app-1
   - dependencies (individual)
 - app-2
  - dependencies (individual)
```

There are specific tools to help working with the shared dependencies. A good overview can be found at [monorepo.tools](https://monorepo.tools/). The projects of a monorepo usually share the software stack, not only the same programming language, but also a framework on top of that.

At fortrabbit, we use a monorepo for our JavaScript based frontend stack. Not only Node modules can be shared directly, but also web components can be shared across the different web properties easily.

### PHP monorepos
{#php-monorepos}

Monorepos are not that popular in PHP, at least at the time of this writing. Symfony and Laravel have basic monorepo structure support. PHP monorepos require consideration to ensure each application can be deployed independently while leveraging shared code effectively.

### Multi stack web projects in one Git repo
{#multi-stack-web-projects-in-one-git-repo}

Like outlined with [project organization](#project-organization), some web projects may include a frontend and a backend stack in one repo.

```raw
website-project
  - frontend (JS)
  - backend (PHP)
```

That's not really a classical monorepo, but more like a repo that contains two different projects.

### CMS multi-site features
{#cms-multi-site-features}

An alternative approach to host multiple different projects with one code base can be a multi-site feature, Craft CMS, Kirby WordPress and Statamic support that.

### Monorepo support on fortrabbit
{#monorepo-support-on-fortrabbit}

The fortrabbit [git deployment features](#deployment-intro) are mainly designed for classical polyrepo (or multirepo) use cases, where each web project will have it's own Git repo.

#### Available features
{#available-features}

- Add the same repo to multiple apps
- Add the same branch to multiple environments
- Define which path of the repo is deployed where
- Enable/disable automatic deployments

#### Features not available
{#features-not-available}

- Add multiple repos to one app
- Using Git subtree or Git submodules

#### Using external build pipelines
{#using-external-build-pipelines}

The builtin deployment tools are just one option to deploy code. It's also possible to connect fortrabbit to external CI/CD systems such as [GitHub Actions](#using-github-actions) by providing third party services direct SSH access through [deploy keys](#deploy-keys).

---

## Headless hosting workflows
{#headless-hosting-workflows}

Considerations for hosting and deploying headless web projects.

### About headless mode
{#about-headless-mode}

Headless PHP applications separate the backend from the frontend. They communicate through APIs rather than traditional server-rendered templates.

- The PHP backend - a framework like Laravel, Symfony, or headless a CMS like Craft CMS, Kirby, Statamic - exposes a RESTful API or GraphQL endpoints.
- The JS frontend - a frameworks like Vue.js, React, or Next.js - consumes this data to create dynamic user interfaces, often in form of Single Page Applications (SPA).

A headless setup is more sophisticated. It allows different frontends to share the same backend and supports separation of concerns.

### Hosting headless
{#hosting-headless}

Consider project requirements carefully before jumping into headless adventures. There are also some considerations when it comes to hosting headless web projects.

#### Project organization
{#project-organization-1}

One thing to decide, is how the hosting will be organized. Two independent systems can be deployed separately or together:

##### 1 - Separated hosting
{#1-separated-hosting}

This is the more professional and the often propagated mode. The backend is hosted with a PHP server, hopefully fortrabbit. The frontend is hosted at a JAM Stack hosting service, like Netlify or Vercel.

##### 2 - Coupled hosting
{#2-coupled-hosting}

It's also possible to have both systems run side by side in one environment at fortrabbit. This has the benefit that the project code base can stay together (maybe in a single repo) and does not have to be separated over two different hosting systems.

See the [project organization](#project-organization) for more options.

#### SEO considerations
{#seo-considerations}

Some web projects require to be indexed by search engines. That's something classical SPAs are not good at by definition. Here are the most common approaches:

##### CSR - Client Side Rendered
{#csr-client-side-rendered}

HTML is only created in the browser (classic). This is OK for any web application that will users to login.

##### SSG - Server Side Generated
{#ssg-server-side-generated}

HTML is getting created during deployment for all pages. This is similar to classical static page generators like Jekyll. But when a human visits, first the static page is going to be loaded and then replaced by dynamic parts, so that any further interaction can be handled through smaller AJAX calls.

But what happens, when an editor changes the content of an article? The generation of the pages only happens when the project get's deployed, not on edit. Deploy webhooks (after edit) and incremental builds are aiming to help. But setting that up can be challenging.

##### SSR - Server Side Rendered
{#ssr-server-side-rendered}

HTML can also be live server side rendered. This is not easily available for fully decoupled headless systems. There are some approaches to couple frontend and backend as modern monoliths.

#### ISR - Incremental Static Regeneration
{#isr-incremental-static-regeneration}

Incremental Static Regeneration (ISR) addresses shortcomings of SSR and SSG by serving the existing static page to the first visitor of an outdated route, hydrating it once the dynamic content loads, regenerating the static version in the background, and then delivering the updated page to subsequent visitors.

This of course also requires two servers to host one website: Backend server provides the API; Frontend server creates new static pages on the fly.

The frontend however can still be hosted on the edge. It's good for SEO and it is fast. But it's more complex to setup too. It's also not the cheapest option.

#### Performance
{#performance-2}

Headless apps, specifically in SSR mode, can cause considerable server load peaks. Imagine a large website that always needs to be completely rebuild every time it get's deployed. Maybe generating thousands of pages with complicated queries and a lot of images. For the server that means, short times of high performance and long periods of idle time.

In our experience GraphQL can also be dangerous. It is a powerful tool to query any content from the backend. It's also very easy to write query that do not perform well. Under certain configuration, specifically with larger data sets, this can lead to performance issues.

---

## PHP info
{#php-info}

Sometimes, you might be unsure on configuration settings, such as which extension in which version is exactly enabled or which ENV vars are actually available. phpinfo to the rescue!

`phpinfo()` is a built-in PHP function that displays information about the current server settings, including:

- PHP version
- Loaded extensions
- Configuration settings
- Environment variables
- Server information
- and more

### Instructions
{#instructions}

1. Create a `info.php` file anywhere in your publicly accessible path
2. Put `<?php phpinfo(); ?>` in that file
3. Call the URL with the browser to see a full config dump `domain.com/phpinfo.php`

Your CMS / framework might have its own dump of that. With Craft CMS for example you can visit a nicely formatted `phpinfo` in the control panel.

### Security advice regarding phpinfo
{#security-advice-regarding-phpinfo}

Don't use phpinfo in production or at least make sure to delete that file right away after you have finished your investigation, or put it behind a password. The output might contain sensitive information you don't want to share with the world. Keys and values of your ENV vars are visible, that can contain database access and API keys to external services.

### Related
{#related-4}

- [offcial docs on php.net](https://www.php.net/manual/en/function.phpinfo.php)

---

## Using a canonical tag
{#using-a-canonical-tag}

In the cases above you forward all requests to the ONE main domain you are using. In some cases you might have two domains serving the same content. Now, search engines need to know which page is the one they should show the results for. To help the search bots, you can use a canonical tag.

Let's say you have the page `fortrabbit.com` and `fort-rabbit.com` registered. And you want both to display the same content but still keep the originally entered URL. Actually, for this example you might want to create a redirect to the domain that matters most to you, but whatever. Now you want the search engines to prefer and link to the first domain, so you add in the head of each HTML page delivered:

```html
<head>
  …
  <link
    rel="canonical"
    href="https://www.fortrabbit.com"
  />
</head>
```

More on [canonical URLs on Google webmasters](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls)

---

## Composer private repos
{#composer-private-repos}

How to access private composer repositories during git deployment.

<!-- TODO: Review and finish. -->

<!--

2024-08-30 14:14:43

-->

### What are private Composer packages?
{#what-are-private-composer-packages}

Modern PHP app development utilizes [Composer](#composer) as a dependency manager. There are many great open source packages [out there](http://packagist.org). But your company code is probably not intended to be released to the public or you rely on a third party package which is not open source. That's when you use private Composer repositories.

### Hosting private Composer repos
{#hosting-private-composer-repos}

Private composer repos can be hosted.

- Private GitHub repos
- Self hosted Satis like service such as [Packeton](https://github.com/vtsykun/packeton)
- [Packagist.com](https://packagist.com) - commercial by makers of Composer with
- [Repman.io](https://repman.io) - by Buddy.works

### A - Using SSH Keys
{#a-using-ssh-keys}

<!-- 2024-08-30 14:17:25 - TODO: there is a key installed with each environment (and it could be visible with the dashboard as well.)  -->

Alternatively you can limit access to a specific SSH keys. To use your private Composer repo in [Git deployment](#deployment-intro) you need to set up authentication so your fortrabbit app can access your external repo (probably hosted on GitHub). For this you need a public and private SSH key-pair.

The private key will be stored in the deployment environment of your App that composer can use it but nobody else. The command shows the public key, in the example is starting with `ssh-rsa AAA...` and ending with `..odTimp`. You can now install the key in your private Git repository. You can re-run this command at any time to view or change the current key of your app.

### B - Using oAuth or HTTP Basic Auth
{#b-using-oauth-or-http-basic-auth}

In the script below we generate a global `auth.json` file that contains credentials to access a GitHub repo using oAuth, and another private repo which is protected with Basic HTTP auth, in our example Laravel Nova. This is just for the sake of demonstration, you will probably need to adjust it to your needs.

Since you don't want to keep secrets in your git history, you can store them in [ENV vars](#env-vars-intro).

```php [add-auth.php]
// Github token example
if ($github_oauth =  getenv("GH_TOKEN")) {
    echo "Configure auth for github-oauth.github.com" . PHP_EOL;
    shell_exec("/usr/local/bin/composer config --global github-oauth.github.com {$github_oauth}");
}

// HTTP basic auth example
if (getenv("NOVA_USER") && getenv("NOVA_PASS")) {
    $nova_username = getenv("NOVA_USER");
    $nova_password = getenv("NOVA_PASS");
    echo "Configure auth for http-basic.nova.laravel.com" . PHP_EOL;
    shell_exec("/usr/local/bin/composer config --global http-basic.nova.laravel.com {$nova_username} {$nova_password}");
}
```

<!-- TODO: Below will be build step  -->

<!-- The script you created needs to be executed before Composer tries to install packages. Create a fortrabbit.yml file with the following structure:

```yaml
version: 2
pre: add-auth.php
``` -->

Additionally, you need to set the `COMPOSER_HOME` env var and the env vars you use in the script in the dashboard:

```yaml
COMPOSER_HOME=/tmp/.composer
GH_TOKEN= ...
```

After deploying the two files you are set to access your private repos.

#### Link your private repo
{#link-your-private-repo}

Now you can add your private repositories to your `composer.json` file as usual:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "git@github.com:my-company/my-package.git"
    }
  ],
  "require": {
    "my-company/my-package": "^1.2.3"
  }
}
```

---

## Dig
{#dig}

Query public DNS entries from the terminal using the dig command.

The `dig` command shows you if there are any DNS entries and where they are pointing to. Here we look up `help.fortrabbit.com`.

```shell
$ dig help.fortrabbit.com
;; Truncated, retrying in TCP mode.

; <<>> DiG 9.8.3-P1 <<>> ANY help.fortrabbit.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 44565
;; flags: qr rd ra; QUERY: 1, ANSWER: 3, AUTHORITY: 0, ADDITIONAL: 0

;; QUESTION SECTION:
;help.fortrabbit.com.       IN  ANY

;; ANSWER SECTION:
help.fortrabbit.com.      600    IN  CNAME   help-frbit..frbit.app.
help-frbit.eu2.frbit.net.  20    IN  A       52.48.51.144

;; Query time: 863 msec
;; SERVER: 192.168.178.1#53(192.168.178.1)
;; WHEN: Wed Jun  1 10:25:40 2016
;; MSG SIZE  rcvd: 122
```

#### Dig an IP
{#dig-an-ip}

```shell
## This will print out the IP of your App
{#this-will-print-out-the-ip-of-your-app}
$ dig +short {{app-env-id}}.frbit.app
```

---

## Encoding
{#encoding}

UTF-8 is assumed as the default encoding. You can set a different encoding manually — if you really want. This is on how to change the character encodings with fortrabbit.

#### PHP
{#php-1}

PHP writes the encoding in the `Content-type` header. The default charset is `UTF-8` — `Content-type: text/html; charset=UTF-8`. You can change the charset via `ini_set`. Here is an example:

```php
ini_set('default_charset', 'iso-8895-15');
```

Make sure to write this in all your "root" PHP files. Alternatively you can use the `header` method of PHP to set the charset explicitly:

```php
header('Content-type', 'text/html; charset=iso-8859-1');
```

#### HTTP/Apache
{#http-apache}

Any static file — `.txt` or `.html` — is delivered directly via Apache. Per default, Apache assumes the file is `utf-8`. You can change the charset via an `.htaccess` directive. Following an example:

```apache
AddDefaultCharset iso-8859-1
```

#### MySQL
{#mysql-3}

When you store or fetch data from MySQL, you need to make sure to fit the encoding of the database when you connect to it. Further more, you can set specific encoding to your columns. To set a different encoding than UTF8 for your database sessions from PHP you can use the `mysql_set_charset` method. Here is an example:

```php
mysql_set_charset('ISO-8895-15', $connection);
```

---

## Git intro
{#git-intro}

This is a quick intro to Git, how to set it up and how to get started with it on fortrabbit.

### About Git
{#about-git}

Git is a distributed version control system. It's quite popular to work with text files — hence in software development. It's fast, assures data integrity and supports non-linear workflows (branching). Git was developed by Linux kernel developers (including Linus Torvalds). It's free and can be used either from the command line or via graphical user interfaces.

Git can help you to collaborate on code projects, keep track of your code changes and rollback to points in time, if needed. It comes with:

- A history of all files included, so you can review or undo changes
- Powerful file merging which makes collaboration easy

To deploy code to fortrabbit you use Git from your local machine and push to the remote on GitHub. So it should be part of your [local development setup](#intro-to-local-development-with-php).

### Learn Git
{#learn-git}

You should be familiar with Git standard operations and concepts — these are: `commit`, `push` and `pull`. If you don't know Git, yet, we recommend to go ahead and learn the basics. You will profit from it either way — whether you keep using fortrabbit or not. It's a cornerstone of todays software development. For developers not used to the shell it might not be very intuitive to start with, but once you got started it soon becomes very, very handy for all kinds of things besides deploying to fortrabbit. There are many good tutorials out there in the interwebs to get started. For example:

- [GitHub: Quickstart](https://docs.github.com/en/get-started/quickstart)
- [Official docs from Git SCM](https://git-scm.com/doc)
- [Try Git in your browser for free](https://try.github.io/levels/1/challenges/1)
- [Guides & ebook from Git Tower](https://www.git-tower.com/learn)
- [Get Git right from Atlassian](https://www.atlassian.com/git)
- and [many more](http://lmgtfy.com/?q=learn+git)

### Install Git
{#install-git}

To use Git, you need to have it installed on your local machine. You might already have Git: open a terminal window and type `git --version`. Good news for macOS and Linux users: you most likely already have it installed.

#### Git on Windows
{#git-on-windows}

You can work it out. The primary problem you have to solve is: which Git distribution are you going to use. There are multiple of those floating around, we recommend to download and install Git from the **[official Git website](https://git-scm.com/downloads)**. This one comes with the "Git Bash".

### The hidden .git folder
{#the-hidden-git-folder}

Git never forgets. It can bring back any content from any file, even deleted ones. To do so, it stores all the stuff in the hidden `.git` folder at the top level of the repo. Over time that file can get big too. It can also contain unreachable blobs and other stuff you are not aware of. Depending on the situation, there are many ways to clean this up: delete files of a certain type, delete the history before a certain date, or even start again from the current state.

### Git desktop GUIs
{#git-desktop-guis}

Most people probably use Git from the command line (aka bash, terminal, shell). But there are also GUIs (desktop Apps) to manage Git. Those help to get started and to see visually what's going on:

- [Git desktop GUIs](#git-clients)

### About GitHub
{#about-github}

You hopefully already know that [GitHub](https://github.com) is the most popular choice for versionized code hosting and collaborating. It is free to use with private and public projects. Sometimes people confuse Git with [GitHub](https://github.com). Git is the version control system established by Linus Torvalds. GitHub is the service, which offers Git remote hosting and additional extra magic collaboration features. GitHub has extended Git workflows with neat communication tools around the basic Git usage. Most notable is the "pull request" workflow.

See our [GitHub intergration guide](#github).

### Large Git repos
{#large-git-repos}

A bloated Git repository slows down deployment. You might even hit limits. In most cases the repo can and should be small.

### Large files in Git
{#large-files-in-git}

You should not put big binary files (> 2 MB) into your Git repo.

In general we also advise not to put assets and most importantly images or even videos in Git. Some images that belong to your website layout, like your company logo (a small SVG) are ok. But when you have a lot of images in Git, odds are that this is bad practice.

For almost all cases, your uploaded content images (`.jpg`, `.png`, `.gif`) do not belong in Git. Remember that the Git repo and the web-space are different things here at fortrabbit, Git is a one-way street here. The next user upload will not be in Git anyways. It's a good practice to **separate code from content** for many reasons. So we advise to deploy user uploads, static assets and other runtime data separate from the core code deployment done with Git.

---

## GitHub API limits and Composer
{#github-api-limits-and-composer}

The reason why you can run into this issue temporarily is that GitHub limits it's API per IP.

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

---

## Hosts file
{#hosts-file}

Let's say you are developing a website soon to launch and want to test your custom domain before actually switching the DNS routing it to fortrabbit. Just add the domain to fortrabbit, as you would do with any actually routed domain, then modify your local hosts file, which lets your local machine know ahead of time that the domain is to be served from your fortrabbit e.

#### hosts file location
{#hosts-file-location}

The hosts file is a text file (without file type ending). It can be found here:

- MacOS & Linux: `/etc/hosts`
- Windows: `c:\windows\system32\drivers\etc\hosts`

#### Editing your local hosts file
{#editing-your-local-hosts-file}

Your local file contains many entries: do not edit those. Just add a new line with the IP of your App and the domain you want to see routed there like so:

```shell
## pattern (how it works)
{#pattern-how-it-works}
[your App's IP address] [your fully qualified domain name]

## example (what it looks like)
{#example-what-it-looks-like}
12.0.0.1 mydomain.com www.mydomain.com
```

#### Undo changes to your hosts file
{#undo-changes-to-your-hosts-file}

After your domain has been moved/propagated be sure to remove the entry from your hosts file.

---

## HTTPS troubleshooting
{#https-troubleshooting}

Are you seeing a certificate error in the browser? This article aims to help developers troubleshooting such errors.

TLS certificates are provided for all [domains](#the-domain). See the [HTTPS article](#https) for general features and configuration.

### Review certificates in the browser
{#review-certificates-in-the-browser}

To troubleshoot TLS/SSL issues, it's often helpful to view the certificate in the browser. In Chrome and Firefox you can:

1. open `https://www.{{domain}}.com` < make sure to use https not http
2. click on the lock icon
3. click on the "certificate" to reveal the cert

### You see a certificate warning
{#you-see-a-certificate-warning}

You visit your Apps domain under the `https://` address and the browser throws an error that the certificate can't be verified. If you inspect the cert in the browser, you see that the cert is issued for `*.frbit.app` not for your domain. The error might be:

```raw
NET::ERR_CERT_COMMON_NAME_INVALID
```

This can happen, if the domain is brand new and the cert is not yet installed. It can take up to 24 hours for the certs to get installed. The cert for the apex domain (for forwarding) usually takes a bit longer than the other one.

This can also happen, if your domain is not routed to fortrabbit (yet). Only domains that are already routed to fortrabbit will receive a TLS cert. Please see the domain settings in the Dashboard.

There are also other edge cases when this can happen, for example, if your domain has set CAA records with DNS.

### The browser shows a mixed content warning
{#the-browser-shows-a-mixed-content-warning}

The cert is installed but you are seeing an error like this:

> Mixed Content: The page at '{{domain}}' was loaded over HTTPS, but requested an insecure XMLHttpRequest endpoint '{{domain}}'. This request has been blocked; the content must be served over HTTPS.

Your website is requesting external resources over non-secure addresses (http). Check the source code of your website and find and replace all `http://` requests. This can be CSS files, fonts, images or AJAX calls.

You can use `https://` instead or you just leave out the protocol entirely like so: `//`. The last method will use whatever has been used before, so that works especially well, with different environments, for instance when your local development machine doesn't have TLS.

### Solve SSL verification errors
{#solve-ssl-verification-errors}

This is the fix for verification errors when using ssl_verify. If you are receiving an error like the following:

```raw
error:14090086:SSL routines:SSL3_GET_SERVER_CERTIFICATE:certificate verify failed
```

You need to set the `capath` as well. Assuming you are using PHP streams, it would look like this:

```php
$context = stream_context_create();
stream_context_set_option($context, 'ssl', 'verify_peer', true);
stream_context_set_option($context, 'ssl', 'capath', '/etc/ssl/certs'); # <<< that's the one
stream_context_set_option($context, 'ssl', 'allow_self_signed', false);

$fp = stream_socket_client("thedomain.tld:443", $errno, $errstr, 5, STREAM_CLIENT_CONNECT, $context);
## ..
{#}
if (stream_socket_enable_crypto($fp, true, STREAM_CRYPTO_METHOD_SSLv3_CLIENT) === false) {
    die("Failed to verify certificate");
}
#...
```

For cURL, the option `CURLOPT_CAPATH` needs to be set to `/etc/ssl/certs`.

---

## Learn
{#learn}

Tips, tricks, workflows, practices, tactics - all more or less loosely related to the fortrabbit platform.



---

## Security tips
{#security-tips}

Some basic tips to keep your fortrabbit account and your code base secure.

### Dashboard and passwords security
{#dashboard-and-passwords-security}

- The password to login with the fortrabbit dashboard must be secure.
  - Use a password manager or a long pass-phrase.
  - Don't share your account password, use our collaboration features instead.
- Rotate internal passwords via the dashboard:
  - Object storage
  - When team members leave
- Go over the list of imported SSH public keys periodically and keep only those being used.

### PHP code security
{#php-code-security}

- Make sure to follow common security guidelines - see [PHP the right way](http://www.phptherightway.com/#security).
- Mind the [OWASP Cheat Sheets](https://www.owasp.org/index.php/OWASP_Cheat_Sheet_Series) to negate attacks before they can start.
- Best practice for security and portability is to store secrets like database password not with code but with our App Secrets or ENV vars (as long as they are not exposed as well).
- Don't store sensitive information in plain text in the database, use ciphertext.
- Make sure you keep your software up-to-date

---

## ENV vars intro
{#env-vars-intro}

ENV vars help to create and shape the environment of where the code runs.

### Problem
{#problem}

You most likely run at least two environments for your app: a [local one for development](#intro-to-local-development-with-php) and one on fortrabbit for production. Both instances probably have access to a database, but your local MySQL credentials will differ from the remote ones. Your `config.php` file is under Git version control, so how do you manage different environment-specific configurations, from database credentials to API keys? Additionally, how do you work in a team where everyone has their own local settings? How do you separate code from configuration to ensure portability and keep secrets secure?

### Solution
{#solution}

Store everything specific to the environment in environment variables, or 'ENV vars' for short. An ENV var is a key-value pair, like so: `MY_SQL_PASS=sCRAmblEDegGGs`. The concept of ENV vars is widely used across different software systems, including Apache, Node.js, and PHP. Accessing ENV vars from PHP is straightforward, and it is a commonly accepted best practice to use them for configuration management.

#### Benefits
{#benefits-1}

- **Security**: Store sensitive information like database credentials and API keys outside of your codebase. See [ENV var security](#security-considerations-for-env-vars).
- **Portability**: Code can run in different environments without modification. Allow each team member to have their own local settings without affecting the shared codebase.
- **Separation**: Keep code and configuration apart.

---

## Accessing ENV vars from PHP
{#accessing-env-vars-from-php}

How to read values from environment variables in PHP.

```php
## 1. use the getenv function
{#1-use-the-getenv-function}
echo getenv("MY_ENV_VAR");

## 2. use the global
{#2-use-the-global}
echo $_SERVER["MY_ENV_VAR"];
```

1. The [getenv() PHP function](https://www.php.net/manual/en/function.getenv.php) accepts a key and returns it's value.
2. Use the global variable `$_SERVER`.

Frameworks and content management systems will parse and use ENV vars automatically. Usually [.env files](#env-vars-intro) are supported for local development. A config file to grab may `$dbHost = env('DB_HOST');`.

- **Laravel**: Use the `env()` helper function
- **Craft CMS**: `getenv()` in `config/general.php`
- **WordPress**: `getenv()` to access environment variables in `wp-config.php`

---

## Understanding the .env file
{#understanding-the-env-file}

What is a .env file in PHP and why maybe not to use on fortrabbit.

### The .env file
{#the-env-file}

The `.env` file format is a plain text configuration file that lives on top level of your code base. It has `KEY=VALUE` pairs, is easy to write for humans and runtime agnostic. You need an additional parser library, that reads the file and makes the ENV vars accessible from the code base. Here are the most popular .env parsers for PHP:

- [github.com/vlucas/phpdotenv](https://github.com/vlucas/phpdotenv) - Everyone
- [github.com/symfony/dotenv](https://github.com/symfony/dotenv) - Symfony

Modern PHP frameworks like [Laravel](#install-laravel-locally) and [Symfony](#symfony-guide) …) and some CMS like [Craft CMS](#install-craft-cms-local) use `.env` files for configuration and include a parser already.

### Don't put .env files on the server
{#don-t-put-env-files-on-the-server}

Use a `.env` file the local development environment. Use pre-configured ENV vars from the fortrabbit dashboard, add custom ones via the dashboard. BUT PLEASE DON't put `.env` files on fortrabbit. Avoid confusion about conflicting sources and increase security.

Many CMS and frameworks will parse that file automatically. Now depending on the configuration set by the parser, the ENV vars from the `.env` file may or may not overwrite the values provided by the fortrabbit dashboard. To avoid mixed states, either use the ENV vars provided by the dashboard (recommended) or an `.env` file.

We highly recommend to NOT include a `.env` with your Git repo for obvious security concerns. The .env file can include secrets about your application. You can manually create or copy a `.env` file by SSH/SFTP. This might be automated. In that case, you may remove all custom ENV vars from the dashboard. Please see [ENV var security](#security-considerations-for-env-vars).

---

## Security considerations for ENV vars
{#security-considerations-for-env-vars}

ENV vars are the predominant way to configure PHP based websites on a per environment basis. Often sensitive data like database passwords and API keys are stored with ENV vars. Take care to keep your secrets a secret.

### Don't deploy a .env file to production
{#don-t-deploy-a-env-file-to-production}

Best don't deploy your `.env` file to production or anything that is public. The `.env` should really be excluded from Git. Don't deploy it by SSH/SFTP either. When the `.env` is in the root folder, the whole internet can maybe read it by calling `yourdomain.com/.env`.

### Don't expose phpinfo
{#don-t-expose-phpinfo}

A phpinfo will expose all environment variables. Make sure not to expose a public phpinfo. Mind that many debugging toolsbars will also include a phpinfo.

### Encode and decode ENV vars
{#encode-and-decode-env-vars}

Use a base64 encoded string and decode it when applying it to your configuration in your code. Encoding works like this:

```php
php -r "echo base64_encode('YOUR-M$Pa#A-VALUEx') . PHP_EOL;"
```

And [this example](https://github.com/laravel/ideas/issues/416#issuecomment-280436034) should give you an idea how you can do the decoding.

---

## ENV vars
{#env-vars-1}

Working with with environment variables on fortrabbit.



---

## Reduce hosting costs
{#reduce-hosting-costs}

Reviewing and cutting down hosting costs with the fortrabbit hosting platform.

### Use the costs overview
{#use-the-costs-overview}

With our dashboard under each of your [payment methods](#the-payment-method) you can find an invoice archive. There is also an invoice draft for the currently ongoing costs for the month so far. The [pro-rated daily billing](#postpaid-billing) helps you to remove unnecessary [components](#components-intro) with immediate effect.

### Review apps and environments
{#review-apps-and-environments}

See if you have any unnecessary [apps](#the-app) or [environments](#the-environment) hanging around — maybe some out-of-date side project, or something half finished? Delete! Make sure you have an up-to-date and complete local backup. That way, you can easily re-deploy it again at a later stage.

### Check component plans
{#check-component-plans}

Review your currently selected [components](#components-intro). Compare with visitors. You can experiment with a lower scaling of PHP and MySQL. Keep an eye on PHP requests and performance.

---

## How to download a full website
{#how-to-download-a-full-website}

This guide explains how to download all necessary application data from a hosting provider to run a website elsewhere. Technical skills are required.

### Get ready
{#get-ready-30}

It's assumed that you have access to your hosting provider. We recommend maintaining a local development environment for your website. Development should occur locally first, and the local copy should be kept up-to-date. For more information, see our [local development article](#intro-to-local-development-with-php). That means, under normal situations the developer should always have a working copy of the website running locally already.

### Use cases
{#use-cases-15}

But there are some real world scenarios why downloading a website might still be required:

- A new developer is joining the project
- A previous developer has left without transferring the project
- Your hard disk crashed
- You have accidentally deleted your local setup somehow
- Archiving your project before shutting it down
- Moving away to a different hosting provider

### Downloading data directly
{#downloading-data-directly}

A hosting environment of a typical LAMP stack PHP setup consists of different parts that play together to display a functional website or application. The different parts need to be treated separately. The steps required are depending on your previous deployment workflows.

#### Code by Git
{#code-by-git}

When you deployed using Git, you can clone the existing Git repo. Most likely your Git repo is hosted on GitHub. The benefit is that the Git repo contains all the history of the project as well. Make sure that the Git repo is an up-to-date state.

#### Composer dependencies
{#composer-dependencies-1}

After cloning the Git repo, you might need to install the dependencies to make your local installation complete. The `composer.json` contains all the instructions. Run `composer install` locally in your root folder. See our [Composer article](#composer) for more details. This insures the installed dependencies are up-to-date and match you local development environment.

#### Runtime data
{#runtime-data}

Beside the code base which you might have received via Git, take care to grab assets and runtime data as well. This can be some compiled CSS/JS files that got deployed along with pipelining or uploads done by users of the application.

#### Assets and other files
{#assets-and-other-files}

Remember Git works in [one direction only here](#git-works-only-one-way). So you might find files, like uploads, that are not covered with the Git repo, or files in the Git repo are not up-to-date. Options on your disposal:

- Login by SFTP and just download what is required - [see here](#sftp-access)
- Login by SSH, zip the files and question and them from a public URL - [see here](#ssh-access)
- Use rsync to download a folder or even the entire project - [see here](#rsync-deployment)

You can use the methods above for the whole code base when you haven't been deploying with Git before or you are unsure if the Git repo contains the latest changes.

#### Database backup
{#database-backup}

Last not least you likely will need the contents of your database. Use a local MySQL client to connect to your fortrabbit database and export a dump of it. Detailed instructions over [here](#database-access-intro).

### Using our backups
{#using-our-backups}

When the above is not working for you for some reason and your website is hosted with fortrabbit, you might just use our [backups](#backups) (when booked) as a source. With that you can download the latest state from the dashboard.

### Check for data consistency
{#check-for-data-consistency}

We highly advice to double-check your new backup for completeness. You can run diffs on other copies. We also advice to run your App locally and see it with your eyes.

---

## How to
{#how-to-1}

Git things done.



---

## Migrate to fortrabbit
{#migrate-to-fortrabbit}

How to transfer your website to fortrabbit with confidence.

fortrabbit is not your traditional shared or VPS hosting. It may require some tinkering on your application and we recommend reading the [intro](#project-organization) as well as our specific install guides for various frameworks & CMS to get the concepts and features.

This article covers the general basics as well as some deep links for moving your App from any hosting provider to fortrabbit. This will hopefully cover everything you need to realize a smooth transition. Each App is different, adjust your plan accordingly and don't hesitate to contact us with your specific questions.

### 1. Create your fortrabbit app
{#1-create-your-fortrabbit-app}

Each website or web application is represented by an [app](#the-app) with at least one [environment](#the-environment) on fortrabbit. You can have as many apps with as many environments as you want. So in order to move your project you need to create an app on fortrabbit first. Do so in the fortrabbit dashboard as a first step.

### 2. Prepare your domains
{#2-prepare-your-domains}

To minimize downtimes caused by DNS cache propagation you should change the Time to Live (TTL) of your domains to the lowest possible value. Something like five minutes would be just great. If you have some kind of web control panel with your domain provider, then you can most likely change it yourself. If not, just get in touch with the provider and ask them to reduce your TTL for you. You should do this 48-72 hours before you start with the migration.

After that's done make sure to add all the domains to your new fortrabbit App in the dashboard.

### 3. Migrate your code
{#3-migrate-your-code}

If you already subscribe to a Git based workflow, then there is probably not much to do here. If not, then you should familiarize yourself with Git. We promise: You won't regret it. Once you've used it, you won't go back without being forced.

### 4. Migrate your runtime data
{#4-migrate-your-runtime-data}

Runtime data means all kinds of data, which is created by your App at runtime. Usually these are user uploads or uploads from a CMS or some-such. When working with a clean Git workflow, the runtime data and the code should be separated.

### 5. Migrate your databases
{#5-migrate-your-databases}

If your App is using a MySQL database, you will need to migrate the database data as well. Export the MySQL database from your old hosting and import it to the fortrabbit database.

### 6. Sending e-mails
{#6-sending-e-mails}

Take care when you application needs to send mails. Simple `sendmail` won't work, see our [quirks article](#mailing) on how to send mails, either via SMTP or 3rd party provider.

### 7. HTTPS
{#7-https}

All fortrabbit Apps can be accessed using a free HTTPS URL. There is also a free HTTPS Let's Encrypt certificate for [custom domains](#the-domain).

### 8 Final switch: DNS
{#8-final-switch-dns}

Now that you have migrated your code, runtime data and database - and all the other stuff you needed - you are ready to push the button.

Now that your App is fully mirrored on fortrabbit and ready to handle traffic, you can [route your Domains DNS records to fortrabbit](#the-domain). If you waited the 48-72 hours for DNS caches to clear, downtime will be minimal as traffic is routed to your App on fortrabbit.

### Migrating away from fortrabbit
{#migrating-away-from-fortrabbit}

We don't lock you in. You can cancel at any time. Due to the distributed nature of services it's even easier to move somewhere else then. The steps are essentially the same as above.

---

## rsync deployment
{#rsync-deployment}

rsync is one of the best ways to deploy code fast and without hassle. It's also an often overlooked option. Let's change this! This article gives you some direction on how to use it in general and especially here on fortrabbit.

### About rsync
{#about-rsync}

`rsync` is a shorthand for **r**emote **sync**hronization. It's a command line tool to synchronize files over the network. It's open source. It's old but really good and it's up to **10 times faster than FTP** as it uses compression and diffs to only transfer changes. rsync is a mighty sharp sword. Use it carefully. Please mind that providing the falsy parameters or the wrong order can result in data loss. rsync works on top of [SSH](#ssh-access). Usually, like most deployment related tasks here, you will **use rsync from your local machine**, not on your fortrabbit environment directly.

### Installing rsync
{#installing-rsync}

Chances are that you already have it: **rsync is built-in with Linux and macOS**. Check if it is installed. Run this command in the Terminal of your local machine:

```shell
rsync --version
## If installed, it will output the version number.
{#if-installed-it-will-output-the-version-number}
```

For Windows 10 we recommend to install the Linux subsystem (WSL). For Windows 7 or even below you might use cwRsync which also requires Cygwin. There are some other clones and desktop GUI clients around as well. But don't be afraid of the Terminal, it's easier than you might think.

### Use cases
{#use-cases-16}

You can [deploy with Git](#deployment-intro) or [upload files with SFTP](#sftp-access) and/or [use SSH](#ssh-access). Hook in rsync, either as an enhancement or as a replacement. These are your main options for using `rsync` to deploy code:

#### rsync instead of SFTP
{#rsync-instead-of-sftp}

Consider `rsync` as a replacement for SFTP. With SFTP - unless your SFTP client has some kind of synchronization method (which still will be slower) - you will copy each file manually, one by one. This is mundane and can also be dangerous when forgetting to copy critical files. `rsync` can work as a two way street directly on the file system. Easily synchronize files up and down from your [local development](#intro-to-local-development-with-php) to the [environment](#the-environment).

#### rsync in addition to Git
{#rsync-in-addition-to-git}

Consider `rsync` as an essential addition. Why? Your dependencies are managed with Composer and thus excluded from Git. They will be installed and managed with [Composer](#composer). So you are keeping your Git repo clean by just including the source files of your very own code. But there is more. Your project includes run time data and static assets:

### The rsync command structure
{#the-rsync-command-structure}

```shell
## sync all files UP
{#sync-all-files-up}
## #      options
{#options}
## ─┴─
{#-1}
$ rsync -av ./ {{app-env-id}}@ssh.{{region}}.frbit.app:
## ─┬─ ──────────────────┬────────────────────────
{#-2}
## source           destination
{#source-destination}
```

- **options**: How to sync, see [below](#options).
- **source**: This is your local source directory.
- **destination**: The target URL, where the files should end up.

### Usage
{#usage-1}

Here are the most common rsync commands. Likely you will even come by using only the first two:

```shell
## DOWN: from remote to local
{#down-from-remote-to-local-1}
$ rsync -av {{app-env-id}}@ssh.{{region}}.frbit.app: ./

## UP: from local to remote
{#up-from-local-to-remote-1}
$ rsync -av ./ {{app-env-id}}@ssh.{{region}}.frbit.app:


## LOCAL: two local folders
{#local-two-local-folders}
$ rsync -av ~/projects/{{app-env-id}}/ ~/projects/{{app-env-id}}.copy/

## REMOTE TO REMOTE: from App to App
{#remote-to-remote-from-app-to-app}
$ rsync -av {{app-env-id}}@ssh.{{region}}.frbit.app: {{app-name-2}}@ssh.{{region}}.frbit.app:
```

#### Remote paths
{#remote-paths}

Remote URLs consist of `{{user}}@{{host}}:{{folder}}`. In the examples here fortrabbit placeholders are used.

#### Local paths
{#local-paths}

rsync accepts all ways to define local paths. `./` will translate to the current directory. You can also use absolute paths like `/home/your-user/projects/{{app-env-id}}` or relative paths like `../{{app-env-id}}`.

#### Options
{#options-1}

Here are some common options to alter the sync mode:

| Option      | Description                                                                                                                                       |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| `-a`        | Shorthand for `--archive`, like the set of options: `-rlptgoD`.                                                                                   |
| `-v`        | Verbose output shows all transmitted files and statistical data. Increase verbosity using `-vv` or `-vvv`                                         |
| `-n`        | Shorthand for `--dry-run`. See [below](#previewing-changes).                                                                                      |
| `-r`        | Recursive, so all files and directories below the source directory.                                                                               |
| `-l`        | Keep symbolic links.                                                                                                                              |
| `-p`        | Permissions will be synchronized.                                                                                                                 |
| `-t`        | Preserve modification times.                                                                                                                      |
| `-g`        | Set Unix group of file/folder on destination to group in source. Also: use group as check criteria                                                |
| `-o`        | Set Unix group of file/folder on destination to group in source. Also: use group as check criteria                                                |
| `-c`        | Instead of modification time and size, use checksum of the file contents. Use with caution when modification time on destination is not reliable. |
| `-C`        | Shorthand for `--cvs-exclude`. Exclude version control files like `.git`, `.hg`, `.svn`.                                                          |
| `-h`        | Human readable output: display byte sizes in MiB, GiB instead of plain bytes.                                                                     |
| `--delete`  | Remove unused files. See [below](#dealing-with-obsolete-files)                                                                                    |
| `--exclude` | Omit files from being synced. See [below](#excluding-files)                                                                                       |

For an exhaustive list of all the possible options and more in depth info on the above options, check out the official [rsync man page](https://linux.die.net/man/1/rsync). Mind that rsync options can be chained, `rsync -av` combines the two flags `-a` and `-v`.

#### Previewing changes
{#previewing-changes}

The handy `--dry-run` option can be shortened to just `-n` and also be merged with other options to something like `-avn`. It will give you a preview of what will happen before doing anything:

```shell
$ rsync -avn ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/
sending incremental file list
./
index.php
wp-content/themes/your-theme/404.php
wp-content/themes/your-theme/archive.php
wp-content/themes/your-theme/content-link.php

sent 39,119 bytes  received 196 bytes  11,232.86 bytes/sec
total size is 23,325,044  speedup is 593.29 (DRY RUN)
```

Now, running this will print out everything that `rsync` **would** transfer - without doing anything. Better always execute a dry run before actually syncing. Once you're sure, that only files which you want to transfer are in the change set, you can just remove the `n` again from the options and execute it normally.

#### Syncing single folders
{#syncing-single-folders}

This is a use-case for rsync as an additional step when primarily working with Git. In this case you only want to include a specific folder and its contents. You might want to "upload" your `dist` folder with your compiled CSS, JS and images. Or you want to "download" the assets folder, when an editor has uploaded new images to the CMS. This is the basic command:

```shell
rsync -av --include='/{{folder}}/***' --exclude='*' ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/
```

With the `--include` parameter you can specify the path to include, but you still need to exclude everything else. The include/exclude syntax is flexible as you can include patterns and multiple folders at once. Alternatively you can also just define the local folder and the remote folder.

#### Excluding files
{#excluding-files}

Sometimes you want to omit files from being synced. You can just add `--exclude=path/to/file`. Say we don't want the `404.php` from the previous example to be transferred, you would just do:

```shell
## use absolute path, as viewed from the source root
{#use-absolute-path-as-viewed-from-the-source-root}
$ rsync -avC --exclude wp-content/themes/your-theme/404.php ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/
```

The value of `--exclude` is a pattern. It can be matched against the files to be transferred. In this case, the following patterns will have the same effect:

```shell
## use partial path
{#use-partial-path}
$ rsync -avC --exclude themes/your-theme/404.php ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/

## use smallest possible partial path
{#use-smallest-possible-partial-path}
$ rsync -avC --exclude 404.php ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/
```

NOTE: The initial `/` character is important. `--exclude 404.php` and `--exclude /404.php` are _not_ the same. The former means: Any path which contains "404.php" is to be excluded. The latter means: Any path which starts with "/404.php" is to be excluded.

#### Advanced exclude patterns
{#advanced-exclude-patterns}

You can also use wildcard characters. For example:

```
$ rsync -av --exclude "*.jpg" --exclude "*.jpeg"` ...
## exclude all JPEG files
{#exclude-all-jpeg-files}

$ rsync -av --exclude "/wp-content/themes/*/404.php" ...
## exclude all files, which start with `/wp-content/themes`, followed by an arbitrary name (no slashes! so only one level of sub directory!) and ending in `404.php`. So basically: All `404.php` files of all themes.
{#exclude-all-files-which-start-with-wp-content-themes-followed-by-an-arbitrary-name-no-slashes-so-only-one-level-of-sub-directory-and-ending-in-404-php-so-basically-all-404-php-files-of-all-themes}

$ rsync -av --exclude "themes/**/*.css" ...
## exclude all files, which path name contains `themes/` then followed by anything (including any amount of sub directories) and ending in `.css`. So all `.css` files in all Themes.
{#exclude-all-files-which-path-name-contains-themes-then-followed-by-anything-including-any-amount-of-sub-directories-and-ending-in-css-so-all-css-files-in-all-themes}
```

Also, as you can see, in the JPEG example, you can add any amount of `--exclude` options to the command.

#### Remembering excludes in a file
{#remembering-excludes-in-a-file}

If you have a set of files which you always want to exclude, you can create an file containing all exclusions and then use it via `--exclude-from <file>`:

```shell
## add two excludes to a plain text file named ".rsyncignore"
{#add-two-excludes-to-a-plain-text-file-named-rsyncignore}
$ echo 404.php >> .rsyncignore
$ echo something-else.php >> .rsyncignore

## run rsync, using the .rsyncignore file
{#run-rsync-using-the-rsyncignore-file}
$ rsync -av --exclude-from .rsyncignore ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/
```

NOTE: The file name `.rsyncignore` is just an example name, use any name you want for your excludes.

There is still a lot more you can do with exclude and filtering. Not only is there `--include`, which allows to granulate previous `--exclude` patterns, but there is also `--filter`. Here is a [very interesting blog post by Ira Cooke](http://blog.mudflatsoftware.com/blog/2012/10/31/tricks-with-rsync-filter-rules).

#### Dealing with obsolete files
{#dealing-with-obsolete-files}

`rsync` will work in a non-destructive way by default, like our overwrite but not delete strategy. So new files will be written and replaced, but old files will not get deleted. Sometimes that's not what you want. Sometimes you want an exact copy - a mirror.

So, how to remove obsolete files on the remote? The short answer is: add the option `--delete` to your command line and you are done. To give you and example, using the WordPress setup from before: say you deleted this pesky `404.php` file locally. Now, if you run `rsync` without the `--delete` option (and no other added or modified files), `rsync` would tell you that it will do nothing:

```shell
$ rsync -av ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/
sending incremental file list
wp-content/themes/your-theme/

sent 39,037 bytes  received 162 bytes  15,679.60 bytes/sec
total size ...
```

Although it marks the folder `wp-content/themes/your-theme/`, as if there have been changes (the removal of `404.php`), rsync will not apply any changes. Now, if you run it with the `--delete` option, the file will be removed from the destination. **This is a feature, not a bug**, meaning: `rsync` won't let you down by deleting files without your say-so. Either way, on the first delete run, as always, use the condensed form `-n` of the `--dry-run` option, to show you exactly what would be deleted:

```shell
$ rsync -avn --delete ./ {{app-env-id}}@ssh.{{region}}.frbit.app:~/
sending incremental file list
deleting wp-content/themes/your-theme/404.php

sent 39,062 bytes  received 231 bytes  15,717.20 bytes/sec
total size ...
```

After you confirm that `rsync` will only delete what you want (otherwise: `--exclude` works also to exclude files which are not in your local file set but remote, and you don't want to remove them from remote), you can go ahead and remove the `-n` option and run again.

`rsync` even gives you four different ways to handle deletes: Besides the `--delete` flag, there is also `--delete-before`, `--delete-after`, `--delete-during` and `--delete-delay` (and `--delete-excluded`, but that's another special case of its own). Those four variants of `--delete` just let you control when files are removed. This is actually quite handy: When dealing with larger amounts of changed files to a live website, you might want to use `--delete-after` instead of `--delete-before`, so that first all new files are in place, then obsolete files are removed, which makes it more likely that your website is not "interrupted" when handling a request during the synchronization, which relies on files which would be removed.. I think you get the gist.

### Advanced topics
{#advanced-topics}

#### SSH edge-cases
{#ssh-edge-cases}

Should you need to set specific SSH options, for example, if you need to provide a specific private key, then you can use the `--rsh` option, which stands for "remote shell" and can be shortened to `-e`. Here an example:

```shell
## use specific private key
{#use-specific-private-key}
$ rsync -av -e 'ssh -i /path/to/your/key' {{app-env-id}}@ssh.{{region}}.frbit.app:~/ ./

## enforce password authentication
{#enforce-password-authentication}
$ rsync -av -e 'ssh -o PreferredAuthentications=password' {{app-env-id}}@ssh.{{region}}.frbit.app:~/ ./
```

#### How rsync transfers only changes
{#how-rsync-transfers-only-changes}

Say you have changed ten files in your local code set and want to deploy them now. `rsync` will first build a local set of files and directories and a remote set of files and directories. For each item in either set it will generate a check value. This check value, can be either the timestamp of the last change of a file, the size of a file, the current permissions or even a checksum (think MD5) of the file contents. Or any combination of those. Using the `-a` option rsync is gonna use timestamp + file size which is a good balance between performance and accuracy.

### Further reading
{#further-reading-1}

This article is loosely based on our still popular [blog post](https://blog.fortrabbit.com/deploying-code-with-rsync) which is even more complete and includes more details. Also of interest:

- [Manual page of rsync](https://linux.die.net/man/1/rsync)
- [How does rsync work](https://rsync.samba.org/how-rsync-works.html)

---

## Using Secure Copy
{#using-secure-copy}

SCP (Secure Copy Protocol) enables secure file transfers between your local machine and remote servers using SSH encryption.

### About SCP
{#about-scp}

`scp` (Secure Copy Protocol) is a command-line utility for securely transferring files between a local host and a remote host over SSH. It provides the same authentication and security as SSH while enabling efficient file copying operations.

- Encrypted file transfers using SSH
- Preserves file permissions and timestamps
- Supports recursive directory copying
- Works with SSH key authentication
- Available on most Unix-like systems (Linux, macOS)

::CallOut{alert}
We suggest to use [rsync](#rsync-deployment) instead of scp. It's more flexible with more features. It can upload directories.
::

### Get ready
{#get-ready-31}

Before using SCP with fortrabbit, ensure you have:

1. **SSH access configured** - See [SSH access guide](#ssh-access)
2. **SSH key pair set up** - See [SSH key setup](#ssh-key-setup)
3. **SCP installed** - Usually pre-installed on Linux/macOS, via WSL on Windows

```shell
which scp
## If installed, it will show the path
{#if-installed-it-will-show-the-path}
```

:BlockLink{title="See SSH access for {{app-name}} / {{env-name}}" path="/environments/{{app-env-id}}/ssh/"}

### Examples
{#examples-4}

```bash
## Upload
{#upload}

### Upload a file to the web root
{#upload-a-file-to-the-web-root}
scp local-file.php {{app-env-id}}@ssh.{{region}}.frbit.app:

### Upload with verbose output
{#upload-with-verbose-output}
scp -v config.json {{app-env-id}}@ssh.{{region}}.frbit.app:

### Upload multiple files at once
{#upload-multiple-files-at-once}
scp file1.php file2.css file3.js {{app-env-id}}@ssh.{{region}}.frbit.app:

### Upload with wildcards
{#upload-with-wildcards}
scp *.php {{app-env-id}}@ssh.{{region}}.frbit.app:


## Download
{#download}

### Download a file from the web root
{#download-a-file-from-the-web-root}
scp {{app-env-id}}@ssh.{{region}}.frbit.app:config.php ./

### Download to a specific local path
{#download-to-a-specific-local-path}
scp {{app-env-id}}@ssh.{{region}}.frbit.app:.env ./local-config/

### Download log files (Craft CMS)
{#download-log-files-craft-cms}
scp -r {{app-env-id}}@ssh.{{region}}.frbit.app:storage/logs/ ./
```

#### Common options
{#common-options}

- `-r` - Recursive copy (for directories)
- `-p` - Preserve file permissions and timestamps
- `-v` - Verbose output for debugging

### Comparison with other tools
{#comparison-with-other-tools}

| Feature                 | SCP           | SFTP          | rsync         |
| ----------------------- | ------------- | ------------- | ------------- |
| **Security**            | SSH encrypted | SSH encrypted | SSH encrypted |
| **Resumable transfers** | No            | Yes           | Yes           |
| **Bandwidth limiting**  | Yes           | Limited       | Yes           |
| **Directory sync**      | Basic         | Manual        | Advanced      |
| **Progress indication** | Limited       | Yes           | Yes           |
| **File comparison**     | No            | Manual        | Automatic     |

---

## PHP version upgrade
{#php-version-upgrade}

Best practices upgrading the PHP version.

### PHP versions at fortrabbit
{#php-versions-at-fortrabbit}

- fortrabbit will provide new PHP versions some time after they became available
- New PHP versions are available to select per environment in the dashboard
- There are usually multiple PHP version to choose from
- You need to update software you are using
- You can opt-out of automatic PHP version updates
- Outdated PHP versions will be removed, remaining environments will be upgraded then

### Simple PHP version upgrade path
{#simple-php-version-upgrade-path}

1. Make sure the software you are using is up-to-date
2. In the dashboard
3. Navigate to the environment and then click on Settings > PHP version
4. Change to a newer PHP version and hit "save"
5. Check if your website is still working after a few minutes
6. You can safely switch back the version if it doesn't work

:BlockLink{title="Change the PHP version for {{app-env-id}}" path="/environments/{{app-env-id}}/settings/php-version"}

This will update the PHP runtime on fortrabbit. You may also want to update your local development environment as well, read on.

### Sophisticated PHP version upgrade path
{#sophisticated-php-version-upgrade-path}

First update your local version, once that is working, deploy to fortrabbit and change the version. Here are the steps one by one:

#### 1 - Update your local development environment
{#1-update-your-local-development-environment}

We recommend to have a local development environment, also see our [help article on that](#intro-to-local-development-with-php). First, make sure that your local PHP version is up-to-date. Depending on how your local development is set up, the path to upgrade is different.

If you are running PHP directly on your computer, then a simple `php -v` prints out the PHP version. Beware, if you are using [MAMP](https://www.mamp.info/en) or [XAMPP](https://www.apachefriends.org/index.html), this is not the version of PHP your code runs on. With these tools you have to use their GUI to select the PHP version you want.

To upgrade your local PHP on macOS, [Homebrew](https://brew.sh) is a popular package manager you can use. Homebrew also controls the PHP version used by [Laravel Valet](https://github.com/laravel/valet). When you are running a more complex setup with PHP virtualized, such as Vagrant, DDEV, Virtual Box or Docker, you have to dig in to your specific virtualization setup to see how to upgrade PHP.

#### 2 - Update your software dependencies
{#2-update-your-software-dependencies}

Get your dependencies up-to-date:

##### 2.1 - Updating with Composer
{#2-1-updating-with-composer}

Applications based on PHP frameworks like Laravel and Symfony are usually updated with [Composer](#composer) which keeps track of all dependencies.

Issuing `composer outdated` in the Terminal will give you a list of outdated packages. Those in red need can easily be updated. Those in yellow also need to be updated but might cause trouble because they are major version upgrades.

You can also ask Composer why you currently can not upgrade to a PHP version:

```shell
composer why-not php 8
```

To update a dependency, simply change any required versions in your `composer.json` to a newer version and then issue a `composer update` to actually install the required updates. Keep in mind that the `composer outdated` command does not care about PHP versions. It will only tell you about available updates for your dependencies, but hopefully newer packages should support newer PHP versions as well.

##### 2.2 - Updating a CMS
{#2-2-updating-a-cms}

Many Content Management Systems, like WordPress and Craft CMS come with a built in update feature. So you can simply login to the admin area of the CMS and hit a button to update.

**Beware:** With fortrabbit, those changes only happen on the file system and are not reflected in Git. This is fine when you are using SFTP, otherwise read more in our [setup guide for WordPress](#wordpress-quick-setup-guide) or [update guide for Craft CMS](#updating-craft-cms).

#### 3 - Test it locally
{#3-test-it-locally}

When you have upgraded your local PHP version as well as your projects dependencies, it's time to make sure nothing is broken. Open your browser and try out as many views and actions as you can in your local development setup. If you are running a lot of custom code you have written yourself, we recommend that you run an automated code analysis. It checks your code and finds any deprecated functions that might break.

#### 4 - Go live with the updated version
{#4-go-live-with-the-updated-version}

Now, as everything is up-to-date and tested in your **local** development environment, it's time to bring the updates to fortrabbit.

##### 4.1 - Change the PHP version on fortrabbit
{#4-1-change-the-php-version-on-fortrabbit}

Updating the PHP version for your fortrabbit App is as simple as pie:

1. Visit your environment in the fortrabbit dashboard
2. Go to the PHP settings
3. Select a newer PHP version from the drop-down menu
4. Hit save

Changes can take two minutes to be applied. You can also test-run this. When your App is not running under the newer version of PHP you can switch back to the deprecated version for another while and find out why first.

:BlockLink{title="Change the PHP version for {{app-env-id}}" path="/environments/{{app-env-id}}/settings/php-version"}

##### 4.2 - Deploy changes
{#4-2-deploy-changes}

Now, quickly after the new PHP version is in place, deploy your updated code from your local development, either with [Git](#deployment-intro) or simply by [SFTP](#sftp-access) or by [rsync](#rsync-deployment).

Don't forget that you might also have to run database migrations so that your database structure matches the latest code version. WordPress and Craft CMS automatically handle this in the web UI. For any other system, see their documentation on how to properly update the database.

---

## Configure .user.ini
{#configure-user-ini}

How to use .user.ini files to configure PHP settings on fortrabbit

At fortrabbit, php-fpm is used for performance and security reasons. This means that adding `php_value` directives to `.htaccess` files has no effect. You can instead use `.user.ini` files to configure PHP settings that aren't available through the fortrabbit dashboard.

### When to use .user.ini
{#when-to-use-user-ini}

While the fortrabbit dashboard provides access to commonly needed PHP settings, there are cases where you might need `.user.ini`:

- Settings that cannot be changed at runtime (like `max_file_uploads`)
- Advanced configuration options not exposed in the dashboard
- Project-specific PHP configurations
- Settings that need to be version-controlled

### Creating a .user.ini file
{#creating-a-user-ini-file}

The `.user.ini` file should be placed in the document root or in the sub-directories where settings should be applied. Common locations:

- `/public/` (for Laravel, Symfony)
- `/web/` (for Drupal, some Symfony setups)

#### Example .user.ini file
{#example-user-ini-file}

```ini
; Set maximum file upload size
upload_max_filesize = 50M
post_max_size = 50M

; Configure file uploads
max_file_uploads = 50

; Set timezone
date.timezone = "Europe/Berlin"

; Session settings
session.cookie_lifetime = 7200
session.gc_maxlifetime = 7200
```

### File placement and inheritance
{#file-placement-and-inheritance}

- Settings in `.user.ini` apply to the directory where the file is located and all subdirectories
- If multiple `.user.ini` files exist in the path hierarchy, settings are inherited and can be overridden
- Place the file as close to where it's needed as possible for better organization

### Security
{#security}

- The `.user.ini` file should not be served by the web server
- By default, files starting with a dot are not served, but ensure your web server configuration doesn't expose them
- Never include sensitive information like database credentials in `.user.ini`

### Performance impact
{#performance-impact}

- `.user.ini` files are parsed on every request by default
- Consider the performance impact when adding many settings
- Use the dashboard settings when possible for better performance

### Troubleshooting
{#troubleshooting-3}

Not seeing desired results?

#### Settings not taking effect
{#settings-not-taking-effect}

1. **Check file location**: Ensure the `.user.ini` file is in the correct directory
2. **Verify syntax**: Invalid INI syntax will cause the entire file to be ignored
3. **Check permissions**: The file should be readable by the web server
4. **Test with phpinfo()**: Use `phpinfo()` to verify which settings are active

#### Memory usage
{#memory-usage}

You can use `.user.ini` to increase the `memory_limit` setting, but beware that we already set this to the same size as the booked [PHP plan](#php). If you increase it further, the platform will start to randomly kill your PHP-FPM process any time it uses more memory than the booked plan. To safely get more PHP memory, book a larger plan using our dashboard.

#### Debugging
{#debugging}

Create a simple PHP file to check your configuration:

```php
<?php
// Show all PHP settings
phpinfo();

// Or check specific settings
echo "Memory limit: " . ini_get('memory_limit') . "\n";
echo "Upload max filesize: " . ini_get('upload_max_filesize') . "\n";
echo "Max file uploads: " . ini_get('max_file_uploads') . "\n";
?>
```

### Best practices
{#best-practices-2}

1. **Use dashboard first**: Always check if the setting is available in the fortrabbit dashboard before using `.user.ini`
2. **Document your changes**: Add comments to explain why specific settings are needed
3. **Version control**: Include `.user.ini` files in your repository for consistent deployments
4. **Environment-specific**: Consider different settings for development vs production
5. **Minimal configuration**: Only override settings that you actually need to change

### Related
{#related-5}

- [.htaccess introduction](#htaccess-intro)
- [php.net/configuration.file.per-user](https://www.php.net/configuration.file.per-user) - Official PHP documentation

---

## .htaccess intro
{#htaccess-intro}

Browsing the docs here you will find lot's of reference to an invisible file called ".htaccess". What's that about? How can you make use of it?

`.htaccess` is a hidden file that usually lives in the web root folder of your code base. It enables altering the web server's configuration directives. `.htaccess` rules apply to all subdirectories. `.htaccess` is usually not excluded in `.gitignore` so it will be deployed alongside your code. Take care: htaccess is a sharp sword. With great power comes great responsibility.

### .htaccess on fortrabbit
{#htaccess-on-fortrabbit}

Your fortrabbit Apps are running on the Apache web server. You can make use of `.htaccess`. Missing (remember it's hidden) and wrong `htaccess` directives are common issues. These sensitive defaults are set on the fortrabbit platform regarding .htaccess:

- Apache configuration syntax 2.2 and 2.4 are supported
- GZIP compression is enabled per default for text based content types
- Access on all `.ht*` files is disabled, so nobody can read your .htaccess

### .htaccess and your framework or CMS
{#htaccess-and-your-framework-or-cms}

When you are using a framework or a CMS, chances are high, that you don't need to wrangle with `.htaccess` at all, as that comes built-in. Here are the most used ones:

- **Laravel** comes with a [boilerplate htaccess](https://github.com/laravel/laravel/blob/master/public/.htaccess) you can extend
- **Craft CMS** comes with a [boilerplate htaccess](https://github.com/craftcms/craft/blob/main/web/.htaccess) you can extend
- **WordPress** [manages htaccess](https://codex.wordpress.org/htaccess) for you

---

## Redirects with .htaccess
{#redirects-with-htaccess}

The most common use case for `.htaccess` is to re-write URLs with `mod_rewrite`. You can direct requests to a subdirectory, or specific domain, prettify URLs by omitting file endings, force https and much more.

<!-- TODO: Review. Old Stuff -->

### Redirect all requests to https
{#redirect-all-requests-to-https-1}

**Force https!** There is no need for your application to be reached over a non-secure connection. Use `.htaccess` to redirect all `http://` requests over to `https://`. This is how:

```raw
RewriteEngine On
RewriteCond %{HTTP:X-Forwarded-Proto} !=https
RewriteRule .* https://%{HTTP_HOST}%{REQUEST_URI} [R=301,L,N]
```

**Order matters. This rule should be one of first rules, so right on top of your htaccess file** Please also note the X-Header part. Other code snippets you find elsewhere might not work here. This is because we are running our Apache behind a set of load-balancers. They are performing the HTTPS encryption and not Apache. Many CMS and frameworks are already offering convenient settings and configurations for this.

### Redirect all requests to the primary domain
{#redirect-all-requests-to-the-primary-domain}

Once you've added a [custom domain](#the-domain) you may want to prevent requests to your test domain. The example below shows how to set up a domain based redirect in your `.htaccess` file.

```raw
## From test domain to your domain
{#from-test-domain-to-your-domain}
RewriteEngine On
RewriteCond %{HTTP_HOST} ^.*\.frb\.io$ [NC]
RewriteRule .* https://www.your-domain.example%{REQUEST_URI} [r=301,L,N]
```

A CMS will have it's own options for that. If you don't use a redirect, make sure to at least set the "canonical URL" to be on your primary custom domain so that that search engines know that there is only one content.

---

## HTTP auth with .htaccess
{#http-auth-with-htaccess}

To limit access to your cloud development environment, you can use HTTP (basic) authentication with .htaccess to prompt a username and password for a selected few.

The [fortrabbit dashboard also provides](#password-protection) a setting for this.

### Set a root path below htdocs
{#set-a-root-path-below-htdocs}

When no framework or CMS was chosen when creating the [environment](#the-environment), `htdocs` is the default root folder of the App. Create a new folder, called something like `web` or `root`. Move all your web contents into that folder. Set the newly created folder containing everything now, as the new root path in the dashboard. This is required to secure the password file from access.

### Create the .htaccess file
{#create-the-htaccess-file}

Create a `.htaccess` file in the directory you want to secure, also see our [.htaccess articles](#index). Likely that this is your new root directory, can also be below that. Be careful, the dot at the beginning of the file names indicates that it is a hidden file. You can upload the file by any deployment method: with Git, by SFTP or create it on remote via SSH. Please note, that all frameworks and CMS systems will already have an `.htaccess` file in their own root path. You can modify that as well. This is, what your `.htaccess` should contain for HTTP auth:

```apache
Authtype Basic
AuthName "Welcome to my awesome project. Please Login."
AuthUserFile /srv/app/{{app-env-id}}/htdocs/.htpasswd
Require valid-user
```

The first line starts the directive. The second line set a hello message which is printed to greet the user. The third line points the server to the file that stores the username and password to login, this is an absolute path. This `.htpasswd` file should NOT be reachable from the outside, via http. That's why you have moved all the files one level deeper. The last line finally sets the rule, that only valid users are allowed to browse.

### Create the .htpasswd file
{#create-the-htpasswd-file}

As you can already guess by now, the `.htpasswd` file hosts the required username and password to enter your project. And this is how that file can look like:

```raw
john:$aSr1$jw6nGOHx$f/HpoNv9thNMd6w35Ttl80
```

The username is before the colon. The long string after the colon is the password. It needs to be Base64 encrypted. "htpasswd" is a command line tool likely installed on your local machine (sorry not on fortrabbit yet, so you have to run that locally):

```shell
htpasswd -c ~/directory/.htpasswd john
```

The -c flag create a new file. The first param defines the file name and (absolute) pat to store it. The second param the username. The tool will prompt for the password.

### Deploy HTTP Auth
{#deploy-http-auth}

So now, as you know how to create a password protected area for your website, you need to figure out how to implement it. Most likely you want this for a "staging" area — a version of your website that is publicly served, but not intended to be open for everyone. That can be your website before it get's live or even a dedicated permanent staging area. Please see our [multi staging article](#staging-environments) for more on this.

Likely, your goal is, to ask users for a password only on the staging area, but not on your local environment or even a live version. Unfortunately HTTP Auth does not play very well with standard practices of environment detection, as this is happening on a different layer. Here is what you can do:

#### Upload via SSH / SFTP
{#upload-via-ssh-sftp}

You can upload the two files `.htaccess` and `.htpasswd` directly via SSH or SFTP into your App on fortrabbit. This is not very programmatic, but pragmatic. And it works.

#### Create while deploying
{#create-while-deploying}

When deploying with Git, you can use a post-deploy hook, to trigger automatic generation (or placement) of the required files.

### Alternative solutions
{#alternative-solutions}

HTTP Auth is a basic, standard, minimally invasive solution. There is no UI and no dependency you need to take care of. Even database access is not required. That's the beauty of it. So it's most likely compatible with the rest of your application. But HTTP Auth is not the only way to protect your website with username and password. Your CMS or framework might bring their on solutions for this. There are plenty plugins for Craft CMS and WordPress.

---

## GZIP with .htaccess
{#gzip-with-htaccess}

Enable compression for other HTTP responses for the production environment.

<!-- TODO: Review by Infra. Quickly! -->

HTTP responses are compressed if the `content-type` header indicates a text document, for example `text/css` or `text/html`. To enable GZIP compression for other HTTP responses, like your REST or GraphQL APIs, use the `AddOutputFilterByType` directive:

```raw
AddOutputFilterByType DEFLATE application/json
```

### 1. Make sure environment variables are set
{#1-make-sure-environment-variables-are-set}

In the dashboard with your fortrabbit environment, make sure an ENV var key-value pair like this is present:

```shell
ENVIRONMENT=production
```

In some cases we have pre-populated that for you already. See also our [environment variables topic](#env-vars-intro) for more details on how environment variables are handled here.

### 2. Setup .htaccess files
{#2-setup-htaccess-files}

Now in the local code base of your project, setup a custom `.htaccess` file for each environment in the web root of your project:

- `.htaccess` in general and for local development
- `.htaccess_production` for your fortrabbit App

This can also be extended to more environments. All `.htaccess` files should be under version control with Git.

### 3. Configure Composer
{#3-configure-composer}

Add this to the script part of your `composer.json` in your local code base:

```json
"scripts": {
  "post-install-cmd": [
    "@php -r \" define('HTSRC', 'web/.htaccess_' . getenv('ENVIRONMENT')); echo (file_exists(HTSRC) && copy(HTSRC, 'web/.htaccess')) ? HTSRC.' copied to web/.htaccess'.PHP_EOL : ''; \""
  ]
}
```

This Composer post install command will replace the contents of the `.htaccess` file with the contents of the file `.htaccess_production`, if that file is present and the environment variable `ENVIRONMENT` is set to `production`.

You can extend the concept to have more stages of course. To add custom rules for a staging environment. This example also assumes that the root path of your App is `web`. In the Composer example above, replace the `web` with the root path of your project.

---

## Environment detection with .htaccess
{#environment-detection-with-htaccess}

You might want some `.htaccess` rules only to be applied in a certain environment. A common use case is that is to forward all traffic to HTTPS on your fortrabbit App in production, but not in your local development environment.

### 1. Make sure environment variables are set
{#1-make-sure-environment-variables-are-set-1}

In the dashboard with your fortrabbit environment, make sure an ENV var key-value pair like this is present:

```shell
ENVIRONMENT=production
```

In some cases we have pre-populated that for you already. See [environment variables topic](#env-vars-intro) for more details on how environment variables are handled here.

### 2. Setup .htaccess files
{#2-setup-htaccess-files-1}

Now in the local code base of your project, setup a custom `.htaccess` file for each environment in the web root of your project:

- `.htaccess` in general and for local development
- `.htaccess_production` for your fortrabbit App

This can also be extended to more environments. All `.htaccess` files should be under version control with Git.

### 3. Configure Composer
{#3-configure-composer-1}

Add this to the script part of your `composer.json` in your local code base:

```json
"scripts": {
  "post-install-cmd": [
    "@php -r \" define('HTSRC', 'web/.htaccess_' . getenv('ENVIRONMENT')); echo (file_exists(HTSRC) && copy(HTSRC, 'web/.htaccess')) ? HTSRC.' copied to web/.htaccess'.PHP_EOL : ''; \""
  ]
}
```

This Composer post install command will replace the contents of the `.htaccess` file with the contents of the file `.htaccess_production`, if that file is present and the environment variable `ENVIRONMENT` is set to `production`.

On fortrabbit, depending on build steps, usually each time you deploy with Git, composer install runs automatically.

You can extend the concept to have more stages of course (see our [multi staging article](#staging-environments)). To add custom rules for a staging environment, like http-auth - see [HTTP auth article](#http-auth-with-htaccess) - create a matching `.htaccess_staging` file and set the `ENVIRONMENT` accordingly.

This also assumes that the root path of your App is `web`, which is true for Craft CMS. In the Composer example above, replace the `web` with the root path of your project.

---

## Force HTTPS with HSTS in .htaccess
{#force-https-with-hsts-in-htaccess}

This tells the browser to not accept any unsecured connection. In other words, http will no longer work, only https.

In your `.htaccess` file you can add this line:

```raw
<IfModule mod_headers.c>
Header always set Strict-Transport-Security "max-age=31536000"
</IfModule>
```

This will make your browser remember to always use the secured version of your website. It makes use of the "[HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)" policy and improves security by eliminating the risks of man-in-the-middle TLS-protocol-downgrade attacks. Be careful: setting this header will tell the browser never (or that is: until max-age) to use `http://` again. So if you later on decide to serve (parts of) your site using no encryption, all those clients (browsers) which saw the header will not comply and keep using `https://`.

---

## More .htaccess tips
{#more-htaccess-tips}

Here more examples what .htaccess can be used for.

### Tip: Comment your .htaccess file
{#tip-comment-your-htaccess-file}

Apache directives with regular expressions tend to look gibberish. Make sure to comment what you have been doing there so that "the later you" can understand what's going on.

### Block all common WordPress files
{#block-all-common-wordpress-files}

```apache [.htaccess]
<Location ~ "(wp-login\.php|wp-comments-post\.php)$">
  Order allow,deny
  Deny from all
</Location>
```

#### Limit WP Admin to an IP if possible
{#limit-wp-admin-to-an-ip-if-possible}

```apache [.htaccess]
<Files wp-login.php>
  Order deny,allow
  Deny from all
  Allow from <YOUR IP>
</Files>
```

### Block specific file extensions
{#block-specific-file-extensions}

```apache [.htaccess]
## Archives you probably don't want to expose
{#archives-you-probably-don-t-want-to-expose}
<FilesMatch "\.(bz2|gz|zip)$">
   Order allow,deny
   Deny from all
</FilesMatch>
```

### Allow access only for you
{#allow-access-only-for-you}

You may want to prevent accessing your website for anyone except your company. If your company has a fixed IP, you can use `.htaccess` to only allow traffic from that IP or range of IPs.

```apache [.htaccess]
#### 1st deny all
{#1st-deny-all}

ErrorDocument 403 "Not Allowed"
Deny from all

#### 2nd Allow your IPs
{#2nd-allow-your-ips}

Allow from 11.11.11.11
Allow from 12.12.12.12
```

An alternative to this is to use a password check with [HTTP Auth article](#http-auth-with-htaccess).

### Custom error pages
{#custom-error-pages}

You can define custom pages to make your error pages look more cool like so:

```apache
ErrorDocument 404 /404.html
```

This has to be a publicly accessible URL. You can do this with 4XX and 5XX errors. When using a framework or CMS likely the router will catch such errors and use PHP logic to resolve it, still some 5XX errors might appear before the program can execute the router.

---

## .htaccess troubleshooting
{#htaccess-troubleshooting}

### Missing .htaccess
{#missing-htaccess}

A common mistake we see quite often is to miss out the `.htaccess` file. The dot at the beginning of the file name indicates that this file should be invisible in your operating system. So when you dragged files in your FTP client from the Downloads folder, it's very likely that the `.htaccess` file was left home. This can cause 403 errors.

In macOS Finder you can toggle invisible files with `CMD + SHIFT + .`, easy to remember, like dot files. SFTP clients with a split view option are mostly showing those files by default. Take care, there are possibly other hidden files in your project, like `.gitignore` and `.env`.

### Changes are not applied
{#changes-are-not-applied}

`.htaccess` contents are cached (web browser), so it might take a while until you see changes you have made to `.htaccess` files to be applied. You can try `curl` to test the new rules or you can try another browser or incognito mode.

### Wrong location
{#wrong-location}

The `.htaccess` file is usually placed in the root path of the website. Per default, that is the `htdocs` folder. But certain modern frameworks and CMS have path below that, like Laravel with `public`. So make sure to place your `.htaccess` in the correct directory. You can place the `.htaccess` files in folders below the root path as well, those will have a higher specificity and can override rules.

### Possible performance issues
{#possible-performance-issues}

The fortrabbit hosting platform is managed. Therefore your access to critical services is limited. This is actually good for most parts. We believe in a clear separation of concerns: We run the servers, you do the coding. One consequence is that we can not give you direct access on the Apache web server configuration (httpd.conf).

The `.htaccess` file is a very common method to achieve common web server configurations. In fact, almost every framework and CMS comes with a `.htaccess` out of the box. `.htaccess` lives in your code base and is deployed along with Git and therefore it's just very convenient to use.

Consider it a workaround that got too popular. The official Apache docs have a whole section on "[When NOT to use .htaccess](https://httpd.apache.org/docs/current/howto/htaccess.html#when)". The NGNIX team has setup a marketing page [bad-mouthing .htaccess](https://www.nginx.com/resources/wiki/start/topics/examples/likeapache-htaccess) for a bad design, performance-wise.

Now, usually we prefer clean, smooth and fast implementations. But sometimes one have need to make trade-offs. `.htaccess` brings convenience and security (separation of concerns).

In our experience, the possible performance degradation can not be experienced.

---

## HTTP headers
{#http-headers}

HTTP headers are part of an Hyper Text Transfer Protocol request and response. HTTP headers are defining the operating parameters of an HTTP transaction. Use htaccess to modify these.

### Cache-Control
{#cache-control}

Don't serve the same content to the same client twice! Control how the browser of the client caches results and files locally. This is especially useful for asset resources that don't change often. Caching reduces the number of request and the data transmitted. On the HTTP part of your App/website caching is achieved by using HTTP headers. You can control the caching in htaccess like so:

```apache [.htaccess]
## Example to cache images and CSS files
{#example-to-cache-images-and-css-files}
## adjust and extend to your needs
{#adjust-and-extend-to-your-needs}
<ifModule mod_headers.c>
  #  images expire after 1 month
  <filesMatch ".(gif|png|jpg|jpeg|webp|ico|pdf|svg|js)$">
    Header set Cache-Control "max-age=2592000"
  </filesMatch>
  # CSS expires after 1 day
  <filesMatch ".(css)$">
    Header set Cache-Control "max-age=86400"
  </filesMatch>
</ifModule>
```

If you are using a CMS this is usually already managed for you in PHP code. You can open the web inspector on your website, go to the network tab and check the headers for any images, to see if they already have cache headers.

Beware: Adding this also introduces the main problem of caching. If you later decide to change the image or css file, you must either wait the full cache time, or give the file a new name to make the browser retrieve it again. Otherwise it will use the old cached version.

### CORS headers
{#cors-headers}

For "Cross-Site XMLHttpRequests" you'll need "Cross-origin resource sharing" or in short CORS headers. Those are mostly used in context of JavaScript AJAX requests across different domains. Like when `domain-a.com` loads a script from `domain-b.com`. Per default this is not possible for security reasons. But you can enable it for certain or even all origins:

```apache [.htaccess]
## Access all areas (use carefully)
{#access-all-areas-use-carefully}
Header add Access-Control-Allow-Origin "*"
Header add Access-Control-Allow-Methods: "GET,POST,OPTIONS,DELETE,PUT"
```

Use this with care and only open what you really need. Reduce the risk of XSS. Also check out the new Content Security Policy (CSP) for more advanced control on what you allow and what not. This website is a good reference: [content-security-policy.com](https://content-security-policy.com)

---

---
title: .htaccess overview
naviTitle: .htaccess
navigation.excerpt: All about .htaccess
lead: Meet the powerful Apache .htaccess configuration file.
navigation: false
head:
  meta:
    - name: keywords
      content: HTTP Auth, Apache config, apache2.conf, php, ssi, gzip, Core
---

---

## Troubleshoot 404 errors
{#troubleshoot-404-errors}

The 404 HTTP status code means "File Not Found" and is super common.

The server can be reached and is answering but there is nothing to show under this address.

### 404 error behavior
{#404-error-behavior}

- 404 errors will usually be shown on screen immediately
- 404 errors often occur during setup or after code or configuration changes
- 404 errors here are often rendered using a fortrabbit error page template

**In most cases this is not a server issue, but a problem with your code and configuration.** Please check the following common issues first:

### No code deployed
{#no-code-deployed}

Login by SSH or SFTP to see if anything is there to be delivered.

### Wrong root path
{#wrong-root-path}

Maybe your software is using a different root path than the one that is currently set? Check the root path settings `htdocs` is the default root path if no specific software has been chosen in the [software template](#software-templates). Now, if you decide to install another software later on, you might have to set the root path accordingly. Best upload all files into `htdocs` directly, not into an extra folder that contains the files.

See your environments root path settings and compare with what is deployed.

#### .htaccess is missing
{#htaccess-is-missing}

Another common cause for 404 errors is a missing `.htaccess` file. This file is hidden from your Operating System by default (as it starts with a period) but contains important rules for your application to function properly.
So if you are uploading with SFTP and have dragged the files from your Desktop (Finder) into your SFTP application (Cyberduck, Transmit, FileZilla), this file will likely be missing. You might be able to use the file explorer from your SFTP application or temporarily show hidden files in your OS to make the `.htaccess` file visible to you. Just make sure that when an `.htaccess` file is present (most likely it is), that it gets uploaded as well.

#### Wrong address
{#wrong-address}

You might have an error with URL. Check for typos in the address bar (URL) of your browser.

#### The app or domain is not yet ready
{#the-app-or-domain-is-not-yet-ready}

Creating an environment can sometimes take a few minutes. If you visit the test domain during that time, you'll get a 404 error. It's possible that this DNS response gets cached locally. The same is true for new domains.

### It could also be something on our side
{#it-could-also-be-something-on-our-side}

It is also possible — although less likely - that this error is caused by a network, hardware or configuration issue on the side of your hosting provider — us. Please check our status page under [status.fortrabbit.com](https://status.fortrabbit.com) if there are any ongoing maintenance windows or service issues known.

### Memorize the code
{#memorize-the-code}

- 4 = file
- 0 = not
- 4 = found

---

## Troubleshoot 500 errors
{#troubleshoot-500-errors}

The 500 HTTP status code means "Internal Server Error".

- 500 errors will usually be shown on screen immediately
- 500 errors often occur after code or configuration changes
- 500 errors are sometimes just printed as a "service unavailable" message, check the browser's developer tools for the response's HTTP status code to be sure this is indeed a 500 error
- 500 errors here are often rendered using a fortrabbit error page template

**In most cases this is not a server issue, but something with your code and configuration.** Good news is that they are mostly easy to debug for you:

### Check the logs
{#check-the-logs}

Examine the logs of your App. See [here](#logs). There you'll likely find where the application exited with which error.

### Review your latest changes
{#review-your-latest-changes}

Since 500 errors often appear during installation, setup or code changes: Review your code and configuration changes. Compare this with your [local development environment](#intro-to-local-development-with-php) and see if it fails the same way. Have you ran an update recently?

#### Check your .htaccess file
{#check-your-htaccess-file}

Our experience in support shows us that many 500 errors are caused by wrong rules in your `.htaccess` file. See our [main article on `.htaccess`](#htaccess-intro) for some background. Have you made any changes to `.htaccess` lately?

### It could also be something on our side
{#it-could-also-be-something-on-our-side-1}

It is also possible — although less likely - that this error is caused by a network, hardware or configuration issue on our side, your hosting provider. Please check our status page under [status.fortrabbit.com](https://status.fortrabbit.com) if there are any ongoing maintenance windows or service issues known.

---

## Troubleshoot 503 errors
{#troubleshoot-503-errors}

The 503 HTTP status code means "Service Unavailable".

- 503 errors will usually be shown on screen immediately
- 503 errors often occur after code or configuration changes
- 503 errors are sometimes just printed as a "service unavailable" message, check the browser's developer tools for the response's HTTP status code to be sure this is indeed a 503 error
- 503 errors here are often rendered using a fortrabbit error page template

503 and [504 errors](#troubleshoot-504-errors) are two sides of the same coin. PHP-FPM (the PHP process manager here) has too much to do. 503 and 504 errors are often happening simultaneously. 503 and 504 are two sides of the same coin. PHP-FPM has too much to do. Happening at the same time. **In most cases this is not a server issue, but something with your code and configuration.** [Performance problems are often people problems](#people-problems)

### Check the logs
{#check-the-logs-1}

503 errors are often associated with uncontrolled termination, in many cases no PHP error logs will be written. It's anyhow worth a try. See [the logs article](#logs). Maybe you can find where the application exited with which error. Compare this with your local development environment and see if it fails the same way.

### 'AH1067: Failed to read FastCGI header' Apache error
{#ah1067-failed-to-read-fastcgi-header-apache-error}

If you see the error "Failed to read FastCGI header" in the App's error log stream, there are these likely causes:

- A bug in the App's PHP code, such as a buggy WordPress plugin
- The App is using too much memory
- A bug in a PHP extension you've enabled
- When this error occurs, the response sent to the browser will be "503 Service Unavailable"

#### What the error means
{#what-the-error-means}

The error message "Failed to read FastCGI header" means that while Apache was waiting for PHP-FPM, the PHP process did not respond properly. This error does not mean there is a problem with Apache.

### Restarting PHP (workaround)
{#restarting-php-workaround}

In some cases, to the the App working again, it may be enough to restart the environment from the Dashboard. If the issue is caused by buggy code, or slow queries, or 3rd party APIs, the problem is likely to happen again.

### Review your latest changes
{#review-your-latest-changes-1}

Review your code and configuration changes. Compare this with your [local development environment](#intro-to-local-development-with-php) and see if it fails the same way. Have you ran an update recently?

### Look for errors and slow endpoints
{#look-for-errors-and-slow-endpoints}

The most common cause of these errors is buggy PHP code. You can try disabling Craft CMS or WordPress plugins, custom themes, and other custom code until you identify which code is causing the problem. If some or several scripts or endpoints of you App are slow, new connections will get backed up, ultimately resulting in PHP-FPM not being able to respond any more. If this is the case, then the solution is to optimize the slow PHP code.

### Running out of memory
{#running-out-of-memory}

If your application uses more memory than the plan allows for, the website will crash every time the limit is exceeded. environments are configured with swap to avoid crashes, but if you see more than 10-30 MB of swap usage in the dashboard, then this is a strong indicator that your app is using too much memory.

#### Upgrade the plan
{#upgrade-the-plan}

One solution is to upgrade your PHP plan, if possible. Otherwise, you wil have to profile the App to figure out why it's using so much memory.

### It could also be something on our side
{#it-could-also-be-something-on-our-side-2}

It is also possible — although less likely - that this error is caused by a network, hardware or configuration issue on our side, your hosting provider. Please check our status page under [status.fortrabbit.com](https://status.fortrabbit.com) if there are any ongoing maintenance windows or service issues known.

---

## Troubleshoot 504 errors
{#troubleshoot-504-errors}

The 503 HTTP status code means "Service Unavailable".

Usually, the request is taking too long to process or something is blocking execution and many requests are piling up. This article aims to help developers troubleshooting 504 and 503 errors.

- **504 errors often occur without code changes**
- 504 errors will be shown after a longer time of trying to load a page
- 504 errors here are sometimes rendered using a fortrabbit error page template
- 504 errors are sometimes connected to traffic patterns
- 504 errors are sometimes caused by editorial changes in a CMS
- 504 errors often come and go - from offline to online and back again
- 504 errors usually will not show up in the PHP error logs
- Sometimes you'll find: "AH01079: failed to make connection to backend" in the logs, this is what Apache is reporting back

504 and [503 errors](#troubleshoot-503-errors) are two sides of the same coin. PHP-FPM (the PHP process manager here) has too much to do. 504 and 503 errors are often happening simultaneously.

### Behavior
{#behavior}

504 errors are usually a frustrating experience, they suddenly appear and are hard to trace.

#### Errors out of the blue
{#errors-out-of-the-blue}

Our experience shows that 504 (and 503) errors most often occur without direct interaction from the developer, like directly after deploying new code or changing configuration. 504 appear suddenly out of nowhere. In most cases this is not a server issue, but related to code and configuration.

- [Performance problems are often people problems](#people-problems)

#### No traceable logs
{#no-traceable-logs}

504 and 503 errors are hard to debug, because usually no error logs are written, as the process, when it times out will not exist.

### Common causes
{#common-causes}

504 errors are usage based. The errors usually start to appear when a certain threshold is reached. Among many other reasons, this can be the number of concurrent visitors, the size of the database or certain actions by an editor in the control panel of a CMS. We have seen many 504 issues appearing without human interaction at all.

#### Poorly performing database queries
{#poorly-performing-database-queries}

The most common cause of individual downtime are slow database queries. A MySQL query might work in a testing environment, but not in production at a certain point of traffic and more data. Your application might be making MySQL database queries that are too heavy. MySQL queries can be CPU intensive and long running. Sometimes this is a technical requirement, often this is unawareness on the part of the developer.

Review your code for inefficient queries. If unsure consult a senior colleague or use a profiler like [Blackfire](#blackfire) to find the bottlenecks. Refactor your query design to write better performing MySQL queries or even rethink your data model. Caching certain database results can be another tactic after refactoring.

#### Too many database queries
{#too-many-database-queries}

Your application might be making too many database queries. This issue is similar to the one above. Sometimes too many and poorly written MySQL queries come in tandem. In Craft CMS for example it's easy to write a lot of queries. Review your code and see if you can avoid or optimize queries.

#### Image transforms
{#image-transforms}

Image transformations can happen when an editor is uploading new photos into a CMS. For web delivery these images then need to be transformed into smaller sizes. imageMagick is often the tool of choice. Mind that such image crunching tasks are expensive in terms of performance - and they can stack up. Usually image transformations should only run once per image. Then the required sizes should be saved to the file system for later usage. This image cache should not be cleared in production.

For most use cases we advise lazily creating required images one by one instead of an eager (upfront) creation approach. The size of the original image also matters. One mitigation can be to use the GD library instead of imageMagick. Though it creates slightly more artifacts in JPG compression and maybe slightly bigger files, GD is often less resource hungry.

#### External API calls
{#external-api-calls}

Sometimes a 504 error is caused when you call an external API that is not responding, or that responds too late. This should be relatively easy to debug. Try turning off any blocking external API calls.

#### Bots
{#bots}

Sometimes bots come visiting your website, scraping each page to feed an AI or a search machine. When not configured correctly, your website may provide such bots an infinite of almost identical pages that still need to be rendered and cached.

#### Plugins
{#plugins}

CMS plugins are also a common source of performance problems. This includes plugins that are designed to improve performance. Sometimes plugins interact in unpredicted ways.

#### Something else on application level
{#something-else-on-application-level}

Basically anything that will end up in an endless loop can cause a 504 error. This can be a plugin of a CMS or something within your templates. Imagine a template that is endlessly including itself. It will go on for a while until either the memory, the CPU or the runtime come to an end.

There are many technical measurements which can be taken by the client to dramatically lower the chances of having any downtime at all. Our multi-node production plans are offering high availability when correctly implemented. For CMS systems such as Craft CMS, it's often possible to cache the whole frontend in a CDN by using edge caching with a third party service such as Cloudflare.

### Ways to proceed
{#ways-to-proceed}

- Decrease/increase the `max_timeout` setting for debugging
- Share results of your research with us in our client support

#### Identifying 504 errors with the dashboard
{#identifying-504-errors-with-the-dashboard}

The fortrabbit dashboard provides some useful metrics. You can see 5xx metrics by following the "Show all metrics" link. The 5xx metric is a mix of 500, 502, 503 and 504 errors. Have a look at the PHP response time metric as well. The PHP response time always goes up when there are 504 errors. Aim for no swap usage and a low PHP response time of not more than 200 ms.

#### It could also be something on our side
{#it-could-also-be-something-on-our-side-3}

It is also possible — although less likely - that this error is caused by a network, hardware or configuration issue on our side, your hosting provider. Please check our status page under [status.fortrabbit.com](https://status.fortrabbit.com) if there are any ongoing maintenance windows or service issues known.

---

## HTTP errors
{#http-errors}

HTTP response errors explained by numbers.



---

## Troubleshoot 400 errors
{#troubleshoot-400-errors}

A 400 HTTP status code means "Bad Request".

The server was reached but rejected the request before it reached your application logic. Understand and fix 400 responses on fortrabbit.

### 400 error behavior
{#400-error-behavior}

- 400 errors appear immediately after the browser sends the request
- They often surface during integration work with third-party services or new client-side code that posts JSON or form data
- They can be triggered by your application framework, by a reverse proxy, or by the fortrabbit edge when the request is malformed

**Most 400 responses indicate something is wrong with the request that is sent, not with the platform itself.** Work through the following checks first:

### Check the request that is sent
{#check-the-request-that-is-sent}

- Inspect the request in your browser developer tools or with `curl -v`.
- Ensure the `Host` header matches your App domain. Requests to the wrong hostname or without TLS will be rejected.
- Validate query strings and payloads: truncated JSON bodies, illegal characters, or an unexpected content type will cause a 400.

### Review application level validation
{#review-application-level-validation}

- Many frameworks respond with 400 when CSRF tokens or form validations fail. Confirm that cookies, sessions, and CSRF headers are present.
- Double-check any custom middleware you added. Rate limiters and API gateways frequently send a 400 when a prerequisite header (API key, signature) is missing.
- Compare with your local environment: reproduce the failing request locally to see if the framework reports the same problem.

### Check the logs
{#check-the-logs-2}

- Application and web server logs will often mention the exact reason. See [Logs](#logs) for where to find them.
- Consider enabling verbose logging temporarily to capture raw request details (remember to disable again afterwards).

### It could also be something on our side
{#it-could-also-be-something-on-our-side-4}

Less common, but still possible: a transient network hiccup or edge misconfiguration could cause 400 responses. Have a look at [status.fortrabbit.com](https://status.fortrabbit.com) for active incidents, and contact support if everything above checks out and the issue persists.

---

## Troubleshoot 403 errors
{#troubleshoot-403-errors}

The 403 HTTP status code means "Forbidden".

This happens when access is denied, or in other words: the resource is not allowed for some reason. This article aims to help developers troubleshooting 403 errors.

- 403 errors will usually be shown on screen immediately
- 403 errors often occur during setup or after code or configuration changes

**In most cases this is not a server issue, but a problem with your code and/or configuration.** Please check the following common issues first:

### .htaccess problems
{#htaccess-problems}

Sometimes 403 errors are caused by issues with `.htaccess`. Check your `.htaccess` file. Developers using SFTP often forget to upload that hidden file. See our [.htaccess help](#htaccess-intro).

### Wrong root path
{#wrong-root-path-1}

Our software templates help to choose the right root path for the App. You may have chosen no software template or installed a different software than originally selected. In such cases you need to manually set the root path to what your software requires. See environment root path help.

### File permissions
{#file-permissions}

Sometimes 403 errors are caused by wrong file permissions. This can happen when you deploy with SFTP or SSH or sometimes Git. Make sure that PHP has write permissions for files like `composer.json`, `composer.lock`, `storage/*`, `vendor/*`. Set the file permissions for those files to `744` with your SFTP client or by SSH. All `*.php` files should also be executable.

```shell
## Use for a folder and all it's contents recursively
{#use-for-a-folder-and-all-it-s-contents-recursively}
$ chmod -R 744 directoryname

## Change a specific file name
{#change-a-specific-file-name}
$ chmod 744 filename
```

### No code deployed
{#no-code-deployed-1}

A common reason for the 403 page is that no code has been deployed yet. Please deploy some code.

### Missing `index.php` or `index.html` file
{#missing-index-php-or-index-html-file}

Sometimes people forget to upload an index file. The web server will look for that. When it's not present, it can nto deliver anything. Check your directory if either an `index.php` or `index.html` file is present.

### Missing http-auth credentials
{#missing-http-auth-credentials}

If you have used HTTP auth to protect your website from unwanted visitors and someone is trying access that without entering the correct username and password, a 403 access denied error will occur.

### DNS issues
{#dns-issues}

Sometimes it takes a while until DNS is propagated. This can be when your App is new, you have upgraded the scaling or you have just routed a domain. Wait a little and try again.

### Wrong address
{#wrong-address-1}

You might have an error with URL. Check for typos in the address bar (URL) of your browser.

### It could also be something on our side
{#it-could-also-be-something-on-our-side-5}

It is also possible — although less likely - that this error is caused by a network, hardware or configuration issue on our side, your hosting provider. Please check our status page under [status.fortrabbit.com](https://status.fortrabbit.com) if there are any ongoing maintenance windows or service issues known.

---

## Troubleshoot 408 errors
{#troubleshoot-408-errors}

The 408 HTTP status code means "Request Timeout" and it is very rare.

The server timed out waiting for the request to complete.

### 408 error behavior
{#408-error-behavior}

- 408 errors will usually be shown on screen after a delay
- 408 errors can occur when the client connection is slow or unstable
- 408 errors can be rendered using a fortrabbit error page template

**In most cases this is not a server issue, but a problem with the client connection or request handling.** Please check the following common issues first.

### Slow client connections
{#slow-client-connections}

A common cause of 408 errors is when the client takes too long to send the complete request. This can happen with:

- Slow internet connections
- Large file uploads that exceed timeout limits
- Mobile connections with poor signal quality
- Network interruptions during the request

### Large request payloads
{#large-request-payloads}

When uploading large files or sending requests with substantial data:

- Check if your upload exceeds the maximum allowed size
- Consider breaking large uploads into smaller chunks
- Verify that your application properly handles multipart uploads
- Review PHP settings like `max_execution_time` and `upload_max_filesize`

### Client-side timeout configuration
{#client-side-timeout-configuration}

Sometimes the issue is with how the client application handles requests:

- Check your application's HTTP client timeout settings
- Ensure your JavaScript fetch or AJAX calls have appropriate timeout values
- Review any proxy or CDN timeout configurations
- Consider implementing retry logic for important requests

### Check the logs
{#check-the-logs-3}

Examine the logs. See [here](#logs). The logs may show patterns of when these timeouts occur and help identify the root cause.

### Network troubleshooting
{#network-troubleshooting}

- Test your connection speed and stability
- Try the same request from a different network
- Check if the issue occurs consistently or only sporadically
- Monitor your application during peak traffic times

### It could also be something on our side
{#it-could-also-be-something-on-our-side-6}

It is also possible — although less likely - that this error is caused by a network, hardware or configuration issue on our side, your hosting provider. Please check our status page under [status.fortrabbit.com](https://status.fortrabbit.com) if there are any ongoing maintenance windows or service issues known.

---

## Troubleshoot 502 errors
{#troubleshoot-502-errors}

The 502 HTTP status code means "Bad Gateway".

- 502 errors will usually be shown on screen immediately
- 502 errors often occur after code or configuration changes
- 502 errors are sometimes just printed as a "service unavailable" message, check the browser's developer tools for the response's HTTP status code to be sure this is indeed a 502 error
- 502 errors here are often rendered using a fortrabbit error page template

The Apache web server will return a 502 error if it can't proxy a request to the PHP engine - PHP-FPM in our case. This can be because PHP is not running or busy with something else timing out.

**In some cases this is not a server issue, but something with your code and configuration.** Good news is that they are mostly easy to debug for you.

### Check the logs
{#check-the-logs-4}

Examine the logs of your environment. See [here](#logs). There you'll likely find where the application exited with which error. Compare this with your local development environment and see if it fails the same way. Review your latest code changes.

### It could also be something on our side
{#it-could-also-be-something-on-our-side-7}

It is also possible that this error is caused by a network, hardware or configuration issue on our side, your hosting provider. Please check our status page under [status.fortrabbit.com](https://status.fortrabbit.com) if there are any ongoing maintenance windows or service issues known.

---

## Development
{#development}

Best practices, tips and tricks



---

## Intro to local development with PHP
{#intro-to-local-development-with-php}

A local development environment is key for successful application lifetime management and continuous deployment.

### Why local development?
{#why-local-development}

- See code changes in real time
- Test your code before deploying
- Debug issues with dev flags enabled
- Experiment with new features
- Validate compatibility
- Maintain an up-to-date backup
- Stay independent from your hosting provider

Not having a local PHP development environment can lead to chaos. Developers may perform "open heart surgery"—running major updates directly on the server. The fortrabbit platform aims to make deployment from local development to remote environments seamless and safe.

### Requirements
{#requirements-1}

The following open source software should run in your local development environment to match with the fortrabbit platform:

- **Apache** or NGNIX — a web server
- **MySQL** - database
- **PHP** - server side scripting language
- **Git** - version control - [see Git into](#git-intro)
- **Composer** - dependency manager for PHP - [see intro](#composer)
- **Node.js** and NPM (or similar) - frontend build processes

There are various ways to set up your local development stack, depending on your skills, needs, and operating system (Windows, macOS, or Linux). Choose the approach that best suits you. Luckily with Composer driven PHP development it's usually enough to roughly match the remote environment. Specifically major and minor PHP versions should be kept im sync.

### Local development with virtualization
{#local-development-with-virtualization}

Utilizing containers allows replication of local setup across a team. Having everything stashed into a virtual machine very much nullifies any interference with the local host system. It keeps things clean. A project with a containerized local development environment can also be frozen to the software specific versions used at that time. Modern container technology is lightweight and fast and usually headless.

- **DDEV** (recommended): [See guide](#local-development-with-ddev)
- **Laravel Herd**: [See guide](#local-development-with-laravel-herd)
- **Laravel Sail**: [See guide](#local-development-with-laravel-sail)
- **Docker**: maximum flexibility and control, more configuration.

### Local development on the host
{#local-development-on-the-host}

Run a web server and PHP directly on your laptop. This is often quick and lightweight to get up and running. Your options:

- **Laravel Valet**: [See guide](#laravel-valet)

#### PHP built-in server
{#php-built-in-server}

For simple tasks or quick tests, you don't strictly need a full web server stack. PHP comes with a built-in web server.

```bash
php -S localhost:8000
```

If you are using Laravel, you can use the Artisan command which wraps the PHP built-in server:

```bash
php artisan serve
```

This is great for quick prototyping but not recommended for complex applications or production parity.

#### Desktop virtualization
{#desktop-virtualization}

This is the old school way. Example VM applications are: [VirtualBox](https://www.virtualbox.org)(free by Oracle) or [VMware](http://www.vmware.com)(paid). VirtualBox controlled by [Vagrant](https://developer.hashicorp.com/vagrant) helps when setting up reproducible development environments. [Homestead](https://laravel.com/docs/homestead#main-content), which builds upon Vagrant is still popular with Laravel.

#### Other options
{#other-options}

**Classical GUIs** These solution stacks are easy to handle through a graphical interface and they interfere with the rest of your system as little as possible. The most commonly used here are [MAMP](https://www.mamp.info) (free and paid version) and [XAAMP](https://www.apachefriends.org/index.html). Please mind that those don't include Git and Composer.

**Manual setup** Install and manage a web server to run your laptop. Specifically for lightweight applications, such as Kirby CMS, which does not need a database, installing the PHP runtime might be sufficient.

---

## Local development with DDEV
{#local-development-with-ddev}

Local PHP development with Docker made simple. That's DDEV.

**We can not recommend DDEV enough.** It is an abstraction layer on top of Docker to simplify local PHP development. It's rooted in the Drupal world but is also popular with [Craft CMS](#install-craft-cms-local), [Symfony](#symfony-guide), [Laravel](#install-laravel-locally) and [WordPress](#wordpress-quick-setup-guide). DDEV is sponsorware, use it for free to use, donations welcome. It's a command line tool and has many nice features and even plugins.

- [ddev.com](https://ddev.com/)

### Installation
{#installation-1}

DDEV runs on macOS, Linux, and Windows. It requires a Docker provider to be installed first. [Docker Desktop](https://www.docker.com/products/docker-desktop/) is the standard, [OrbStack](https://orbstack.dev/) (macOS) is a lightweight alternative.

```bash
## Install DDEV is via Homebrew (macOS)
{#install-ddev-is-via-homebrew-macos}
brew install ddev/ddev/ddev

## One-time initialization for local HTTPS
{#one-time-initialization-for-local-https}
mkcert -install
```

For Windows or other installation methods, please refer to the [official DDEV installation docs](https://ddev.readthedocs.io/en/stable/users/install/ddev-installation/).

### Example usage
{#example-usage}

```bash
## 1. Initialize
{#1-initialize}
## Navigate to your project's root directory and run:
{#navigate-to-your-project-s-root-directory-and-run}
ddev config
## This wizard will ask you a few questions about your project.
{#this-wizard-will-ask-you-a-few-questions-about-your-project}

## 2. Start
{#2-start}
## Spin up the containers:
{#spin-up-the-containers}
ddev start

## 3. Develop
{#3-develop}
## See project details:
{#see-project-details}
ddev describe

## Open project in browser:
{#open-project-in-browser}
ddev launch

## Access the container's shell:
{#access-the-container-s-shell}
ddev ssh
```

### SSH Keys
{#ssh-keys}

To deploy code or sync data with fortrabbit from within the DDEV container, your local SSH keys need to be available. Run this command once per session:

```bash
ddev auth ssh
```

---

## Laravel Valet
{#laravel-valet}

A macOS development environment not only Laravel fans.

Laravel Valet is an easy-to-use local solution not only for Laravel developers on macOS. It's a command line interface, so you install it with the Terminal. It bundles NGNIX, DnsMasq and some other magic to an easy to use CLI.

- [laravel.com/docs/valet](https://laravel.com/docs/valet)

### Installation
{#installation-2}

It's best installed with Homebrew and it requires PHP and Composer.

```bash
## Install Valet via Composer
{#install-valet-via-composer}
composer global require laravel/valet
```

### Examples
{#examples-5}

```bash
## Run the installer
{#run-the-installer-1}
valet install

## Park: Register a directory for all your projects
{#park-register-a-directory-for-all-your-projects}
cd ~/Sites
valet park
## Now ~/Sites/my-project is available at http://my-project.test
{#now-sites-my-project-is-available-at-http-my-project-test}
## The `park` command registers a directory on your machine that contains your applications. All directories within that directory will be accessible in your web browser at `http://<directory-name>.test`.
{#the-park-command-registers-a-directory-on-your-machine-that-contains-your-applications-all-directories-within-that-directory-will-be-accessible-in-your-web-browser-at-http-directory-name-test}

## Link: Serve a single site
{#link-serve-a-single-site}
cd ~/path/to/project
valet link
## Now available at http://project.test
{#now-available-at-http-project-test}
## The `link` command is useful if you want to serve a single site in a directory and not the entire directory.
{#the-link-command-is-useful-if-you-want-to-serve-a-single-site-in-a-directory-and-not-the-entire-directory}

## Secure: Serve over HTTPS
{#secure-serve-over-https}
valet secure my-project
## You can serve your sites over encrypted TLS using HTTP/2 with the `secure` command.
{#you-can-serve-your-sites-over-encrypted-tls-using-http-2-with-the-secure-command}

## PHP Versions: Switch globally or per site
{#php-versions-switch-globally-or-per-site}
valet use php@8.5
cd ~/Sites/legacy-project
valet isolate php@7.4
```

### Database
{#database}

Valet does not include a database management tool.

### Working with fortrabbit
{#working-with-fortrabbit}

Since Valet runs directly on your host machine, it uses your local SSH keys by default.

### Graphical interface
{#graphical-interface}

- [phpmon.app](https://phpmon.app/) - a nice UI for Valet

---

## Local development with Laravel Herd
{#local-development-with-laravel-herd}

Paid local development environment for macOS and Windows from the Laraverse.

Laravel Herd provides a streamlined local development environment specifically optimized for PHP applications on macOS and Windows. It bundles NGNIX, DnsMasq and some other magic to an easy to use statusbar app. For using MySQL the Pro upgrade must be bought.

- [herd.laravel.com](https://herd.laravel.com)

Laravel Herd is newer than [Laravel Valet](#laravel-valet) and [Laravel Sail](#local-development-with-laravel-sail).

### Installation and usage
{#installation-and-usage}

Download the installer from the official website and run it. Herd runs in your menu bar. It automatically creates a `~/Herd` directory. Any folder you put in there will be automatically served as a `.test` domain. For example:

1. Create `~/Herd/my-project`
2. Open `http://my-project.test` in your browser

You can switch PHP versions for individual sites or globally directly from the Herd menu bar icon.

The free version of Herd does not include database management.

### Working with fortrabbit
{#working-with-fortrabbit-1}

Herd uses your system's SSH keys, so interacting with fortrabbit git repositories works out of the box if your keys are set up correctly in `~/.ssh`.

---

## Local development with Laravel Sail
{#local-development-with-laravel-sail}

The official, lightweight Docker development environment for Laravel.

Sail is Laravel's own take on a Docker-based local development environment. It's essentially a `docker-compose.yml` file and a CLI wrapper script stored in your project. It's a good match if you want a per-project isolated environment that matches the "Laravel way" of doing things.

- [laravel.com/docs/sail](https://laravel.com/docs/sail)

### Installation
{#installation-3}

It comes pre-installed with new Laravel projects. For existing ones:

```bash
composer require laravel/sail --dev
php artisan sail:install
```

### Usage
{#usage-2}

It's just Docker under the hood. You use the `sail` command to interact with it.

```bash
## Start the environment
{#start-the-environment}
./vendor/bin/sail up

## Run artisan commands
{#run-artisan-commands}
./vendor/bin/sail artisan migrate

## Run composer
{#run-composer}
./vendor/bin/sail composer require guzzlehttp/guzzle
```

**Tip:** Configure a [shell alias](https://laravel.com/docs/sail#configuring-a-shell-alias) so you can just type `sail` instead of `./vendor/bin/sail`.

### Comparison
{#comparison}

Unlike [Valet](#laravel-valet) or [Herd](#local-development-with-laravel-herd), Sail runs everything in containers. This means no pollution of your local machine, but it also means it's a bit heavier on resources (Docker Desktop required).

### Working with fortrabbit
{#working-with-fortrabbit-2}

Sail is for local development. When you deploy to fortrabbit, you are pushing your code, not the Docker containers. The platform handles the runtime environment for you.

---

## Local development
{#local-development}

It works on my machine. Always develop your PHP projects locally.



---

## Domain registration providers
{#domain-registration-providers}

fortrabbit is not offering direct domain registration and management. What to look for when choosing a domain provider.

### About domain registration
{#about-domain-registration}

Domain registration is the process of acquiring a web address for a website - a Top Level Domain. To do this, you need to go through a domain registrar, which will check availability and let you purchase the domain, usually for a year in advance. Once registered, you can link the domain to your fortrabbit environments by setting appropriate DNS records.

Domains are often bundled with consumer hosting packages. But in most cases domains can also be purchased individually. There are dedicated domain providers too. This decoupled approach is perfect for modern cloud hosting platforms like fortrabbit, where you bring your own domain.

It's common to choose a local domain registration provider, since they sometimes offer better rates for your country TLDs and will provide pricing in your currency. There are various offerings, so you should consider upfront what you'll need. We look at:

1. Specialized in advanced DNS configurations
2. IMAP/POP3 e-mail accounts - see [email providers](#email-account-providers)
3. Exotic TLD-endings
4. General domain forwarding with HTTPS
5. Support for forwards with [ALIAS or ANAME records](#aname-alias-records)

Many of our clients are using classical offerings combining domain ordering and e-mail hosting. Others are using separate services for domain registration and e-mail hosting, there are also dedicated services that only offer DNS.

### How does the domain provider relate to fortrabbit?
{#how-does-the-domain-provider-relate-to-fortrabbit}

fortrabbit does not provide domain registration or name servers. Instead you point the external domain to fortrabbit using DNS instructions.

---

## DNS and domain registration providers
{#dns-and-domain-registration-providers}

Here are some popular domains services that we know are often used and that we can recommend.

### Classical hosting
{#classical-hosting}

Sell domains, often bundled with email or shared hosting. Domains can also be purchased individually.

* [GoDaddy](https://www.godaddy.com) - US, market leader, domains, hosting and email.
* [Gandi](https://www.gandi.net) - FR, classical hosting too
* [Hover](https://www.hover.com) - CA, domains and email, simple interface.
* [Namecheap](https://www.namecheap.com) - US, popular, competitive pricing, hosting and email.

### Dedicated domain providers
{#dedicated-domain-providers}

Focus purely on domain registration with a clean interface. Best matches with fortrabbit.

* [Porkbun](https://porkbun.com) - US, quirky branding, transparent pricing, no upsells.
* [Dynadot](https://www.dynadot.com) - US, advanced domain management.
* [iwantmyname](https://iwantmyname.com) - NZ, simple interface.

### Specialized DNS and more
{#specialized-dns-and-more}

Focus on high-performance, programmable DNS resolution.

* [DNSimple](https://dnsimple.com) - US, developer-centric, excellent API, offers domain registration.
* [Cloudflare](https://www.cloudflare.com) - US, domains, DNS, DDOS (see [integration guide](#cloudflare)).
* [AWS Route 53](https://aws.amazon.com/route53) - US, B2B, DNS and domain registration

### Others
{#others}

* Squarespace also has domains

---

## Domain provider instructions
{#domain-provider-instructions}

How to configure the domain provider to point to fortrabbit.

### Get ready
{#get-ready-32}

You should have a domain created with the fortrabbit dashboard. See the [domain setup guide](#point-a-domain-to-fortrabbit). You should also have a domain registered somewhere. See [domain provider intro](#domain-registration-providers).

### Instructions for domain providers
{#instructions-for-domain-providers}

Below are links to instructions to set CNAME and A-records for specific domain providers. These settings are typically configured through the provider's control panel.

#### GoDaddy
{#godaddy}

- [GoDaddy: CNAME instructions](https://www.godaddy.com/help/add-a-cname-record-19236) sub domains such as www
- [GoDaddy: A record instructions](https://www.godaddy.com/help/add-an-a-record-19238) forwarding apex domains

#### NameCheap
{#namecheap}

- [Namecheap: CNAME instructions](https://www.namecheap.com/support/knowledgebase/article.aspx/9646/2237/wwwhow-to-create-a-cname-record-for-your-domain) sub domains such as www
- [Namecheap: A record instructions](https://www.namecheap.com/support/knowledgebase/article.aspx/319/2237/how-can-i-set-up-an-a-address-record-for-my-domain) forwarding apex domains

#### Google Domains
{#google-domains}

- [Google Domains: Create a CNAME record](https://support.google.com/domains/answer/3290350?hl=en) sub domains such as www
- [Google Domains: Create an A record](https://support.google.com/domains/answer/3290309?hl=en) forwarding apex domains

#### Squarespace
{#squarespace}

- [Squarespace: Adding a CNAME record](https://support.squarespace.com/hc/en-us/articles/205812378-Adding-custom-records-to-your-domain) sub domains such as www
- [Squarespace: Adding an A record](https://support.squarespace.com/hc/en-us/articles/205812378-Adding-custom-records-to-your-domain) forwarding apex domains

#### DNSimple
{#dnsimple}

- [DNSimple: Create a CNAME record](https://support.dnsimple.com/articles/cname-record) sub domains such as www
- [DNSimple: Create an A record](https://support.dnsimple.com/articles/a-record) forwarding apex domains

#### AWS Route 53
{#aws-route-53}

- [AWS Route 53: Creating a CNAME record](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-creating.html#resource-record-sets-creating-cname) sub domains such as www
- [AWS Route 53: Creating an A record](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-creating.html#resource-record-sets-creating-a-alias) forwarding apex domains

#### Cloudflare Domains
{#cloudflare-domains}

- [Cloudflare: Adding a DNS record](https://support.cloudflare.com/hc/en-us/articles/360019093151-Adding-DNS-records) -  [Cloudflare intro](#cloudflare).

---

## Cloudflare
{#cloudflare}

### About Cloudflare
{#about-cloudflare}

Cloudflare is a "magical" multi-purpose website performance & security service, which works at the DNS level. It can be used as a kind of Content Delivery Network and as a protection against Denial Of Service Attacks. It is also a popular choice to get SSL certificates for your domain without the costs and hassle.

### Pricing and signup
{#pricing-and-signup}

There is a free plan with basic features to get you started. [cloudflare.com/plans/](https://www.cloudflare.com/plans?utm_source=fortrabbit). Go to the [sign up page](https://www.cloudflare.com/a/sign-up), enter an email and choose a password.

### Integrating Cloudflare with fortrabbit
{#integrating-cloudflare-with-fortrabbit}

There is no technical connection between Cloudflare and fortrabbit. Cloudflare will sit in between your DNS provider and fortrabbit — think of it as a proxy. You will set your nameservers (NS records) to point to Cloudflare.

#### Setup Cloudflare
{#setup-cloudflare}

In the following example you first register your domain with your domain provider, then point it to fortrabbit using our standard settings, then Cloudflare will scan the DNS records for you:

1. Make sure to have a domain registered with a domain provider
2. Make sure to have added the domain in the fortrabbit Dashboard
3. Route the domain using our instructions still with your old DNS provider
4. Set up the domain with Cloudflare
5. Cloudflare will scan and use the DNS settings already in place
6. DONE

You might also start with a fresh domain from scratch within Cloudflare. Then Cloudflare will act as your DNS provider. Enter the DNS settings from the fortrabbit Dashboard with Cloudflare.

#### Crypto setting
{#crypto-setting}

Each domain on Cloudflare comes with a bunch of settings. One is called "Crypto" and is about SSL. Your goal is that the whole communication between the user of your website is encrypted of course. Now, Cloudflare, as described above, is a proxy between your user and fortrabbit. The first lap from the user to Cloudflare is secured by default, but what about the the next one, between Cloudflare and fortrabbit?

```
┌──────┐       ┌────────────┐             ┌────────────┐
│ User ├─HTTPS─▶ Cloudflare ├─ ? HTTPS ? ─▶ fortrabbit │
└──────┘       └────────────┘             └────────────┘
```

Cloudflare is the domain endpoint for the user. Cloudflare itself will actually talk to the App URL. The connection between the App and Cloudflare should also be encrypted.

The App URL has HTTPS, so you can and should set SSL to **full** to ensure end-to-end encryption. The default **flexible** setting is not enough (as we think). "Full (strict)" mode will not work but is not necessary.

### Advanced topics
{#advanced-topics-1}

#### Cloudflare DNS and fortrabbit Dashboard Status
{#cloudflare-dns-and-fortrabbit-dashboard-status}

Cloudflare is a bit of black box, DNS-wise. When you visit a domain in the fortrabbit Dashboard that is routed via Cloudflare an accurate response is not possible. The Dashboard is aware of many Cloudflare IPs, so it will likely guess that the domain is routed via Cloudflare. But you might still see an error, even if the domain is in fact routed correctly.

#### Cloudflare SSL VS Let's Encrypt
{#cloudflare-ssl-vs-let-s-encrypt}

Many fortrabbit clients have used Cloudflare to get SSL for their own custom domain, without the need to book and set up a custom cert here. Now, fortrabbit also offers free SSL certificates via (free and zero-config) Let's Encrypt. So if that is your aim, you might not need Cloudflare.

#### Cloudflare and 2nd level subdomains
{#cloudflare-and-2nd-level-subdomains}

If you see an `SSL_ERROR_NO_CYPHER_OVERLAP` error, but you think you have set up everything correctly, check the domain you are trying to route. Is it a second level of a subdomain like `dev.www.example.com`? If so, further actions might be required: please see the [Cloudflare help](https://support.cloudflare.com/hc/en-us/articles/200170566-Troubleshooting-SSL-errors#h_55e4d315-c60d-4798-9c4c-c75d9baed1b7).

#### Other reasons to use Cloudflare
{#other-reasons-to-use-cloudflare}

While free SSL has become a commodity, there are other reasons to use Cloudflare:

- Enhanced DDoS protection
- CNAME Flattening for [apex domains](#apex-domains)
- Domain analytics

#### Prevent direct access
{#prevent-direct-access}

You may want to ensure all traffic is routed through Cloudflare. This is important to secure 360 DDoS protection. You'll basically disable the App URL to be accessible. To block direct access and whitelist only Cloudflare's IPs, extend your `.htaccess` file with the following rules:

```
ErrorDocument 403 "Not Allowed"
Deny from all

#### Cloudflare IPs ###
{#cloudflare-ips}

Allow from 103.21.244.0/22
Allow from 103.22.200.0/22
Allow from 103.31.4.0/22
Allow from 104.16.0.0/12
Allow from 108.162.192.0/18
Allow from 131.0.72.0/22
Allow from 141.101.64.0/18
Allow from 162.158.0.0/15
Allow from 172.64.0.0/13
Allow from 173.245.48.0/20
Allow from 188.114.96.0/20
Allow from 190.93.240.0/20
Allow from 197.234.240.0/22
Allow from 198.41.128.0/17
Allow from 2400:cb00::/32
Allow from 2405:8100::/32
Allow from 2405:b500::/32
Allow from 2606:4700::/32
Allow from 2803:f800::/32
Allow from 2c0f:f248::/32
Allow from 2a06:98c0::/29
```

As the IP ranges might change from time to time, you should update them on a regular basis.

### Alternatives to Cloudflare
{#alternatives-to-cloudflare}

Cloudflare is a magical package of different services all combined and streamlined in a single offering. Mind: by using Cloudflare, you make yourself dependent that this critical component (DNS/NS)) of your infrastructure is working correctly. It's another point of failure that makes your setup more complex. But overall, it's more likely that your website will stay up with Cloudflare enabled. Some of our clients prefer a separation of services. Instead of Cloudflare, they might use dedicated services for DNS/domain and CDN.

---

## ANAME / ALIAS records
{#aname-alias-records}

To serve apex domain directly some domain providers allow ALIAS or ANAME records to resolve host names to IPs. It is sometimes called CNAME flattening. The host name is resolved to an IP.

::CallOut{alert}
Due to potential upcoming changes, we recommend using the [WWW forwarding service](#domain-forwarding) instead of ANAME/ALIAS records with our service at this time.
::

### Domain providers with ANAME support
{#domain-providers-with-aname-support}

More and more domain providers - [see intro](#domain-registration-providers) - are supporting ANAME / ALIAS records:

- [AWS Route53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosing-alias-non-alias.html)
- [Cloudflare: CNAME flattening](https://developers.cloudflare.com/dns/cname-flattening), also see [Cloudflare integration](#cloudflare)
- [DNS made easy: ANAME records](https://support.dnsmadeeasy.com/hc/en-us/articles/34327231731227-What-is-an-ANAME-Record)
- [DNSimple: ALIAS records](https://support.dnsimple.com/articles/alias-record)
- [Dreamhost: Custom DNS records](https://help.dreamhost.com/hc/en-us/articles/360035516812-Adding-custom-DNS-records)
- [Easy DNS: ANAME records](https://kb.easydns.com/knowledge/aname-records)
- [Google domains: ALIAS records](https://cloud.google.com/dns/docs/records-overview#alias-records)
- [Namecheap: ALIAS records](https://www.namecheap.com/support/knowledgebase/article.aspx/10128/2237/how-to-create-an-alias-record)
- [Porkbun: ALIAS records](https://kb.porkbun.com/article/68-how-to-edit-dns-records)

As far as we know, by the time of this writing, the following providers do not support ANAME records:

- GoDaddy - see [this SO question](https://webmasters.stackexchange.com/questions/141075/aname-record-not-accepted) ☠️

If your provider does not support CNAME flattening, but you would like to take advantage of it, we recommend switching to that does or consider using our [www forwarding service](#domain-forwarding).

---

## DNS
{#dns}

Integrate domain and DNS services.



---

## Git providers
{#git-providers}

fortrabbit does not host Git repositories. Instead, you connect your external Git repository to deploy your code. Which providers are supported.

### GitHub
{#github}

GitHub has first-class support. We offer a native [GitHub App](#the-fortrabbit-github-app) that integrates deeply with the platform. This is the recommended way to deploy with Git.

### Other providers
{#other-providers}

You can also use other Git providers like [GitLab](#gitlab) or [Bitbucket](#bitbucket). Since there is no native integration, you will need to set up a deployment pipeline using their respective CI/CD tools (GitLab CI, Bitbucket Pipelines) to sync your code to fortrabbit.

Codeberg is under consideration too.

---

## GitHub
{#github-1}

Learn how the most popular Git-as-a-service provider is integrated with fortrabbit.

### About GitHub
{#about-github-1}

You hopefully already know that [GitHub](https://github.com) (by Microsoft) is the most popular choice for versionized code hosting and collaborating. It is free to use to some extend. Similar alternatives are Bitbucket and GitLab.

**GitHub is not Git**: GitHub is so popular that beginners sometimes confuse GitHub with Git. Git is the version control system; GitHub provides Git hosting plus collaboration features. If you're new to Git, check out our [getting started with Git article](#git-intro).

### Built-in GitHub integration
{#built-in-github-integration}

fortrabbit services tightly integrate with GitHub. Install the [fortrabbit GitHub app](#the-fortrabbit-github-app) to connect GitHub repos with apps hosted on fortrabbit. See the [deployment intro](#deployment-intro) to get started.

The built-in GitHub integration is easiest way to enable automatic deployments on `git push`. It includes automatic stack detection and [software templates](#software-templates) to auto-configure [build commands](#build-commands), [post-deploy commands](#post-deploy-commands) and other deployment related settings.

### Using GitHub Actions
{#using-github-actions}

GitHub is also offering [Github Actions](https://github.com/features/actions), an integrated continuous integration solution. Combining GitHub Actions with fortrabbit can help to integrate even more advanced CI/CD workflows. fortrabbit does not offer predefined GitHub Actions (currently), [this blog post](https://blog.fortrabbit.com/how-to-use-github-actions) contains two templates to get started.

To use GitHub Actions, disable the built-in integration. Use [rsync](#rsync-deployment) or some other [SSH based workflow](#direct-code-access) to deploy code to the web space.

Create an SSH key on GitHub and add this as a [deploy key](#deploy-keys) to fortrabbit so that GitHub can has access on the desired environments.

---

## Bitbucket
{#bitbucket}

Integrate the second most popular Git-as-a-service provider with your fortrabbit workflow.

::CallOut{alert}
At the time of the writing, there is no fortrabbit Bitbucket app to automatically integrate Bitbucket. Also, this article might be outdated. Get in touch with us if you want this feature or something is not working out.
::

### About Bitbucket
{#about-bitbucket}

[Bitbucket](https://bitbucket.org?utm_source=fortrabbit), similar to GitHub, is a Git hosting service that offers advanced Git work-flows, such as 'pull requests'. It offers private repos in a free plan. It also offers [paid plans](https://www.atlassian.com/software/bitbucket/pricing) for "growing teams".

### Deployment pipeline
{#deployment-pipeline}

You can use Bitbucket Pipelines to deploy your code to fortrabbit. This involves creating a pipeline that syncs your code to the fortrabbit App using rsync.

#### Prerequisites
{#prerequisites}

1. Generate a dedicated SSH key pair locally (e.g. `ssh-keygen -t ed25519 -f bitbucket_deploy_key -C "Bitbucket CI"`).
2. Copy the public key (`bitbucket_deploy_key.pub`) and add it as a deploy key in the fortrabbit dashboard.
3. Copy the private key (`bitbucket_deploy_key`) and add it to your Bitbucket repository variables as `SSH_PRIVATE_KEY`.

#### Example pipeline
{#example-pipeline}

Create or update your `bitbucket-pipelines.yml` file in the root of your repository. The following code is UNTESTED:

```yml
image: alpine:latest

pipelines:
  branches:
    main:
      - step:
          name: Deploy to Production
          script:
            - apk add --no-cache rsync openssh-client
            # Setup SSH agent
            - eval $(ssh-agent -s)
            - echo "$SSH_PRIVATE_KEY" | tr -d '\r' | ssh-add -
            - mkdir -p ~/.ssh
            - chmod 700 ~/.ssh
            
            # Add fortrabbit to known hosts (replace region if necessary)
            - ssh-keyscan -H ssh.{{region}}.frbit.app >> ~/.ssh/known_hosts
            
            # Sync to fortrabbit
            - rsync -av --delete ./ {{app-env-id}}@ssh.{{region}}.frbit.app:
```

---

## GitLab
{#gitlab}

Integrate GitLab with your fortrabbit workflow using CI/CD pipelines.

::CallOut{alert}
At the time of writing, there is no native fortrabbit GitLab app. This article describes how to set up a manual integration using GitLab CI/CD. Ping us with your requirements or something is not working out here.
::

### About GitLab
{#about-gitlab}

[GitLab](https://about.gitlab.com/) is a popular tool that provides a Git-repository manager with wiki, issue-tracking and CI/CD pipeline features. You can use GitLab CI/CD to deploy your code to fortrabbit. This involves creating a pipeline that syncs your code to fortrabbit using [rsync](#rsync-deployment).

### Prerequisites
{#prerequisites-1}

1. Generate SSH key: You need a dedicated SSH key pair for the pipeline. Generate one locally (e.g. `ssh-keygen -t ed25519 -f gitlab_deploy_key -C "GitLab CI"`).
2. Add to fortrabbit: Copy the public key (`gitlab_deploy_key.pub`) and add it as a deploy key in the fortrabbit dashboard.
3. Add to GitLab: Copy the private key (`gitlab_deploy_key`) and add it to your GitLab project's CI/CD variables as `SSH_PRIVATE_KEY`.

### Example workflow
{#example-workflow}

Create or update your `.gitlab-ci.yml` file in the root of your repository. The following code is UNTESTED:

```yaml
stages:
  - deploy

deploy_production:
  stage: deploy
  image: alpine:latest
  only:
    - main
  script:
    - apk add --no-cache rsync openssh-client
    # Setup SSH agent
    - eval $(ssh-agent -s)
    - echo "$SSH_PRIVATE_KEY" | tr -d '\r' | ssh-add -
    - mkdir -p ~/.ssh
    - chmod 700 ~/.ssh
    
    # Add fortrabbit to known hosts (replace region if necessary)
    - ssh-keyscan -H ssh.{{region}}.frbit.app >> ~/.ssh/known_hosts
    
    # Sync to fortrabbit
    - rsync -av --delete ./ {{app-env-id}}@ssh.{{region}}.frbit.app:
```

---

## Codeberg
{#codeberg}

Integrate Codeberg with your fortrabbit workflow using Woodpecker CI.

::CallOut{alert}
At the time of writing, there is no native fortrabbit Codeberg app. This article describes how to set up a manual integration using Codeberg CI (Woodpecker). Ping us with your requirements or if something is not working out here.
::

### About Codeberg
{#about-codeberg}

[Codeberg](https://codeberg.org/) is a democratic community-driven, non-profit software development platform operated by Codeberg e.V. It is based on Forgejo (a fork of Gitea) and provides a privacy-friendly alternative to commercial Git hosting services.

### Deployment pipeline
{#deployment-pipeline-1}

Codeberg uses [Woodpecker CI](https://woodpecker-ci.org/) for its CI/CD pipelines. You can use it to deploy your code to fortrabbit. This involves creating a pipeline that syncs your code to fortrabbit using [rsync](#rsync-deployment).

#### Prerequisites
{#prerequisites-2}

1. **Generate SSH key**: You need a dedicated SSH key pair for the pipeline. Generate one locally (e.g. `ssh-keygen -t ed25519 -f codeberg_deploy_key -C "Codeberg CI"`).
2. **Add to fortrabbit**: Copy the public key (`codeberg_deploy_key.pub`) and add it as a deploy key in the fortrabbit dashboard.
3. **Add to Codeberg**:
    * Go to your repository settings in Codeberg.
    * Navigate to **Settings** > **Secrets**.
    * Add a new secret named `SSH_PRIVATE_KEY` and paste the content of your private key (`codeberg_deploy_key`).

#### Example pipeline
{#example-pipeline-1}

Create a `.woodpecker.yml` file in the root of your repository. The following code is UNTESTED:

```yaml
steps:
  deploy:
    image: alpine:latest
    secrets: [ ssh_private_key ]
    when:
      branch: main
      event: push
    commands:
      - apk add --no-cache rsync openssh-client
      # Setup SSH agent
      - eval $(ssh-agent -s)
      - echo "$SSH_PRIVATE_KEY" | tr -d '\r' | ssh-add -
      - mkdir -p ~/.ssh
      - chmod 700 ~/.ssh
      
      # Add fortrabbit to known hosts (replace region if necessary)
      - ssh-keyscan -H ssh.{{region}}.frbit.app >> ~/.ssh/known_hosts
      
      # Sync to fortrabbit
      - rsync -av --delete ./ {{app-env-id}}@ssh.{{region}}.frbit.app:
```

---

## Git hosting
{#git-hosting}

Integrate your Git workflow with fortrabbit.



---

## Application Performance Monitoring
{#application-performance-monitoring}

Application Performance Monitoring (APM) tools are essential for professional software development. Think PHP profiling.

APM tools help you look inside your running application to identify performance bottlenecks, slow database queries, and runtime errors. Instead of guessing why your app is slow, APM tools give you data-driven insights to optimize your code effectively.

fortrabbit hosting aims to provide you [actionable metrics](#metrics) to help you identifying issues without the need of an extra service. But professional APM tools are more than just server metrics. They can be essential.

### Relation to web analytics
{#relation-to-web-analytics}

APM tools focus on application and infrastructure performance, while [web analytics](/4.integrations/11.web-analytics) track user behavior and traffic patterns. Some modern APM tools like Sentry and PostHog include analytics features, providing error tracking, user insights and more in one platform. Consider using APM tools for sophisticated backend monitoring and web analytics for simple user interactions.

### Open source alternative
{#open-source-alternative}

* [PHP SPX](https://github.com/NoiseByNorthwest/php-spx)

---

## Blackfire
{#blackfire}

Blackfire is a popular PHP profiling tool from the makers of Symfony. Integrate it with fortrabbit.

### About Blackfire
{#about-blackfire}

Blackfire empowers all developers and IT/Ops to continuously verify and improve their app's performance, throughout its life cycle - by getting the right information at the right moment. Blackfire enables to write performance tests that can be run along your standard test suite. It also provides recommendations to help you improve the performance of your application.

Using Blackfire in production will gain even better insights, once your App will receive traffic. Knowing about the performance of your code will make you a better developer and you will also likely be able to reduce hosting costs here by refactoring your code for a better performance.

### Pricing
{#pricing-2}

Blackfire is integrated with a BYO (Bring Your Own) license model. Once your project is ready for production and you have routed a domain, you will need a [Blackfire paid plan](https://www.blackfire.io/pricing).

### Integration
{#integration}

To use Blackfire with your fortrabbit environment, you only need to paste the Agent credentials from Blackfire into the fortrabbit dashboard. Here is a detailed step by step guide:

#### Over at Blackfire
{#over-at-blackfire}

- Sign up or log in to [Blackfire](https://blackfire.io).
- Click your Profile > Account -> Credentials -> [My Server Credentials](https://blackfire.io/my/settings/credentials)
- Copy the credentials: Server ID and Server Token

#### At fortrabbit
{#at-fortrabbit}

- Log in to the dashboard
- Navigate to your app > environment > PHP > Debugging
- Enable Blackfire
- Paste the Blackfire Server ID and Server Token
- Save the PHP settings
- Wait at least one minute, so that the containers are restarted with the new configuration

#### At your browser
{#at-your-browser}

- Install the [Chrome Extension](https://blackfire.io/docs/integrations/chrome) or the [Firefox one](https://blackfire.io/docs/integrations/browsers/firefox) depending on your favorite browser
- Browse to your App
- Hit the Blackfire button to start profiling

### Limitations
{#limitations-3}

There is no way to profile CLI calls (except through [PHP SDK](https://blackfire.io/docs/integrations/php/sdk)) for now.

---

## New Relic
{#new-relic}

Combine the popular software analysis tool with fortrabbit.

### About New Relic
{#about-new-relic}

[New Relic](https://www.newrelic.com) is a suite of professional software analysis tools. It offers analytics and deep insights on your Apps' performance and possible bottle necks. New Relic integrates as a PHP extension, which is installed (but not enabled) on all fortrabbit Apps.

### Usage
{#usage-3}

fortrabbit has a Bring-Your-Own-License integration with New Relic. That basically means: you need an account over at New Relic. Then you only need to paste the license key in our dashboard.

#### Over at New Relic
{#over-at-new-relic}

1. Sign up or log in to [New Relic](https://newrelic.com).
1. Add a new application
1. Copy the license key

#### At fortrabbit
{#at-fortrabbit-1}

1. Log in to the dashboard
1. Navigate to your environment > settings > New Relic
1. Paste the New Relic license key
1. Save

You are all good! After 5 minutes you should start to see data in your NewRelic dashboard. To get more information about how to use NewRelic, head to their [documentation](https://docs.newrelic.com/docs/apm/new-relic-apm/getting-started/introduction-new-relic-apm).

---

## Tideways
{#tideways}

::CallOut{alert}
Tideways is currently not supported.
::

[Tideways](https://tideways.com/) is an Application Performance Monitoring (APM) tool specifically designed for PHP. It's from Germany, the makers are deeply rooted in the PHP scene. It helps developers identify performance bottlenecks and optimize their applications.

Tideways is currently under consideration. It requires a custom PHP extension and a daemon process, which are not part of our standard stack yet. We are monitoring demand for this integration.

Want it? Let us know! :ContactUs{text="Get in touch"}

---

## Laravel Nightwatch
{#laravel-nightwatch}

::CallOut{alert}
Laravel Nightwatch is currently not supported.
::

Laravel Nightwatch is a new PHP profiling tool. It is part of the Laravel eco system and thus hyped a lot. The daemon process shall run on a [worker job](#jobs). But per requirement that process needs to be reached from the outside, which currently is not possible.

Let us know if you want it. Your signal help us. :ContactUs{text="Get in touch"}

---

## SigNoz
{#signoz}

::CallOut{alert}
SigNoz is currently not supported.
::

[SigNoz](https://signoz.io/) is an open-source APM and observability tool. It provides a unified UI for metrics, traces, and logs. It is native to OpenTelemetry.

SigNoz integration requires running the OpenTelemetry Collector and instrumenting your application. This is currently not supported on our platform. We are monitoring demand for this integration.

Want it? Let us know! :ContactUs{text="Get in touch"}

---

## DataDog
{#datadog}

::CallOut{alert}
DataDog is currently not supported.
::

[DataDog](https://www.datadoghq.com/) is a service for large applications, providing monitoring of servers, databases, tools, and services, through a SaaS-based data analytics platform. It's especially useful when your business has multiple different stacks.

DataDog requires the DataDog Agent to be installed on the server, which is not possible in our shared environment. We are monitoring demand for a potential integration.

Let us know if you want it. Your signal help us. :ContactUs{text="Get in touch"}

---

## Flare
{#flare}

::CallOut{alert}
Flare is currently not supported.
::

[Flare](https://flareapp.io/) is a popular error tracker for Laravel developers. It is created by Spatie. It helps you track exceptions and errors in your application. Recently

We look into supporting Flare. :ContactUs{text="Get in touch"}

---

## Application Performance Monitoring
{#application-performance-monitoring-1}

Monitor where your app is slow.



---

## Email account providers
{#email-account-providers}

fortrabbit is not offering any email accounts, think IMAP, POP3. Here is how to choose a provider to host your personal mails.

### About email accounts
{#about-email-accounts}

There are two types of email services you may require to run your business, but which are not included with fortrabbit services:

1. **Email accounts for you humans**, this article
2. Emails sent from your application, see [transaction mails](#transactional-email-services)

### Integration with fortrabbit
{#integration-with-fortrabbit}

There is actually no connection between fortrabbit and your email account provider. You need to connect the mail provider with your external domain. Just point the MX (DNS) records to the email provider.

---

## Email account providers
{#email-account-providers-1}

### Email account provider types
{#email-account-provider-types}

There are roughly two paths to host email accounts with your own domain:

- Classical web-hosting packages often include domain registration and e-mail services. Some [domain providers](#domain-registration-providers) also offer email accounts.
- A dedicated email service may has advanced features such as office integration, team management, a more fancy mail client, backups …

### Considerations
{#considerations-2}

- Privacy and security
- GEO location
- Pricing

### Some email account providers
{#some-email-account-providers}

Here are some IMAP/POP3 email account providers popular with our clients:

- [Goolge Workspace](https://workspace.google.com/) - Full fledged office suite w Gmail for your domain
- [Namecheap Email](https://www.namecheap.com/hosting/email.aspx) - Email offering from domain provider
- [ProtonMail](https://protonmail.com) - Secure mail from Switzerland
- [FastMail](https://www.fastmail.com)- Original email as a service
- [Zoho mail](https://www.zoho.com/mail)- Office solution with free entry
- [AWS workmail](https://aws.amazon.com/workmail) - AWS has everything
- [runbox](https://runbox.com) - Secure mail from Norway

We have no business relation with any of the above mentioned providers. These are not affiliate links.

### Self hosted
{#self-hosted}

- [Stalwart](https://stalw.art/) - A modern, high-performance mail server written in Rust.

---

## Personal and work email
{#personal-and-work-email}

Which mail provider to choose in combination with fortrabbit.



---

## Database clients
{#database-clients}

fortrabbit is not offering a hosted phpMyAdmin. Database clients can help you connect to the remote database and your local databases.

* safe: You connect via SSH tunnel
* fast: Native app
* smart: Auto-complete, history, bookmarks
* unified: Handle local and remote DBs in one place

---

## MySQL Workbench
{#mysql-workbench}

Connect to your fortrabbit database using MySQL Workbench.

[MySQL Workbench](https://www.mysql.com/products/workbench/) is the official unified visual tool for database architects, developers, and DBAs. It provides data modeling, SQL development, and comprehensive administration tools.

It's free to use and is popular among Windows users. We don't have much first hand experience setting it up.

### Connection setup
{#connection-setup}

To connect to your fortrabbit database, you need to set up a **Standard TCP/IP over SSH** connection.

1. Open MySQL Workbench and click the **+** icon to add a new connection.
2. **Connection Name**: Give it a name (e.g., `My App`).
3. **Connection Method**: Select `Standard TCP/IP over SSH`.
4. **SSH Hostname**: `ssh.{{region}}.frbit.app`
5. **SSH Username**: `{{app-env-id}}`
6. **SSH Key File**: Browse and select your local private SSH key (e.g., `~/.ssh/id_rsa`).
7. **MySQL Hostname**: `mysql` (Do not use localhost or an IP address).
8. **MySQL Server Port**: `3306`
9. **Username**: `{{app-env-id}}`
10. **Password**: Click **Store in Keychain** and enter your database password from the Dashboard.
11. **Default Schema**: `{{app-env-id}}`

Click **Test Connection** to verify everything is working, then **OK** to save.

---

## Sequel Ace
{#sequel-ace}

Connect to your fortrabbit database using Sequel Ace.

[Sequel Ace](https://sequel-ace.com/) is a fast, open-source, native MySQL/MariaDB client for macOS. It is the successor to the popular Sequel Pro. It's free to use. We like it.

### Connection setup
{#connection-setup-1}

To connect to your fortrabbit database, use the **SSH** connection tab.

1. Open Sequel Ace and select the **SSH** tab.
2. **Name**: Give it a name (e.g., `My App`).
3. **MySQL Host**: `mysql` (Do not use localhost or an IP address).
4. **Username**: `{{app-env-id}}`
5. **Password**: Enter your database password from the Dashboard.
6. **Database**: `{{app-env-id}}`
7. **Port**: `3306`
8. **SSH Host**: `ssh.{{region}}.frbit.app`
9. **SSH User**: `{{app-env-id}}`
10. **SSH Key**: Select your local private SSH key (e.g., `~/.ssh/id_rsa`).

Click **Test Connection** to verify, then **Connect** or **Add to Favorites**.

---

## TablePlus
{#tableplus}

Connect to your fortrabbit database using TablePlus.

[TablePlus](https://tableplus.com/) is a modern, native, and friendly tool for relational databases. It supports macOS, Windows, and Linux. We don't use it, but like it.

### Connection setup
{#connection-setup-2}

To connect to your fortrabbit database, you need to configure the connection with **Over SSH**.

1. Open TablePlus and create a new connection.
2. Select **MySQL** as the driver.
3. **Name**: Give it a name (e.g., `My App`).
4. **Host**: `mysql` (Do not use localhost or an IP address).
5. **Port**: `3306`
6. **User**: `{{app-env-id}}`
7. **Password**: Enter your database password from the Dashboard.
8. **Database**: `{{app-env-id}}`
9. Enable **Over SSH**.
10. **Server**: `ssh.{{region}}.frbit.app`
11. **Port**: `22`
12. **User**: `{{app-env-id}}`
13. **Use SSH Key**: Select your local private SSH key.

Click **Test** to verify the connection, then **Save**.

---

## phpMyAdmin
{#phpmyadmin}

It's considered bad practice to install phpMyAdmin on fortrabbit. However, you can also manage the remote MySQL with a local phpMyAdmin installation.

### Configure local phpMyAdmin
{#configure-local-phpmyadmin}

Add an additional server configuration to your local phpMyAdmin `config.inc.php` file like so:

```raw
$cfg['Servers'][$i]['verbose']      = '{{app-env-id}}';
$cfg['Servers'][$i]['host']         = '127.0.0.1';
$cfg['Servers'][$i]['port']         = '13306'; // like specified with tunnel command
$cfg['Servers'][$i]['connect_type'] = 'tcp';
$cfg['Servers'][$i]['extension']    = 'mysqli';
$cfg['Servers'][$i]['compress']     = FALSE;
$cfg['Servers'][$i]['auth_type']    = 'cookie';
$i++;
```

Then open a terminal tunnel, then visit your local phpMyAdmin in the browser. You will be asked for the MySQL user and password. Using a local phpMyAdmin with your remote database requires you to always open a tunnel first.

### Why not install phpMyAdmin on fortrabbit
{#why-not-install-phpmyadmin-on-fortrabbit}

**Security**: Don't expose a UI to access your production database. **Practical reasons**: Don't pollute your git or keep the remote out of sync.

### Better alternatives
{#better-alternatives}

Connect to the remote database from your machine directly. [AdminNeo](https://www.adminneo.org/) is a modern phpMyAdmin alternative.

---

## Database clients
{#database-clients-1}

fortrabbit does not have phpmyadmin, use a GUI to access the remote database.



---

## Git clients
{#git-clients}

While the terminal is the universal interface for Git, graphical clients can make complex tasks easier and help visualize history.

### Prerequisite
{#prerequisite}

Have a look at our [git intro](#git-intro) if that is new to you.

### Options to use Git
{#options-to-use-git}

* **Terminal**: Fast, scriptable, universal. Great for standard commands.
* **GUI**: Visual, discoverable. Great for reviewing diffs, resolving merge conflicts, browsing commit history, squashing commits.
* **IDE**: Integrated, close, good for daily tasks, also PRs.

### IDEs with Git support
{#ides-with-git-support}

Most modern code editors come with excellent Git integration out of the box.

* **VS Code**: Has a built-in Source Control tab. Great for staging changes and handling merge conflicts inline.
* **PhpStorm**: Features a very powerful Git GUI. The "Local History" feature is a life saver.

### Git integration at fortrabbit
{#git-integration-at-fortrabbit}

The fortrabbit platform does not offer a git repo. You connect to a GitHub repo with a Git client.

---

## GitHub CLI
{#github-cli}

[GitHub CLI](https://cli.github.com/) brings GitHub to your terminal with the `gh` command. It reduces context switching between browser and terminal. It is available for macOS, Windows, and Linux for free.

```bash
## Install it with brew on macOS
{#install-it-with-brew-on-macos}
$ brew install gh
```

### Difference to Git
{#difference-to-git}

`git` is the version control system. You use it to track changes, commit code, and sync with a remote repository - [see git intro](#git-intro).
`gh` is the GitHub CLI. You use it to interact with GitHub features that are not part of Git itself, like Pull Requests, Issues, and Releases. Think of it this way:

* **git**: `commit`, `push`, `pull`, `merge`, `checkout`
* **gh**: `pr create`, `issue list`, `release create`, `repo view`

### Create a repo and connect it to GitHub
{#create-a-repo-and-connect-it-to-github}

Here is an example on how to use `git` to create a local repo and `gh` to create and connect a remote repo at GitHub. This will also push the content right away.

```bash
## Initialize a new git repository
{#initialize-a-new-git-repository-1}
git init

## Add files and commit
{#add-files-and-commit-1}
git add .
git commit -m "Init"

## Create a new public repository on GitHub from the current directory
{#create-a-new-public-repository-on-github-from-the-current-directory-1}
gh repo create --public --source=. --push
## Follow the steps
{#follow-the-steps-2}

## Once this is done, just push like this
{#once-this-is-done-just-push-like-this}
git push
```

### More examples
{#more-examples}

```bash
## Create a pull request from your current branch
{#create-a-pull-request-from-your-current-branch}
$ gh pr create
 
## Checkout a pull request locally
{#checkout-a-pull-request-locally}
$ gh pr checkout 123

## List open issues assigned to you
{#list-open-issues-assigned-to-you}
$ gh issue list --assignee "@me"

## View a specific issue in the browser
{#view-a-specific-issue-in-the-browser}
$ gh issue view 123 --web

## Clone a repository
{#clone-a-repository}
$ gh repo clone fortrabbit/docs

## Open the current repository in your browser
{#open-the-current-repository-in-your-browser}
$ gh browse
```

---

## Fork
{#fork}

[Fork](https://git-fork.com/) is a fast and friendly Git client for Mac and Windows and has gained popularity for being extremely fast and having a clean, intuitive interface. It offers a generous free evaluation version (almost free). It's a very good tool for individuals. It's also good as a companion app, when using Git in the terminal or through IDE integration.

---

## Tower
{#tower}

[Tower](https://www.git-tower.com/) is a premium graphical Git client for macOS and Windows. It's great for complex operations like interactive rebase and managing multiple remotes. It's specifically useful to align on git workflows across a team. The pricing is yearly per user.

---

## GitHub Desktop
{#github-desktop}

[GitHub Desktop](https://desktop.github.com/) is an open source Git client by GitHub. It's designed to work seamlessly with GitHub, but it works with any Git repository too. It simplifies many Git concepts, which makes it great for beginners.

---

## Git clients
{#git-clients-1}

Terminal or GUI?



---

## SFTP clients
{#sftp-clients-1}

SFTP clients allows you to transfer files in a visual fashion.

You mostly deploy code via Git. However, SFTP is useful for browsing files, downloading logs, uploading assets, and troubleshooting. See our [SFTP guide](#sftp-access) for connection details and use cases. There are many good clients available. We have guides for the most popular ones.

The older protocols FTP and FTPs are not support on fortrabbit, only the newer SFTP protocol is supported. All clients speak that too.

fortrabbit also does not support username/password authentication for SSH/SFTP. SSH keys need to be used, see [code access](#direct-code-access).

---

## Cyberduck
{#cyberduck}

[Cyberduck](https://cyberduck.io/) is a popular, (free) open-source client that supports SFTP, FTP, WebDAV, Amazon S3, and more. It is available for macOS and Windows. It has a cute icon, but might have become a bit bloated over the years.

### Setup
{#setup}

1. Open Cyberduck and click **Open Connection**.
2. Select **SFTP (SSH File Transfer Protocol)** from the dropdown.
3. **Server**: `ssh.{{region}}.frbit.app`
4. **Port**: `22`
5. **Username**: `{{app-env-id}}`
6. **SSH Private Key**: Select your private key file from the dropdown or browse for it.
7. Click **Connect**.

You can also save this as a bookmark for easier access later.

---

## Transmit
{#transmit}

[Transmit](https://panic.com/transmit/) by Panic is widely considered the best file transfer client for macOS. It's fast, reliable, and integrates well with the OS. Unlike other tools here it is paid.

### Setup
{#setup-1}

1. Open Transmit.
2. Click the **Protocol** tab and select **SFTP**.
3. **Address**: `ssh.{{region}}.frbit.app`
4. **User Name**: `{{app-env-id}}`
5. **Password**: Leave blank.
6. Click the **Key** icon next to the password field to select your SSH key.
7. Click **Connect**.

You can save this connection as a "Server" in Transmit for quick access.

---

## FileZilla
{#filezilla}

[FileZilla](https://filezilla-project.org/) is one of the most well-known FTP clients. Its is free software and works on Windows, Linux, and macOS.

::CallOut{alert}
Be careful when downloading the installer, it sometimes bundles optional software.
::

### Setup
{#setup-2}

1. Open FileZilla and go to **File > Site Manager**.
2. Click **New Site**.
3. **Protocol**: Select `SFTP - SSH File Transfer Protocol`.
4. **Host**: `deploy.{{region}}.frbit.com`
5. **Logon Type**: Select `Key file`.
6. **User**: `{{app-env-id}}`
7. **Key file**: Browse and select your private SSH key.
8. Click **Connect**.

---

## PuTTY (PSFTP)
{#putty-psftp}

[PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/) is a classic command line tool for Windows users. PuTTY itself is for SSH terminal access, but the suite includes `PSFTP` for secure file transfers via command line. If you prefer a graphical interface on Windows, we recommend [WinSCP](https://winscp.net/eng/index.php) or [Cyberduck](#cyberduck).

We do not recommend using puTTY on Windows any more. Better use the command `ssh` as it is included Windows Subsystem for Linux (WSL), starting with Windows 10.

---

## WinSCP
{#winscp}

[WinSCP](https://winscp.net/eng/index.php) is a widely used open source SFTP client for Windows. It offers a dual-pane interface and integrated text editor. It's quit old, but it works.

### Setup
{#setup-3}

1. Open WinSCP.
2. **File protocol**: Select `SFTP`.
3. **Host name**: `ssh.{{region}}.frbit.app`
4. **Port number**: `22`
5. **User name**: `{{app-env-id}}`
6. **Password**: Leave blank.
7. Click **Advanced...** > **SSH** > **Authentication**.
8. **Private key file**: Browse and select your private key file.
9. Click **OK** to close Advanced settings.
10. Click **Login**.

You can save the session for quick access later.

---

## SFTP clients
{#sftp-clients-2}

Connect to your App's file system.



---

## Database hosting
{#database-hosting}

fortrabbit provides an optional [MySQL component](#mysql). Some applications require specialized database solutions. Keep your app on fortrabbit, disable the database component, and use an external database provider.

### Connecting to external databases
{#connecting-to-external-databases}

Since fortrabbit allows outgoing connections, you can connect to any external database service that is accessible over the internet.

1. **Provision**: Set up your database with the external provider.
2. **Credentials**: Get the hostname, username, password, and database name.
3. **Env Vars**: Store credentials in [environment variables](#env-vars).

The standard MySQL port 3306 for making outgoing connections is open by default. If your external database uses a different port, open it up by using the [outgoing firewall setting](#outgoing-firewall).

### Latency considerations
{#latency-considerations}

When using an external database, the physical distance between your application (hosted on fortrabbit AWS eu-west-1) and your database matters. Always try to provision your external database in the same region (AWS eu-west-1 / Ireland) to minimize latency.

---

## PlanetScale
{#planetscale}

[PlanetScale](https://planetscale.com/) offers a scalable, serverless MySQL-compatible database. It is built on Vitess, the database clustering system used by YouTube.

### Configuration
{#configuration-5}

Since PlanetScale is MySQL compatible, you can use it with standard PHP MySQL drivers (PDO, mysqli) and frameworks like Laravel or Symfony without special adapters.

#### CA Certificate
{#ca-certificate}

PlanetScale requires a secure connection using a CA certificate. You need to download the CA certificate and make it available to your application.

1. Download the CA certificate from PlanetScale documentation.
2. Add it to your repository (e.g., `config/cacert.pem`).
3. Reference it in your database configuration options.

#### Laravel example
{#laravel-example}

In your `config/database.php`:

```php
'mysql' => [
    'driver' => 'mysql',
    'url' => env('DATABASE_URL'),
    'host' => env('DB_HOST', '127.0.0.1'),
    // ...
    'options' => [
        PDO::MYSQL_ATTR_SSL_CA => base_path('config/cacert.pem'),
    ],
],
```

### Region
{#region}

Select a matching region when creating a PlanetScale database to ensure low data latency with fortrabbit.

---

## Neon
{#neon}

[Neon](https://neon.tech/) is a serverless open-source Postgres database. It separates storage and compute to offer a modern serverless Postgres experience. It features branching, autoscaling, and bottomless storage.

### PHP and Postgres
{#php-and-postgres}

While fortrabbit is currently offers a LAMP stack (Linux, Apache, MySQL, PHP), you can absolutely use Postgres if your application supports it.

#### Extensions
{#extensions}

You need to ensure the `pgsql` or `pdo_pgsql` extensions are enabled. On fortrabbit, these are available. You might need to enable them in your `composer.json` or just use them if they are standard. (Actually, `pdo_pgsql` is usually enabled by default on fortrabbit).

#### Laravel example
{#laravel-example-1}

Laravel supports Postgres out of the box. Just change your default connection:

```bash
DB_CONNECTION=pgsql
DB_HOST=ep-random-name-123456.eu-central-1.aws.neon.tech
DB_PORT=5432
DB_DATABASE=neondb
DB_USERNAME=user
DB_PASSWORD=password
```

### Region
{#region-1}

Neon runs on AWS. Choose a region that is close to your fortrabbit app.

---

## CrateDB
{#cratedb}

[CrateDB](https://crate.io/) is a distributed SQL database built on top of a NoSQL foundation.
It  is a distributed SQL database that makes it easy to store and analyze massive amounts of data in real-time. It is good for IoT and time-series data. CrateDB uses the PostgreSQL wire protocol. So you can use many standard PostgreSQL clients and libraries to interact with it.

### Use Cases
{#use-cases-17}

CrateDB is often used alongside a primary relational database (like the one provided by fortrabbit) to handle high-volume ingest and analytical queries (OLAP), while the primary DB handles transactional workloads (OLTP).

### PHP Integration
{#php-integration}

You can use the `pdo_pgsql` driver to connect to CrateDB.

```php
$dsn = 'pgsql:host=crate-cluster.example.com;port=5432;user=crate;password=';
$pdo = new PDO($dsn);
```

---

## Database hosting
{#database-hosting-1}

Connect to PlanetScale, Neon, TiDB and others.



---

## Transactional email services
{#transactional-email-services}

With fortrabbit you can not use sendmail. Meet transactional mail services.

### Sendmail is not an option any more
{#sendmail-is-not-an-option-any-more}

Back in the days you might have just used the [PHP mail function](http://php.net/manual/en/function.mail.php) like so:

```php
$to      = 'firstname.lastname@gmail.com';
$subject = 'Welcome to awesome service';
$message = 'hello, nice to have you here …';
$headers = 'From: webmaster@mycoolapp.com'

mail($to, $subject, $message, $headers);
```

This does not work any more, since such mails are sent anonymously — not from a real mail server. Your email will simply be ignored by big providers. Sendmail is disabled with our hosting service for this reason, see [quirks](#mailing).

### About transactional emails
{#about-transactional-emails}

Your web application needs to send personalized, triggered emails. For example:

1. double-opt in email to confirm an account
2. an email with the monthly invoice
3. an email to reset a password to login to your service again

This is not a newsletter where one person is sending out the same mail to a bulk of receivers, but a service that sends personalized mails one by one.

Commercial transactional mail offerings are here help. Beside an SMTP interface you'll get: an easy to use restful API, instant delivery, help with setting up your DKIM and SPF records for your domain, email templates, logging, statistics, bounce alerts, click tracking, inbound emails and much more.

---

## More transactional email services
{#more-transactional-email-services}

Here are some commercial services for transactional emails. Sorry, we can't tell you which is the best one — haven't got the time to test them all. Well known are:

- [Amazon SES](https://aws.amazon.com/ses)
- [Postmark](https://postmarkapp.com) - see [article](#postmark)
- [SendGrid](https://sendgrid.com) - see [article](#sendgrid)
- [Mailgun](https://www.mailgun.com)
- [Mailjet](https://www.mailjet.com)
- [SendInBlue](https://www.sendinblue.com)

Not so well known but also available:

- [Doppler Relay](https://www.dopplerrelay.com/en)
- [Dyn email](https://dyn.com/email)
- [GrennArrow](https://www.drh.net)
- [Pepipost](https://pepipost.com)
- [Socketlabs](https://www.socketlabs.com)
- [Sparkpost](https://www.sparkpost.com).

Special mention goes top [mailtrap](https://mailtrap.io) which is a service dedicated to bring you safe email testing with a fake SMTP server to test and view the mails your application is sending. We are using Postmark app ourselves but beside that we have no other business relation to any of the services mentioned here. No affiliate links.

### Self hosted
{#self-hosted-1}

You can also host your own transactional email server. This gives you full control and data privacy, but comes with the responsibility of maintaining the server and — most importantly — managing IP reputation to ensure deliverability.

- [Postal](https://postal.atech.media/) - Open source mail delivery platform for incoming & outgoing e-mail.

---

## Postmark
{#postmark}

### About Postmark
{#about-postmark}

[Postmark](https://postmarkapp.com) is a transactional email service known for its high deliverability and speed. It focuses purely on transactional email (and recently broadcast streams), ensuring your important application emails don't get stuck in queues behind marketing newsletters. Originally it was built by Wildbit and was bought bought by ActiveCampaign in 2022. fortrabbit uses Postmark.

### Booking
{#booking-4}

Head over to [postmarkapp.com](https://postmarkapp.com) to sign up. You can start with a free developer account to test integration.

### Set up
{#set-up}

Set up authentication records in your DNS. Since fortrabbit does not host your DNS, you will need to add these records at your domain registrar or DNS provider (e.g., Cloudflare, GoDaddy, AWS Route53).

Postmark requires the following:

1. DKIM (DomainKeys Identified Mail): A TXT record that verifies the email was sent by a server authorized by the domain owner. Postmark will provide the specific value for this record.
2. Return-Path (Custom Return-Path): A CNAME record (usually `pm-bounces.yourdomain.com`) pointing to `pm.mtasv.net`. This handles bounce processing and aligns the Return-Path domain with your From domain, which is crucial for DMARC alignment.

Once these records are added, you can verify them in the Postmark dashboard.

### Using Postmark with fortrabbit
{#using-postmark-with-fortrabbit}

The official PHP library for Postmark is available on Packagist as `wildbit/postmark-php`.

To install it in your project, run:

```bash
composer require wildbit/postmark-php
```

#### Example usage
{#example-usage-1}

Here is a simple example of how to send an email using the Postmark PHP library. You will need your Server Token from the Postmark dashboard.

```php
use Postmark\PostmarkClient;

// Create a client with your Server Token
// Best practice: Use an environment variable
$client = new PostmarkClient(getenv('POSTMARK_SERVER_TOKEN'));

// Send an email:
// From, To, Subject, Body
$sendResult = $client->sendEmail(
    "sender@example.com",
    "receiver@example.com",
    "Hello from Postmark!",
    "This is just a friendly 'Hello' from your friends at Postmark."
);

echo "Message ID: " . $sendResult->MessageID;
```

There are additional abstraction plugins for CMS and frameworks.

---

## SendGrid
{#sendgrid}

::CallOut{alert}
Heads up. SendGrid was bought by Twilio some time ago. We don't plan to update this guide.
::

### About SendGrid
{#about-sendgrid}

SendGrid offers an e-mail delivery service that assists businesses with transactional e-mail management.

### Booking
{#booking-5}

Choose your desired plan to initiate the sign up. You'll first just need to choose a user name, tell them your email address and choose a password. Later on they want to know a little more about you. "Provisioning" your account includes human! checks.

### Set up
{#set-up-1}

In order to get your mails through the SPAM filter of your users, you'll need to authorize the ownership of the domain you are using — think DNS modifications. fortrabbit is not involved here. You do this with your domain or DNS provider of choice. This is done with DKIM and SPF.

### Using SendGrid with fortrabbit
{#using-sendgrid-with-fortrabbit}

Once you have the setup done, you can finally start using SendGrid from your fortrabbit App. This is straight forward:

The **SendGrid PHP library** [here on GitHub](https://github.com/sendgrid/sendgrid-php) can be required like so:

```json [composer.json]
{
  "require": {
    "sendgrid/sendgrid": "~4.0"
  }
}
```

To send e-mails via the API, you'll need to specify your SendGrid API key. There is also an [PHP SendGrid example on GitHub](https://github.com/sendgrid/sendgrid-php-example) which makes use of both, the API and the SMTP gateway.

---

## Transactional mail providers
{#transactional-mail-providers}

Integrate transactional mail services with fortrabbit.



---

## Web analytics services
{#web-analytics-services}

Web analytics help you understand how visitors interact with your website or application.

Web analytics services provide insights into your website's traffic, user behavior, and content performance. They help you make data-driven decisions about content, design, and marketing strategies.

### Privacy-focused analytics
{#privacy-focused-analytics}

Modern analytics solutions prioritize user privacy while still delivering valuable insights. Privacy-focused alternatives to traditional analytics platforms respect visitor privacy, comply with regulations like GDPR, and often don't require cookie consent banners.

### Integration with fortrabbit
{#integration-with-fortrabbit-1}

All web analytics services work by including a tracking script in your website's HTML. Since you have full control over your application code, you can integrate any analytics service of your choice. All services provide a JavaScript snippet that you add to your page templates. So, there is no integration with fortrabbit required.

### Relation to fortrabbit metrics
{#relation-to-fortrabbit-metrics}

fortrabbit provides server-side analytics called [metrics](#metrics) too. What's the difference?

Server side analytics can be an alternative to client-side JavaScript tracking. Instead of sending data from the browser, analytics data is generated and collected on the web server. Server-side analytics work well in combination with client-side solutions to get a complete picture of user behavior and application performance. In many cases server-side analytics can provide enough insights. Mind that the data aggregation and type of data is different and can not be directly compared.

Before modern browser based web analytics become popular, tools like [Webalizer](https://webalizer.net/), [AWStats](https://www.awstats.org/), and [Analog](https://analog.gsp.com/) analyzed web server log files to generate statistics. Those tools where basically a web UI for the server log files. It's kinda sad that these tools are rarely used today.

### Cookie-less tracking
{#cookie-less-tracking}

Many modern analytics solutions use cookie-less tracking methods that comply with privacy regulations without requiring user consent. This approach often relies on fingerprinting.

#### Limitations of fingerprinting
{#limitations-of-fingerprinting}

Browser fingerprinting attempts to identify users based on technical characteristics like device type, screen resolution, installed fonts, and other device attributes. There are some gotchas with that.

- Modern browsers include privacy features that limit fingerprinting effectiveness (Safari's Intelligent Tracking Prevention, Firefox's Enhanced Tracking Protection)
- Browser extensions like uBlock Origin may block tracking requests as well

Fingerprinting-based analytics may miss data from users with privacy-conscious browser settings, resulting in incomplete visitor insights.

### APM tools with analytics features
{#apm-tools-with-analytics-features}

[Application Performance Monitoring (APM) tools](#application-performance-monitoring) primarily focus on error tracking and performance metrics, but many also include analytics and user behavior features. These tools can also serve as an all-in-one solution for error monitoring and analytics. They may be more expensive and complex than dedicated analytics tools. PostHog is multi-purpose tool, that does error tracking, web analytics, dashboards and more in one go.

---

## Fathom Analytics
{#fathom-analytics}

Fathom Analytics is a Google Analytics alternative that provides simple, useful insights without tracking or storing personal data.

[Fathom Analytics](https://usefathom.com) is a privacy-focused analytics tool. It doesn't use cookies, doesn't track users across websites, and complies with GDPR and CCPA without requiring cookie consent banners.

Founded by Paul Jarvis and Jack Ellis, Fathom was built as a response to increasing privacy concerns with traditional analytics platforms. The founders advocate for ethical data collection and transparency.

Fathom offers a free trial and paid plans for the hosted version. Pricing scales based on the number of page views.

---

## Plausible analytics
{#plausible-analytics}

Plausible is a lightweight and open-source web analytics tool that is privacy-friendly and doesn't use cookies.

### About Plausible
{#about-plausible}

[Plausible Analytics](https://plausible.io) is a web analytics tool. It doesn't use cookies and complies with GDPR and CCPA without requiring consent banners. Plausible offers a  free trial and paid plans for the hosted service. You can also self-host the open-source version for free.

---

## Rybbit analytics
{#rybbit-analytics}

Rybbit is a privacy-focused web analytics platform designed for developers who want simple, fast insights without compromising user privacy.

### About Rybbit
{#about-rybbit}

[Rybbit](https://rybbit.com) is a privacy-focused analytics tool. It doesn't track personal data or use cookies, making it GDPR compliant without requiring consent banners Check [rybbit.com](https://rybbit.com/pricing) for current pricing.

---

## Umami Analytics
{#umami-analytics}

Umami is an open-source analytics tool that can be self-hosted or used as a cloud service.

### About Umami
{#about-umami}

[Umami](https://umami.is) is an open-source analytics tool. It doesn't track personal data, making it GDPR compliant without requiring cookie consent banners. Available as a cloud service or self-hosted. Umami Cloud offers a free tier and paid plans. Self-hosting is free.

It's bit hard to see who is behind Umami. Business appears to be registered in the US.

---

## Matomo
{#matomo}

Matomo is an open-source analytics platform that can be self-hosted or used as a managed cloud service.

### About Matomo
{#about-matomo}

[Matomo](https://matomo.org) is an open-source analytics platform. It doesn't rely on third parties and complies with GDPR, CCPA, and other privacy regulations. Available as a cloud service (paid) or self-hosted (free).

Matomo is well known in the PHP scene and can be self-hosted on fortrabbit services.

---

## Google Analytics
{#google-analytics}

Google Analytics is the most widely used web analytics service, providing comprehensive insights into website traffic and user behavior.

### About Google Analytics
{#about-google-analytics}

[Google Analytics](https://analytics.google.com) is a web analytics service from Google. The current version, Google Analytics 4 (GA4), uses an event-based data model.

### Privacy considerations
{#privacy-considerations}

Google Analytics collects user data and uses cookies. In many jurisdictions, this requires explicit user consent through cookie consent banners. Consider using privacy-focused alternatives like Fathom or Plausible if GDPR compliance without consent banners is important to you. You should review Google's data processing terms and configure Analytics to comply with applicable privacy laws in your region.

### Pricing
{#pricing-3}

Google Analytics is free for most websites. There is a paid version called Google Analytics 360 designed for enterprise customers with advanced needs.

---

## Web analytics
{#web-analytics}

Track and understand your website visitors.



---

## Integrations and combinations
{#integrations-and-combinations}

Extend and combine fortrabbit with other services and tools.



---

## fortrabbit docs
{#fortrabbit-docs}

Welcome! This repo contains the contents of the (new) fortrabbit docs.

### Git repo (this)
{#git-repo-this}

- [github.com/fortrabbit/docs](https://github.com/fortrabbit/docs)

### Contributing
{#contributing}

Found a typo or an error? Do you want to add something about your framework or service of choice? Do you run a 3rd party service or an open source project that can be integrated with fortrabbit? You are more than welcome to contribute.

#### Pull requests
{#pull-requests}

Please find a good balance in the number of commits contained with a pull request. For small typos, just use one commit and one PR. For larger text changes, consider combining commits for readability.

### Frontmatter tags
{#frontmatter-tags}

```yml
---
reviewed: 2024-06-12 # Last reviewed date (and time)
title: # Long title with page
naviTitle: # short title for list views
navigation.excerpt: # additional details for list views
lead: blabla # large text shown at the beginning
navigation: true # lists this page with navigation
sidebar: craft-cms # shows meta data with
nextNav: true # will show
---
```

### Code blocks
{#code-blocks}

Any code block should have a language defined. If applicable also define the file name like so ````php [info.php]`. The following languages are installed: 'apache', 'js', 'json', 'php', 'shell', 'sql', 'ts', 'twig', 'vue', 'yml'. Use apache for`.htaccess` & `.env` files. Use plain for anything else. Use `shell` not `bash` as the language label for terminal stuff.

Indent with two spaces.

### Markdown editor setup
{#markdown-editor-setup}

#### VC Code
{#vc-code}

- Plugins: Markdownlint
- Settings: Auto update Markdown links

See the `.vscode` folder.

#### Obsidian
{#obsidian}

- Plugins: Linter
- Templates: See templates folder

See the `.obsidian` folder.

### Links in general
{#links-in-general}

Don't add tailing slashes to links.

### Internal links
{#internal-links}

Use relative links to local files including the full folder and file name.
Example:

```md
…if not see [here](#setup).
```

Your editor should offer autocomplete for this. Also such links can be automatically updated when the file name changes. Make use of that to avoid dead links.

### Navigation structure
{#navigation-structure}

The content get's rendered by Nuxt Content using Navigation to structure content based on the given folder structure. Please be aware of that. The numbers in front of the folder and files names are for sorting the navigation. The folders are creating a navigation structure.

### Local development
{#local-development-1}

fortrabbit staff can run the fortrabbit docs locally to see documents rendered in the browser. See the instructions of the repo on how to integrate this.

### Deployment
{#deployment-3}

There is currently no automatic deployment set up.

### Dynamic code examples
{#dynamic-code-examples}

Those values will be replaced by JavaScript when users are logged in:

```raw
region: {{region}}
environment-id: {{app-env-id}}
app-env-name: {{app-env-name}}
app-name: {{app-name}}
```

It will dynamically show the correct code examples and dashboard links.

### MDC components
{#mdc-components}

There are some Markdown Components (powered by Nuxt Content) to use:

#### DashboardLink
{#dashboardlink}

```md
:BlockLink{title="" path=""}
```

This parses markdown inside the DIV. With the data-user attribute it checks if the user is logged in, links to the dashboard will be styled as buttons — use a verb to start them!

### Writing conventions
{#writing-conventions}

#### Support driven documentation
{#support-driven-documentation}

These help pages are often used to point clients to answers on common questions. That's why some topics are covered im much detail. Clients are asking for it. So instead of writing an answer in client support, one might just update the help pages and point the client to the new section.

#### Know the target audience
{#know-the-target-audience}

While some implicit technical details are obvious to you, they might not be for the client. Explaining one acronym only with another acronym might not help. Sometimes it needs some more words.

#### Code examples
{#code-examples}

- Open and close code blocks with ````shell` where shell is the language for
  syntax highlighting
- Try to keep code examples together in one block, avoid mixing paragraphs and
  code blocks
- Code blocks follow standard markdown formatting
- Show output only when necessary
- Output should be a comment `#`
- Use comments in between commands to explain what's going on
- `$` to start a command
- Start code examples right away
  - PHP without `<?php`
  - Bash without `#!/bin/bash`

#### Writing
{#writing}

- Use sentence case in headlines
- Don't use too many headlines to structure text
- Available headlines in text: h2, h3, h4, don't go deeper
- Avoid "eg", otherwise choose one style to write it
- Keep lists readable (no sublists, etc)
- Text structure is important, but readability is even more important
- Use ASCII art to illustrate topographies and such things
- Don't use italic > it looks ugly, it's rendered by the browser not the font
- Don't use a paragraph for every sentence
- Write speaking links, not like so: `[here](http://somewhere)` but so:
  `[GitHub project](http…)`
- Don't bullshit. Avoid the use of marketing buzzwords

#### Maintainability
{#maintainability}

- Find the right balance between being general and being precise (aka Captain
  Obvious)
- Very detailed step-by-step articles are easy to follow but get outdated very
  quickly
- Don't use screenshots and images, use words and ASCII graphics
- Don't bury numbers (like prices and limits) in articles
- All those numbers must be managed in the "pricing" and the "specs" page
- Keep it DRY! Don't repeat yourself
- Have one SSOT, link to it
- Don't fully cover the same topic on different places, just link to the
  location

#### File name conventions
{#file-name-conventions}

When creating new files:

- use dashes instead of spaces or low dashes for file names

#### fortrabbit owned words and common casing
{#fortrabbit-owned-words-and-common-casing}

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

#### Times & dates
{#times-dates}

- use the same time-zone E V E R Y W H E R E when communicating times
- the communicated time-zone is UTC
- use relative times (an hour ago, a few seconds ago)
- Markup example:
  `<time datetime="2016-01-01 08:22:10 UTC" title="2018-01-01 08:22:10 UTC">A few minutes ago</time>`
- **ms** — ~~MS~~
- **s** - ~~scds~~
- **m** - ~~mins~~, ~~min~~
- **h** - ~~hrs~~

#### Metric units
{#metric-units}

- **16 MiB** — ~~mb~~, capital letters, a space between value and unit
- **3 GiB** ~~3078 MB~~ < prefer a readable unit
- **0 B**
- **16 KiB**
- 10k — ~~10,000~~
- times a value: ×, `&times`; ~~x~~

#### Other words
{#other-words}

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
- **storage** — ~~webspace~~
- **Composer** — ~~composer~~
- **macOS** — ~~Mac OS X~~

### Avoid words list
{#avoid-words-list}

Please do not use the following "bullshit" words:

- great
- awesome
- innovative
- game-changing
- empowering
- revolutionizing

#### Gender-neutral language
{#gender-neutral-language}

When referencing a hypothetical person, such as "a user with a session cookie", use gender-neutral pronouns (they/their/them). For example, instead of:

- he or she, use they
- him or her, use them
- his or her, use their
- his or hers, use theirs
- himself or herself, use themselves

---

