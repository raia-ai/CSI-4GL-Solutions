---
title: "Rpt In76 Detailed Adjustment Report"
source: "madcap.md"
tags: ["4GL", "REPORTS", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rpt In76 Detailed Adjustment Report - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rpt In76 Detailed Adjustment Report in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the REPORTS module."
---


IN76 - Detailed Adjustments By Date
===================================

This function is used to produce Detailed Adjustment Report by Date range, totaled by adjustment.

1. Choose Inventory Control » Inventory Reports » Detailed Adjustments by Date [IN76].
2. If you run the report for “All” warehouses, the output depends on the setting of the “Change Report Warehouse” operator option (in MS32):  
   - If set to “A”, then the report will return results from all warehouses  
   - If set to “Y”, then the report will return results from warehouses that share the same division as the operator’s warehouse.
3. Enter the Start and End  dates that goods were received (both default to today's date).
4. Indicate if you want to Include Average Cost Adjustments: enter Yes, Only average cost adjustments, or leave blank for no.
5. Indicate if you want to Exclude Log Transfers.

Output
------

|  |  |  |  |
| --- | --- | --- | --- |
| column heading | needs description? (if yes, populate one of the next two columns only) | glossary description | report-specific description |
| Log No |  |  |  |
| Description |  |  |  |
| Heat |  |  |  |
| Weight |  |  |  |
| Pieces |  |  |  |
| Quantity |  |  |  |
| Price |  |  |  |
| Value |  |  |  |

---
