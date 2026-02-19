---
title: "Rn 3.16 Po"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rn 3.16 Po - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rn 3.16 Po in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Purchasing
==========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 37737 | Task notification for purchase price changes | If the price is updated on a purchase order line and material from that purchase order line has been allocated to sales order(s), a task notification will be generated to the sales people assigned to the sales orders. The sales people can then review the price change and decide whether they need to take action regarding the price change. | PO31, TK1 |  |
| 37817 | New switches used when allocating incoming | Two new switches are used when a sales order is reserved against an incoming PO or IP/OP:  • “Set Only Used Quantity When Allocating Incoming” – only sets the used quantities for logs that are allocated to the order when the PO/IP/OP is received  • “Release Orders When Allocating Incoming” – move the line(s) to PCK if they are in PBP status | , PO41, PR36, PP36 |  |
| 37995 | New Material Requirements Planning report | The Purchasing MRP Report identifies inventory on hand and what materials are needed for orders in the pipeline. This is a new reorder report version. | IN7YR |  |
| 38006 | Convert the Material Requirements Planning report output to PO Excel import format | A new utility will convert the IN7YR output, where you have entered order quantities and prices, into another Excel file formatted for import into a purchase order. | IN7YR, PO3E, PO31 | Importing Line Items from Excel |
| 38223 | Direct Delivery overrides PO Allocation Method | If the Receipt Allocation Method for a product line is set to “N” but the order is flagged as Direct Delivery, it will still allocate and a delivery note will be generated. |  | is Direct Receipts the right place to expand upon this? |
| 38240 | Auto allocate and print shipping labels in PO41/PP36 | A new switch has been created to “Print Shipping Label When Allocating Incoming”. If enabled, when you receive in PO41 or PP36, shipping labels will print for any order lines that are already in PCK status (e.g. if you previously released the order line from OE3L) or any lines that will become PCK as a result of receiving the PO/OP document (i.e. if the new “Release Orders When Allocating Incoming” switch=“Y” and as a result the order would be released to PCK status in the same process). | PO41, PP36 |  |
| 38559 | Switch to not close PO line when processing RPs | There is a new switch (“Leave PO Lines Open When Processing Pre-Receipt”); if enabled, PO lines remain open after processing the pre-receipt. If the switch is disabled, then the PO lines will be closed once the full quantity if received. | PO41 |  |

---
