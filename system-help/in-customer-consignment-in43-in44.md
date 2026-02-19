---
title: "Managing Customer Consignments"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Managing Customer Consignments"
long_description: "Help documentation for Managing Customer Consignments in the 4GL system."
---


Managing Customer Consignments
==============================

Customer Consignment allows you to send material to a customer that they will store and will only be billed for once it has been used.

The consignment program works like a branch transfer (this will go to a virtual “consignment” warehouse) and assigns the customer's Bill To and Ship To (so you know where your material is physically) to the logs. Each consignment warehouse can “hold” inventory for multiple customers.

When the customer uses the material, you will enter a sales order in the consignment warehouse for the amount consumed. You can generate the Stock List By Customer [IN7YB] report on the consignment warehouse to see the inventory levels remaining for each customer.

Document numbers for consignment orders begin with “c”, and consignment confirmations begin with “j”.

The Credit Inquiry window from the Customer dropdown displays (in the Consignment Stock field) the sum of the value on all inventory logs that belong to the consignment customer in the consignment warehouse.

Configuration
-------------

1. For each stocking warehouse from which you will ship material, you must set up a virtual “consignment” warehouse. This warehouse will be referenced for all inventory that is sent on consignment to any number of customers. To set up this consignment warehouse:
   1. Use the Duplicate a Warehouse utility [IN10V] to copy from your stocking warehouse.
   2. Open the consignment warehouse in [IN19] and change the following:
      * Select the Consignment check box to identify that this is a consignment warehouse.
      * Enter the stocking warehouse code in the Parent Whse. [was there a purpose to this other than for changing the GL posting?]
      * Press F4 on Forms to define the Customer Consignment Acknowledgment, Picking Slip, and Delivery Note. [why are these different from parent whse? or maybe the question should be: why are they defined in the stocking whse? Should probably include, in the procedures below, which form is sent when?]
2. Open the stocking warehouse in [IN19] and select the Consignment Whse (that you defined in step 1). DO NOT select the check box.
3. Identify each customer who will be receiving consignment materials (Customer file [AR17] > More Info > Consignment?). You can only ship consignment material to customers that have this check box selected.

In the example below, warehouse 10 is the stocking warehouse, and warehouse ZY is its consignment warehouse:

![](../Resources/Images/consignment_whses.png)

Sending Inventory to a Consignment Customer
-------------------------------------------

To set up a consignment transfer:

1. Choose Inventory Control » Branch Transfer » Consignment Fillup Program [IN43].
2. Create a new document. Complete the document the same as an order, with the exception being that you cannot change the Sales Price on the line item. [is this statement accurate/sufficient?]
3. When you process the document, the Customer Consignment Picking Slip is generated from the stocking warehouse.[true?]

When you are ready to ship the material:

1. Choose Inventory Control » Branch Transfer » Consignment Fillup Confirmation [IN44].
2. Select the consignment document, and complete it the same as a regular picking confirmation.
3. When you process the confirmation document, the materials are automatically received into the consignment warehouse, the selected logs are assigned to the customer, and the Customer Consignment Acknowledgment and Delivery Note are generated from the consignment warehouse.[true?]

Invoicing for Inventory Used
----------------------------

You may decide to bill for consignment materials when they are used or after a certain time period.

In either case, generate a sales order from the consignment warehouse. When you are selecting the logs, you can press F9 to see which ones are assigned to the customer you are billing. You can now change the Sales Price for the line items.

---
