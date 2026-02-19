---
title: "Log Split"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Log Split"
long_description: "Help documentation for Log Split in the 4GL system."
---

Log Split
=========

[may revise after finishing Handling Log Splits]

Manipulate inventory within the system as a result of processing. This screen is document-driven and the document must be in “Pick Status” (approved, Pick Slip printed) to be able to process log splits. Kerf1 and scrap2 calculations will also be included if set up in the system.

![](../Resources/Images/WH_log_split_1.png)

1. Scan or enter the Doc number from the pick slip.
2. Scan the Log number from the tag on the bar/bundle.
3. The first line below the Pc# reflects the order requirements; subsequent lines are drops resulting from cuts of material. If drops are to be scrapped, remove these subsequent lines.
4. The FT, IN, and Pcs in the first line default to the length required by the order. Change these if required, or change the values for the subsequent lines if you want to control the length of the drops.
5. The IUM displays the total quantity in Inventory Unit of Measure. When calculating the IUM quantity of the piece(s) that are going to be allocated to the order and/or returned back to stock, you can have one of two scenarios:
   * If the on-hand quantity of the log being split has one piece, the IUM quantity will be calculated based on actual quantity by comparing the length being produced to the original length (IUM prod = (IUM use \* Len prod) / Len use).
   * If the on-hand quantity of the log being split contains more than one piece (e.g. bundle), the IUM will be calculated using theoretical weight factors.
6. When satisfied with piece details, press F3. You are prompted to confirm the scrap tolerance.

Scrap percentage could be positive or negative. For example, the Log length of a bar is 145” in the system, but the actual Log length is 148”. If a 120” piece is sold, 28” will go back to inventory, and -3” will be costed as a negative scrap variance.

* If the actual Scrap percentage exceeds the Scrap Tolerance Allowable3, the Outside Scrap Tolerance window displays. Select the Process Action:   
  2=Edit (return to the original Log Split screen to make changes);   
  3=Abort transaction [returns to blank Log Split window, or to the top level menu?];   
  4=Usage (change quantity consumed from the original log).

![](../Resources/Images/WH_log_split_OST.png)

* If the Scrap percentage falls within the Scrap Tolerance Allowable, and the Scrap percentage is positive, the Inside Scrap Tolerance window displays. Select the Process Action:  
  1=Allocate (allocate the scrap variance to the sales order or back to the original log depending on quantity of original log; see below);  
  2=Edit (return to the original Log Split screen to make changes);   
  3=Abort transaction [returns to blank Log Split window, or to the top level menu?];

![](../Resources/Images/WH_log_split_IST.png)

Allocation:

+ If the original log has an on-hand piece count of one, the scrap quantity will be allocated to the order.
+ If the original log has an on hand piece count greater than one, scrap quantity will be allocated back to original log.

Examples:

+ If an existing log has one piece (100lbs), let’s say the system calculates the weight to be shipped on the order to be 80lbs and the weight to go back to inventory to be 18lbs for a drop. There will be a 2lb scrap quantity which will be allocated to the order. Therefore, 82lbs will be costed to the order and 18lbs will be returned to inventory as a drop.
+ If an existing log has 10 pieces at 1000lbs (one piece 100lbs), let’s say the system calculates the weight to be shipped on the order to be 80lbs and the weight to go back to inventory to be 18lbs for a drop. There will be a 2lb scrap quantity which will be allocated back to the original log. Therefore, 80lbs will be costed to the order and 18lbs will be returned to inventory as a drop - the original log will be reduced by 98lbs, leaving 902lbs in the original log.

If you split an order line that is a buyout (source vendor), any line that is not being returned to the order may have a scrap type of “Z” stamped on it.4

Configuration


1 Machine Master [PR11]

2  Scrap Policy [IN1T]

3  > Max Scrap Variance Percent Allowed During Log Split

4  > Default Scrap Type to Zero for Buyouts in Log Split

---