---
title: "IN71 - Stock List By Logs/Product/Grade"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "IN71 - Stock List By Logs/Product/Grade"
long_description: "Help documentation for IN71 - Stock List By Logs/Product/Grade in the 4GL system."
---

IN71 - Stock List By Logs/Product/Grade
=======================================

This function is used to create Inventory Stock list - Logs by product displaying inventory logs on-hand.

To display available quantity, use the Available Inventory Report by Log or Product report [IN7YG].

1. Choose Inventory Control » Inventory Reports » Stock List by Log/Product/Grade [IN71].
2. Produce report at the Product level (default), Log level, or Grade level.
3. Enter or select the Product code (by default all products are selected).




9. Enter or select the Product Line code (by default, all are selected).
10. Enter or select the Spec Type code (by default, all are selected).
11. Enter or select Specification code (field defaults to ALL if Spec Type is ALL).

The Excel output includes columns for each possible spec. Logs that have legs will have the leg size description(s) listed in a separate row below them in the "Size" column D.

Output
------

|  |  |  |  |
| --- | --- | --- | --- |
| column heading | needs description? (if yes, populate one of the next two columns only) | glossary description | report-specific description |
| Warehouse |  |  |  |
| Pln |  |  |  |
| Product |  |  |  |
| Weight / Unit |  |  |  |
| On Hand Quantity |  |  |  |
| On Hand Pieces |  |  |  |
| Average Cost |  |  |  |
| Value |  |  |  |

---