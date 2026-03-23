---
title: OE77 - Sales Order/Quote Report
source: madcap.md
version: '1.0'
last_updated: '2026-02-19'
short_description: OE77 - Sales Order/Quote Report
long_description: Help documentation for OE77 - Sales Order/Quote Report in the 4GL system.
---

# OE77 - Sales Order/Quote Report

This report lists sales orders and/or quotes.

1. Choose Sales Order Entry » Order Entry Reports » Sales Order/Quote Report \[OE77].
2. Enter or select the Warehouse code plus _Child Warehouse_ indicator (defaults to warehouse assigned to operator).
3. Select the Order Types to include on the report:  Sales orders (default), Quotes, or All.
4. Select which order statuses to include:  Open, Released, Shipped, or All orders.
5. Specify how to group data: by order Writer, Salesperson, or Invoice number.
6. Indicate if you want to Group by Currency on the orders.
7. In the Operator field, select a salesperson to report on, or leave “ALL”. If you did not select “ALL” you can select Additional Operators.
8. Indicate whether you want to view data for the Customer Salesperson (on the customer file); or leave blank to reference the salesperson on the invoice.
9. Indicate if the report should use the Order date or the Expected Ship date.
10. Enter or select a Customer (by default, all are selected).
11. Indicate if credit and debit notes should reference their corresponding invoice date, and if invoices should reference the sales order date.
12. Indicate if invoices should reference the sales order date (i.e. only show orders generated in the specified date range).
13. Indicate if you want to only include sales adjustments in extras for margin calculation.
14. Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
15. Indicate if you want to only generate a Summary report.
16. Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
