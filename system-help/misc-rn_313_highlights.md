---
title: "Rn 3.13 Highlights"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rn 3.13 Highlights - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rn 3.13 Highlights in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Highlights
==========

Automatic Branch Transfer from Order Entry
------------------------------------------

If you are processing an order where the material is sourced from multiple warehouses, this will save you a few steps. When adding a line item to an order, there is a new Source option (Whse). When you select this “Whse” option, you are prompted to select the warehouse that the inventory will be transferred from.

When you process the sales order, a branch transfer is created for and linked to that order line:

* If the order is placed on credit hold, the transfer will also be placed on credit hold.
* When the order passes the checks and is released the transfer will also be released.
* Any sales order line notes and header notes are copied to the transfer.
* The pick slip for the branch transfer prints the original sales order number (and may print the customer name below the order line1).

When the branch transfer is processed through picking confirmation, the delivery note for the branch transfer also prints the original sales order number (and may print the customer name below the order line2).

Link Order to New Branch Transfer
---------------------------------

Related to the change above, when you create a branch transfer you can link it to an existing sales order. Transfer lines will be created from the sales order lines. When the transfer is processed, the incoming part of the transfer will allocate to the sales order.

Simplified Point of Sale Order Processing
-----------------------------------------

Point of Sale orders are now entered in the regular sales order form (OE31). If a POS payment term is selected, you can capture multiple types of payments on the new Payment tab. Payments can also be recorded in the standalone Payment Entry form (OE5C).

Customers can now be identified as members (trusted customers) (AR17 > More Info). Depending on the definition of the payment type used, an order may automatically go on credit hold unless the customer is a member.

A new Payment Report (OE7XV) displays all unposted payments for all customers. You can use this report for reconciliation before posting. Then run the new Payment Posting form (OE5D) to post the payments and process the cash receipts in AR31.

Pick Slip Printing Improvements
-------------------------------

* Printing pick slips for stock lines: A pick slip will print for order lines that have no primary process as well as processes identified as stock lines in PR11. When reprinting pick slips by machine, processes defined as stock lines are treated the same as a blank process.
* A new screen (OE72B) reprints pick slips for all open sales order lines in PCK or PBP status that have the selected delivery date. Pick slips will print by sales order number.

Adding Customer Parts to Database from Sales Orders
---------------------------------------------------

You can now easily add a new part to  when adding a product to a quote or order by selecting the new check box next to the Part Number field.

Configuration


1 IN19 > Forms > Branch Transfer Picking Slip > Options > Display Customer Info for Branch Transfer

2 IN19 > Forms > Packing List > Options >  Display Customer Info for Branch Transfer

---
