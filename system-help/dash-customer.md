---
title: "Customer Dashboard Widgets"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Customer Dashboard Widgets"
long_description: "Help documentation for Customer Dashboard Widgets in the 4GL system."
---


Customer Dashboard Widgets
==========================

Main Tab
--------

| Widget | Type Of Entry | Statuses | Dashboard Filters | Other |
| --- | --- | --- | --- | --- |
| Open Quotes MTD | SQ | OPN | DOCUMENT\_DATE: Current Month | Customer warehouse is blank |
| Open Orders | SO | PCK, PRA, PUR, APR, PBP, WEB, PCB, QCH, BKO | DOCUMENT\_DATE for Overdue label: Orders before Current Day | Customer territory is not '999' Customer warehouse is blank |
| Invoices |  |  |  | Customer AR Inquiry Sales Window |
| Sales By Product Line | IV, CM, DM | INV, END, POS | IVHDR\_DOCUMENT\_DATE: "Month to Date": Current Month | Customer warehouse is blank. Inventory lines only. Sales within current fiscal year |
| Sales By Previous 36 Months | IV, CM, DM | INV, END, POS | Every Table and Chart in this section IVHDR\_DOCUMENT\_DATE: Range: (Current Month-36) to Current Month | Customer warehouse is blank. Inventory lines only |
|  |  |  |  |  |
|  |  |  |  |  |
| 2nd Tab - Open Quotes | SQ | OPN |  | Customer warehouse is blank |
| 2nd Tab - Open Orders | SO | PCK, PRA, PUR, APR, PBP, WEB, PCB, QCH, BKO |  | Customer territory is not '999' Customer warehouse is blank |

Open Quotes, Orders & Invoices Tab
----------------------------------

| Widget | Type Of Entry | Statuses | Dashboard Filters | Other |
| --- | --- | --- | --- | --- |
| Open Quotes | SQ | OPN |  | Customer warehouse is blank |
| Open Orders | SO | PCK, PRA, PUR, APR, PBP, WEB, PCB, QCH, BKO |  | Customer territory is not '999' Customer warehouse is blank |
| Invoices | IV, CM, DM | INV, END, POS |  | Customer warehouse is blank |

---
