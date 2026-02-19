---
title: "Rn 3.20 Highlights"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rn 3.20 Highlights - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rn 3.20 Highlights in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Highlights
==========

38802

EDI Processing Between  Customers
---------------------------------

Fields have been added to the Vendor Maintenance, Warehouse options, and Customer Maintenance to allow clients to record their own and their vendors’/customers’ EDI Mailbox IDs. This automates the process of sending a PO to a vendor and creating the sales order. 38514

POA (purchase order acknowledgement) and ASN (advanced shipment notification) EDI transaction types are now catered for, which completes the loop of purchasing/selling between  customers. 39034

See Electronic Data Interchange (EDI).

Dashboards Introduced
---------------------

The Dashboards menu was introduced in this release, including the following dashboards: Salesperson, Sales Manager, Customer, and Production. See About the Dashboards.

Export to Excel from PO31 and PO61
----------------------------------

An Excel Export button has been added to the PO Inquiry and PO entry Details tab. This exports the PO lines in the same format as the Excel Import template (PO3D) with the exception of Rebate columns after the remark columns. 38488

PO Delivery Date Change task for OP docs
----------------------------------------

If a PO is reserved against a sales and OP order and the delivery date is later changed, a PO Delivery Date Change task is created for both the sales order and OP document. 39052

Preview Added to IP/OP Inquiry
------------------------------

A Preview button has been added to the IP/OP by Order Number inquiry. This prints the IP/OP document the same as PR75/PP76. 38889

Pay Partial OP Accruals
-----------------------

You can now pay partial OP accruals. Once the voucher has been processed and updated, the remainder of the receipt can be selected and paid on a new voucher. 38494

Holiday Schedule
----------------

You can now define your holiday schedule so that orders take into account holidays in addition to weekends when calculating the Requested Date, order status, etc. 38913  See Recording Holidays

Document Tracking for PO Receipts
---------------------------------

Document tracking has been added for RC, BR, RR, and RP documents. 38702

MTR Archive Folder
------------------

New switches (“MTR Archive Folder (Mounted)” and “MTR Archive Folder (Windows)”) allow you to set up an archive folder so that you can move older MTRs out of the main MTR folder to keep the main folder at a manageable size. When retrieving an MTR,  will look first in the main folder, then in the archive folder if the file is not found in the main folder. 39001 See MTR Storage Location(s)

---
