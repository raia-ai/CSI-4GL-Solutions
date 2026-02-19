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
| 30561 | Ship Date to default to Required Date picking | New switch to “Default Release Date to Required Date”. If set, then the release date defaults to the required date. Otherwise, it defaults to today's date. | , OE41, WF11 |  |
| 36143 | PDFs can print in A4 or letter size | New form option allows PDFs to be generated in A4 or Letter size. This applies to credit/debit notes, invoices, quotes, sales orders, and customer statements. | IN19 > Forms > [form] > Form Options > Page Size |  |
| 36622 | Search cash sale by customer name | If a cash customer is set to allow the address to be modified (AR17>Mod Addr), and the billing information was changed in an order, then the Customer Name can be searched in OE61 and OE62. | OE61, OE62 |  |
| 36648 | BCC salespeople on emails | Order and quote confirmation emails are sent to all contacts in the same email (instead of separate emails) and the salesperson is included in the BCC field. Salesperson's email must be defined in MS32, and Salesperson Maintenance [OE13] must be set to email the quote and SO to the salesperson. | OE31, OE32  MS32, OE13 |  |
| 36677 | Create a single PDF when batch printing documents | When printing multiple related documents (e.g. multiple invoices from OE75, a sales order or delivery note with MTRs, etc.) all documents are combined in a single PDF. |  |  |
| 36693 | Ability to have multiple pricing methods | If using Price Book pricing method, you can now also set up a customer price for a specific product and customer that will be used instead. | IN1S, OE4M | Understanding Sales Pricing |
| 36822 | Master pick slip | New screen reprints pick slips for all open sales order lines in PCK or PBP status that have the selected delivery date. Pick slips will print by sales order number. | OE72B |  |
| 36823 | Print pick slips for stock lines | A pick slip will print for order lines that have no primary process as well as processes identified as stock lines in PR11. When reprinting pickslips by machine, processes defined as stock lines are treated the same as a blank process. |  |  |
| 36906 | Add customer parts to database from sales orders | New check box next to the Part Number field (when adding a product to a quote or order) to add a new part to . | OE31, OE32, 5PR17 |  |
| 36949 | Add total weight and order value to OE61 | Columns added to the Sales Orders By Order Number inquiry for Weight, Value and Currency. | OE61 |  |
| 37058 | OE3F ability to change Req Date for multiple lines | New Req Date button on Details tab allows Required date change for one or more selected line items. | OE31, OE32, OE3F |  |
| 37097 | Manifest Assign tab additions | New columns (Index and SI (shipping instructions)) added to the Unassigned Items and Run Items lists. Packages button (same as on Pick/Load tab) to allow viewing of package information including package Type and Count (number of components in the package). | MN31 |  |
| 37170 | Pseudocode entry in order entry | Can now enter a product line or product pseudocode to select a product instead of having to select from the window. | OE31, OE32 |  |
| 37179 | Prevent user from deleting run with assignments | A manifest run cannot be deleted if documents are assigned to it. | MN31 |  |
| 37192 | Populate Cust Part field with order # and index | The customer part # field for a cut product in an order can be set to a default value (warehouse-type of entry-document-index) but the value can be overwritten for the order. If the product is not a cut product, the customer part # field is enabled but not pre-populated. | > Enable Customer Parts Field In Order Details=W |  |
| 37307 | Add Refresh button in all Manifest tabs | Refresh icon added at bottom of each manifest tab to allow user to refresh the page results. The time the data was last built is also displayed. | MN31 |  |
| 37308 | POS Payment screen to allow document selection | The existing OE5D form posts all unposted POS payments. The new form OE5DA allows users to select individual payments to be posted. | OE5DA |  |
| 37309 | Set line status to 'PBP' for new lines | New switch “Default New PCK Order Line to PBP”. If set, when adding a new line to an order or branch transfer in PCK status, the new line will be in PBP status and the order/BT will be in PCB status. If not set, new lines will be in PCK status (matching the order/BT header). | , OE3F, IN41 |  |
| 37317 37512 | Ability to hide price on sales quote form;  flag to hide pricing qty on sales quote | New Hide Price and *Hide Pricing Qty* check boxes on quote header allows user to hide the prices on the quote. New switches “Hide Quote Price by Default” and “Hide Quote Pricing Quantity by Default” set the default value of these check boxes. If selected, only the final sales value will be printed on the quote. | , OE32 |  |
| 37400 | Display selling qty shipped under pricing qty ship | If an invoice line has different SUM and PUM, the Shipped column will display the selling qty and UOM below the pricing qty and UOM. If the SUM and PUM are the same, the qty is printed once without the UOM. |  |  |
| 37415 | Sales pricing approval hierarchy | New operator switch “Price Approval Discount Limit Percent” defines the percent difference between the sales price and the default price that the user is allowed to release from a price check task. If the limit is set to zero, the user may release all orders/quotes from the Task Manager. | MS32 > Options > OE > Add'l Options | Setting Up Pricing Categories for Tier Pricing |
| 37523 | Add Primary Process to OE74 for 'L'ines to Excel | Primary Process column added to report when outputting detail **L**ines to Excel. | OE74 |  |
| 37636 | Print product bin location on pick slip | A new value (“N”) in the “Additional Details Print Order” form option for pick slips allows you to print the bin location below the order line. | IN19 > Forms > 05 Picking List > Additional Details Print Order = “N” |  |
| 37654 | Display salesperson in OE42 | Sls column added to the Shipping Confirmation screen | OE42 |  |
| 37661 | Whs Src changes for manifest (BT route, pick slips) | The manifest run for branch transfers will use the route code from the destination warehouse customer.  An “Omit Pick Slips” option has been added to MN33 and the Runs tab on MN31 to skip specified runs when printing picking slips from the Process page. | MN31, MN33 |  |
| 37763 | Package, shipping & inventory label changes | New labels: LRLBLLGO  LRSHPLBM  LRPKGLB3 | IN19 > Label Options > Label Printer Defaults |  |
| 37960 | Display due date on shipping label | The shipping label generated from the “Shipping Label Print By Work Order” now includes “Due:” and the required date from the order. | OE7AI |  |

---
