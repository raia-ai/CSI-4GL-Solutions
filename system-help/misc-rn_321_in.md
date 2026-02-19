---
title: "Rn 3.21 In"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rn 3.21 In - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rn 3.21 In in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Inventory
=========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 39283 | IN9ZQ can run for multiple product lines | When exporting replacement costs, you can now select one or more product lines or leave the default “All”. | IN9ZQ |  |
| 39300 | Available and On-hand weight added to IN62 | Two new columns have been added to the Detailed Inquiry > Inventory tab: “Avl Wgt” and “Onhand Wgt”. | IN62 |  |
| 39390 | Canada Customs paperwork | now caters for the paperwork required by Canada Customs for US>Canada shipments. This includes: • a field on the product line to capture the HTSUS code • a new function to export/import the HTSUS codes for all products in one or all product lines • new forms added to IN19: USMCA Certificate of Origin and Canada Customs paperwork and new functions to print these (OE7WA/OE7WB). | IN16, IN9YE, IN19, OE7WA, OE7WB |  |
| 39522 | Inventory count changes | • In the Inventory Count Initialization, the first Description line is now mandatory. • In the Variance Report, when selecting a document number a new column displays the warehouse. | IN5B, IN5G |  |
| 39810 | Changes to IN7ZI | Several functional changes have been made to the Inventory Sales Usage Report: - It can now be run for all product lines (this disables the spec and dimension filters) - Min/Max quantities (maintained using PO19) have been added to the report - Available Quantity has been added (This is the on-hand minus the sum of the open quantity processed and unprocessed; unprocessed refers to commit-out quantity that is not picked on logs yet, while any logs that are picked on the order are counted as processed and deducted from unprocessed.) - A “Group compatible” option has been added to the report. If left blank then no grouping is done. If set to L or B for long products, cut and fixed products are combined and only the fixed is shown. If set to F or B for square/flat products, cut and fixed products are combined and only the fixed is shown. If there are multiple fixed, the cut is combined with the first fixed product. | IN7ZI |  |
| 39812 | New inventory logs report | The Offcut Stock Listing report is similar to IN71 by log and IN7ZG, but only displays reservations of logs from cut products. | IN7YT |  |
| 39821 39888 | Minimum stock import | A new utility allows you to create a spreadsheet, populate it with minimum stock levels per product code, and then import the values into  products. The exported spreadsheet includes  product codes and descriptions, but you can overwrite these with external codes from IMP6 if you prefer. | IN9YF |  |
| 39879 | Average and replacement cost per length/square added to product summary | The Summary page of the Detailed Inquiry now shows the average and replacement cost per length unit (FT) and per square unit (SFT) set up on the product line. If the product is a fixed product the cost per PC is also displayed. | Inventory dropdown > Detailed Inquiry |  |

---
