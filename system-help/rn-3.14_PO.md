---
title: "Purchasing"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Purchasing"
long_description: "Help documentation for Purchasing in the 4GL system."
---

Purchasing
==========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 37258 | Abort associated PO if SO withdrawn | If a sales order is on hold of some kind (e.g. pricing hold, credit hold, etc.) and the user withdraws the order, any POs that were created from buyouts on that order will be aborted. If the sales order is later reprocessed, the POs should be recreated. |  |  |
| 37313 | Add pseudocode entry to PO entry | Can now enter a product line or product pseudocode to select a product instead of having to select from the window. | PO31 |  |
| 37478 | Add Category to vendor export PO9V | New Vendor Category field allows the Vendor Export to be filtered to one or ALL vendor categories. The resulting Excel file now includes a Vendor Category column; if a vendor category was specified on the starter screen, then only vendors belonging to that category will print on the report. | PO9V |  |

---