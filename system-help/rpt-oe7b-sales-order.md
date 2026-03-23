---
title: OE7B - Sales Order
source: madcap.md
version: '1.0'
last_updated: '2026-02-19'
short_description: OE7B - Sales Order
long_description: Help documentation for OE7B - Sales Order in the 4GL system.
---

# OE7B - Sales Order

This function reprints/fax/emails a branch transfer (BT), processing purchase order (PP), production order (PR), or sales order (SO).

If you have alternate headings [defined](https://4glsol.com/sm3-helpdocs/Content/Admin/Config/FM_FL_Util/FM_OE_Alternate_Form_Headings_OE1Q.htm), use OE7BB instead to reprint the sales order; OE7BB is the same as OE7B but includes an additional field to select the alternate heading to use.

1. Choose Sales Order Entry » Order Entry Reprints » Sales Order \[OE7B].
2. Enter or select the Warehouse code (defaults to the warehouse assigned to you).
3. The Entry Type defaults to SO, but you can change this if required to branch transfer (BT), processing purchase order (PP), or production order (PR.
4. Enter or select the Document you want to reprint (the list is filtered according to the Entry Type selected).
5. Indicate if a mill report (material test report/MTR) is required: Yes (include the original MTR), Overlayed (include the original with company header overlaid), Sys (system-generated MTR from company, not mill), Both (original and system-generated), or blank for no. See also [MTR Delivery Options](https://4glsol.com/sm3-helpdocs/Content/OrderEntry/MTR_delivery_options.htm).
6. Indicate if you want to include the word “Reprint” in the top right corner of the reprint.
7. Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.

<br>
