---
title: "Oe One Step Invoicing"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Oe One Step Invoicing - 4GL Help Documentation"
long_description: "This topic provides detailed information about Oe One Step Invoicing in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
One Step Invoicing
==================

One-Step Invoicing allows you to create a sales order and a packing slip in one step (rather than creating the packing slip in Picking Confirmation). All documents (sales order, pick slip, packing slip) are printed, and  automatically confirms the logs, prior to material being picked in the warehouse.

The following rules must apply (for all lines on the sales order):

* One-Step Invoicing must be enabled1
* the sales order cannot be created from a quote
* all lines on the order must be pulling from stock and not sourced from a vendor
* the sales order cannot be held in credit or margin check queues, otherwise the sales order will have to be picked in the normal manner after credit or margin approval
* documents will print on default printers – there is no opportunity to change printer.

To process a sales order using One-Step Processing:

1. Create a sales order.
2. When the sales order is complete and you are ready to process the order, enter “O” to use One-Step Invoicing. If the above criteria is not met, “O” is not displayed as a processing option.
3. will print the sales order and pick slip.
4. The Sales Order Shipments window opens; logs will already be picked and Sales Order Line status = **C**losed). The sales order status will remain “ASG” (Assigned).

When there are multiple logs to be selected, the system will pick those logs with one piece remaining, removing all weight in the “Picked” Inventory Quantity – the theoretical weight will be in the “Used” Inventory Quantity. Total Picked Quantity = Work Order quantity.

The formula used by system for calculation of Picked / Used Quantity:  
*Total Sale Order Qty \* Used quantity for each log line / Total Used quantity for all Logs:*

5. If logs were not assigned when the sales order was created, they will have to be picked (press F4 on the Picked Quantities – Inventory to open Inventory Log Information window).
6. After confirmation of sales order shipments, press F3 to exit. The packing slip will print, the sales order status will change to PRT and an invoice number will be assigned. An invoice can now be printed in the normal manner.

Configuration


1 MS32 > Options > Order Entry > One-Step Invoicing

---
