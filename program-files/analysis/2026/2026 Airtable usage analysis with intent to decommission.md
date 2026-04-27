---
Title: 2026 Airtable usage analysis with intent to decommission
Wiki-link: https://utinternational.jira.com/wiki/spaces/AUTO/pages/4564877316
---

# 2026 Airtable usage analysis with intent to decommission

## 📋 Overview

Perform an analysis of the current usage of Airtable, and evaluate options for how to offload / transition usage, with the intent to decomission Airtable.

This document provides only an analysis, while the decision process for the renewal is with IT / Head of IT.

| **Team** | Automation Leads |
| --- | --- |
| **Date** | 2026-01-21 |
| **Due Date** | 2026-02-23 |
| **Workstream** |   |
| **Work record** |   |

### Context

Previously, we intended not to renew our Airtable license at the current contract's term end date of 2026-04-30.

However, that date is fast approaching, and to off-load users now, cause a serious risk in our team's workflows.

Instead, the proposed plan is to renew, _**BUT with a strong intention to decomission sooner**_ than the default 1 year renewal term.

### Reference Files

[Google Drive Folder in IT Apps shared drive](https://drive.google.com/drive/folders/11GFdfK-G-XwGp-qblJwyPk6pPfwzAhd8?usp=drive_link)

## Mapping

We bought 40 paid editor seats, and as of 2026-01-21, **39** is in use.

Airtable is structured across Workspaces and Bases.

The list of workspaces in our account are as follows:

1. RISE
2. RISE Delivery
3. RISE IT
4. RISE Sales 2024
5. Staging
6. Archive

A detailed list of bases is as follows:

| **Basename** | **Purpose** | **Assigned Analyst(s)** | **In Solution?** |
| --- | --- | --- | --- |
|  |  |  |  |
| **RISE** |  |  |
| BIG Glass OAN Internal | **Purpose:** Created for Accounting use. Interface here contains an overall dashboard showing the total number of circuits activated and newly activated circuits within Mandani Bay Suites and Mandani Bay Boardwalk per RSP. **Risk:** High. Currently being maintained as the source for Accounting's monthly billing. To decommission, this can be transferred to the system where the main BIG Glass OAN data will be migrated, for as long as analytics are supported. | IT Apps / @Harold Aviso | ✅ |
| BIG Glass OAN RSP | **Purpose:** Created for RSP use. The interface here shows the circuit information specific to an RSP. Information includes: Location, Floor/Unit, connected Port ID, RSP service ID, Service connected date, request date, and test results. This view also includes the different RSP request forms: Tenant Connection, Tenant Disconnection, and Fault Reporting. **Risk:** High. Currently the main base of operations for the RSP (mainly Globe). To decommission, this can be transferred to the system where the main BIG Glass OAN data will be migrated, for as long as analytics and service requests are supported as well. | IT Apps / @Harold Aviso | ✅ |
| Deal Analysis | Test workspace. For decommissioning since it's not used anymore. **No of Users:** 0 **Risk Assessment:** No risk for decommissioning this workspace. | IT Apps / @Ronnie Kris Dominguez | ✅ |
| Finance Reporting |  | Software / @Hemant Sureshkumar | ✅ |
| HubSpot Companies | Test workspace. For decommissioning since it's not used anymore. **No of Users:** 0 **Risk Assessment:** No risk for decommissioning this workspace. Sync automation which is triggered from HubSpot can be turned off. | IT Apps / @Ronnie Kris Dominguez | ✅ |
| OpenAI Prompt Log | Test workspace for OpenAi before. For decommissioning since it's not used anymore. **No of Users:** 0 **Risk Assessment:** No risk for decommissioning this workspace. | IT Apps / @Ronnie Kris Dominguez | ✅ |
| Operations and Performance | Test workspace for Operations Team (Karla's). For decommissioning since it's not used anymore. **No. of Users:** 2 **Risk Assessment:** No risk for decommissioning this workspace. | IT Apps / @Ronnie Kris Dominguez | ✅ |
| Pathfinders - Delivery | **Purpose:** Originally created as a dashboard for requestors to check the current status of their requests. This is no longer in use. **Risk:** No risk. OK to decommission immediately. | IT Apps / @Harold Aviso | ✅ |
| Product Catalog | Essentially a copy of FR Products and FR Plans. Data is pulled from this base for reports on plans and products. **Risk Assessment:** We will need to point the reports to retrieve products and plans from the new source. | Software / @Hemant Sureshkumar | ✅ |
| Sales Central Planning | Serve as the primary workspace for Sales by consolidating core datasets synced from HubSpot, including Deals, Deal Owners, and Transition Records (Tasks are deprecated). The workspace also provides interface dashboards to support Sales reporting and performance analysis. **No. of Users:** 46 **Risk Assessment:** High. Transition-based reports and dashboards have already been replicated in QS, reducing dependency on AirTable for those use cases. However, the majority of Sales reporting and analysis still relies on the Deals dataset, which remains a key risk area if AirTable access is reduced or decommissioned before full migration. | IT Apps / @Ronnie Kris Dominguez | ✅ |
| Sales Central Planning (Testing Ground) | This is a temporary duplicate base of SCP used for testing automation updates prior to implementation to Prod. **No. of Users:** 13 **Risk Assessment:** No risk. This can be decommissioned. | IT Apps / @Ronnie Kris Dominguez | ✅ |
| Service Records Data QA | Contains data from Sites, Podio SRs, SR vs Circuit Recon, Customer and Service Count Recon. All of these tables are being used to support Service and Customer metrics audits. **Risk Assessment:** The base is our key reference for SR audits so it should be migrated to another audit platform before deprecation. | IT Apps / @Jan Frances Ranada | ✅ |
| Services Monitoring | Purpose: Contains synced Deals, Sites, Circuits, Customers, and Service Records. Used to assist with the initial import of Service Records into Podio. **~~Risk Assessment:~~** ~~None. Confirmed with previous users that this is no longer in use. Can be removed.~~ **Risk Assessment:** We have used this Base in the Make scenarios that sync SR in Podio to SR in HubSpot. | Software / @Olivia Pangilinan | ✅ |
| Sites contribution workflow | Workflow/Form is linked to Birdy search results with the intention of allowing anyone using birdy to submit proposed site data changes. **Risk Assessment:** The workflow is partially in use with not much requests being received. This can be migrated to another platform. | IT Apps / @Jan Frances Ranada | ✅ |
| Sites Data QA | Contains synced data from SAQ Deals, Acquisition, Contracts, Sites, Circuits, and Delivery Sites to support monthly audits of acquired, wired, and lit sites. **Risk Assessment:** There is a defined audit process in place. The base is actively used for monthly audits and should be migrated to another audit platform before deprecation. | IT Apps / @Jan Frances Ranada | ✅ |
| Sites, Circuits, and Customers | A base that syncs Sites, circuits and customers (Billing entities) from Podio. This changes in this base is then pushed to another base called Sites, circuits and customers (synced) that is used across airtable for Billing Entity, Sites and Circuit References. **Risk Assessment:** All the relationships from other bases that reference Billing Entities, Circuits or Sites must be rebuilt in the new platform | Software / @Hemant Sureshkumar | ✅ |
| Third Party Services Audit |  | Software / @Hemant Sureshkumar | ✅ |
|  |  |  |  |
| **RISE Delivery** |  |  |
| Pathfinders Installation and… | **Purpose:** This base currently holds the entirety of circuits installed under RISE. Used as an order management and task/resource management system. SDMs and FE do the majority of their work here including job triaging and management. **Risk:** High. As this functions as the main work order management and resource allocation platform, it would require an equal (or greater) system to migrate the entirety of this base. To be decommissioned after Odoo development efforts are fully completed. | IT Apps / @Harold Aviso | ✅ |
| Sites, Circuits, and Customers (synced) | A copy of Sites, Circuits and Customer used by other tables in airtable for reference. **Risk Assessment:** Can be deprecated after pointing references to original source. | Software / @Hemant Sureshkumar | ✅ |
| BIG Glass OAN As-Built Network | **Purpose:** This base currently holds the entirety of circuits installed under the BIG Glass OAN product. Used as a master database to record all available and used ports across all installed buildings. **Risk:** High. While mainly a database, this base is also used to receive and support Connection, Disconnection, and Fault requests. To decommission, this will require migration not only to a database, but also to a work order management system. | IT Apps / @Harold Aviso | ✅ |
| STAGING - Customer Build & Engineering | **Purpose:** Originally used to imitate a staging + production development workflow on Airtable. This did not work as intended since the transfer of developments on staging to production was too manual and tedious. **Risk:** No risk. Can be decommissioned immediately. | IT Apps / @Harold Aviso | ✅ |
| \[Backup\] Pathfinders Installation and… | **Purpose:** Kept for legacy data and dashboarding. Created as a backup of the main Pathfinders Airtable base to reduce record count. **Risk:** Minimal risk. Can be decommissioned after transferring data to another database with dashboarding/analytics capabilities. (AWS + Quicksight) | IT Apps / @Harold Aviso | ✅ |
|  |  |  |  |
| **RISE IT** |  |  |
| Application User Access Grants | This can be offloaded, and archived in NocoDB. Can be done as soon as we have a NocoDB instance. | Automation / @Mark John Buenconsejo | ✅ |
|  |  |  |  |
| **RISE Sales 2024** |  |  |
| SCP 2025 Test | **Purpose:** This base served as a temporary environment to model interface behavior and layout following the archival of pre-2025 records. **Risk Assessment:** No risk. This is a non-production test environment ready for decommissioning. | Software / @Len Laurito | ✅ |
| SCP Archive 2024 | **Purpose:** Base was established to offload 2024 transition records from SCP, ensuring the system remained within its record count limits while maintaining data visibility. **Current Status:** Since stakeholders have migrated to QuickSight for all transition-related reporting, the base is no longer required. **Risk Assessment:** No Risk. This can be decommissioned. | Software / @Len Laurito | ✅ |
|  |  |  |  |
| **Staging** |  |  |
| Sandbox: MRC Analytics | Can be removed. | Automation / @Mark John Buenconsejo | ✅ |
| Testing: HubSpot | Can be removed. | Automation / @Mark John Buenconsejo | ✅ |
| Sandbox: Building Saturation | Can be removed. | Automation / @Mark John Buenconsejo | ✅ |
|  |  |  |  |
| **Vi's Workspace** |  |
| DE Sandbox | Can be removed. | Software / @Olivia Pangilinan | ✅ |
|  |  |  |  |

## 🤔 Problem statements

1. What are the risks if moving users off Airtable and into another platform, BEFORE 2026-04-30?
2. How may we offload or transfer use cases to existing systems or new platforms?
    1. Keep in mind, different platform differs in features, where even if we miss some features, as long as they're not critical, perhaps they're worth moving to.

### Side Quest

If we can move a base / use case off Airtable before the renewal, it may lower the user count we need to renew. So ideal to aim for it. So there's caveat, our agreement is in an "enterprise contract", that has a minimum number of users – which the key benefit is, we are priced per user across workspaces.

## Tasks

- [x] For each base, assigned analyst writes the purpose for each base, and assess the risks for moving off before 2026-04-30. **Please complete by** 2026-02-02**.**
- [ ] Compile the list solutions for all base. **Please complete by** 2026-02-16.
- [ ] Compile the list of users, and with the bases being removed, identify who are for removal / consolidation. **Please complete by** 2026-02-19.

## ⚠️ Risks

These risk assessments are for the **moving off Airtable before** 2026-04-30.

| **Base** | **Potential Issues** | **Recommendation** |
| --- | --- | --- |
| BIG Glass OAN Internal BIG Glass OAN RSP BIG Glass OAN As-Built Network | These contain the inventory of OAN ports available and connected by RSPs. Used primarily by Delivery team, and Finance AR team for billing purposes. We can't move this out immediately. Though there are ideas on how to replace this with WL feature, but the development is not in the 2026 roadmap. | Keep in AT for the time being. Unsure if we can schedule the development of this soon. |
| Sales Central Planning | Still actively used by Sales team as Sales/JEDI Dashboard for Deal performance. An objective in Automation roadmap deprecates this, and is scheduled for effort in 2026 H1. | Keep in AT through the renewal in Apr 2026, and deprecate when able in automation roadmap. |
| Pathfinders / Delivery Airtable | Still actively used by Delivery team as job information system. An objective in Automation roadmap (Fulfillment project) deprecates this in its Phase 2 milestone, which is scheduled for effort in 2026 H2. | Keep in AT through the renewal in Apr 2026, and deprecate when able in automation roadmap. |
| Service Records Data QA Third Party Services Audit Sites Data QA | Still actively used by BI team for the data audit process. Requires effort to transition to NocoDB (considered as one of the solution, see below). But unlikely effort can be scheduled before the renewal. But effort will definitely start, to try to lower the user count at renewal. Since decommissioning of Airtable is managed in the Automation roadmap, effort towards deprecating these bases will progress with the automation roadmap. | Keep in AT through the renewal in Apr 2026, and deprecate when able in automation roadmap. |

## 🌱 Solutions

These solutions are for how to move off a base from Airtable, whether that is before 2026-04-30 or before end of 2026.

| **Description of Solution** | **Status** |
| --- | --- |
| Export data to CSV/JSON and remove base from Airtable: **RISE IT / Application User Access Grants** **Vi's Workspace / DE Sandbox** **Staging / Sandbox: MRC Analytics** **Staging / Testing: HubSpot** **Staging / Sandbox: Building Saturation** **RISE Sales 2024 / SCP 2025 Test** **RISE Sales 2024 / SCP Archive 2024** **RISE / Deal Analysis** **RISE / HubSpot Companies** **RISE / OpenAI Prompt Log** **RISE / Operations and Performance** **RISE / Sales Central Planning (Testing Ground)** **RISE / Pathfinders - Delivery** **RISE Delivery / STAGING - Customer Build & Engineering** |    |
| Setup NocoDB in our IT Office environment (IT RISE AWS Account), and migrate the following base: **Service Records Data QA** **Third Party Services Audit** **Sites Data QA** **Finance Reporting** **Sites, Circuits, and Customers** **TPS Audit** **Sites Contribution Workflow** Implement a NocoDB form within the migrated base to replace the Birdy linked form. | **IMPORTANT: Because each base differs in their features, we'll have to migrate them individually and tracked by their own task.** |
| Setup BaseRow (allegedly Best Airtable alternative) in IT Office environment. |  |
| **Pathfinders Installation / Delivery Airtable** will be deprecated as part of Phase 2 objective in Fulfillment project, that is scheduled to be active in 2026 H2. | _No task card needed, will be tracked in the Fulfillment project (see objectives below)._ **Timeline: Phase 2 is set in 2026 H2** |
| **Sales Central Planning** **Setup NocoDB for SCP** **Identify usable dashboard interfaces from AirTable** Coordinate with Sales Team to confirm the list of usable interfaces Review interface fields to check availability in Deals cache. **Replicate feasible dashboard interfaces in QS using Deals cache** c/o Mindaugas to replicate SCP AirTable dashboards into QS On-board Sales team to utilize QS dashboards **Completely establish new sync methods of data from HS to QS** Synching of Transition Records through synthesizer Synching of Deals and Deal Owners information Replicate dashboards from AT (c/o Mindaugas) **Deprecate SCP from AirTable** Restrict access to SCP base Decommission SCP Base | _No task card needed, will be tracked in the Sales Is objectives (see below)._ **Timeline: end of 2026 Q2** |
| Refactor the synching of SR (in Podio / in WL) to sync directly to HubSpot. **Services Monitoring** | _Development by software, no timeline yet._ |
| Setup NocoDB in our IT Office environment (IT RISE AWS Account), and migrate the base below. Allow analytics through NocoDB/QuickSight to look through legacy data. **\[Backup\] Pathfinders Installation and…** |  |
| Setup NocoDB in our IT Office environment (IT RISE AWS Account), and migrate the base below. Allow NocoDB forms to receive work order requests. **BIG Glass OAN As-Built Network** **BIG Glass OAN Internal\*** Explore NocoDB what's possible in replicating analytics, or may go straight to QS. |  |
| Develop an RSP portal for OAN in WL, and replace the base **BIG Glass OAN RSP**. | _Development by software, no timeline yet._ |
