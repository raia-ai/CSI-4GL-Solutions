---
title: "In35 Adjustment By Log"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "In35 Adjustment By Log - 4GL Help Documentation"
long_description: "This topic provides detailed information about In35 Adjustment By Log in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Adjusting Inventory By Log Number
=================================

[probably combine with IN31 - adj by product]

This function is used to enter Inventory Log adjustments by log number. Adjustment entries can remove/modify existing logs. New logs or adjustments cannot be created in this window. You will have to use adjustment by product.

1. Choose Inventory Control » Inventory Adjustment » Adjustment By Log [IN35]
3. Enter Remarks.
4. Optionally, select a Reason for the adjustment.
5. Enter or select Document Date (defaults to today's date).
6. Enter Type: Change log, Introduce new log, transfer log Out, Price adjust, Quantity only, Value.
7. Enter log number in Lognum field.
8. Enter or select input Spec/Size.
9. Enter adjusted quantity in inventory units, in Invent Qty field.
10. Enter adjustment number of Pieces on-hand, e.g. if removing 1 piece type -1.
11. Enter or select Remarks specific to adjustment quantity in inventory unit of measure.

---
