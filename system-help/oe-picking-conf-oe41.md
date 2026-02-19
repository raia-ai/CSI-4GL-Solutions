---
title: "Completing a Picking Confirmation"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Completing a Picking Confirmation"
long_description: "Help documentation for Completing a Picking Confirmation in the 4GL system."
---

Completing a Picking Confirmation
=================================

[is this an OK title, or s/b “Picking an Order” or ... ??]

After a sales order has been processed, the next step is for the warehouse staff to pick the inventory to fulfill each order line to ready for shipping. The Picking Confirmation created here is used to generate the Packing Slip that will accompany the shipment. [accurate?] [copied to handheld:Pick Orders/Transfers]

When the quantity ordered = the quantity picked, the line item is considered Complete.   
Partial quantities can be released from an order, resulting in a back order. The status of line will remain Partial, and the inventory is still reserved. Alternatively, if configured1, the “P” line will be closed and a quote generated for the remaining quantity (with the same header information as the original sales order). [last bit is from old help - still true?]

An order may be picked via the Picking Confirmation screen (described here) or via a handheld scanner in the warehouse.

1. Choose Sales Order Entry » SO Entry/Maintenance » Picking Confirmation [OE41].
2. All orders in “PCK” status are displayed; . This list may also display orders with “HOLD” status that are partially picked. Open the order you want to pick.

If an order was previously picked and you are ready to create the packing slip, select the order and click Process.

On the Details tab, the top portion of the table displays all order lines in the order, and the bottom portion shows the inventory logs picked for the currently selected order line.

Use the arrow keys on your keyboard to navigate between lines in each section, and then Tab (or Shift+Tab) to switch between sections. [if this is a generic function that is used other places, create a snippet for re-use]

3. Cost or surcharge lines may be automatically picked2[config path?]; if not, double-click on a line to edit or confirm the value (see Adding a Non-Inventory Charge). When you click Save, the line is marked as “Picked”.
4. To add a log for an order line, double-click on the line at the top, or select the order line and press Enter or click Add Log.

This topic describes adding logs that do not need to be cut [you used the term “straight pulls” - is that a term that should be used/would be well understood?]. If there are no logs of the exact dimensions you require, you’ll need to select a larger log and cut it to size (splitting it into logs of multiple dimensions). See Handling Log Splits.

5. In the Inventory Log Information screen:
   1. Enter the Log No (if known) or click … to retrieve it (see below).
   2. The Ship check box may be enabled3; this allows you to direct how backorders are handled: [need more info re how this relates to the P/C/blank state referenced in step 5]
      * If the check box is selected, this log will be included on the packing slip.
      * If not selected, this log will not be included on the packing slip, but it will remain picked on the order after the packing slip has been created.

      To quickly change the Ship check box after a log has been picked, select the log line(s) and click Ship Log. This allows you to quickly change the S column to Y or blank (N).
   3. The Quantity fields and the Used Pieces field default to the quantity ordered (as shown in the top right) [to be confirmed]. Change any of these fields as required:
      * Selling Quantity - the UoM is defined by the order, but you can change the quantity if necessary.
      * Picked Quantity - calculated theoretically based on the Selling Quantity; an error may appear if the Picked Quantity is greater than the ordered quantity (based on IUM, SUM, or both).4
      * Picked Pieces - you cannot change this field if the Selling Quantity or Picked Quantity unit of measure is “PC”.

      Selling Quantity, Picked Quantity, and Picked Pieces determine what the customer will be billed for, and will be visible to the customer on the packing slip and invoice. Used Quantity and Used Pieces are used to define the cost of the order and how much inventory is removed from , and are not visible to the customer.

      * Used Quantity - the default quantity is calculated in one of two ways depending on the product line configuration5:
        + Theoretical weight based on the Picked Quantity.
        + Actual weight calculated by taking a proportion based on the actual on-hand values, e.g. (Available Quantity /Available Pieces) x Picked Pieces.
   4. Click Save to complete the log selection and return to the Picking Confirmation screen; the log is added to the Inventory Logs section on the Details tab.
