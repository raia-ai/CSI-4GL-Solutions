---
title: "Entering/Maintaining Purchase Order"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Entering/Maintaining Purchase Order"
long_description: "Help documentation for Entering/Maintaining Purchase Order in the 4GL system."
---


Entering/Maintaining Purchase Order
===================================

This function is used to create a purchase order or maintain a previously created purchase order. You may be restricted to what POs you can access, or whether you can create, modify or close a PO you or another user created1.

1. Choose Purchasing » Entry/Maintenance » Purchase Order Entry/Maintenance [PO31].
3. Enter or select Type Of Entry: PO = purchase order, PQ = PO quotation (typically used for intercompany inventory transfers).
4. Enter Document number or New or Duplicate.
5. The Costing window opens2 [confirm when this happens]
6. Enter or select Order Number.
7. \*Function goes in depth through many tabs

[copied from OE31/31, need to confirm field and placement] In the Product field, enter a product line or product pseudocode, or press F4 to select the product.

[necessary to note switch to skip Allocate tab? BG35327]

When you view the pricing details for a line, if you have set up vendor pricing, the base price will reflect the vendor pricing for this product if both PUMs are the same. If the PUMs are different between the inventory line and the vendor pricing, the price shown will be the converted price based on the inventory line PUM. For example, if the vendor price is $12 per foot and the PUM on the line is inches, then the resulting price will be $1 per inch.

If a product in an order does not have a current price for the vendor, the price will be zero, allowing the price to be entered manually.

When you process the PO, if a contact is specified to receive an email (on the Contacts tab), you can edit the default subject and message for this order.

3.17 BG 38409 - if PO has been processed and you later add lines to the PO, the new lines will not be added to the manifest until you reprocess the PO (if MS32>PO Re-Approval is required). If PO Re-Approval is not required, the new lines will be added to the manifest when you exit the PO. If the pick-up date is updated, the PO is moved to a new manifest (again, depending on the PO Re-Approval setting).

3.19 BG 35941 - user may be able to override the default buying qty (“MS32>PO> Allow Override PO Bundle Quantity”); if not set, the quantity must be a multiple of the default bundle quantity defined for the vendor and product (in PO17). If you try to change this value,  will round the buying quantity that you entered to the nearest multiple of the bundle quantity.

3.20 BG 38488 - An Excel Export button has been added to the PO Inquiry and PO entry Details tab. This exports the PO lines in the same format as the Excel Import template (PO3D) with the exception of Rebate columns after the remark columns.

3.23 BG 40033 - If you change the pickup date on the Header tab, you are asked if you want to update the delivery date on all lines.

Configuration


1 MS32 > Options > Purchase Order > Restrict PO Access

2  > Pop-up PO Costing Window

---
