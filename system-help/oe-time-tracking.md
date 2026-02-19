---
title: "Tracking Processing Time for an Order or Nesting Project"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Tracking Processing Time for an Order or Nesting Project"
long_description: "This topic provides detailed information about Tracking Processing Time for an Order or Nesting Project in the 4GL system."
---


Tracking Processing Time for an Order or Nesting Project
========================================================

The machine time required to process an order line can be estimated as part of the quote or order, then updated to reflect the actual time once processing has been completed. This time tracking requires several steps:

Set Up Time Parameters
----------------------

In the Machine Master [PR11]:

1. Find the machine. This can be category “M” for flat rolled products, or category “C” or “D” for long products.
2. For flat rolled products:
   1. F4 in “C” field (Machine Costing Factors) and enter the IPM (cutting speed) per thickness.
   2. F4 in “P” field (Pierce Pricing Values) to enter the pierce time per thickness.

   For long products, F4 in “C” field (Machine Cut/Drilling Time) to enter the Min Per Cut per various specifications and dimensions.

Viewing the Estimated Time for an Order
---------------------------------------

In the order:

1. Expand the Sales Price field for a line item – there will be an M line with the Estimated time calculated based on the order qty, product, and machine process selected.
   This time can be overwritten.
2. Expand the M line – this shows for each piece the cut length (the perimeter value of the cut piece), plus the pierce time, then the M line reflects this x qty.
3. For long products, add a drilling line. You must enter the quantity manually but the time will be calculated.
4. Process the order.

The estimated time is also available in the Production Schedule [PR41B]. Filter to the process to find the order. The estimated time shows per the order’s M line(s).

Input Actual Time
-----------------

This can be done in  at any status of the order (even if already invoiced), or via the handheld during processing (the sales order or IP/nesting doc must be in Pick status).

* In , go to the Machine Production Time [PR43B] form. Retrieve the order document and enter the Actual Time.  
  or
* On the handheld, go to the Time Tracking [WF19] function:
  + Scan the doc #, the line #, and the machine.
  + Use the Act field to manage the accumulated job processing time:  
    1 – schedule the job|  
    2 – start the job  
    3 – pause  
    4 – unpause  
    5 – stop the job

Viewing Estimated vs Actual Times
---------------------------------

Use the Sales Order Inquiry [OE61]:

1. Retrieve the order.
2. On the Details tab, open the Inv line.
3. On the Scheduled tab you will see the start/pause/end times.

Alternatively, use PR7G to generate a report on Est vs Actual Time.

---
