---
title: "Wireless Handheld"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Wireless Handheld"
long_description: "Help documentation for Wireless Handheld in the 4GL system."
---


Wireless Handheld
=================

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 36985 | WF1X option to print one label per PC or 1 per log | New switch (Allow Multiple Labels in Linear Nest Picking); when picking for a linear nest document, this switch controls whether one label is printed or one label per piece/log. | IN16 > Warehouse > Additional Options, Linear Nesting Picking |  |
| 37086 | WFL2 report missing package as error | When viewing work orders with logs not yet loaded on a run (VIEWMISS), you can now F4 on the Err field to view the packages and logs picked for the work order that have not yet been loaded. For packages, you will see the count and the number of logs within it. | Manifest Load Confirmation |  |
| 37649 | Auto allocate and print shipping labels in WF1F | If the product line's warehouse options' Receipt Allocation Method is set to “N”, when you receive the branch transfer in WF1F you will be asked if you want to allocate the logs and print shipping labels for the logs reserved against the order. | Branch Transfer Receiving |  |
| 37815 | Auto release orders in handheld BT Receiving | If the order is in PBP status, when you choose to allocate and print labels, the order is changed to PCK status. | Branch Transfer Receiving |  |

---
