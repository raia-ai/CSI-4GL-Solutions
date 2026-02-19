---
title: "Pick Slip Batch Queue"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Pick Slip Batch Queue"
long_description: "This topic provides detailed information about Pick Slip Batch Queue in the 4GL system."
---


Pick Slip Batch Queue
=====================

may be configured1 so that when an order is released (either through credit or manually by the salesperson), the pick slip is not printed immediately but is instead held in a queue that must be manually released and print the slips as a batch.

The configuration allows for the queue to be bypassed to print pick slips immediately if there is stock and the Required Date is today or the next business day; see 1 below.

User security2 identifies who has authority to release the pick slips from the queue.

Pick slips held in the Pick Slip Batch Queue are assigned a status of “PBP”.

There are operator and warehouse options that control what you can edit on an order, based on its status, and whether the status reverts to ASG/OPN.

Viewing and Releasing Pick Slips
--------------------------------

1. To view and release the pick slip queue, choose Sales Order Entry » SO Entry/Maintenance » Pickslip Release [OE3L].

   The Batch Print tab displays all orders for which pick slips are on hold. The order may have one or more of the following indicators:

   * C – Customer will not pass a credit check. The credit check is not redone upon releasing the order from this queue.
   * B – Order is a Buy-in/Buy-out. It may have been received, but at time the order was created, it was linked to an inbound PO.
   * U – There is insufficient stock to 100% fill the order. This is a dynamic switch and will change depending on stock availability.
   * S – The order is selected to be released from the queue upon **Process**.

   The On-Hold tab displays all orders that are on hold in  (i.e. for Credit Check, Pricing approval, Margin approval). Once released from the hold queue, the order will move to the Batch Print tab.

   If you have appropriate security2, you may click **Edit** on an order in the queue to open the order to make any necessary changes. Changes made to sales orders in this way will not be subjected to Task Manager edits.
2. Select the orders that you want to release (use the Shift or Ctrl key to select multiple, or click **Select All**). A “Y” will appear in the S column.
3. Click **Process** to release the pick slips for the selected orders. The linear nest production order for each nesting document that belongs to the sales order will also print, based on the form printer options in IN19 for form 57.

Removing an Order from the Queue
--------------------------------

A salesperson may want to “pull back” a sales order for further modifications.

In the Sales Order Entry/Maintenance [OE31] search screen, enter the Document number in the Search pane. A message will display “Document is awaiting batch release. Withdraw from batch?”. If you click **Yes**, the order status reverts from “PBP” back to “ASG” and the order is removed from the Pick Slip Batch Queue.

Configuration


1  > Enable Batch Printing of Pick Slips   
Options are:

* blank - pick slips are not held and are printed when the order is processed (assuming no checks (margin, price, credit) are enabled)
* **Y**es - all pick slips are held in the pick slip batch queue
* Yes with **B**ypass - pick slips will be held in queue, except those with a Required Date of today or the next business day, which will print automatically. Pick slips will not bypass if there are any lines with unavailable stock on the order, or lines that are reserved against committed-in; a switch (Check IUM Quantity Or Pieces for Availability) determines whether to check against IUM, pieces or both.
* Yes with **L**ine Level Bypass - pick slips will be held in queue, but inventory lines will print automatically if all of the following criteria are true:
  + a machine is defined against the order line (a “stock” machine can be used if there is no processing involved); the machine code must have the “R” flag (Auto Release Order Line) set in the Machine Master [PR11].
  + Required Date is today or the next business day
  + inventory stock is available and there are no reserves against incoming material (same as **B**ypass above).

2 MS32 > Options > Order Entry > Pick Slip Batch Sec   
Options are:

* P - full security to release pick slips, modify all orders
* S - restricted view of pick slips for inside salesperson logged in - cannot process but can edit orders
* M - can view all pick slips, edit/modify orders
* O - can process pick slips only, cannot modify orders

---
