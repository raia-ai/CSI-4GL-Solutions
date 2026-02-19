---
title: "Rn 3.23 In"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rn 3.23 In - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rn 3.23 In in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Inventory
=========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 39873 | Pcs Open added to Detailed Inquiry | A new column, Pieces Opn, has been added to the Committed-In tab of the Detailed Inquiry to show the open pieces on the PO for the product. | Inventory dropdown > Detailed Inquiry |  |
| 40003 | Copy UDFs and remarks from SO to BT | Two new switches have been added: - “Copy Order Line UDFs To Source BT” - if the order warehouse and source warehouse have the same UDF descriptions (in IN19), any UDFs on the order are copied to the branch transfer document. - “Set Order Customer Remarks On Source BT” - any order remarks on the order are copied to the branch transfer document, and canned remarks from the order customer will be added to the BT instead of the canned remarks from the BT customer (the receiving warehouse). | , IN41 |  |
| 40023 | IN9G allows for external product codes | The Export/Import Bin Locations utility now supports external product codes. The exported spreadsheet includes  product codes and descriptions, but you can overwrite these with external codes from IMP6 if you prefer. | IN9G |  |
| 40105 | Filter count initialization by bin location | The Inventory Count Initialization function includes a new option to Count By Location. After selecting a location type, you can select the locations within that type. The inventory count pre-stock report will only show logs that belong to the product lines and bin location selected. | IN5B |  |
| 40318 | Changes to IN16 warehouse options, new buyout allocation options | The warehouse options for a product line have been organized into groups (Inventory, Receiving, Order Entry Navigation, Pricing, Picking & Reserving) to make the options easier to locate. New Receiving options allow you to enable buyout-specific allocation on receiving, and to set the buyout allocation method (full piece, none, piece, quantity). | IN16 |  |
| 40399 | Change to inventory label LRLBLLGG | The LRLBLLGG inventory label now includes the product bin location. | IN19 > Label Options > Label Printer Defaults |  |
| 40407 | IN5B to Excel | The Inventory Count Initialization report can now be output to Excel. There will be two Excel reports: one for non-committed inventory and one for committed inventory. | IN5B |  |
| 40416 | Change to Log UDFs | The UDF field has been moved from the Physical properties window into its own field on IN1E, IN5E, PO41, PR34, PR36, PP34, PP36. | IN1E |  |
| 40460 | Changes to IN7ZG | The Log Type field in the Log Reservation Report parameters now includes the option “O” (Open) to only return logs with available pieces or quantity. The Excel output includes new columns for Reserved Pcs, Reserved Qty, Available Pcs and Available Qty. The available pieces and quantity are the on hand pieces/quantity minus the reserved pieces/quantity. If the result is negative, it will print 0 for available. | IN7ZG |  |

---
