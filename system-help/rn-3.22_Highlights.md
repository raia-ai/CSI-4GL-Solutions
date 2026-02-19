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

Check out the webinar that covered some of our 3.22 changes!

Automatic Surcharge Calculations
--------------------------------

The cost line definitions in the Warehouse Order Defaults now allow for a C line to be defined with a percentage of the total order up to a maximum value, instead of defining a specific value, to be applied to all orders. For example this may be used to apply an automatic environmental surcharge. 39785

Option to Print Delivery Note Added to AR17
-------------------------------------------

The Document Delivery options in the Customer Maintenance file now include an option to print the delivery note. The packing list/delivery note will print when the Customer Copy (“C”) checkbox is not selected in the IN19 print options; however if the Customer Copy checkbox is selected in the IN19 print options, then the delivery note will only print if the checkbox in AR17 is also selected. 39329

Document Delivery Options for Pre-Invoice Added to AR17
-------------------------------------------------------

New Document Delivery > Delivery Note options in the Customer Maintenance file allow you to set up fax and/or email for pre-invoices for a customer ship-to. 39624

Email Subject and Body Added to AR7V
------------------------------------

Email fields (Subject and Message) have been added to the Fax/Email Statement to Contacts function. These default from MS33 the first time the function is run but then use the last value for each subsequent run. 39605

Use Order Writer as Sender When Emailing Delivery Note/Packing List
-------------------------------------------------------------------

A new switch (“ Email Packing Lists With Writer As Sender”) controls who a packing list email is sent from: if the switch is enabled, the email is sent from the order writer. If not enabled, the email is sent from the salesperson. 39653

Include MTRs Option Added to OE7B
---------------------------------

The Sales Order reprint now includes an option to Include MTRs. 39706

Barcode Added to MTRs
---------------------

System and Overlayed MTRs now include a barcode at the top for the warehouse code, document number, and document index. 40029

Inquiry Button Added to Manifest Assign Tab
-------------------------------------------

A magnifying glass icon at the bottom left of the Unassigned and assigned Run Items sections on the Assign tab allows you to open the inquiry window for the selected item (there is no inquiry for miscellaneous documents). 39676

Approval Task Added for Branch Transfers
----------------------------------------

Two warehouse switches have been added that can require approval for all branch transfers (“Branch Transfer Approval”) or for those over a set amount (“Branch Transfer Approval Limit”; this requires the first to also be set). 39672

PO1G Allows Approval Matrix by Warehouse
----------------------------------------

A Warehouse field has been added to the PO Approval Limit Maintenance form so that approval matrices can be set up per warehouse. Entries defined with no warehouse selected are considered the “master” matrix entries; these are used unless entries for a specific warehouse are entered. 39840

Reopen Closed Bank Periods
--------------------------

A new function, “Open Cash Book Period”, reopens a closed fiscal period. The B/F and C/F are reverted to the amounts before the period was closed. You can only reopen one period at a time, so if you need to reopen multiple periods you would work backwards one at a time from the most recently closed period. 39765

---