6. The corresponding order line will display a “C” if picking is complete for that line item, or “P” if it is partially picked. The unpicked quantity will be backordered and the backordered amount will be listed on the packing slip. You have three options:
   * To add another log for the selected line item, repeat steps 3 and 4. Note that you cannot add the same log to the line; if you want to change the quantity, change the inventory log that you previously added.
   * To force the system not to back order a partially-picked line, click Part/Comp and change the line to “Complete”.
   * To prevent the line from printing on the packing slip, click Part/Comp and change the line to “Blank”. The order line is in effect cancelled. [true?]

![](../Resources/Images/OE_pck_conf.png)

> * Edit an existing inventory log line - select it and press Enter or click Chg Log
> * Delete one or more inventory log lines - select and click Rem Log
> * Override the quantity calculated for pricing, e.g. you are selling by the PC, the inventory is LB, and the pricing unit is by the foot. Select the order line and click Pricing Qty to adjust the value in the second Picked column in the table.
> * Edit the Remarks entered against the order detail line.
> * View the order Inquiry. [xref]

7. The Header tab allows you to change the following:
   * Label Type - The type of shipping labels that will be produced when the picking confirmation is processed. These labels will include the I number (the packing slip/invoice number). Select Heat (one label per log, includes all product information), Package (e.g. 1 of 3, 2 of 3, etc. based on the number defined in the Packages field, includes no product information), Generic (one label with customer information for the order e.g. PO, address, etc.), or blank if no label is required. This can be set by default.6[config path?]
   * Packages - The number of packages of each type that have been created for the order; this information prints at the bottom of the packing slip. If the Label Type is “P”, it determines the number of labels that will be produced. The package types are configurable7  [config path?].
   * Release Date - When the shipment will be released. This defaults either to the Required Date or today's date.8
   * Ship Instructions are printed at the top right corner of the packing slip.
8. The Summary tab displays a summary of what was ordered compared to what has been picked for shipping.
9. Enter the Release Date when the order should be shipped, and select one of the following options:
   * Process the document - if enabled9 [IN19 config path?], the packing slip(s) will be generated and the order updated; a warning may appear10 if reserved logs have zero picked quantity.
   * Change Printer or change method of delivery

   If you are using the manifest load/planning [MN31], skip this step; processing is finalized in the manifest.

Selecting an Inventory Log


This screen displays the logs in inventory of the selected product, showing details including:

* Log number, Heat, Bin, Size, Available Qty, etc.
* *Type* - ![](../Resources/Images/i_on_hand_icon.png) indicates on-hand inventory, ![](../Resources/Images/i_dogleg.png) indicates that the plate has dog-legs [true?](click Legs to view the legs that have been entered against the plate).
* ![](../Resources/Images/i_round_green_check.png) or ![](../Resources/Images/i_round_red_x.png) in the following columns:
  + R - whether there are reservations against this log (click Reserves to view the orders that have reserves))
  + V - whether the inventory has been verified
  + M - whether there’s a mill test report for the log (click View MTR to view the report or Sys MTR to view the system report)
  + C - whether the log is tied to a customer [to be verified]
  + P - whether the log is associated with a program [to be verified]
* Open - Y indicates the log bundle has previously been opened and therefore contains partial quantity.

Click ![](../Resources/Images/i_wrench.png) to filter the list to logs of specific dimensions.  
Click Enquire to view the Inventory Log Inquiry.



Configuration


1  > Backorder Method = Q

2 
[config path?]

3  > Allow Log Backorders in Picking Confirmation

4  > Issue Hard Warning When Picked Quantity is Greater Than Ordered Quantity

5 ![](../Resources/Images/i_arrow_down.png) > Warehouse > Calc Used Qty Proportionally

6 [config path?]

7 [config path?]

8  > Default Release Date to Required Date

9
 [config path?]

10 MS32>Options>OE>Additional Options>Warning If Used Logs Not Picked:  
- If set to “N” (no warning) - the order is processed without any warning  
- If set to “S” (soft warning) - a message will appear but the order can be processed.  
- If set to “H” (hard warning) - a message will appear and the order cannot be processed.

---