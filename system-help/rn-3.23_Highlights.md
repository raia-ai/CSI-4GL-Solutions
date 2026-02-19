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

Copy Voucher
------------

A Copy button has been added to the Vendor Invoice Entry (AP21B) search page. Click **Copy** and select an existing voucher to copy. This will only work for vouchers with no accrual sub-accounts. 39813

Filter Count Initialization by Bin Location
-------------------------------------------

The Inventory Count Initialization function (IN5B) includes a new option to Count By Location. After selecting a location type, you can select the locations within that type. The inventory count pre-stock report will only show logs that belong to the product lines and bin location selected. 40105

Changes to IN16 Warehouse Options, New Buyout Allocation Options
----------------------------------------------------------------

The warehouse options for a product line have been organized into groups (Inventory, Receiving, Order Entry Navigation, Pricing, Picking & Reserving) to make the options easier to locate. New Receiving options allow you to enable buyout-specific allocation on receiving, and to set the buyout allocation method (full piece, none, piece, quantity). 40318

Duplicate a Receipt to Generate Lines and Logs for a Return
-----------------------------------------------------------

On the Details tab of a PO receipt (PO44), the Select checkbox has been changed to enter “Y” to select all receipt lines, “D” to duplicate, or leave blank. 40129

Display Open Balance on Invoice
-------------------------------

A new form option for invoices (Display Open Balance) will print the open balance on the second last line in the bottom left of an invoice. The open balance is the sales order total minus the sum of all POS payments made to the sales order. 39871

Convert IN7YI Output to Excel Import Format
-------------------------------------------

A new utility (PO3F) will convert the Excel output of the Inventory Sales Usage report, where you have entered order quantities and prices, into another Excel file formatted for import into a purchase order. 39811

---