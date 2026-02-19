---
title: "Stock Inquiry By Warehouse"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Stock Inquiry By Warehouse"
long_description: "Help documentation for Stock Inquiry By Warehouse in the 4GL system."
---


Stock Inquiry By Warehouse
==========================

This function is used to inquire on the inventory status, including on hand, inbound, outbound, quarantined and log movements for one or more products. Products can be searched by providing a number of parameters in the inquiry screen. The more parameters entered, the narrower the search. If no parameters are entered, the system will list all products for selected product line.

allows for search by keyword as well as the ability to filter by country of origin.

1. Choose Inventory Control » Inventory Inquiry » Stock Inquiry By Warehouse [IN62].
3. Optional addition entry of pseudo code and keyword.  
   or  
   Enter or select specifications for the product line. Specifications available will vary by product line.
4. Press F4 in Available to view stock available. This is equal to current stock minus outbound commitments for selected warehouse.
5. Press F4 in Incoming to view incoming stock available. This is equal to incoming stock available minus reserved against inbound quantity for selected warehouse.

   Quantities in red signify pre-receipts for incoming purchase orders.
6. The Avail All Whse value for each product is the total available quantity in all warehouses that belong to the same division as your operator warehouse. Press F4 in this field to display all inventory available at all warehouses.

   On the All Warehouses tab, you can:

   * Select a warehouse and click Switch to view the summary tab for that warehouse. This button is disabled if you are viewing warehouses for a different division than the one your operator belongs to.
   * Click Whse/Entity to view all divisions and their available and commit-in quantities. Select a division and click Whse/Entity again to display all the warehouses that belong to that division. If your operator does not belong to this division, only the available and commit-in quantities will be shown for each warehouse.

The user's warehouse is defined in MS32. A warehouse is associated with a division in IN19.

Inventory Inquiry icons:  
![](../Resources/Images/Inv_inquiry_type_icons.png)  
If a log is both quarantine/program and compatible, it will be listed as compatible; if a log is both quarantine/program and pre-receipt, it will be listed as pre-receipt.  
If more than one condition is met, only one icon is shown in the following hierarchy:  
1. Pre-receipt
  
2. Verified
  
3. Compatible
  
4. Dog Leg
  
5. Location type

---
