---
title: "Terms and Concepts"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Terms and Concepts"
long_description: "Help documentation for Terms and Concepts in the 4GL system."
---

Terms and Concepts
==================

Log Numbering
-------------

Whenever a parent log generates baby logs up to Z and then generates a new log starting with L, that new log doesn’t generate logs starting with A. This is because the odometer is always kept on the original log.

For example, if L000123 is the parent log and it generates A000123 to Z000123 and then it generates L000124. Then L000124 would generate L000125, and not A000124. This is because the odometer is only stored on L000123 which would max out at Z.

Theoretical vs Actual Weight Calculations
-----------------------------------------

Theoretical weight is set for a product in the Detailed Inventory Inquiry.

Product Lines [IN16] > ![](../Resources/Images/i_arrow_down.png) > Warehouse > Calc Used Qty Proportionally?

---