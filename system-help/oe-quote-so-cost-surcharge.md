---
title: "Adding a Non-Inventory Charge"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Adding a Non-Inventory Charge"
long_description: "Help documentation for Adding a Non-Inventory Charge in the 4GL system."
---


Adding a Non-Inventory Charge
=============================

On the Details tab for a quote or sales order you can add a revenue cost or surcharge that is not related to inventory.

The charge may be added as a line item on the order, or apportioned to existing inventory line items so that it is hidden from the customer.

A default charge, e.g. a freight charge, may be set up for the customer, associated with the Ship Via code on the Billing tab. This charge may be added to the Details tab by default (but can be removed), or it may be mandatory and not removable.

Adding a Charge as a Line Item
------------------------------

A cost allows you to enter the flat $ amount. A surcharge is calculated based on a unit of measure, quantity, and unit price. Both of these charge types are added to the quote/order at 100% margin.

1. Click Add Cost.
2. Enter the Type (“C” for a cost, or “S” for a surcharge), then select the specific Cost code which will associate the charge with a G/L account [xref to OE16]. The Description defaults to the one associated with the selected Cost code, but you can edit it for this charge if required.
3. Enter any Remarks as required.
4. If you are entering a C line (cost), enter the amount of the charge in the Sales Value field.

   If you are entering an S line (surcharge), select the PUM (Pricing Unit of Measure), Pricing Qty, and Sales Price (per unit). For example, you may want to apply a surcharge based on the number of pounds ordered. The Sales Value is calculated automatically.
5. Click Save.

Adding a Hidden Charge
----------------------

You can add a cost or surcharge that will be added to existing inventory line items. These charges may be a calculated cost based on the weight of the inventory line item, or a flat Lot price that will be split amongst the line items based on their proportion (by weight) of the entire order.

1. Click Cst/Rev.
2. Click Add.
3. Select a Cost code. These codes are associated with a Type of C (cost), S (surcharge) or B (both), which determines which fields are enabled.
4. If you are entering a C line (cost), select the first PUM (Pricing Unit of Measure) and enter the Cost Price.

   If you are entering an S line (surcharge), select the second PUM and the Revenue Price.

   If you are entering a B line (both), you may enter all fields.

   The PUM must be a unit of weight or “Lot”.
5. Click Close. Costs are added to the Cost Price of each inventory line item, while Surcharges are added to the Sales Price of each inventory line item.

To reverse a cost or revenue charge, open it and change the amount to zero.

---
