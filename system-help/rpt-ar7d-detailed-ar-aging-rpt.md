---
title: AR7D - Detailed AR Aging Report
source: madcap.md
version: '1.0'
last_updated: '2026-02-19'
short_description: AR7D - Detailed AR Aging Report
long_description: Help documentation for AR7D - Detailed AR Aging Report in the 4GL system.
---

# AR7D - Detailed AR Aging Report

This function produces a detailed Accounts Receivable Aging report, including customer and transaction remarks.

**NOTE:** Amounts due beyond the Aging date print in the “Unrealized AR” column of the report.\
Customer General Remarks print for all remarks entered assigned with Category AR and Print remarks is set to Y in Contact Type Maintenance (MS3P).

A subset of this report is available for export to a bank in XLS format: Accounts Receivable Aging Export \[AR7U].

1. Choose Accounts Receivable » AR Reports » Detailed AR Aging Report \[AR7D]
2. Enter or select Warehouse code (defaults to all warehouses).
3. Enter or select the Territory code (defaults to all).
4. Enter or select the Customer code (defaults to ALL).
5. Select whether to produce a Detailed or Summary report.
6. Select whether to display only those documents in the Customer AR Credit file that have a status of Open, that is, do not have monies applied against them (by default, ALL documents are shown).
7. Select the Aging Date to include (defaults to today's date).\
   Amounts due beyond the Aging date are shown in the “Unrealized AR” column.
8. Enter the number of Aging Days 1, that is, days the customer payment is overdue) (by default, 30 days).
9. Enter the number of Aging Days 2 (by default, 60 days).
10. Enter the number of Aging Days 3 (by default, 90 days).
11. Enter the number of _Aging Days 4_ (by default, 120 days).
12. Enter the number of Past Due Days a document must be in order to be included in the report (by default, all documents are included).
13. Indicate the currency type: Functional (currency assigned to warehouse) or Source (customer’s currency). See below for information about how “Source” affects Summary vs Detailed reports.
14. Select whether to age data by Invoice date (default) or Due date.
15. Select how to sort customers: by Currency, Salesperson, or Territory (default).
16. Select whether to include Inside Salesperson (default) or Outside Salesperson.
17. Select whether to include Customer Details and Remarks.\
    Note Customer Details are excluded from Excel output; for PDF output, the customer details are printed below each customer depending on your selection:
    * “S” - summary - only prints YTD Sales, Last Payment, and Last Payment Amount below each customer line.
    * “D” - prints all customer details
    * blank - does not print any customer details
18. Select the Future Applications checkbox if you want to apply any post-dated payments to the open balance.
19. Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.

## When Currency Type = “Source”

Excel output (Summary report):

* If the currency is the same as the system currency, the spreadsheet includes one line per customer. Otherwise, it will include one line for the source currency and another line for the system currency per customer.

PDF output (Summary or Detailed report):

* If the currency is the same as the system currency, the report prints one line for the totals per customer. Otherwise, it prints one line for the source currency totals and another line for the system currency totals per customer.
* The sort (by territory, by salesperson, or by currency) totals print the currency next to the heading. The totals print once if already in local currency, otherwise, it prints the local and the foreign currency.

***
