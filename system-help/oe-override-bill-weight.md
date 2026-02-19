---
title: "Overriding the Billing Weight of an Order Line"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Overriding the Billing Weight of an Order Line"
long_description: "Help documentation for Overriding the Billing Weight of an Order Line in the 4GL system."
---

Overriding the Billing Weight of an Order Line
==============================================

There may be occasions when you want to override the billing dimensions of a piece that you will be cutting.

For example:

* You have an order for a 10M (100kg) piece but you are cutting from a 13.5M (135kg) piece and you want to charge the customer for 13.5M.
* You would enter the order for 10M and then override the billing dimensions to 13.5M.
* would “charge out” 135kg but the customer would see a billing weight of 100kg (if your pricing unit was kg).
* If the selling price is $2/kg, the selling value would be calculated to be $270 ($2 \* 135kg) and the price would be back-calculated to be $2.70 ($270 / 100kg). The invoice would then show 100kg \* $2.7/kg = $270.

The following switches must be set:

* > Override IUMs in Order Entry - set to “Y” to be able to override the dimensions which will, in turn, calculate the billing weight
* IN16 > Warehouse > Skip Onhand Reserves - must be unselected in order to access the reserve field

To override the billing weight of an order line:

When adding a line item to an order, on the Product tab, click ![](../Resources/Images/i_wrench.png) beside the On Hand Reserve Qty to view the calculated weight and override it as necessary. Note that the calculated weight includes kerf and squaring allowance if set up against the primary process.

---