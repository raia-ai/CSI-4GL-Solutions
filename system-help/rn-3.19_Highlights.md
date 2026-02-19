---
title: "Highlights"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Highlights"
long_description: "This topic provides detailed information about Highlights in the 4GL system."
---


Highlights
==========

Modify Price/Value of Processes and Apply to Selected Lines
-----------------------------------------------------------

A Processing button has been added to the mass Reprice window where you can modify the price/value of processes for selected lines. You can also add new codes for lot charges that would be distributed across the selected lines.  
Related, the Summary tab of the order now includes two new columns (Stock Value and Proc Value) and a Processing button that shows a summary of the processes for the whole order. 38766

Send Statements to Customer Contacts
------------------------------------

A new report function sends statements to contacts at one or all customers. The statement contains the same details as AR7E (assuming default selections). To facilitate this, the Document Delivery form in Customer Maintenance now includes statement options for each contact. 32615

Preview Pick Slips in Order Inquiry
-----------------------------------

A new Pick Slip button on the sales order inquiry for BT, CC and SO documents allows you to view a PDF of the pick slip. 38767

View Scanned Order Documents in Order Inquiry and Invoice Inquiry
-----------------------------------------------------------------

A new Order Docs button on the Billing/Shipping tab of the order/invoice inquiry allows you to view any scanned documents attached to the order.

The storage location for such scanned documents must be defined in one of two new switches (“Order Documents Linux Directory” and “Order Documents Windows Directory”) to allow for them to be retrieved.

Scanned files must be named the sales warehouse of the order + document number.pdf (e.g. 10W012345.pdf). 38899

Inventory Adjustments Allow Reason Codes
----------------------------------------

Both Inventory Adjustment by Product (IN31) and by Log (IN35) now allow users to capture a reason for the adjustment. The reason is included in the Detailed Adjustments by Date report; this report also now includes a flag to exclude log transfers. 38421

A new table, IN1ZD, has been created to maintain these reason codes. 39341

Enter Trip Times for Each Drop on a Manifest
--------------------------------------------

A new screen (MN32) allows you to go into a manifest run after it has been processed to enter trip times for each customer delivery. 34345

Reprint Delivery Notes from Manifest
------------------------------------

When processing a manifest, if you select a previously processed run, the prompt to reprint reports now includes delivery notes. 38164

Manifest Information Visible in CM Inquiry
------------------------------------------

If a credit memo is added to a manifest, when you select it and click Inquire on the Documents tab the CM Inquiry that appears now includes a Run button and Manifest tab. 38520

“Government Approved” Mills
---------------------------

The Mills form (IN1F) now includes an “Approved” check box to identify if the mill is approved for government projects.   
The Material Origin field on a sales order Header tab now includes a “Government Approved” option. If this is selected, only logs from mills identified as Approved can be picked for that order. 38414

Global and User-Specific Timeouts
---------------------------------

logs out after a defined period of inactivity. This period is set both at the operator level as well as a global timeout. Operators are set up with a default timeout of 30 minutes, and global timeout is set to 5 minutes. If the operator is changed to a timeout value of zero, the global timeout will be used instead.

The global timeout is set in MS33 > System Timeout. Operator timeouts are set in MS32 > Security > Timeout; a new form (MS9E) allows you to change the value for multiple users at the same time.

A new inquiry form, MS61, allows you to view any operators who had their session time out, along with which function/screen they were in at the time and what the timeout value (i.e. 30 minutes) was. 38517

Increase Email Body Limit
-------------------------

You can now enter up to 2000 characters in the body of an email. 38909

Set a Default Email Body Based on Type of Entry
-----------------------------------------------

You can define a email body to be used for sales orders, quotes, and purchase orders. If a message body is not defined specific for SO, SQ, or PO, emails will use the default message body. 38992

---
