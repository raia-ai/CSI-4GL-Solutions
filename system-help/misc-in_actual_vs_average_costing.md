---
title: "In Actual Vs Average Costing"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "In Actual Vs Average Costing - 4GL Help Documentation"
long_description: "This topic provides detailed information about In Actual Vs Average Costing in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Average vs Actual Inventory Costing
===================================

What is the Costing Method?
---------------------------

Average or Actual costing defines a method of maintaining cost/inventory value and applying cost of goods sold to transactions.

The Average or Actual cost method is set initially at the product line level1, but can be overwritten at the product level2 with appropriate security permissions3. At the order entry line item level, you can select a Freeze flag to use the actual cost of the logs that are picked on the order even if the product is set to average costing.

Many reports have the option to be displayed using actual cost or product average cost.

Regardless of whether the product is set to average or actual cost, users will always have access to both the average cost and the landed cost of goods.

Configuration


1 IN16 > ![](../Resources/Images/i_arrow_down.png) > Options > Costing Method

2 IN17/IN18 > Costing Method

3 MS32 > Options > Inventory > Add'l Options > Allow Costing Method Change

How Average Cost Works
----------------------

Average cost is calculated within individual products. It combines the value of each log (inventory units) and divides it by the quantity of on-hand inventory in that product code.

Average cost is affected during a goods receipt transaction.  will calculate the total value of the current on-hand inventory, add the value of the new receipt and divide the total value by the new on-hand quantity.

The only other transactions that can affect average cost are Inventory Adjustments- Average cost adjustments or introducing new material through an adjustment screen.

Receipt returns also affect average cost as they take out the original value of the receipt, regardless of the current average cost, and re-average with the remaining quantities and value.

When inventory is invoiced, the system credits the inventory account the quantity at the current average cost and applies that value as the COGS to the invoice.

How Actual Cost Works
---------------------

A flag is set against the product line (or product) to indicate that the inventory will be valued using actual cost.

When goods are received the landed cost (base price plus any additional vendor or third party charges) is assigned to the logs (inventory units) and remains as a static value as cost of that inventory.

The cost of inventory logs already received can only be affected by inventory adjustments.

When a sales order or sales quotation is entered, the cost of material is based on average cost, if no specific log is selected. If logs are allocated during sales order entry, the actual cost of the Log is applied.

When inventory is invoiced with an actual cost setting, the landed cost of the specific log is applied to the Cost of Goods Sold of the invoice.

![](../Resources/Images/INV_actual_cost.png)

Pros and Cons
-------------

### Average Cost

| Pros | Cons |
| --- | --- |
| Base-line for reporting—the cost is consistent throughout the product | Not able to reduce cost on remnants/short ends |
| Always have access to individual landed cost information | Require a separate product code for all items which have any cost variance |
| Less fluctuation in cost of goods sold | Cannot always keep domestic and foreign material in the same code if there is a cost difference |
| Less fluctuation with the anticipated margin (quotes and work orders) and the invoice margin |  |

### Actual Cost

| Pros | Cons |
| --- | --- |
| Down Cost material remnants, short ends, scrap, quarantine, etc. | Material can be ‘cherry picked’ meaning high costing material will remain in stock for too long |
| Ability to manage multiple types of material in the same product code without cost distribution (finishes, compatible)—added value processing | When analysing reports and statistics, it is difficult to establish a comparative base-line |
| Contracts, blankets, and stock and release programs are easily managed | Estimated sales margins can fluctuate extensively |
| Ability to control buying costs for specific jobs more effectively |  |
| Always have access to the average cost of a product |  |

---
