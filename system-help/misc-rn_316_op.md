---
title: "Rn 3.16 Op"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rn 3.16 Op - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rn 3.16 Op in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Outside Processing
==================

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 37735 | Outside processing price matrix | A new pricing matrix form allows you to maintain cost and sales price information by machine by vendor. | AP1B |  |
| 37947 | Display Set/Seq# in Committed tab | The Committed tab on incoming production orders will show the Set # and Line #. | PP34 |  |
| 37817 | New switches used when allocating incoming | Two new switches are used when a sales order is reserved against an incoming PO or IP/OP:  • “Set Only Used Quantity When Allocating Incoming” – only sets the used quantities for logs that are allocated to the order when the PO/IP/OP is received  • “Release Orders When Allocating Incoming” – move the line(s) to PCK if they are in PBP status | , PO41, PR36, PP36 |  |
| 37911 | Create multiple OP documents from a sales order; shortcut if raw material same as finished goods. | On processing a sales order, all outside processes are presented for set allocation. An Auto Set button creates one document per vendor, even if their sets are split over different order lines. These documents will be linked and presented back-to-back for processing. In the resulting OP document(s), if the raw material will be the same as the finished goods for at least one line, the new Raw Mat button on the Set tab allows you to build both Details sections at the same time. You will be asked if the raw material is the same as the finished goods for all lines or selected lines. | PR41B |  |
| 38030 | Copy remarks from SO to FG | When creating an OP from a sales order, cost and price remarks are copied from the sales order to the finished goods. | PR41B |  |
| 38031 | Switch to auto-create/select sets when creating from SO | A new switch (“Open Set Numbering Window”), when disabled, allows you to skip the Set Allocation screen entirely when automatically creating OP documents from sales orders. This performs the Auto Set allocation and opens the resulting OP documents immediately for processing. | PR41B |  |
| 38240 | Auto allocate and print shipping labels in PO41/PP36 | A new switch has been created to “Print Shipping Label When Allocating Incoming”. If enabled, when you receive in PO41 or PP36, shipping labels will print for any order lines that are already in PCK status (e.g. if you previously released the order line from OE3L) or any lines that will become PCK as a result of receiving the PO/OP document (i.e. if the new “Release Orders When Allocating Incoming” switch=“Y” and as a result the order would be released to PCK status in the same process). | PO41, PP36 |  |

---
