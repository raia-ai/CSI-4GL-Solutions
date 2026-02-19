---
title: "Setting Up Machine Pricing and Setting Up Machine Costing"
source: "purchasing-setting-up-machine-pricing-and-setting-up-machine-costing-for-reporting-profits-on-machine-usage-via-oe7xc.md"
tags: ['SM3', 'Purchasing']
version: "1.0"
last_updated: "2026-02-19"
short_description: "Setting Up Machine Pricing and Setting Up Machine Costing"
long_description: "This document provides detailed information about setting up machine pricing and setting up machine costing in the 4GL system. It includes procedures, reference information, and best practices for users and administrators."
---

title: "Setting Up Machine Pricing and Costing"
source: "Purchasing-Setting_Up_Machine_Pricing_and_Setting_Up_Machine_Costing_for_reporting_profits_on_machine_usage_via_OE7XC.pdf"
tags: ["machine costing", "machine pricing", "sales order", "OE7XC report", "4GL Solutions", "PR11", "Machine Master", "COGS", "profit tracking", "metal industry"]
version: "1.0"
last_updated: "2025-12-03"
short_description: "A guide on setting up machine pricing and costing in 4GL Solutions' software to accurately track profits on processed items. Covers manual entry during sales order creation and setting up default values in the Machine Master (PR11) for automated cost application."
long_description: "This document provides a comprehensive guide for users of 4GL Solutions' 'Technology for the Metal Industry' software on how to configure machine-related costs and prices. The primary goal is to enable accurate profit tracking for items processed through machines, like plasma cutters, with data reflected in the OE7XC report. The guide details two methods for capturing these costs: 1) Manual Entry, where users can directly input values into the 'Cost Price' or 'Sales Price' fields during sales order creation, and 2) Using Default Values, which involves pre-configuring costs and prices in the Machine Master function (PR11). When a machine is selected as the Primary Process, these defaults are automatically imported. The document includes detailed, screenshot-supported examples for both cost application (affecting Cost of Sales/COGS) and sales price application. It also explains the default cost behavior using the 'Dflt Cost' field in PR11 for consistent cost application."
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

