---
title: "Rpt Po7Za Minmax Reorder"
source: "madcap.md"
tags: ["4GL", "REPORTS", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rpt Po7Za Minmax Reorder - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rpt Po7Za Minmax Reorder in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the REPORTS module."
---


PO7ZA - Min/Max Reorder Report
==============================

Specs from attachment to BG 37533; ask Robin if any questions:

|  |  |  |
| --- | --- | --- |
| Column | Heading | Details |
| A | Product Code | Product code |
| B | Product Description | Product description |
| C | Pcs On Hand | # of pieces on hand for all ‘L’ logs in the product. Do not include child logs. |
| D | Min | Value for Min Pieces in PO19 |
| E | Below Min | Absolute value of C - D |
| F | Max | Value for Max Pieces in PO19 |
| G | Pcs Ordered | Number of pieces on open POs (including IP/OP documents) |
| H | Reorder Qty | Value for F - E |
| I | Average Cost |  |
| J | Replacement Cost |  |
| K | Last Vendor |  |
| L | Last Received Price |  |
| M | Top Vendor |  |

Filters

Warehouse – Cannot select ‘ALL’

Product Line – Specific or ALL

Only Show Below Min – Default to unchecked (If checked, only show products where column E is greater than zero, before apply ABS to it)

Include inactive products – Default to unchecked

Ignore Zero Mix/Max – Defaults to checked (If checked, ignore products that have both min and max set as zero in PO19)

Min Pcs / Max Pcs - return products with the same Min Pcs and/or Max Pcs if you had entered any number other than 0.

Cut Percent - will filter out additional logs if the percentage that has changed from the original size is more than the selected value.   
If the cut percent is set to 100%, then it should include all of the logs that you had received.  
If the cut percent is set to 0%, then it should only include the logs that have not been split into smaller sizes.  
If the cut percent is set to 60%, then it should only include logs where all their cut dimensions have changed less than or equal to 60%. For example, a 12' length log that has been split into a 6' log should be included since (12 - 6) / 12 = 0.5 = 50%. A 12' length log that has been split into a 4' log should not be included since (12 - 4) / 12 = 0.75 = 75%.

---
