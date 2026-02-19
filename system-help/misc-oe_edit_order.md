---
title: "Oe Edit Order"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Oe Edit Order - 4GL Help Documentation"
long_description: "This topic provides detailed information about Oe Edit Order in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Editing an Order
================

When editing orders in OE31, the following operator and warehouse options control what you can edit, based on the order status, and whether the status reverts to ASG/OPN.

* Operator-level access options control whether the operator can modify an order on hold1, and whether the operator can modify the Header and/or Detail section of an order in PCK/PCB status2.   
  If Detail Access is enabled, a further switch controls access to lines with logs picked: if this Picked/Delivered Lines switch is enabled, the operator will see a warning and, when editing the line, a notification that changes may need to be reflected in paperwork. If the Picked/Delivered Lines switch is not enabled, the operator will not be able to edit, delete, or nest any lines with logs picked, and will be prompted to contact admin to make such changes.
* Warehouse-level access options3 control whether an order/quote in PBP, CRD, PRA, and/or QCH status is withdrawn (changed to ASG/OPN status) or whether the status remains unchanged. Orders in PCK or PCB status will remain unchanged. By default all statuses (except PCK and PCB) will be set to be withdrawn.  
  An order in PBP status can be modified even if it was partially delivered. You will be prompted to confirm that you want to proceed with editing the order. The order's status will not change (regardless of PBP settings in the Order Withdraw Options).

An order may also be changed through OE3L or through the Task Manager; in this case the order status remains unchanged.

Changing the Required Date


There are several options to change the Required Date on a sales order:

* To change the date for the entire order, change the Required Date on the Billing/Shipping tab.
* Depending on the configuration for the warehouse4, you may be able to change the date at the line level in one of the following ways on the Details tab (OE31/OE32):
  + Open the line item and change the date. You can change individual lines to different dates in this way.  
    or
  + To change one or more line items to the same new date, select the line items, then click the green arrow ![](../Resources/Images/i_arrow_down.png) at the bottom twice and click Req Date, then select the new date.

may or may not allow you to change the Required Date to a past date5.

If you change the date on a line item that has already been assigned to a manifest, the order line is removed from the old manifest and added to the new manifest according to the new date.

If you change the date on a stock line in PCK status, the line status is changed back to PBP.

If you change the date on an order line that has a nesting project number, you will be advised that the required date on other lines from the same project will be changed.

There are operator and warehouse options that control what you can edit on an order, based on its status, and whether the status reverts to ASG/OPN.



Configuration


1 MS32 > Options > Order Entry > Hold Order Access  
— Define access for each hold status (PBP, CRD, PRA, and/or QCH status); operators who had access to OE31 prior to v3.14 can modify orders on hold.

2 MS32 > Options > Order Entry > PCK Order Access  
— Operators who had access to OE3C and OE3F prior to v3.14 can change orders in PCK status, otherwise they should not have access.

3 IN19 > OE Options > Order Withdraw Options

4  > Required Date Header or Line Level — This switch can be set to allow line level date change for POS orders only, non-POS orders only, or both types of orders. If the switch is set to “None”, the date can only be changed at the header level.

5  > Check If Requested Date On Order Line Is Before Today:  
If set to “N” - the date will be changed as normal  
If set to “S” - a message will appear but user can choose to continue, the date will change  
If set to “H” - a message will appear and the date will not change.

---
