---
title: "Highlights"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Highlights"
long_description: "Help documentation for Highlights in the 4GL system."
---

Highlights
==========

Simplified Path to Modifying Sales Orders
-----------------------------------------

previously offered four ways to change an order, depending on its status. We have now simplified this process:

* OE3C and OE3F have been decommissioned.
* All order changes are now done in OE31, but may also be done through OE3L or through the Task Manager.
* For editing orders in OE31:
  + Operator-level access options control whether the operator can modify an order on hold1, and whether the operator can modify the Header and/or Detail section of an order in PCK/PCB status2.
  + Warehouse-level access options3 control whether an order/quote in PBP, CRD, PRA, and/or QCH status is withdrawn (changed to ASG/OPN status) or whether the status remains unchanged. Orders in PCK or PCB status will remain unchanged. By default all statuses (except PCK and PCB) will be set to be withdrawn.
* If an order is edited in either OE3L or through the Task Manager, the status of the order remains unchanged.

**3.15 Update:** The operator-level PCK Order Access now includes an option to warn or prevent changes to lines that have logs picked. See Editing an Order.

Configuration


1 MS32 > Options > Order Entry > Hold Order Access  
— Define access for each hold status (PBP, CRD, PRA, and/or QCH status); operators who currently have access to OE31 can modify orders on hold.

2 MS32 > Options > Order Entry > PCK Order Access  
— Operators who currently have access to OE3C and OE3F can change orders in PCK status, otherwise they should not have access.

3 IN19 > OE Options > Order Withdraw Options

---