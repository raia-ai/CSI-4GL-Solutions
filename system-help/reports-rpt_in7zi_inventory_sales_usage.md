---
title: "Rpt In7Zi Inventory Sales Usage"
source: "madcap.md"
tags: ["4GL", "REPORTS", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rpt In7Zi Inventory Sales Usage - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rpt In7Zi Inventory Sales Usage in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the REPORTS module."
---
IN7ZI - Inventory Sales Usage Report
====================================

This report shows inventory stock usage (including open sales orders), by product code, displaying last 12 months of sales history. It also displays Min/Max quantities (as maintained in PO19)

The Available Quantity shown in the report is the on-hand minus the sum of the open quantity processed and unprocessed. Unprocessed refers to commit-out quantity that is not picked on logs yet, while any logs that
are picked on the order are counted as processed and deducted from unprocessed.

If you output to Excel, you can enter order quantities and prices into the resulting spreadsheet, then run PO3F to convert it into another Excel file formatted for import into a purchase order.

1. Choose Purchasing » PO Reports » Inventory Sales Usage Report [IN7ZI].
3. Enter or select the Product Line or enter “ALL” (entering “ALL” disables the spec and dimension filters).
4. Optionally, further refine the report by entering the Grade, STD or Finish (or select “ALL”), or the Diameter or Length.
5. Optionally enter an option to Group Compatible:
   * L or B for long products: cut and fixed products are combined and only the fixed is shown
   * F or B for square/flat products: cut and fixed products are combined and only the fixed is shown.
   * If there are multiple fixed, the cut is combined with the first fixed product.
   * Leave blank for no grouping.
6. Enter the Date the report should include data up to; it will include open work orders and invoices 12 months prior to this date.

---
