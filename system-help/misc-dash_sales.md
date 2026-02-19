---
title: "Dash Sales"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Dash Sales - 4GL Help Documentation"
long_description: "This topic provides detailed information about Dash Sales in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Salesperson / Sales Manager /  Sales Territory Dashboard Widgets
================================================================

The widgets on the Salesperson dashboard show figures for the selected salesperson; the widgets on the Sales Manager dashboard show figures for all sales people; the widgets on the Sales Territory dashboard show figures for all territories.

| Widget | Type Of Entry | Statuses | Dashboard Filters | Other Filters |
| --- | --- | --- | --- | --- |
| Top Sales Today | SO | ASG, PCK, PRA, PUR, APR, PBP, WEB, PCB, QCH, BKO, PRT, INV, END | DOCUMENT\_DATE by Current date/"Today" | Customer warehouse is blank |
| Daily Sales | SO | ASG, PCK, PRA, PUR, APR, PBP, WEB, PCB, QCH, BKO, PRT, INV, END | DOCUMENT\_DATE by Current date/"Today" | Customer warehouse is blank |
| Daily Sales All Warehouses | SO | PCK, PRA, PUR, APR, PBP, WEB, PCB, QCH, BKO, END, PRT, INV | DOCUMENT\_DATE by Current date/"Today" | Operator parent warehouse is sales parent warehouse. Customer territory is not '999'. Customer warehouse is blank |
| Open Orders | SO | ASG, PCK, CRD, PRA, PUR, APR, PBP, WEB, PCB, QCH, BKO, PRT, INV |  | Customer warehouse is blank |
| Open Quotes MTD | SQ | OPN |  | Customer warehouse is blank |
| Invoices Today | IV, CM, DM | INV, END, POS | IVHDR\_DOCUMENT\_DATE by Current date/"Today" 1 | Customer warehouse is blank |
| Invoices MTD | IV, CM, DM | INV, END, POS | IVHDR\_DOCUMENT\_DATE by Current Month | Customer warehouse is blank |
| Invoices YTD | IV, CM, DM | INV, END, POS | Date Range to exclude dates past "Today" "Before Today" + 1 | Customer warehouse is blank. Sales within current fiscal year. |
| Top 10 Customers YTD | IV, CM, DM | INV, END, POS | SALES\_VALUE, Top 10 descending records Date Range to exclude dates past "Today" "Before Today" + 1 | Customer warehouse is blank. Sales within current fiscal year. |
| Last 12 Months Sales | IV, CM, DM | INV, END, POS | IVHDR\_DOCUMENT\_DATE: Range: '(Current Month - 12)' to 'Current Month' Date Range to exclude dates past "Today" "Before Today" + 1 | Customer warehouse is blank |

Configuration


1 MS33 > BI > Invoices Today Days Back - The number of days to look back for the Invoices Today field in the Salesperson and Sales Manager dashboards. For example, if the switch is set to 0, then only invoices for today should be shown. If the switch is set to 1, then only invoices for today - 1 should be shown, etc. You may need to refresh the page after saving the switch value to see the change.

---
