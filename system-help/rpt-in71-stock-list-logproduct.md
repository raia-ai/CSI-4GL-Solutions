---
title: IN71 - Stock List By Logs/Product/Grade
source: madcap.md
version: '1.0'
last_updated: '2026-02-19'
short_description: IN71 - Stock List By Logs/Product/Grade
long_description: >-
  Help documentation for IN71 - Stock List By Logs/Product/Grade in the 4GL
  system.
---

# IN71 - Stock List By Logs/Product/Grade

This function is used to create Inventory Stock list - Logs by product displaying inventory logs on-hand.

**TIP:** To display available quantity, use the [IN7YG - Product Availability](https://4glsol.com/sm3-helpdocs/Content/Reports/rpt_IN7YG_Available_Inv_Rpt_by_Log_Customer.htm) report \[IN7YG].

1. Choose Inventory Control » Inventory Reports » Stock List by Log/Product/Grade \[IN71].
2. Produce report at the Product level (default), Log level, or Grade level.
3. Enter or select the Product code (by default all products are selected).
4. Indicate if you want to show products with inventory On Hand .
5. Indicate if you want to Show Program (defaults to Y).
6. Indicate if you want to show inventory in Quarantine.
7. Indicate if you want to Show Zero logs (logs/products with zero quantity); by default, they are not shown.
8. Enter or select the Warehouse code plus _Child Warehouse_ indicator (defaults to warehouse assigned to operator).
9. Enter or select the Product Line code (by default, all are selected).
10. Enter or select the Spec Type code (by default, all are selected).
11. Enter or select Specification code (field defaults to ALL if Spec Type is ALL).
12. Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.

The Excel output includes columns for each possible spec. Logs that have legs will have the leg size description(s) listed in a separate row below them in the "Size" column D.

***
