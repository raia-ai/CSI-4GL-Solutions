---
title: "Rn 3.18 In"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rn 3.18 In - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rn 3.18 In in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Inventory
=========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 38227 | Variance Report includes Operator column | The Variance Report now displays the operator who recorded the count information for a log in IN5E. | IN5G |  |
| 38344 | Can access Purch by Product from Detailed Inquiry | When viewing the Top Vendors for a product in the Detailed Inquiry, a new Receipts button displays the same Purch by Product window as from the Vendors top menu. | Inventory>Detailed Inquiry>Top Vendors |  |
| 38733 | Changes to IN7L | “Receipt” added to the Stock List by Bin Location report. If the document is an RC or TF, the corresponding PO#, Buyer, and Writer are also shown (only for regular PO and OP). | IN7L |  |
| 38762 | Show quotes in log reserves inquiry | The Log Inquiry reserves window includes an option to Show Quotes. | IN6B |  |
| 38801 | Don’t allow BT if Required Date is in the past | The switch that controls what happens if a user changes the Required Date on an order to a past date now applies to branch transfers as well: If set to “N” (no check) - the BT can be processed as normal If set to “S” - a message will appear but user can choose to continue If set to “H” - a message will appear and the BT cannot be processed. | IN41,   > Check If Requested Date On Order Line Is Before Today |  |
| 38846 | Piece cost shown in Detailed Inventory Inquiry | The Cost box on the Summary tab of the Detailed Inventory Inquiry now shows the average cost per piece (below the "Avg Cost") and the replacement cost per piece (below the "Rep Cost"). These per piece numbers are only shown if a theoretical weight per piece exists for the product (e.g. if the product is a fixed product) and the product line is not already costed by piece (e.g. MUN). | IN62 |  |
| 39045 | IN7ZQ output to Excel | The Open Branch Transfers Report can now be output to Excel. | IN7ZQ |  |

---
