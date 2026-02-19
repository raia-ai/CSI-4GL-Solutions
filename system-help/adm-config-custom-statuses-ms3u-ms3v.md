---
title: "Using Custom Status Codes"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Using Custom Status Codes"
long_description: "Help documentation for Using Custom Status Codes in the 4GL system."
---

Using Custom Status Codes
=========================

In addition to the system statuses, you can create your own statuses that can be applied to any document. For example, you may want to create a status code to identify that the order has been shipped (or is on the truck for delivery) but not yet invoiced. You can create an unlimited number of status codes; some customers will change the status code when the order is in the process of being picked, when the PO has been issued to a vendor or when a sales order confirmation has been sent to a customer.

There are two forms for Document Status Maintenance:

* MS39 contains the system status codes that are assigned automatically at different stages, such as ASG when a sales order is first entered, then PCK when the order goes to picking confirmation, etc. System status codes are shown in Document Tracking with a type of “SYS”. These status codes should not be edited other than to enter an eCom Description if you are using the customer portal.
* MS3U is where you can create user-defined status codes, as described below. Custom status codes are never written to a document automatically from , but can be applied to a document in MS3V or WF1D. Custom status codes are shown in Document Tracking with a type of “USR”.

Creating a Custom Status
------------------------

1. Choose Administration » Administration » User Def Doc Status Maintenance [MS3U].
2. Enter a Status code and Description (Location in System is an optional internal reference field). Custom status codes must be unique and not exist in the system status table (MS39).

![](../../Resources/Images/ADM_doc_status1.png)

Assigning a Custom Status to a Document
---------------------------------------

1. Choose Administration » Administration » Document Status Scanning [MS3V].
2. Enter the Doc Num, e.g. for a sales order document.
3. Select the Status code.

![](../../Resources/Images/ADMIN_admin_doc_status2.png)

You can also update a document’s status with a wireless handheld scanner.

---