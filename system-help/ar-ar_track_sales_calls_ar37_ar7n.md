---
title: "Ar Track Sales Calls Ar37 Ar7N"
source: "madcap.md"
tags: ["4GL", "AR", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Ar Track Sales Calls Ar37 Ar7N - 4GL Help Documentation"
long_description: "This topic provides detailed information about Ar Track Sales Calls Ar37 Ar7N in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the AR module."
---


Tracking Sales Calls
====================

Capture and review sales call information for current or potential customers. Any call remarks captured for a potential customer is carried forward if the customer is converted to an actual customer.

Entering Call Information
-------------------------

1. Choose Sales Order Entry » SO Entry/Maintenance » Outside Sales Call Reports [AR37].
2. In the T column, indicate if the call is to a **C**ustomer or **P**otential customer, then select the Customer.
3. Select or enter the customer Contact that you spoke with.
4. Enter the Date of the call.
5. In the P column, indicate the priority of the call: **H**igh, **M**edium, or **L**ow.
6. In the C column, select the Remark Category. These are defined in OE1O; if a remark type is marked as the default in OE1O, it will be defaulted here but can be changed.
7. Click … beside the R field, then enter the remarks you want to capture about the sales call.
8. The U column allows you to view any customer UDF values populated in AR17 or AR1L.

You can import sales call remarks into : first download the Excel template using AR38, complete the spreadsheet, then import it using AR39. If a remark type was marked as default in OE1O, you can leave the Category blank in the spreadsheet.

Viewing Calls
-------------

You can view call remarks via inquiry or report:

* View calls with a specific customer in your database: choose Customer » General Inquiry from the top dropdown menu and retrieve the customer. If the Call Report field shows a **+**, there are calls captured.   
  Open the field to view the list, and press F4 on the **+** beside an entry to view the full remark.
* Generate a report of sales call remarks using AR7N. You can filter the report for one or all salespeople (inside or outside), for a given date range, filter by category and/or priority.

---
