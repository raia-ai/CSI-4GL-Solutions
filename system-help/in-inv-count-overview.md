---
title: "Inventory Count - Workflow"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Inventory Count - Workflow"
long_description: "Help documentation for Inventory Count - Workflow in the 4GL system."
---


Inventory Count - Workflow
==========================

The following are the steps for performing a physical inventory count.

1. Review the pre-count checklist and  configuration considerations.
2. Run/download the Stock List By Log/Product/Grade report [IN71]. Keep this as a permanent file, it will be used for balancing after the inventory count is posted.
3. Schedule the count [IN5B]. A count may be initialized for one or all product lines.

Once a physical inventory count is scheduled, ALL inventory logs are reduced to zero (for the selected product lines); entering
the count tags puts inventory back into stock. DO NOT post your inventory until all inventory
count tags are entered.  
You can still enter sales orders or purchase orders for the product lines being counted, but cannot post a PO/OP/IP receipt, confirm or create packing slips until the inventory count is posted.

4. Perform the physical count and add inventory count tags:
   * Using the handheld Physical Inventory function, or
   * If you are not using  handheld devices, download this sample Excel spreadsheet for counting inventory on paper.

Inventory counts are completed more efficiently if performed in teams of two: one person to count and the other to record (on paper or via handheld). After the physical count is complete, staff should walk the warehouse floor to ensure all stock has been counted.

5. If your count was recorded on paper, make sure you have all the sheets (check the page numbers), and then manually enter the counts in  [IN5E].

A user must have appropriate access permission1 to create new logs when entering inventory count tickets.

6. Generate the following reports (print or output to Excel) to aid in reconciliation. These reports may be regenerated numerous times; the final outputs should be kept as permanent records for audit purposes.
   * Inventory Count Variance Report [IN5G]. This lists all tags that have a variance (percent, quantity or $ value) greater than the selected acceptable variance.

   This report may be run by Product Line. If you know all tickets are in for a product line, you do not have to wait until the full count is finished – run a Variance report for that product line to review variances.

   * Inventory Count Tag Report [IN5K] for all Used/Voided tags (U). Verify voided tags are indeed voided.
   * Inventory Count Tag Report for all Missing (M) tags. This is important if you did not use handhelds to count. Verify missing tags do not have data from your count sheets.
7. Once the physical inventory reconciliation is complete, use the Inventory Count Update [IN5I] to post the inventory.
8. After posting your inventory, run/download IN71 before normal business activity starts on
   your system. Keep this report/file as a permanent record.  
   Inventory Value prior to count (IN71) +/- Variance value from Inventory count (IN5G) =
   Inventory value after count (IN71)

Configuration


1 MS32 > [operator] > Options > Manager (this permission is not used for any other purpose in )

Refer to the pre-count checklist for additional  configuration considerations.

---
