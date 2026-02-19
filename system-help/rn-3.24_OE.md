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
| 39775 | New inquiry for quotes | The new Quotes by Customer by Product inquiry includes the same fields as the Sales by Customer by Product, but for quotes only. | OE6P |  |
| 40258 | CM/DM switch to warn if warehouses different | A new system switch, “Display Warning For CM/DM Different Warehouses” can warn you if you attempt to create a credit note with a different sales warehouse than the one on the invoice. | , OE45 |  |
| 40324 | Columns added to MN71 | The Manifest Loading Summary Report now includes columns for the “Ship-To Address” of the document and the “Drop Sequence” from the manifest run. | MN71 |  |
| 40337 | MN71 includes miscellaneous documents | The Manifest Loading Report now includes the pieces, length, weight and bin location for the sales order/invoice log on miscellaneous documents. | MN71 |  |
| 40338 | New doc type for miscellaneous docs generated in MN31 | Miscellaneous documents created from an existing order/invoice with the Generate Misc button are now identified as XD doc type. Miscellaneous docs created with the Misc Doc button are still identified as XX doc type. | MN31 |  |
| 40355 | Changing “Ship-to” to “P” also changes “Ship Via” | On the Billing/Shipping tab of an order or quote, if you set the Ship To to “P”, the Ship Via will change to the Ship Via that has the Pickup flag set in PO13, but this can be changed to a different Ship Via. | OE31, OE32, PO13 |  |
| 40385 | Utility to change sales warehouse on an order | A new utility, Change Sales Warehouse on an Order, allows you to update the sales warehouse on an existing order. Only "ASG", "PCK", and "PCB" orders with no invoices can be selected, and only transactional warehouses allowed for your operator security in MS32 can be selected. | OE9YG |  |
| 40390 | OE61 shows last custom status | The Sales Order inquiry shows the latest status on the sales order, including a custom status. However, if the header status is “DLV”, it will display the status of the latest invoice instead. | OE61 |  |
| 40426 | Pieces and length added to MN71 | The Manifest Loading Report now includes pieces, length, and width for PO lines.  If the Summary checkbox is not selected, the report prints the lines on the PO separately. If the Summary checkbox is selected, the report prints one line for each PO; the pieces and weight are the sum of each PO line from the detailed version. | MN71 |  |
| 40491 | Default reason code when generating lines in a CM/DM | The initial window when creating a credit memo now includes a field to select a Reason Code. If you also select Generate Lines, all lines will have this reason code. If you do not select Generate Lines, when you add the lines manually the reason code defaults to this reason code; if you change the reason code for a line, it becomes the new default reason code for subsequent lines | OE45 |  |
| 40500 | Warehouse switch to email doc writer when CM/DM is approved | You can have an email be sent to the order writer when a CM/DM is approved. The new warehouse switch “Email Body for CM/DM Approval Email” lets you enter the text to appear in the body of the email. | , OE45 |  |
| 40638 | “Random” form option added to packing list | The Form Options for the packing list now includes “R” to print the random dimension if used for logs on an invoice. | IN19 > Forms > Packing List > Options |  |

---
