---
title: "Order Entry"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Order Entry"
long_description: "This topic provides detailed information about Order Entry in the 4GL system."
---


Order Entry
===========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 39771  40054 | OE6M caters for BT, RC, RR | The Document Delivery Tracking form can now track branch transfers, receipts, and receipt returns. | OE6M |  |
| 39871 | Display open balance on invoice | A new form option for invoices (Display Open Balance) will print the open balance on the second last line in the bottom left of an invoice. The open balance is the sales order total minus the sum of all POS payments made to the sales order. | IN19 > Forms > 04 Invoice |  |
| 39877 | OE7YR Excel report for missing MTRs | When reprinting MTRs for a customer purchase order, if any logs are missing MTRs an Excel report is generated that shows the log information and a Status column.  If there is no MTR for a log, the Status column indicates “No MTR Defined”.  If the MTR is invalid, the Status column indicates “MTR Not Found” and includes the filename specified in IN1E. | OE7YR |  |
| 39995 | Total weight added to Sales by Product (Customer dropdown) | The Sales by Product window in the Customer dropdown now includes the Total Wgt in the top right, for All and Selected lines (click Total to update the Selected numbers). | Customer dropdown > Sales by Product |  |
| 40008 | Currency and rate added to OE74 | When sorted by Date or Number, the Excel output of the Invoice Summary by Document report now includes columns for Currency and Currency Rate. | OE74 |  |
| 40065 | OE3J caters for branch transfers | The Order Expediting form now allows for a Document type (SO or BT) to be specified. | OE3J |  |
| 40082 | Allow all or multiple warehouse selection for MN71 | The Manifest Loading Summary now allows user to select a Division and to select multiple warehouses (or enter “ALL”). | MN71 |  |
| 40102 | Blind shipment packing list mirrors regular packing list options | The packing list for blind shipments now looks the same as a regular packing list, but the logo and address at the top are excluded. In addition: - The filename references “17” instead of “03” to more easily identify it as a blind shipment packing list - Form 17 Blind Shipment is now available in OE1Q to define alternative headings - Form 17 Blind Shipment in IN19 > Forms now allows for form options to be defined | OE1Q  IN19 > Forms > form 17 |  |
| 40276 | New customer part shipping label | New 4”x1” shipping label “LRSHPLBR” - Part Shipping Label by Production. Note that it may print upside-down. | IN19 > Label Options > Label Printer Defaults |  |
| 40361 | OE77 to Excel | The Sales Order/Quote Report can now be output to Excel | OE77 |  |
| 40368 | Revision number added to order form | A new form option, Print Revision Number, is available for the sales order form. If set to “Y”, if the sales order has a revision number it will print at the top right corner. | IN19 > Forms > form 08 |  |
| 40437 | Change to IN7YG and custom Open Order report | A “Product Code” column has been added to the IN7YG Excel output.  We have also created a custom version of the Open Order Report(OE7G) with the addition of columns for Primary Process, Second Process, and Third Process. | IN7YG  OE7GB |  |
| 40465 | Option to print surcharge lines when G type | A new form option, “Print Surcharge Lines When Group Invoice Type” is available for forms 04-invoice, 07-sales quote, and 08-sales order. | IN19 > Forms > Form Options |  |

---
