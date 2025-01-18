---
reviewed: 2024-06-07 17:31:05
title: Service cancellation
naviTitle: Service cancellation
navigation.excerpt: How to quit fortrabbit
lead: Fully or partly cancel fortrabbit hosting services with immediate effect, irreversibly.
head:
  meta:
    - name: 'keywords'
      content: 'subscription, membership, cancel, hosting, payment portal, remove my card'
---

You want to fully cancel any connection to fortrabbit, access the payment portal to remove your card? Delete all [payments methods](#delete-payment-methods) you have access on, then [delete your personal access](#cancel-your-account) so there are no left overs.

You want to clean up, remove unnecessary stuff, reduce costs? See our [reduce hosting costs article](/3.dev/reducing-hosting-costs.md) first, then come back here.

## Delete apps

An [app](/1.platform/10.objects/1.app.md) represents a website or web application. When deleting apps, all it's environments and associated domains will get deleted along. Team members might loose access. Files and databases will be deleted. Costs will be billed up until the day of deletion. Make sure to take backups before deleting apps.

## Delete environments

[Environments](/1.platform/10.objects/2.app-environment.md) are versions of websites. When environments associated domains will get deleted along. Team members might loose access. Files and databases will be deleted. Make sure to take backups before deleting environments.

## Delete teams

[Teams](/1.platform/10.objects/4.team.md) are groups of developers sharing app access. Payment methods, apps and environments that are not shared with other teams or clients will be deleted alongside, when deleting a team. Team developers will loose access to the team. Their accounts will not be deleted immediately.

## Delete payment methods

Make sure to review invoices, pay pay past due invoices if any, download previous invoices. When deleting a payment method, all the apps and attached environments it owns will be deleted alongside. Mind that the [pro rated billing](/15.billing/3.pro-rated-billing.md) cycle is monthly after usage. There will be pending charges for the current month. Even after deleting the payment method one last partial invoice will be sent.

## Cancel your account

When cancelling your [account](/1.platform/10.objects/3.person.md#account-settings), you will remove personal access to the fortrabbit hosting system. By cancelling your account, all non-shared payment methods including all it's apps will get irreversibly deleted along.

Everything that is shared with other team members or clients will NOT be deleted when you cancel your personal account. When you are involved in shared [teams](/1.platform/10.objects/4.team.md) with other members, the teams will not be deleted. You will just leave the teams. The same applies to shared [payment methods](/1.platform/10.objects/9.payment-method.md) and the [apps](/1.platform/10.objects/1.app.md) that are owned by them.

:DashboardLink{title="Cancel your account" path="/confirm/account-delete"}

## Auto deletion of inactive accounts

Abandoned accounts without access to paid objects and no activity will get auto-deleted after a period of time. This is a privacy feature.
