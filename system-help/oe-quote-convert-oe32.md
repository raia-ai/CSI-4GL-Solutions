---
title: "Converting a Quote to a Sales Order"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Converting a Quote to a Sales Order"
long_description: "This topic provides detailed information about Converting a Quote to a Sales Order in the 4GL system."
---


Converting a Quote to a Sales Order
===================================

Once the customer approves the quote, you can convert it to a sales order. Since the quote contains the same information as a sales order, you will not need to re-enter any information. A sales order has additional fields to record a customer’s PO number and a specific invoice date. You can bundle multiple quotes to convert to a single sales order.

1. Choose Sales Order Entry » SO Entry/Maintenance » Quote Entry/Maintenance [OE32].
2. Open a quote document that you want to convert, then click Process.
3. Enter V to convert the quote. The quote is added to a list for conversion.
4. Optionally, click ![](../Resources/Images/i_add.png) to add additional quotes to be included in the new sales order.
5. When you are ready, click Convert. The new sales order opens where you can make any changes required and process the order.

[CHM, please confirm if still accurate/relevant:  
“If using an “A” Line (reserve against incoming material) in Quote details , option to select incoming document to reserve against by press <F4> in “+” (D for details) to open Order Details window – operator can change details (modify, add, delete) in this screen.  
If quote includes a Buyout line, system will open the following window: [purchase order modification]  
When quote is accepted (has passed all Credit Policy checks), process is considered complete (document status changes from ASG to OPN)- a list of documents created from the quotation is displayed. A Picking Slip and all Purchase orders (if Sales quote includes Buyouts) are printed if processed. There is an option to put on hold which will change the status of the Work Order to “ASG” and will have to be processed from Work Order Entry.”

---
