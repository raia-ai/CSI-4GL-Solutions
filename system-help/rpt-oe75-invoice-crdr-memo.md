---
title: "OE75 - Invoice/Credit or Debit Note"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "OE75 - Invoice/Credit or Debit Note"
long_description: "This topic provides detailed information about OE75 - Invoice/Credit or Debit Note in the 4GL system."
---


OE75 - Invoice/Credit or Debit Note
===================================

This function is used to reprint/fax/email a credit or debit memo.

1. Choose Sales Order Entry » Order Entry Reprints » Invoice/Credit or Debit Note [OE75].
3. Select the Type of Entry, then enter or select a Single Document number or use the Multiple Document field to select more than one document.
4. Indicate if you want to Include POD (proof of delivery1) in a separate PDF from the invoice.
5. Indicate if you want to include the word “Reprint” in the top right corner of the reprint.

Configuration


1 PODs must be scanned and stored in a network folder, similar to MTRs; the POD folder address is defined in IN19.

Output
------

|  |  |  |  |
| --- | --- | --- | --- |
| column heading | needs description? (if yes, populate one of the next two columns only) | glossary description | report-specific description |
| LN |  |  |  |
| Back Ordered |  |  |  |
| Ordered |  |  |  |
| Unit |  |  |  |
| Description |  |  |  |
| Shipped |  |  |  |
| Unit Price |  |  |  |
| Value |  |  |  |

---
