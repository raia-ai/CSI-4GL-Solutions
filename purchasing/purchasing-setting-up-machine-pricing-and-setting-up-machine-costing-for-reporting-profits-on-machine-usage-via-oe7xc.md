---
title: "Setting Up Machine Pricing and Setting Up Machine Costing"
source: "purchasing-setting-up-machine-pricing-and-setting-up-machine-costing-for-reporting-profits-on-machine-usage-via-oe7xc.md"
tags: ['SM3', 'Purchasing']
version: "1.0"
last_updated: "2026-02-19"
short_description: "Setting Up Machine Pricing and Setting Up Machine Costing"
long_description: "This document provides detailed information about setting up machine pricing and setting up machine costing in the 4GL system. It includes procedures, reference information, and best practices for users and administrators."
---
# Setting Up Machine Pricing and Setting Up Machine Costing

**Description**: Accurately track profits on items processed through plasma or any other machine - via the OE7XC report.

To ensure this works effectively, you have two options for capturing machine-related costs:

### 1. Manual Entry During Sales Order Creation
As shown in the screenshots you provided, you can manually enter the machine cost either in the **Cost Price** or **Sales Price** fields during order creation.

### 2. Using Default Values via the Machine Master (PR11)
Alternatively, you can configure default cost and pricing values for machines in the **Machine Master function (PR11)**. When a machine is selected as the **Primary Process** during order creation, these values will be automatically imported. You can use **F4** in the Cost Price to view and confirm the imported values.

For guidance on setting up machine costing in PR11, refer to this help documentation:
Setting Up Machine Pricing and Costing – PR11

Scroll to the bottom for sections on **Setting Up Machine Pricing** and **Setting Up Machine Costing**.

## Examples from Your Test:

### 1. Cost Price Example:
- You entered a cost of **$5 per PC**, which is applied under **Cost of Sales**.
- This cost does hit the **COGS** as expected.

