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
| 36998 | Total Time added to inquiry | A Total Time column has been added to the Sales Order Inquiry, on the Details>Scheduled tab. This would be populated for machines that have an end date and time, and is calculated as the difference in minutes between end and start minus any elapsed pause time, as tracked in WF19 (Time Tracking) | OE61 | Time Tracking |
| 37716 | Reserve plates in SigmaNEST | New switch (“Allow SigmaNEST Plate Reservations”) allows plates to be reserved in SigmaNEST (stamped with customer name) whenever a log is fully used in  for a sales order, BT or CC.  Partially picking a log (either initially, or changing it from being fully picked) for an order, closing the picked sales order line, or aborting the sales order will remove the reservation. |  | Plate Nesting with SigmaNEST |
| 38049 | OE61 Display all 4 taxes on Summary tab | The Sales Order Inquiry screen has been resized to allow display of four taxes. | OE61 |  |
| 38089 | Sales cost code added to inquiry | The Sales Order Inquiry and Invoice Inquiry now show the cost code. | OE61, OE62 |  |
| 38145 | Auto-populate random lengths from BT | When receiving a BT linked to a sales order, if the full log that was received has been allocated to the sales order, the random length dimensions from the BT are copied to the sales order. | OE41 |  |
| 38146 | Print RFQ# on sales quote form | The quote form now includes a column for the RFQ #. | OE32 |  |
| 38193 | Mass Price Adj allow negative and >100% Markup and Margin | In the Mass Price Adjustment window, the Markup and Margin fields now allow negative values as well as percentage greater than 100%. | OE31, OE32  > Reprice |  |
| 38222 | Open orders alert on sales order | The Shipping section of an order displays a count of open orders for the same customer and ship-to as the current order. The count displays in red text if there are orders with the same required date.  Click the binoculars beside the count to view a list of these orders. It displays one record for each sales order and required date on the order line. A red icon highlights those that match the required date on the current sales order. If there are order lines with different required dates on a sales order, it displays once for each required date.  In this list you can inquire on an order, or print the order lines with the same required date as the current order to Excel. | OE31 |  |
| 38236 | Copy UDF fields from previous line | A check box column has been added to the UDF Descriptions to allow you to flag that a UDF field's value should be copied to subsequent lines in the sales order. | IN19 > OE Options > UDF Descriptions  OE31, OE32 |  |
| 38249 | AutoFill line numbers in Resequence window | In the Resequence window, the Same button has been replaced with an AutoFill button. Enter the new line number for one or more lines, then click AutoFill to populate the remaining lines in sequence. For example, if there are four lines and you change line 4 to “2” and click AutoFill, the lines will be renumbered as 1,3,4,2. | OE31, OE32 |  |
| 38321 | Mass price adjustment window includes margin value columns | The Mass Price Adjustment window now includes columns for Order Margin Value, Average Cost Margin Value, and Replacement Cost Margin. | OE31 |  |
| 38328 | Changes to shipping label with UDFs | Label “LRSHPLBN” has been updated: the barcode now includes the work order and log numbers, and other fields have been adjusted to allow more characters in the UDF fields. | IN19 > Label Options > Label Printer Defaults  IN19 > OE Options > UDF Descriptions |  |
| 38335 | Display picked quantity in OE31 | The Details tab of a sales order now includes a Picked Qty column that displays the picked quantity in selling units. | OE31 |  |
| 38339 | Display line status and P/C in OE31 | The Details tab of a sales order now includes columns for Status and P/C. | OE31 |  |
| 38351 | Move misc docs from one manifest to another | Miscellaneous documents can now be moved from one manifest to another in the Assign tab. | MN31 | SD |
| 38474 | Customer detailed invoice Excel report | New Customer Detailed Invoice Report with additional information about invoice logs such as log number, specs, etc. | OE74A | SD |

---
