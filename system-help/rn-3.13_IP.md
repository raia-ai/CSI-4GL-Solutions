---
title: "In-House Production"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "In-House Production"
long_description: "This topic provides detailed information about In-House Production in the 4GL system."
---


In-House Production
===================

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 34278 | Add a document and date filter to PP38 | Additional search criteria fields (All warehouses, All/specific documents, date range) added. | PR38 |  |
| 36735 | Output PR74 to Excel | Raw Materials Requirements report can now be output to Excel format. | PR74 |  |
| 36248 | Add date filter to PR64/PR65 | Start Date and End Date filters added to the IP By Order Number and IP By Confirmation Number inquiries | PR64, PR65 |  |
| 36839 | Linear nest to look at available log if cut product | If “Linear Nesting by Product Availability” switch is enabled, logs for cut products are now selected as well. |  | Linear Nesting During Order Entry |
| 36932 | PR74 raw material - display sizes and required pieces | The Raw Material Requirements report (PR742) now includes a Pcs column. The number of pieces will be equal to the weight required divided by the theoretical weight for the product and then multiplied by the number of pieces entered for the finished good in PR74. | PR74 |  |
| 37228 | Raw material cost on OP not using replacement cost | New switch “Processing Raw Material Costing Method” allows raw materials on IP/OP orders to be costed using average cost or replacement cost (for IP documents only, OP documents only, or both). | , PR42B | Documented in Linear Nesting During Order Entry; IP documentation is not complete enough to xref to |
| 37474 | Allow PR44B to export NC1 files | Part drawings in NC1 format may be attached to an order for export to SigmaNEST. | PR44B |  |

---
