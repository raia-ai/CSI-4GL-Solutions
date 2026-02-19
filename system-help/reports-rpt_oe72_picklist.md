---
title: "Rpt Oe72 Picklist"
source: "madcap.md"
tags: ["4GL", "REPORTS", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rpt Oe72 Picklist - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rpt Oe72 Picklist in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the REPORTS module."
---
OE72 - Picklist
===============

This function reprints/fax/emails a picklist for a branch transfer. “\*\*REPRINT\*\* will print below the document number. You will not be able to reprint a picklist from a document that has a status of Closed. You can reprint a picklist for orders with a status of PCB, but only lines with a status of PCK will print.

Operator security controls access to this function;  for assistance.

1. Choose Sales Order Entry » Order Entry Reprints » Picklist [OE72].
3. Enter or select the Type of Entry: branch transfer (BT), processing purchase order (PP), production order (PR), or sales order (SO).
4. Enter or select the Document Number you want to reprint the picklist for.
5. If you do not want to include all line items, press F4 on Filter Lines to indicate the lines you want to **S**elect or **D**eselect.
6. If a machine was specified for each line in the order, you can choose to Print by Machine and select the Machine(s) to print.
7. If logs were selected for line items in the order and the logs were assigned to a bin location, you can choose to Print by Bin Loc and select the Bin Location(s) to print.
8. Indicate if you want to Print Product Images for any products that have an image attached to the product code.

If circulating the reprint, be sure to destroy previously-printed documents for same document number.

Output
------

|  |  |  |  |
| --- | --- | --- | --- |
| column heading | needs description? (if yes, populate one of the next two columns only) | glossary description | report-specific description |
| Reference |  |  |  |
| Product Description |  |  |  |
| Qty Ordered |  |  |  |
| Qty Picked |  |  |  |
| Qty B/O |  |  |  |

---
