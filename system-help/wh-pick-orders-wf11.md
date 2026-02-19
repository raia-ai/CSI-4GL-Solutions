---
title: "Picking Confirmation"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Picking Confirmation"
long_description: "Help documentation for Picking Confirmation in the 4GL system."
---

Picking Confirmation
====================

Picking confirmation is used to pick inventory for an order where that inventory does not need to be processed first (straight stock pulls) and can be used once a document has been released to the warehouse (placed in PCK status).

Logs may be picked into a package to create a consolidated label, and the package added to a manifest run.

can be configured1 to automatically print shipping labels and produce packing slips (delivery notes).

You cannot do log splits as part of this function — you must use the separate Log Split function.

![](../Resources/Images/WH_pick_orders_transfers.png)

1. Scan or enter the sales order/branch transfer Doc number (if entering manually, you can omit the letter or leading zeroes).
2. Scan the Log to be picked against the order. You may or may not be able to select compatible logs (e.g. a log that has a different, compatible grade of material).2

![](../Resources/Images/WH_pick_orders_transfers_view_logs.png)

You can also scan the vendor barcode that was assigned during Receiving to retrieve the log(s).

There are two main ways to pick inventory - either by scanning and picking directly from logs or by picking through the Log Transfer function. If you are picking directly from logs you can pick and use part of that log, but when using the log transfer function you will create a “baby log” and the entire quantity of that baby log will be used for the order.

* If the log transfer switch3 is enabled, you will not be able to select any pre-received logs; however if multiple logs were received with the same barcode, the system will try to select the received log with that barcode.   
  If the selected product is set to allow random lengths4, you are prompted to enter the random lengths before the transfer in order to transfer the quantity calculated by the R/L window.
* If the log transfer switch is turned off, you should see all logs; any pre-received logs will be indicated with a ‘Y’ in the ‘R’ column.

Your operator settings5 may prevent you from changing logs that were allocated by the salesperson:  
- if no logs were allocated by the salesperson, you can transfer any log (assuming compatible with order line product, foreign/domestic, etc.)  
- if logs were allocated by the salesperson, you can only transfer the allocated log; they cannot clear the log nor add/transfer other logs.

3. Depending on your configuration3, you may be sent to the Log Transfer window automatically upon scanning a log. If there is more than one line that the log can satisfy, you will be presented with a list to select from. The Qty and Pcs default from the order; you may be able to edit these fields6. Enter “1” to process. A transfer will be invoked and the “baby” log will be returned and you will be returned to the Picking Confirmation. You may be prompted to change or confirm the number of shipping labels to print7, or labels will print automatically according to the number of labels set up in IN198. Continue with step 6 below.
4. If multiple lines on the order can be fulfilled by the same log number, you will be prompted to select which line you are picking for. If the line is barcoded on the picking slip, you can scan the line number.
5. The Pck, Use, and Pcs fields may default9 based on the amount ordered (Opn). If not, enter the picked amount (Pck) for the line item (if already picked, you can revise the amount you are picking from this log).
6. The Quantity fields and the Used Pieces field default to the quantity ordered. Change any of these fields as required:
   * Selling Quantity - the UoM is defined by the order, but you can change the quantity if necessary.
   * Picked Quantity - calculated theoretically based on the Selling Quantity; an error may appear if the Picked Quantity is greater than the ordered quantity (based on IUM, SUM, or both).10
   * Picked Pieces - you cannot change this field if the Selling Quantity or Picked Quantity unit of measure is “PC”.

   Selling Quantity, Picked Quantity, and Picked Pieces determine what the customer will be billed for, and will be visible to the customer on the packing slip and invoice. Used Quantity and Used Pieces are used to define the cost of the order and how much inventory is removed from , and are not visible to the customer.

   * Used Quantity - the default quantity is calculated in one of two ways depending on the product line configuration3:
     + Theoretical weight based on the Picked Quantity.
     + Actual weight calculated by taking a proportion based on the actual on-hand values, e.g. (Available Quantity /Available Pieces) x Picked Pieces.
7. If you need to pick another log for this order, scan the next Log number and repeat the above steps as required.

Inventory lines not completely picked may be backordered11.

You can do any of the following tasks by pressing F4 in the Log field to view the list, then F6 to select:

* VIEW - shows a summary of the order with the amount ordered and picked for each order line; you can filter by process and/or location, or drill down to the log level
* EXIT - return to the previous menu
* CLEAR - remove all logs that have been picked for this order
* CLRONE - remove all logs for one line on the order (you will be prompted to enter the line number)
* CLRLOG - remove one log from the order (you will be prompted to scan the log number)
* FINAL - process the picking confirmation and return to the menu; if enabled1, the packing slip(s) will be generated and the order updated; a warning may appear12 if reserved logs have zero picked quantity
* CANCEL - return to the previous menu
* MODIFY - change picked amounts on the order - press F9 to expand the screen, F6 to change the quantities; alternatively, you can change a log’s picked quantities by rescanning the log number (in effect, re-picking it)
* INQUIRY - do a stock look-up (including bin locations), e.g. to look for inventory that can fulfill a line, or to look for all inventory related to a particular log (i.e. of the same product code); press F9 to view log numbers and product descriptions
* SHPLBL - produce generic, package, or heat shipping labels (after the entire order is picked)
* HEATLB - print a heat label for the previous log scanned (as you are picking the order)
* LOGTRF  - transfer quantity from a log to a new, baby log number. Dimensions can't be changed like log split but it allows you to split one log into multiple logs
* STRPKG - create a new package (see below)
* ENDPKG - close the active package (see below)
* TFRREV - reverse the transfer of a child log; this moves all the quantity on that log back to the parent.

Creating a Package
------------------

After selecting an order, the user scans STRTPKG. This creates a new package and sets it as the active package. All logs picked after this will be added to the package until the package is closed.

When the first log is scanned, the system evaluates the line the log was picked for and assigns the active package to the corresponding manifest and run. If the line is not assigned to a manifest or run, the active package will not be assigned to a manifest or run.

Any logs scanned afterward must be on the same manifest and run as the first log. If the first log was not on a manifest or run, the scanned log must not be on a manifest or run either.

Unpicking logs (using CLEAR or CLRONE) will remove them from the active package.

To close the active package, the user scans ENDPKG. This removes the current package as the active package and prints a label for the package.

Configuration


1  > Process Handheld Confirmations Through to Packing Slip

2  > Disallow Compatible Logs in HH Picking

3  > Only Allow Log Transfer in HH Picking Confirmation

4 IN16 > Options > Input Random Length = “Yes”

5 MS32 > Options > Order Entry > Allow HH Substitution=“S” (lines not picked by Sales)

6  > Allow Override Quantity in Handheld Log Transfer

7  > Confirm Label Print in Handheld Log Transfer

8 Label Options > Label Printer Defaults

9 > Bypass Defaulting of Picked Quantity in Handheld Picking Confirmation

10  > Issue Hard Warning When Picked Quantity is Greater Than Ordered Quantity

11  > Always Back Order regardless of whether that line has been picked or not; if enabled, both partially picked and unpicked (IUM Qty = 0) are back ordered; if not enabled, only partially picked (IUM Qty >0) are back ordered.

12 MS32>Options>OE>Additional Options>Warning If Used Logs Not Picked:  
- If set to “N” (no warning) - the order is processed without any warning  
- If set to “S” (soft warning) - a message will appear but the order can be processed.  
- If set to “H” (hard warning) - a message will appear and the order cannot be processed.

---