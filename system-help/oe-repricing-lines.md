---
title: "Repricing Order Lines"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Repricing Order Lines"
long_description: "This topic provides detailed information about Repricing Order Lines in the 4GL system."
---


Repricing Order Lines
=====================

A switch (“Mass Price Adjustment Option on Reprice”) controls the functionality of the Re-Price button on a sales order, providing a streamlined, efficient way to perform mass price/unit adjustments on quotes and orders.

1. To access the Reprice window: on the Details tab of an order or quote, click the green down arrow ![](../Resources/Images/i_arrow_down.png) in the bottom right corner to display the additional buttons, then click Re-Price.

**If the switch is enabled:**

The Reprice window lists all line items on the quote or order with an option to filter them by grade. You can select all or some of the lines and then apply markup, apply margin, input selling price by variable unit and/or change unit.

2. If there are many lines, you can enter any keyword in the Filter field at the top to filter the list.
3. By default all of the lines will be selected (denoted by a “Y” in the S column). You can deselect a line by clicking the line and clicking Deselect, or click Deselect All. Then select individual lines and click Select, or Select All.
4. Once you have selected the desired lines (make sure there is a “Y” in the S column), use the other fields at the top to apply any of the following changes:
   * Enter a new selling Price in whichever unit you choose — the entered price will apply to all selected lines on the order but the actual unit on the order is not changed. In other words, you could enter a price of $2/lb but the price the customers sees could be $4/FT. Another example: for an order for 100LB/10PC if the PUM is LB and the price is $1/LB you can input $10/LB and it would change the order to $10/LB or you can input $10/PC and it would change the order to $1/LB.
   * If you want to calculate the price using the reserved quantity instead of the pricing quantity, select the flag next to the Price field. For example, if you window into the reserved window and change the pc or dimension so the reserved quantity is 20 LB, but leave the pricing quantity as 10 LB. If you then input an alternate price of $1/LB and do not check the flag, the price on the order would be $1/LB. But if you check the flag the price on the order would be $2/LB (based on 20LB x $1 / 10LB = $2)
   * Apply a Unit Change — this will change the PUM on the selected order lines while keeping the same value and quantity.
   * Apply a Markup and/or Margin  — the percentage entered in either of these fields will be applied to the replacement cost of the item on each individual line in order to arrive at a selling price. These fields allow negative values as well as percentage greater than 100%.
5. Optionally, click Processing to modify the price/value of processes on the selected lines, then click Apply to apply them to the selected lines. You can also add new codes for lot charges that would be distributed across the selected lines.
6. Click Process to apply the changes.

All price changes will affect the material portion of the price only – additional operation charges will remain unchanged.

**If the switch is not enabled:**

The Reprice window groups products that have the same dimensions (except length/width). Enter a new Price to be distributed over all the lines. You can also enter a new Processing Value that will be proportioned across M and C lines.

If an estimated time was entered against multiple processing lines in the pricing window, the summary section at the top of the repricing window will display the total estimated processing time.

---
