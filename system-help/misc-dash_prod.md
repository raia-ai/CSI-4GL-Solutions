---
title: "Dash Prod"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Dash Prod - 4GL Help Documentation"
long_description: "This topic provides detailed information about Dash Prod in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Production Dashboard Widgets
============================

Main Tab
--------

| Widget | Type Of Entry | Statuses | Dashboard Filters | Other |
| --- | --- | --- | --- | --- |
| Processes | SO, BT, CC | PCK,PBP | Drill Down Screen Top-left Box Status: PBP, PCK "Scheduling for" Top-right box: Late column Weight: WEIGHT\_LATE + WEIGHT\_LATER Pieces: PIECES\_LATE + PIECES\_LATER Line Items: OEDTL\_DATE\_REQUESTED: Range: Before Today | Current Day Est. Time: OEDTL\_DATE\_REQUESTED: Range: Before Today | Current Day | PR41B |
| Open Orders | SO, BT, CC | PCK,PBP |  | PR41B |
| Sales | IV, CM, DM | INV, END, POS | SalesByDetailAll Default View - Last 12 Months IVHDR\_DOCUMENT\_DATE: Range: (Current Month-12) to (Current Month) SalesByDetailLastFiscal - for "Last Year" SalesBYDetailThisFiscal - for "Previous Month, Year to Date, Month to Date & Today" | Customer warehouse is blank. Inventory lines only Stock warehouse |

Details Tab
-----------

| Widget | Type Of Entry | Statuses | Dashboard Filters | Other |
| --- | --- | --- | --- | --- |
| Process | SO, BT, CC | PCK,PBP | Drill Down Screen Top-left Box Status: PBP, PCK "Scheduling for" Top-right box: Late column Weight: WEIGHT\_LATE + WEIGHT\_LATER Pieces: PIECES\_LATE + PIECES\_LATER Line Items: OEDTL\_DATE\_REQUESTED: Range: Before Today | Current Day Est. Time: OEDTL\_DATE\_REQUESTED: Range: Before Today | Current Day | PR41B |
| Schedule | SO, BT, CC | PCK,PBP |  | PR41B |
| Orders | SO, BT, CC | PCK,PBP |  | PR41B |

---
