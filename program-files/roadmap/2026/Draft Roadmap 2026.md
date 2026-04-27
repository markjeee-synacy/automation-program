---
Title: Draft Roadmap 2026
Wiki-link: https://utinternational.jira.com/wiki/spaces/AUTO/pages/4397465604
---

# Draft Roadmap 2026

## Overview

As of Feb 4, 2026, objectives have now been published in the Automation Roadmap:

[Automation Roadmap timeline (Jira)](https://utinternational.jira.com/jira/core/projects/AUTO/timeline?rangeMode=quarters)

This page may no longer be updated.

~~All objectives are in **Intention** stage, unless stated otherwise.~~

**LEGENDS**

**Degree of Importance**

🥇 Prime Objective

🥈 Regular Objective

🎲 Potential Objective

**Stage in Development**

🐣 Zero-to-One (major shift in way of work)

🍎 New scope (minor shift)

🥥 Unfinished scope (continuation from previous objective)

**HEIRARCHY**

1. Program Name
    1. Initiative Name
        1. Objective and Key Results

## Network Intelligence

### **Network IS**

Build the initial NIMS implementations.

[Initiative Network IMS](../../programs/network-intelligence/initiatives/Initiative%20Network%20IMS.md)

#### **Prometheus Monitoring with Netbox SoT** 🥇🐣

Deployed a monitoring system, based on Prometheus, with an initial set of devices reporting metrics. This monitoring system is then in-use by NOC as their source of truth for metrics.

**Key results**

1. Re-deployed Netbox using Annie infrastructure code
2. Prometheus and Grafana accessible by NOC staff
3. Integrated Prometheus to Netbox for device inventory and metadata
4. Integrate commercial information from WL to Netbox

## Enterprise Automation

### **Fulfillment IS**

Build an automated Delivery & Install management process based on the Odoo platform.

[Initiative Fulfillment IS](../../programs/enterprise-automation/initiatives/Initiative%20Fulfillment%20IS.md)

#### **Phase 0.5 - Procurement and clean Inventory in Odoo** 🥇🐣

**TODO**

#### **Phase 1 - Inventory Management in Odoo** 🥇🐣

**TODO**

#### **Phase 2 - Order Fulfillment in Odoo 🥇**🐣

**TODO**

### **Service Management**

Build an automated service management process, from inquiry, to order taking, then activation, and ending at deactivation based on the WL platform.

[Initiative Service Management](../../programs/enterprise-automation/initiatives/Initiative%20Service%20Management.md)

#### Import legacy Service Records to WL 🥈🥥

Load all previously deactivated and cancelled Service Records into WL, with complete information.

**Key results**

1. WL supports and imported all deactivated and cancelled services records
2. Ensure all workflows and automation that rely on Service Record information to integrate with WL _(including those relying on Circuit Record information that have already been migrated to Service Record)_

#### **Record OTC Details for Service Records** 🥈🍎

Properly supported all OTC scenarios for SR in WL.

**Key results**

1. Supported _all_ (e.g. deal won, recontract) OTC scenarios for _all_ Service Records, both present and past.
2. Populated OTC payment details of _all_ Service Records.

#### Service Feasibility checks and workflows 🥈🐣

**TODO**

#### Service Quotation and Order Capture 🎲🐣

**MAYBE**

#### ~~Site Acquisition records and workflows~~ 🎲🐣

**MAYBE** - _As of Feb 3, 2026, may not pursue this year, limited time/resources._

### **Sales IS**

Build an automated sales process management system based on the HubSpot platform.

[Initiative Sales IS](../../programs/enterprise-automation/initiatives/Initiative%20Sales%20IS.md)

#### **Sales Dashboard in QuickSight and reliability improvements** 🥈🥥

Sales Dashboard completely transitioned in Quicksight and Sales Dashboard in Airtable deprecated.

**Key Results**

1. Deal metrics saved directly to BI Warehouse accessible in Quicksight
2. Access to Sales Dashboard in Airtable restricted and Base deprecated

#### **RM portfolio reporting and new commission model** 🥈🍎

**TODO**

## Business Intelligence

### **Ops Analytics**

Build the operational metrics and dashboard.

[Initiative Ops Analytics](../../programs/business-intelligence/initiatives/Initiative%20Ops%20Analytics.md)

#### **Service metrics expanded** 🥈🥥

Deployed historical and quarterly service metrics.

**Key Results**

1. Filled-up historical values in Service Metrics
2. Deployed Quarterly Service Metrics, including historical representation

#### Third Party Metrics audited 🥈🍎

Deployed an audited TPS and Site metrics from start of 2025, established a regular reconciliation process moving forward.

**Key Results**

1. Completely deprecated ISP Spend file
2. Audited TPS Metrics from start of 2025 with Expenses, and established a regular recon process moving forward
3. Audited Site Metrics from start of 2025 with Expenses, and established a regular recon process moving forward
4. Migrated Data Audit workflows to NocoDB

#### Revenue and Expense metrics 🥈🍎

**MAYBE**

#### ~~Deal and Cluster metrics~~ 🎲🍎

**MAYBE** _- As of Feb 3, 2026, may not pursue this year, limited time/resources._

### **Finance Analytics 2.0**

Upgrade implementations of consolidated financial reporting.

[Initiative Finance Analytics 2.0](../../programs/business-intelligence/initiatives/Initiative%20Finance%20Analytics%202.0.md)

#### **Upgrade Consolidated Finance Reporting** 🥈🍎

Improved financial data extractions and usability of consolidated reporting configurations.

**Key Results**

1. Better maintainability of code base using Python and AWS architecture
2. Configurations migrated (e.g. Finance Reporting) to use NocoDB
3. Load data and analytics in Quick Suite
4. Completely deprecated Causal, and provided alternative analysis in Quick Suite / Google Sheet

## Upkeep

### Decommission

#### Decommission Airtable

**TODO**

#### Decommission Causal

**TODO**
