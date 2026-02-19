---
title: "Oe Log Split"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Oe Log Split - 4GL Help Documentation"
long_description: "This topic provides detailed information about Oe Log Split in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Handling Log Splits
===================

You may need to cut a product into shorter lengths or smaller pieces. This log splitting does not change the value of the inventory—any remnants or scrap produced from the cutting is returned to inventory: it could be allocated to the order, back to the log, to a scrap code, to remnants, etc. If you are starting with a single-piece log, the remnant is returned to the same log number; if you are starting with a multi-piece log, remnant(s) are assigned new log numbers.

When picking logs on the Picking Confirmation [OE41] screen, you can either split a log and add the required length to the order, or split a log that has already been assigned to the order—in effect this removes the log, splits it, and then allocates the cut piece.

If you split an order line that is a buyout (source vendor), any line that is not being returned to the order may have a scrap type of “Z” stamped on it.1

Log splitting can also be done directly from the  Inventory Control menu (IN6C), or from the handheld. [mention other Log Split-related menu items]

When you split logs, you will be asked if you want to define dog legs.

From the Picking Confirmation
-----------------------------

* If the log you are splitting has not already been picked for the order:
  + Select the order line that you are picking, and click Split Log.
  + Enter the Log No (if known) or click … to retrieve it, then click Save.
  + Process the log split as described below. The log is added to the Inventory Logs section for the order line.
* If the log is already listed in the Inventory Logs section for the order line (Picked quantity=0):
  + Select the Inventory Log line and click Split This Log.
  + Process the log split as described below. The newly created log (with a new log number) is added to the Inventory Logs section for the order line.

In the Split Log Screen
-----------------------

When you open the Log Split screen, one or more pieces of the log are split to obtain the length and quantity ordered, and the remnants (“drops”) are listed. This initial default calculation is performed based on actual or theoretical weight and is set for each product line.2

In the example below, two pieces from the log were used to obtain the three 5’ lengths ordered. The process resulted in five pieces produced:

* One piece was cut twice, resulting in two of the 5’ lengths for the order and a remnant of 2’11-3/4”.
* One piece was cut once, resulting in the third 5’ length for the order and a remnant of 7’11-7/8”. [make sure narrative matches screenshot]

The calculations are based on the original length of the log, or the average length in the case of random length pieces. In our example, the log is 12-14’, so the calculations are based on 13’. So why is the first remnant not 3’ (after the two 5’ lengths were cut)? This is due to the kerf associated with the machine3 used to cut this product. In this example, the kerf accounts for 1/8” per cut. There were two cuts in the first piece, so the remnant lost 1/4”, but there was only one cut in the second piece, so its remnant lost only 1/8”.

![](../Resources/Images/inv_log_split.png)

### What Can You Do Here?

* Optionally adjust the scrap revaluation for a remnant (see Scrap Calculations below).
* Press F4 in the Dtl field for a remnant to define the details for the new log that will be created for the remnant; this information defaults to that of the original log.
* If using random length log pieces, click Used to enter the exact length of the pieces you are cutting.
* Decide what to do with the Scrap Qty:
  + To allocate it to the order or to the original log (depending on the settings for this product line2), click Allocate.   
    If the product line is set to allocate to the order, the Quantity in the order line will change by the Scrap Qty amount.   
    If set to allocate to the original log, the Used Qty will change by the Scrap Qty amount.
  + If the Scrap Qty is within your configured variance4, you can leave it to be assigned to the scrap code associated with the product line5.
* If the original log was a single piece, the Log check box will be selected, indicating that the remnants will be returned to the same log number. You can deselect this check box, in which case the remnant will be assigned a new log number. This check box is not available if the original log comprised multiple pieces.
* Click Process.

### Scrap Calculations

The Scrap Qty is the difference between the Used Qty and the Prod Qty.

A remnant may be automatically revalued by a percentage or a unit cost. The first remnant in our example is going to be revalued by a percentage, because it is a less-than-desirable length, but the second remnant is not, because it is large enough be considered sellable at its current length. This is determined by the Scrap Policy for the product line.6

If a remnant is going to be revalued, double-click on the P to view the percentage and the difference in value which is automatically allocated to the order.

You can remove the R for a remnant, or add an R and percentage to revalue a remnant that is not automatically defined by the Scrap Policy.

Configuration


1  > Default Scrap Type to Zero for Buyouts in Log Split

2 ![](../Resources/Images/i_arrow_down.png) > Log Split

3 Machine Master [PR11] > kerf parameters for selected machine

4  > Max Scrap Variance Percent Allowed During Log Split

5 ![](../Resources/Images/i_arrow_down.png) > Scraps > Scrap Product

6 Scrap Policy Maintenance [IN1T] > for various combinations of parameters (e.g. Gauge, Width, Length), define whether the scrap remnant should be revalued, allocated to the order, tracked, or scrapped at zero

---
