---
Title: Automation Roadmap 2026
Wiki-link: https://utinternational.jira.com/wiki/spaces/AUTO/pages/4399071233
---

# Automation Roadmap 2026

## Status

**DRAFT** _- on-going development of objectives and timelines_

## Chart

[Automation Roadmap timeline (Jira)](https://utinternational.jira.com/jira/core/projects/IT/timeline?rangeMode=quarters&atlOrigin=eyJpIjoiNTFhMzI4Yzk3YTM2NGYxMjlmNWMyZDIwMGI2NWZjYmEiLCJwIjoiaiJ9)

## Changelog

### Production

Published on 2026-03-17.

### Beta

Published on 2026-02-04.

### Alpha

Published on 2026-01-14.

### Draft

Published on 2025-11-18.

## Active Initiatives

1. [Initiative Network IMS](../../programs/network-intelligence/initiatives/Initiative%20Network%20IMS.md)
2. [Initiative Fulfillment IS](../../programs/enterprise-automation/initiatives/Initiative%20Fulfillment%20IS.md)
3. [Initiative Service Management](../../programs/enterprise-automation/initiatives/Initiative%20Service%20Management.md)
4. [Initiative Ops Analytics](../../programs/business-intelligence/initiatives/Initiative%20Ops%20Analytics.md)
5. [Initiative Sales IS](../../programs/enterprise-automation/initiatives/Initiative%20Sales%20IS.md)
6. [Initiative Finance Analytics 2.0](../../programs/business-intelligence/initiatives/Initiative%20Finance%20Analytics%202.0.md)
7. [Upkeep](https://utinternational.jira.com/wiki/spaces/AUTO/pages/4602626050)

## Objectives

### Primary Objectives

| **Opportunity** | **Objective** |
| --- | --- |
|  |  |
| Network Intelligence / Network IS |  |
| **How may we reliably monitor the network traffic in our operation, using modern, automated systems, that can be integrated with other applications we use.** This is our first production deployment of Prometheus and Grafana for monitoring, and integrate device inventory and configuration with Netbox. These will form the foundation of our network information management system moving forward. |  |
|  |  |
| Automation / Fulfillment IS |  |
| **How may we use an automated ERP system to manage our procurement and inventory processes.** This is a partial objective, aimed to first transition towards a clean and accurate inventory data, before we transition the rest of the workflows. |  |
| **How may we use an automated ERP system to manage our procurement and inventory processes.** Aim is to move to a system managed procurement and inventory process, with a system controlled stock releasing procedure for job orders. |  |
| **How may we use an automated system to manage our customer and site installation processes.** Aim is to incorporate workflows by Design team, with BOM data recorded in the system, and entire lifecycle of a job order (e.g. installation) tracked in the system. |  |

### Regular Objectives

| **Opportunity** | **Objective** |
| --- | --- |
|  |  |
| Automation / Service Management |  |
| **How may we reliably report our historical performance for all services sold ever since we started.** This is a follow-up objective after the roll-out of Service Records in WL. In addition to data migration, we will also be validating information for accuracy and completing gaps if any. After this, all reporting based on SR data set will only source from WL. |  |
| **How may we properly record all OTC payables for services sold.** This is an expansion of SR in WL feature, to properly record OTC information, such as its purpose, amount, as well as automate recording based on the state/changes of a service. |  |
| **How may we efficiently check for feasibility of a service as part of a sales development process.** Aim is to consolidate network, TPS records, and Fiber network information in WL, so it can automatically answer inquires for service feasibility. For edge cases, provide an integrated workflow for requesting manual feasibility check, and record results which can be referred to in later inquiries. |  |
| **How may we accurately record customer requirements, product selection, and configuration, as part of an automated service order workflow.** Aim is to standardized and automate the service quoting and order taking process, and implement the feature in WL. |  |
|  |  |
| Business Intelligence / Ops Analytics |  |
| **How may we transition legacy data to form as historical values of Service Records.** SR formally started representing all sold services from 2026. And to support historical values, data extracted based on circuit records and transitionary service records in Podio, will be used to construct a historical data set for SR. |  |
| **How may we accurately rely and report information of services we bought.** Aim is to audit and clean-up all active third party services, and then establish a regular audit process that CB, AP, and NOC can participate. |  |
| **How may we perform detailed analysis of our revenue and expenses, with attribution to services sold/bought, and support for different reporting categories.** Aim is to refactor the existing revenue items extraction and analytics implementation, and introduce expense items analytics. |  |
|  |  |
| **Automation / Sales IS** |  |
| **How may we consolidate and standardized all sales metrics reporting in QuickSight.** This is a continuation of the effort to deprecate Sales Dashboard in Airtable, and move the reporting in QuickSight. |  |
| **How may we assign RM to Company objects in HubSpot and accurately report portfolio size using Service Records.** This is a refinement effort to establish workflows and rules to properly assign RMs to Company, and standardized the basis in calculating portfolio size using Service Records data. |  |
|  |  |
| Business Intelligence / Finance Analytics 2.0 |  |
| **How may we ensure a maintainable and reliable consolidated accounts reporting in Finance.** This is primarily a refactor effort to upgrade the current implementation, so it can be reliably maintained by the software team; as well as usability improvements for Finance team. Part of this effort is to transition the FR configuration data from Airtable to NocoDB and Reporting from Causal to QuickSight. |  |

### Upkeep

| **Opportunity** | **Objective** |
| --- | --- |
|  |  |
| Decommission |  |
| **How may we transition work loads off Airtable to alternative solutions, and clear it for decommissioning.** This is part of our optimization effort, to consolidate and simplify our IT platforms. |  |
| **How may we transition work loads off Causal to alternative solutions, and clear it for decommissioning.** This is part of our optimization effort, to consolidate and simplify our IT platforms. |  |
