---
title: "In41 Branch Transfer Entrymaintenance"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "In41 Branch Transfer Entrymaintenance - 4GL Help Documentation"
long_description: "This topic provides detailed information about In41 Branch Transfer Entrymaintenance in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Branch Transfer Entry/Maintenance
=================================

**Branch Transfer vs Intercompany Sale?**
  
If the branches/warehouses are separate legal entities in a financial sense, use an intercompany sale.   
If the branches keep the same accounting books, use a branch transfer.

A branch transfer is used to create documents to transfer inventory to/from company warehouse locations. Each warehouse address and contact information must be added in the Customer file (AR17).

1. Choose Inventory Control » Branch Transfer » Branch Transfer Entry/Maintenance [IN41]
2. Enter or select From Warehouse.
3. Select Document: New, Duplicate, Link or existing document.
4. Enter or select Customer (defaults to all).
5. Enter or select Salesperson (defaults to your name).
6. Enter or select bill to Contact name.

You can link a branch transfer to an existing sales order. Transfer lines will be created from the sales order lines. When the transfer is processed, the incoming part of the transfer will allocate to the sales order.

may or may not allow you to process the transfer if the Required Date is in the past3. Branch transfers may require approval4 for all transfers or for those over a set amount.

Branch transfer shipping labels will print the information of the sales order that the BT is allocated to if a warehouse option5 is enabled and the log is reserved on a sales order in the receiving warehouse. Log numbers must remain the same between sending and receiving warehouses for BT.

Creating a Branch Transfer Automatically from a Sales Order
-----------------------------------------------------------

If you are processing a sales order where the material is sourced from multiple warehouses, you can save some time by creating the branch transfer automatically: when adding a line item to an order, select “Whse” in the Source field. You are prompted to select the warehouse that the inventory will be transferred from.

When you process the sales order, a branch transfer is created for and linked to that order line:

* If the order is placed on credit hold, the transfer will also be placed on credit hold.
* When the order passes the checks and is released the transfer will also be released.
* Any sales order line notes and header notes are copied to the transfer. UDFs6 and order remarks7 on the order may also be copied to the branch transfer document.
* The user who created the order is listed as the salesperson on the branch transfer.
* The pick slip for the branch transfer prints the original sales order number (and may print the customer name below the order line1).

When the branch transfer is processed through picking confirmation, the delivery note for the branch transfer also prints the original sales order number (and may print the customer name below the order line2).

Configuration


1 IN19 > Forms > Branch Transfer Picking Slip > Options > Display Customer Info for Branch Transfer

2 IN19 > Forms > Packing List > Options >  Display Customer Info for Branch Transfer

3  > Check If Requested Date On Order Line Is Before Today:  
If set to “N” - BT can be processed as normal  
If set to “S” - a message will appear but user can choose to continue  
If set to “H” - a message will appear and the BT cannot be processed.

4 IN19 > IN Options > Additional Options > Branch Transfer Approval *and* Branch Transfer Approval Limit

5  > Print Order Label for Allocated Transfer Logs

6  > Copy Order Line UDFs To Source BT;   
UDFs are configured in IN19 > OE Options > UDF Descriptions. These fields display beneath the Part Number field when adding a line to an order/quote; if there are no UDFs configured in IN19, a UDFs field will be visible but disabled. If the check box beside the UDF Description (in IN19) is selected, the field value will be copied to subsequent lines in the sales order.

7  > Set Order Customer Remarks On Source BT; in addition to order remarks on the order, any canned remarks from the order customer will also be added to the BT instead of the canned remarks from the BT customer (the receiving warehouse).

---
