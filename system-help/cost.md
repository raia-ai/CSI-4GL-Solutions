---
title: "Changing Average Cost"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Changing Average Cost"
long_description: "Help documentation for Changing Average Cost in the 4GL system."
---

Changing Average Cost
=====================

This can be done either through adjustment journal or through an Excel export.

Option 1 – When Only a Few Items Need to Be Changed
---------------------------------------------------

1. Choose Inventory Control » Inventory Adjustment » Average Cost Price Adjustment [IN37].
2. When you enter the product code,  will show the average cost, then prompt you to enter the new average cost.
3. Either approve the adjustment in Adjustment Authorization (IN32), or if the adjustment approval has been set as a task, it can be approved in the Task Manager.

Option 2 – When You Want to Revalue by Product Line
---------------------------------------------------

This option should be done after hours as you do not want any inventory movements between the export and import.

1. Choose Inventory Control » Inventory Adjustment » Average Cost Revaluation Export [IN3C].
2. Select one or more product lines to export.
3. This will create a spreadsheet with columns for the Product, Description, Onhand Qty, IUM, Old Avg Cost, CUM, and New Avg Cost.

   The spreadsheet includes an Instructions worksheet.
4. Open the spreadsheet and enter the New Avg Cost for the products as applicable.

   If you leave the New Avg Cost field blank,  will assume you want the cost to be zero. If you want to keep the cost the same, either delete the line from the spreadsheet, or copy the Old Avg Cost into the New Avg Cost field.
5. When you are finished, save the spreadsheet as a Text (Tab delimited) file.
6. To import it back into , choose Inventory Control » Inventory Adjustment » Average Cost Revaluation Import [IN3D].
7. You will be prompted to confirm. This will create a journal entry in IN37; you still have the option to review and modify if needed before you update.
8. Approve the journal entry in Adjustment Authorization (IN32) or the Task Manager.

---