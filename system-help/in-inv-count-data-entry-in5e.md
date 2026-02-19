---
title: "Entering Inventory Count Data"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Entering Inventory Count Data"
long_description: "Help documentation for Entering Inventory Count Data in the 4GL system."
---


Entering Inventory Count Data
=============================

This function is used to input inventory count numbers into  if the count was not completed using the handheld device.

Make sure you have received all the count sheets (check the page numbers).

1. Choose Inventory Control » Physical Inventory » Inventory Count Data Entry [IN5E].
2. If using inventory tag numbers, enter or select a Tag Number that is within the range specified in IN5B.
3. Enter or select the Log Number (do not need “L” + leading zeroes), or enter “N” to create a new log (if you have appropriate access permission1), or enter “D” to create a new log with duplicate specifications from an existing log.
4. Optionally, record the information about the log (Spec/Size, Product, Case Number, Heat No). A new count ticket must be entered for each change of dimension. If you selected an existing log, the system will jump to the Bin Loc field but you can go back and edit these fields.
5. Enter or select the Bin Location.
6. Optionally enter any Remarks or Physical information.
7. If you selected an existing log, the first set of IUM Qty, Pieces, and Weight display the values on hand when the inventory was created .  
   In the second set of these fields, enter the IUM Qty in the current count. The Pieces will populate based on theoretical values (using Spec/Size and IUM Qty); you can override this number if necessary.
8. Optionally (and if available), click into More Options to view pricing information and change the average cost for the selected log.
9. Optionally, click Label to print a label for this log.
10. Enter “C” to confirm your entry or “V” to void the transaction.

Configuration


1 MS32 > [operator] > Options > Manager (this permission is not used for any other purpose in )

Refer to the Configuration section in the inventory count checklist for additional options.

---
