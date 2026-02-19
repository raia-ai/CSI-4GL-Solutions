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
| 39865 | Changes to linear nesting forms | New Form Options added to both Form 57 - Linear Nesting Production Order and Form 59 - Linear Nesting Pick Slip ("Display Sales Order Header Remarks", "Display Required Date", "Domestic Only Text", and "Foreign Only Text").  Also, for Form 57: - added Sales Whs heading, Ship-to address, Special Instructions, total ship weight, operator name, and brackets and “Tight Nest” text if the drop length is 10mm or less. - removed Scrap% column  For Form 59: - added operator name, weight picked for each line and total weight | IN19 > Forms > 57, 59 |  |
| 39885 | Export additional fields to SigmaNEST | The export to SigmaNEST now includes additional fields: - the Sheets List now displays Material Cost (the cost per standard weight unit for the log) - The Work Orders List now displays the sales price (in the Part Data 16 field) and the sales warehouse (in the Part Data 18 field) | PR44B |  |
| 40269 | Add Govt Approved form option | A new form option has been added to Form 59 - Linear Nesting Pick Slip to define “Gov Approved Only Text”, to print when the material origin on the quote/order is set to “G”. | IN19 > Forms > 59 |  |
| 40316 | New screen to change squaring allowance | A new function, Machine Kerf/Squaring Maintenance, displays all machines for the selected warehouse, and allows you to edit the kerf parameters, squaring allowance, and an option to add an extra cut in linear nesting. | PR1D |  |
| 40367 | Notify if processing IP if WO allocated | When processing an IP document from PR34, if the order has more reserved against committed-in than open, a warning prompt will show the order lines with excess reserves. You can continue to process the production order. | PR34 |  |

---
