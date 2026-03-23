---
title: OE73 - Delivery Note
source: madcap.md
version: '1.0'
last_updated: '2026-02-19'
short_description: OE73 - Delivery Note
long_description: Help documentation for OE73 - Delivery Note in the 4GL system.
---

# OE73 - Delivery Note

This function reprints/faxes/emails a delivery note. “\*\*REPRINT\*\* will print below the document number. You will not be able to reprint delivery notes with a status of Closed.

1. Choose Sales Order Entry » Order Entry Reprints » Delivery Note \[OE73].
2. Enter or select the Warehouse code (defaults to the warehouse assigned to you).
3. Select the Type Of Entryand enter or select the Document number you want to reprint.
4. Indicate if a mill report (material test report/MTR) is required: Yes (include the original MTR), Overlayed (include the original with company header overlaid), Sys (system-generated MTR from company, not mill), Both (original and system-generated), or blank for no. See also [MTR Delivery Options](https://4glsol.com/sm3-helpdocs/Content/OrderEntry/MTR_delivery_options.htm).
5. Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
