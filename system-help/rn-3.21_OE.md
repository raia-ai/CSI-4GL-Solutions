---
title: "Order Entry"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Order Entry"
long_description: "Help documentation for Order Entry in the 4GL system."
---

Order Entry
===========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 36938 | Track changes to orders/quotes/invoices | The Billing/Shipping tab on the Sales Order Inquiry and Invoices/CM/DM By Document Number Inquiry now includes a Revision button that displays all changes to the documents after the order was processed (e.g. change to selling price or delivery date, deleting or closing an order line, etc.). Changes can be exported to Excel in the new function, Document Changes Tracking to Excel (MS73). | OE61, OE62, MS73 |  |
| 39109 | OE1Q allows custom headings for all forms | The Alternate Form Headings function now allows custom headings to be defined for all forms. | OE1Q |  |
| 39199 | Display Blind Shipment on OE61 | The Header tab of the Sales Order Inquiry now indicates if Blind Shipment is enabled for the customer in AR17. | OE61 |  |
| 39240 | OE7YT Excel output includes remarks | The Excel output for the Lost Quote Reason Report now includes up to five remarks on each quote (assuming the Show Remarks check box is selected in the report parameters). | OE7YT |  |
| 39277 | W column in warehouse form print options is now a dropdown | The valid options for the form selected are now presented in a dropdown. | IN19 |  |
| 39294 | Select the same log multiple times in OE45 | When creating a credit memo, you can now return a log to multiple baby logs. Do not select Generate Lines and clear the Select field to add a new log manually. When you return it, you can select the same log and return it to multiple baby logs. | OE45 |  |
| 39359 | OE7YH can run for multiple warehouses | When running the Sales by Salesperson by Customer report, you can now select one or more warehouses. | OE7YH |  |
| 39360 | OE31/OE32 search can now default to a date range and to all operators | Two new switches have been added related to the OE/quote search screen: • “Order Entry Search Days Back” (warehouse switch) allows you to default the From Date to today’s date minus a set number of days back. • “Default Entry Search to ALL Salespeople” (operator switch) allows the Salesperson field on the search screen to default to “All”; if not set, the search defaults to your operator. | , MS32, OE31, OE32 |  |
| 39386 | OE3B displays customer name | A Customer Name field has been added to the Abort Order After Picklist form. | OE3B |  |
| 39465 | Freeze costs, exclude from usage | Two new flags have been added to order line entry, next to the cost price and value: - “Freeze” - use the actual cost of the logs that are picked on the order, even if the product is set to average costing - “Ex Usg” - set the flag against the invoice to exclude the value from usage in PO52. | OE31, PO52 |  |
| 39466 | OE32 has indicator if the quote was created from a backorder | The search tab for Quote Entry/Maintenance now has a “B” column to indicate if the quote was created when an order is on backorder (“Backorder Method” switch = “Q”). | OE32 |  |
| 39470 | New Blanket Order Pickslip Release function | This new screen allows you to print a pick slip for partial quantities on a blanket order. | OE72C |  |
| 39487 | OE7AE will no longer print if doc is in Approval status | Return Slips cannot be reprinted for credit memos in Approval status. | OE7AE |  |
| 39511 | Pick Date and Time displayed on OE61 and PR41B | The Reserves tab for an order line in the Sales Order Inquiry now displays the date and time that the order log was picked (in the Currently Picked or Previously Picked section, as applicable). The picked date and time are also displayed for sales order log details viewed from the Machine Production Schedule. | OE61, PR41B |  |
| 39531 | Warehouse source costing | A new warehouse switch (“Use Replacement Cost for Warehouse Source Orders”) allows the cost of warehouse source orders to be either by the average cost of the product in the sending warehouse, or the replacement cost of the product in the order warehouse. | IN19 |  |
| 39553 | Hide Pricing Qty and Hide Price added to OE61 | The Header tab of the Sales Order Inquiry now includes the Hide Pricing Qty and Hide Price fields. | OE61 |  |
| 39581 | Additional process columns added to OE3Q | Columns to enter nine additional processes have been added to the sales order import template. | OE3Q |  |
| 39597 | Branch transfers created from an order use the order writer as the salesperson | When an order’s Source is set to Whse, the salesperson on the resulting branch transfer is now the order writer instead of the salesperson for that warehouse. | OE31 |  |
| 39609 | New shipping, package and inventory labels | New 4x2” labels: LRSHPLBQ  LRPKGLB4  LRLBLLGP | IN19 > Label Options > Label Printer Defaults |  |
| 39663 | UDF fields and part # added to OE7G | The customer part number and three UDF fields on a sales order are displayed at the end of the Open Order Report. | OE7G |  |
| 39794 | Use stock cost in calculating price book markup | If you are using tier/predefined pricing, a new switch ("Use Stock Cost Only For Pricing") controls if the full cost price (including machine) is used, or only the stock cost price is used. This switch does not affect alternate pricing or repricing. |  |  |
| 39878 | AR7N can output to Excel | The Salesperson Call Report can now be output to Excel. | AR7N |  |
| 40066 | From Logs defaults to full quantity | When you click From Logs and select a log, the full available quantity is selected by default, but you can change the number of pieces if necessary. | OE31 |  |
| 40108 | Open Quote report | A new Excel report displays all open quotes that fit selected criteria. It includes columns for warehouse, writer, outside salesperson, quote number, entry date, follow up date, expiry date, customer, weight, total value, margin %, and remarks. The remarks come from the remarks window in the Quote Follow- up window (OE3D). It will print each line of remarks on a separate row. | OE7GA |  |

---