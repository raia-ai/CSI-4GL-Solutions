---
title: OE74 - Invoice Summary By Document
source: madcap.md
version: '1.0'
last_updated: '2026-02-19'
short_description: OE74 - Invoice Summary By Document
long_description: Help documentation for OE74 - Invoice Summary By Document in the 4GL system.
---

# OE74 - Invoice Summary By Document

This function produces a report containing sales value, inventory quantity and gross margin percentage for each product line by customer within a given date range.

For a detailed breakdown by tax code see the [OE7XI - Invoice/Credit Summary (Tax Breakdown)](https://4glsol.com/sm3-helpdocs/Content/Reports/rpt_oe7xi_Invoice_Credit_Note_Summary_Report.htm) report.

1. Choose Sales Order Entry » Order Entry Reports » Invoice Summary By Document \[OE74].
2. Enter or select Warehouse code (defaults to the warehouse assigned to you), including type (Inventory or Sales warehouse, and enter “C” if you want to include child warehouses.
3. &#x20;Enter or select the Territory code (defaults to all).
4. Enter or select the Type of Entry to report on: CM = credit memo, DM = debit memo, IV = invoice, defaults to all.
5. Optionally enter or select a Customer to only view invoices from that customer.
6. Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
7. Optionally, select a Payment Term to report on (defaults to all).
8. Indicate if you want to sort documents by Salesperson or Order Writer.
9. Indicate if you want to sort the report by: Document Number, Date, Operator, or View detail Lines.
10. Enter “Y” if you want credit and debit notes to reference the corresponding invoice date, otherwise enter “N”.
11. Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.

<br>
