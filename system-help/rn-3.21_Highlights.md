---
title: "Highlights"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Highlights"
long_description: "Help documentation for Highlights in the 4GL system."
---

Highlights
==========

Check out the webinar that covered some of our 3.21 changes!

OE31/OE32 Search Can Default to a Date Range and to All Operators
-----------------------------------------------------------------

Two new switches have been added related to the OE/quote search screen: 39360

* “Order Entry Search Days Back” (warehouse switch) allows you to default the From Date to today’s date minus a set number of days back.
* “Default Entry Search to ALL Salespeople” (operator switch) allows the Salesperson field on the search screen to default to “All”; if not set, the search defaults to your operator.

OE32 has Indicator if the Quote was Created from a Backorder
------------------------------------------------------------

The search tab for Quote Entry/Maintenance now has a “B” column to indicate if the quote was created when an order is on backorder (“Backorder Method” switch = “Q”). 39466

OE1Q Allows Custom Headings for All Forms
-----------------------------------------

The Alternate Form Headings function now allows custom headings to be defined for all forms. 39109

SO Remarks Print on IP/OP Documents
-----------------------------------

The “Display Sales Order Alloc” form option for forms 23, 24, 26, 30, 31, and 32 has been changed to allow “U” and “R” values to print order line UDF and remarks on IP/OP documents. 39746

Available and On-hand Weight Added to IN62
------------------------------------------

Two new columns have been added to the Detailed Inquiry > Inventory tab: “Avl Wgt” and “Onhand Wgt”. 39300

Handheld Version of IN5D
------------------------

A new handheld function has been created to Add/Update Log on Count, WF1Y. You can use this function to add logs to the current inventory count, if the log is not already on the count. You can also use it to refresh the system quantity if that has changed since the count was initialized. 39151

Canada Customs Paperwork
------------------------

now caters for the paperwork required by Canada Customs for US>Canada shipments. 39390  
This includes:

* a field on the product line to capture the HTSUS code (IN16)
* a new function to export/import the HTSUS codes for all products in one or all product lines (IN9YE)
* new forms added to IN19: USMCA Certificate of Origin and Canada Customs paperwork and new functions to print these (OE7WA/OE7WB).

Manage Multiple Handheld Menus
------------------------------

A new screen, Handheld Menu Type Maintenance (MS9H), allows for multiple menus to be created with different menu options. A menu type can be assigned to all operators at one or all warehouses, or can be selected or modified for individual operators in MS32. 39524

Task Manager
------------

### Security Changes

A user identified as Supervisor of other users can view, approve, disapprove, reassign, or edit tasks owned by users who report to them. The supervisor can still only see groups that they are a member of. 39232

A new Task Manager Security option, “Full Control”, allows a user to manage tasks for all users, including those for a group they are not a member of. 39279

Users can now reassign any type of task to another user, provided the recipient’s security profile is configured to access the task type. 39280

See Setting Up the Task Manager

### Consolidating Purchase Quotations into a Single Purchase Order

The Purchase Approval task has changed: If you select multiple PQs and they are all the same currency, you will be asked if you want to consolidate them into one PO. If you choose Yes, you will be prompted to select a vendor (defaults if the PQs all have the same vendor). 39517

---