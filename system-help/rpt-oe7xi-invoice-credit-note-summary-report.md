---
title: "OE7XI - Invoice/Credit Summary (Tax Breakdown)"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "OE7XI - Invoice/Credit Summary (Tax Breakdown)"
long_description: "Help documentation for OE7XI - Invoice/Credit Summary (Tax Breakdown) in the 4GL system."
---


OE7XI - Invoice/Credit Summary (Tax Breakdown)
==============================================

This function prints a summary report of taxable and non-taxable invoices, listing tax codes, within a date range.

1. Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Invoice/Credit Summary (Tax Brk) [OE7XI].
2. Enter or select Warehouse code (defaults to the warehouse assigned to you), including type (Inventory or Sales warehouse, and enter “C” if you want to include child warehouses.
4. Enter or select the Type of Entry to report on: CM = credit memo, DM = debit memo, IV = invoice, defaults to all.
6. Indicate the Invoice Types you want to run the report for: SHP = all shipped but not invoiced, UPD = invoiced sales but not yet paid (default), ALL = all invoices.
7. Indicate if you want to sort documents by Salesperson or Order Writer.
8. Enter “Y” if you want credit and debit notes to reference the corresponding invoice date, otherwise enter “N”.

Output
------

|  |  |  |  |
| --- | --- | --- | --- |
| column heading | needs description? (if yes, populate one of the next two columns only) | glossary description | report-specific description |
| Doc No |  |  |  |
| Inv Dte |  |  |  |
| Name |  |  |  |
| Cost Value |  |  |  |
| Sales Value |  |  |  |
| Extras |  |  |  |
| Tax 1 |  |  |  |
| Tax 2 |  |  |  |
| Total Value |  |  |  |
| Margin |  |  |  |
| G.M % |  |  |  |
| Opr C |  |  |  |

---
