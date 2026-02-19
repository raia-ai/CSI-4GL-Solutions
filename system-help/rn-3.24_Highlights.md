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

New Inquiry for Quotes
----------------------

The new Quotes by Customer by Product inquiry includes the same fields as the Sales by Customer by Product, but for quotes only. 39775

OE61 Shows Last Custom Status
-----------------------------

The Sales Order inquiry shows the latest status on the sales order, including a custom status. However, if the header status is “DLV”, it will display the status of the latest invoice instead. 40390

Utility to Change Sales Warehouse on an Order
---------------------------------------------

A new utility, Change Sales Warehouse on an Order, allows you to update the sales warehouse on an existing order.Only "ASG", "PCK", and "PCB" orders with no invoices can be selected, and only transactional warehouses allowed for your operator security in MS32 can be selected. 40385

New Function to Change Bin Location for Multiple Logs
-----------------------------------------------------

A new function allows for bulk bin location change for multiple logs in a bin. 40517

Ability to Deactivate Bin Locations
-----------------------------------

The bin location window includes a new column to mark a location as Inactive. These locations will be excluded from all areas of SM3 where you can choose a bin location. 40492

IN73 Can Be Exported to Excel
-----------------------------

The Adjustment Authorization report can now be output to Excel format. 40554

Auto-Receive RP Document, Clone Receipt Logs
--------------------------------------------

* When creating a pre-receipt, a new processing option, “O” (one-step), allows you to process the document and automatically create and receive the receipt. “O” is not available for “RC” documents, only “RP” documents. 40536
* The Duplicate button on the receipt log window has been enhanced with additional parameters: 40537
  + MTR filename and case: duplicates the last log with the new MTR file name and case number.
  + Increment Case checkbox: duplicates the last log with a new case number that has been incremented by 1. If Copies is set to more than 1, the case number is incremented for each duplicated log.
  + Pieces
  + Length and Width fields are enabled if the dimensions exist for the product shape and the dimension is not fixed on the product. Fractional fields are enabled if the fractional dimension is set for the product line (e.g. if the length is in FT for the product line and the fractional UOM is in inches for the product line, the fractional field is enabled for inches).
  + BUM Quantity is updated according to the new pieces, length and width, but is editable.

IP from PR41B Allows Multiple Raw Materials
-------------------------------------------

When creating an IP from the Production Schedule, you can now select multiple raw material lines and create many-to-many or many-to-one sets. 40053

---
