---
title: "Pick Inventory [KA34W]"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Pick Inventory [KA34W]"
long_description: "Help documentation for Pick Inventory [KA34W] in the 4GL system."
---

Pick Inventory [KA34W]
======================

This function deals with Order Entry transactions and is executed on the Wireless Handheld. [why isn't it in the WH menu instead like KA37?]

![](../Resources/Images/kasto_KA34W.png)

This function allows you to scan a sales order header plus a number of sales order lines. A document is created in KAH\_HDR and KAD\_DTL. When it is processed it will write out a HLAU KAR\_RCV record for each data line. These records will be processed by the Communication Engine.

---