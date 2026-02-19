---
title: "OE74 - Invoice Summary By Document"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "OE74 - Invoice Summary By Document"
long_description: "Help documentation for OE74 - Invoice Summary By Document in the 4GL system."
---

OE74 - Invoice Summary By Document
==================================

This function produces a report containing sales value, inventory quantity and gross margin percentage for each product line by customer within a given date range.

For a detailed breakdown by tax code see the OE7XI - Invoice/Credit Summary (Tax Breakdown) report.

1. Choose Sales Order Entry » Order Entry Reports » Invoice Summary By Document [OE74].
2. Enter or select Warehouse code (defaults to the warehouse assigned to you), including type (Inventory or Sales warehouse, and enter “C” if you want to include child warehouses.
4. Enter or select the Type of Entry to report on: CM = credit memo, DM = debit memo, IV = invoice, defaults to all.
5. Optionally enter or select a Customer to only view invoices from that customer.
7. Optionally, select a Payment Term to report on (defaults to all).
8. Indicate if you want to sort documents by Salesperson or Order Writer.
9. Indicate if you want to sort the report by: Document Number, Date, Operator, or View detail Lines.
10. Enter “Y” if you want credit and debit notes to reference the corresponding invoice date, otherwise enter “N”.

Output
------

|  |  |  |  |
| --- | --- | --- | --- |
| column heading | needs description? (if yes, populate one of the next two columns only) | glossary description | report-specific description |
| Doc No |  |  |  |
| Inv Dte |  |  |  |
| Req Dte |  |  |  |
| Ent Dte |  |  |  |
| Name |  |  |  |
| Weight |  |  |  |
| Cost Value |  |  |  |
| Sales Value |  |  |  |
| Extras |  |  |  |
| Taxes |  |  |  |
| Total Value |  |  |  |
| Margin |  |  |  |
| G.M. % |  |  |  |
| Opr C |  |  |  |
| Product/Description |  |  |  |
| Pricing Qty |  |  |  |
| Cost Value |  |  |  |
| Loc Sale Price |  |  |  |
| Loc Sales Value |  |  |  |
| Loc Margin |  |  |  |
| Loc G.M.% |  |  |  |
| Weight |  |  |  |
| Primary Process | only included for **L**ines to Excel |  |  |
| Payment Term | only included for Excel output |  |  |

---