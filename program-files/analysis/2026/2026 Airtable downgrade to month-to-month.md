---
Title: 2026 Airtable downgrade to month-to-month
Wiki-link: https://utinternational.jira.com/wiki/spaces/AUTO/pages/4678910016
---

# 2026 Airtable downgrade to month-to-month

## 📋 Overview

Perform an analysis on how may we downgrade our Airtable account to Business Plan monthly billing.

| **Team** | Automation Leads |
| --- | --- |
| **Date** | 2026-03-16 |
| **Due Date** | 2026-03-25 |
| **Workstream** |   |
| **Work record** |   |

## Goal

As we downgrade to monthly billing, we aim to lower our monthly spend as well. How may we bring down our cost without disrupting current workflows.

This downgrade also prepares us for the gradual deprecation of the different bases through this year.

## Cost Analysis

### Cost Comparison

| **Option** | **Seat Count** | **Price per seat** | **Monthly** |
| --- | --- | --- | --- |
| Business MtM | 30 | $54 | $1,620.00 |
| Renew 1Y contract | 40 | $45 | $1,800.00 |

### User List

Proposed user list with a count of not more than 30 paid seats.

| **#** | **Account** | **Purpose** | **Replaces** |
| --- | --- | --- | --- |
| 1 | IT Apps Data Manager | _All bases (account owner)_ |  |
| 2 | Mark | _Consolidate with IT Apps Data Manager (needs review, due to integrations)_ |  |
| 3 | Jan | _Multiple bases_ |  |
| 4 | Shela | _Multiple bases_ |  |
| 5 | Team IT Apps | _All bases_ | RK, Harold |
| 6 | RISE IT | _All bases_ | Niels |
| 7 | Team Technology Lead | _Multiple bases_ | Len, Hemant |
| 8 | Team Hissstorical | _Multiple bases_ | Vi |
| 9 | Team Product Lead | _Multiple bases_ | Ashley |
| 10 | Team Maverick | _Multiple bases_ |  |
| 11 | Mindaugas | Sales Central Planning |  |
| 12 | Allyssa | Sites Data QA |  |
| 13 | Team CB | TPS Audit | Ana, Cheska, Jovel |
| 14 | Team Ops | TPS Audit | Karla, Rue |
| 15 | Finance Leads | Finance Reporting | Pax, Queenne |
| 16 | Finance Reporting | Finance Reporting | Jane, Dina |
| 17 | Maria Cecilia | Pathfinders Installation |  |
| 18 | Jeremy | Pathfinders Installation |  |
| 19 | Design Engineers | Pathfinders Installation |  |
| 20 | Design Leaders | Pathfinders Installation |  |
| 21 | FE Engineers | Pathfinders Installation |  |
| 22 | FE Leaders | Pathfinders Installation | Ronald Marto |
| 23 | PD Leads | Pathfinders Installation |  |
| 24 | PD Staff | Pathfinders Installation |  |
| 25 | RoW | Pathfinders Installation |  |
| 26 | Safety | Pathfinders Installation |  |
| 27 | Jun-Jun | Big Glass |  |
| 28 | Roselle | Big Glass |  |

## Procedure

For the monthly billing, we will setup a Business Plan account (referred as _target_ account), with [itapps.datamanager@rise.ph](mailto:itapps.datamanager@rise.ph) as the Account owner.

To perform the migration, perform the following:

1. Upgrade _target_ account to Business Plan
2. Create the destination Workspace(s) in the target account. Useful to distinguish the Workspace names from the source account to minimize confusion during migration. _Though the name can be reverted back after the migration._
3. Ensure itapps.datamanager has an Owner level access to all Workspaces in the source account.
4. **Important:** To minimize unexpected increase in billed seats, review Base-level permissions, and downgrade as much of the users to Read Only. No worry if accidentally downgrading users, since they can be upgraded to paid seats later on – so downgrade as much as possible, to avoid a spike of paid seat count.
5. In each source Workspace, in the page that lists the Bases, click the menu of a base and select `Move`. Then select the destination Workspace under the target account.
6. Moving should take effect within a few minutes.

### Procedure implications

1. Moving a base from one workspace to another, **affects _only_ the following**:
    1. Account ownership of the base (e.g. billing), which it inherits from the target Workspace.
