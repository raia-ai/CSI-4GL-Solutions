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
| 37524 | Import customer parts into order from Excel | Customer parts can now be imported into an order from an Excel spreadsheet. The line type must be “Prt” and the SUM and PUM must be set to the part's pricing unit of measure. | OE31, OE32 | Importing or Exporting Line Items or Parts |
| 37736 38076 38127 38206 | Improved Tolerances functionality | • If the “Defaults Previous Product Code If A Cut Product” switch is enabled, the product code and tolerances entered for an order line are repeated for subsequent lines. • You can apply tolerances to multiple order lines; the lines must have the same product and the product must accept tolerances. On the Details tab, click the down arrow  in the bottom right of the screen twice until you see the Tolerances button. If any of the lines already have tolerances defined, you will be asked if you want to overwrite them. • If the “Automatically Open Tolerance Window in Or Entry” switch is enabled, when you enter an order line for a product with tolerance input enabled and processing options enabled (Disable Processing Options set to “S” or blank), you will be prompted to apply tolerances. • In the tolerances input window, you can enter negative values and Finished Size. | OE31, OE32 |  |
| 37738 | Show additional operation/revenue lines that have been added to a sales order line | Currently, in quotes and sales orders, additional processing revenue lines are rolled up to a selling price but are invisible to the customer. A new option has been added to the “Break Out Processing Revenue” switch to allow selected revenue lines to be displayed separately. The rolled up price would still be captured against the line for sales history and the GL. | >Break Out Processing Revenue = **S**elected lines  OE31 | Entering Quotes and Orders Adding Line Items to an Order |
| 37946 | Search “All” statuses in OE31/OE32 | The search screen for quotes and orders now defaults to search for “All” statuses (but you can still filter to a particular status if you prefer). | OE31, OE32 |  |
| 37953 | Warehouse filter added to Route Maintenance | Route Maintenance can be filtered to a specific warehouse, or leave “All” to view all defined routes for all warehouses. | MS3S |  |
| 37740 | Warehouse option added to define UDFs to be included on order details | A new warehouse option (“UDF Descriptions”) allows you to define up to three optional lines to print on quotes, orders, pick slip, packing slip, or invoice for each inventory line item. | IN19>OE Options>UDF Descriptions |  |
| 38033 | UDF fields added to order/quote details | Any UDFs configured in IN19 will display beneath the Part Number field when adding a line to an order/quote. If there are no UDFs configured in IN19, a UDFs field will be visible but disabled in the order details. | OE31, OE32 |  |
| 38062 | Form option to include UDFs on sales forms | New form option to include any populated UDF fields on sales forms. | IN19>Forms>[packing list, invoice, picking list, sales quotation, and sales order forms]>Display UDF |  |
| 38011 | Direct Delivery column added to OE61 and OE62 | The Sales Order inquiry includes a new “Dir Dlv” column that will display a green icon for direct deliveries or a red icon for non-direct deliveries. Similarly, the Invoice inquiry will display a red icon for cost lines and credit notes not referencing invoices. | OE61, OE62 |  |
| 38034 | Customer filter added to Invoice Summary Report | The Invoice Summary By Document report can now be filtered to a specific customer. | OE74 |  |
| 38060 | RFQ added to quote header | You can now capture the customer’s RFQ number on the Billing/Shipping tab of a quote. When the quote is converted to an order the RFQ is stamped on the order from the quote, and the customer PO is stamped on the quote from the order; in this way whether you inquire on the order or the quote, both the customer PO and RFQ number are displayed. | OE32 |  |
| 38122 | WF1D store status against sending warehouse for BI docs | If you scan a branch transfer packing slip, the status you assign is attached to both the branch invoice (BI) in the sending warehouse, as well as the BT document in the sending warehouse. | WF1D |  |
| 38174 | MS3V/WF1D allow scanning CM/DM | You can now scan custom statuses for CM and DM documents in MS3V and WF1D. | MS3V, WF1D |  |
| 38175 | New shipping label with UDFs | New 4" x 2" shipping label “LRSHPLBN”  In the example below, “Job” and “Detail” are UDF fields. | IN19 > Label Options > Label Printer Defaults  IN19 > OE Options > UDF Descriptions |  |
| 38176 | Customer part remarks import | Customer part remarks can be imported from an Excel spreadsheet for parts that already exist in 5PR17.  The spreadsheet must include:  • Warehouse • Part number (parts must already exist in 5PR17) • Remark type (must exist in PR13 and have a “Y” in the Comment column in MS36) • Remark (max 50 characters) | Contact 4GL Helpdesk for assistance. | Using Remarks |
| 38197 | Receipt of direct delivery orders may include cost/remark lines | When receiving direct delivery buy-ins, if the "Auto Pick Cost and Remark Lines" switch is enabled, the invoice will include both the inventory line and the cost line. |  | Adding Line Items to an Order |
| 38200 | Allow access to edit orders even if invoice exists | An order in PBP status can be modified even if it was partially delivered. You will be prompted to confirm that you want to proceed with editing the order. The order's status will not change (regardless of PBP settings in the Order Withdraw Options). | OE31 |  |
| 38226 | Ability to run PR7P from batch run | The Production Schedule can be exported to Excel as part of a batch run in BT92 | BT92 - add PR7P1B to a batch run |  |

---