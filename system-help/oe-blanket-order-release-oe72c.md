---
title: "Blanket Order Pickslip Release"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Blanket Order Pickslip Release"
long_description: "Help documentation for Blanket Order Pickslip Release in the 4GL system."
---

Blanket Order Pickslip Release
==============================

When entering a blanket order, add a note or remark on the order to tell the warehouse to ignore the pick slip that will print for the entire order when it is processed.

When you are ready to send partial quantities to the customer, use the Blanket Order Pick Slip Release to create a pick slip for the partial quantity.

1. Choose Sales Order Entry » SO Entry/Maintenance » Blanket Order Pickslip Release [OE72C].
2. Retrieve the sales order from the list of those in PCK or PCB status.
3. Enter the Required Date (in the field at the top) to be applied to all lines. Once you press Enter and the order lines are displayed, you can change the Req Date for order lines individually, or use the Required Date button to change the header date (and optionally apply the new date to all order lines).
4. For each order line, as applicable, enter the Release Pcs and/or Release Qty that you will be sending at this time. If you want to start over, you can click Clear to clear all Release fields.
5. When you are finished, press F3 to exit the screen. You have two options:
   * **H**old – Exit the screen without printing a pick slip; any release amounts entered are retained.
   * **P**rocess – Print the pick slip according to the printer settings in IN19. The pick slip will only print order lines with release quantity or pieces. The quantity shown on the pick slip for each line will be the release quantity and/or pieces.

The next time you retrieve the same sales order in this screen the Open Pcs and Open Qty will reflect the updated amounts.

---