2. **What stays the same**:
    1. The Base ID, and all metadata and records data. This means, the URLs should continue to work.
    2. Permissions are retained, though the target account will inherit the paid seats requirement of the base – thereby affecting the billable paid seats in the target Workspace.

### Continuity Requirements

To ensure a smooth transition to the new account, the following needs to be done ahead:

1. Ensure that the user adjustments as proposed in the User List has been completed, so we won't incur unnecessary surge in paid seats during the migration.
2. Ensure that all Workspace owners (Mark, ITApps.DataManager) are granted Owner permissions in both source Workspaces and target Workspaces.
3. There are API keys attached to Mark and ITApps.DataManager, so having both access to source and the target workspaces, ensures the Apps that depends on these keys continue to work.
4. Un-managed all user accounts from the source Account, using the Admin interface. This ensures the user's account can be managed in the target account.

### More information

- <https://support.airtable.com/docs/moving-airtable-bases-between-workspaces>
- <https://support.airtable.com/docs/transferring-airtable-workspace-base-and-interface-ownership>

## Timeline

Given the annual contract ends on 2026-04-30, ideal to allow at least a few weeks (2 weeks) to start migration – to give time for any issues.

Though not to far ahead, that we'd unnecessarily incur double charges for paid seats. However, we can't avoid it entirely, as the overlap is necessary for a seamless migration.

With this, migration should start from the week of 2026-04-06, and should start with the bases that has less paid seats, so we can migrate and experience the migration early, but not right away scale up the paid seats.

### Migration schedule

Target Workspaces:

* **RISE Target** – where all active bases will go to.
* **Archive Target** – any bases not active, but not ready to be removed yet.

| **Week** | **Bases** | **Paid Seats (Limit 30)** |
| --- | --- | --- |
| 2026-04-06 | _No bases migrated_ _Account creation_ | **Total Paid Seat:** 0+1 = 1 IT Apps Data Manager |
| 2026-04-13 | ✅ RISE IT / Application User Access Grants | **Total Paid Seat:** 1+1 = 2 Mark |
|  | ✅ Staging / Testing: HubSpot | _No new seats_ |
|  | ✅ RISE / Product Catalog ✅ RISE / Services Monitoring ✅ RISE / Sites contribution workflow | **Total Paid Seat:** 2+3 = 5 Jan Team Hisstorical Len _(temporary, to be replaced by Team Technology Lead)_ |
|  | ✅ RISE / BIG Glass OAN Internal ✅ RISE / BIG Glass OAN RSP ✅ RISE / Pathfinders - Delivery | **Total Paid Seat:** 5+1 = 6 Harold |
|  | ✅ RISE / Sites Data QA ✅ RISE / Third Party Services Audit ✅ RISE / Service Records Data QA | **Total Paid Seat:** 6 + 3 = 9 Cecilia Alyssa Shela |
|  | ✅ RISE / Sales Central Planning | **Total Paid Seat:** 9 + 3 = 12 RK _(temporary, to be replaced by IT Apps Dev Lead)_ Mindaugas Team Maverick |
|  | ✅ RISE / Finance Reporting | **Total Paid Seat:** 12 + 4 = 16 Paks _(temporary, may move to team based access)_ Queene _(temporary, may move to team based access)_ Dina _(temporary, may move to team based access)_ Jane _(temporary, may move to team based access)_ |
| 2026-04-20 | ✅ RISE / Sites, Circuits, and Customers | **Total Paid Seat:** 16 + 0 = 16 |
|  | ✅ RISE Delivery / \[Backup\] Pathfinders Installation and Technical Services Co., Inc. ✅ RISE Delivery / STAGING- Customer Build & Engineering | **Total Paid Seat:** 16 + 0 = 16 |
|  | ✅ RISE / Sites, Circuits, and Customers (synced) ✅ RISE / BIG Glass OAN As-Built Network | **Total Paid Seat:** 16 + 2 = 18 Jeremy Jun-Jun |
|  | ✅ RISE / Pathfinders Installation and Technical Services Co., Inc. | **Total Paid Seat:** 18 + 10 = 28 PD Staff PD Leads Safety Right of Way FE Engineers FE Leaders Design Engineers Design Leaders Maria Cecilia Caruscos RISE IT |
| 2026-04-27 | _There should be no more migrations at this week._ |  |
