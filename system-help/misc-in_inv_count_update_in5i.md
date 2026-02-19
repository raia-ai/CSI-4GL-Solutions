---
title: "In Inv Count Update In5I"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "In Inv Count Update In5I - 4GL Help Documentation"
long_description: "This topic provides detailed information about In Inv Count Update In5I in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Updating Inventory Count
========================

Once the physical inventory reconciliation is complete, use this function to post the inventory. This function updates the inventory count to the Inventory subledger and creates adjustment entries for posting to Inventory Variance accounts (set up in Product Line Master [IN16]) in the general ledger.

Prior to executing this update, the following reports should be checked:

* Missing Tag Report - all missing tags must be accounted for
* Variance Report - review variances for errors.

1. Choose Inventory Control » Physical Inventory » Inventory Count Update [IN5I].

A password is required to access this screen. Please contact  if you do not know the password for this screen. You will be disconnected after three incorrect attempts. [pwd is IC4GLSOL]

2. Enter or select the Document Number of the inventory count, and the Warehouse.
3. Indicate if this is the Final update of inventory:
   * **Y**es (all logs which have not been counted will end up with zero quantities)
   * **N**o (more updates will be done; only logs which have been counted will be updated)

\*\*
Important \*\* If you are not returned back to a menu within 10 minutes (no matter
how large your site is), DO NOT break out of this screen! Call 4GL immediately.

\*\* Important \*\* Run IN71 immediately after posting the count and keep as a permanent record.

---
