---
title: "Receipt Returns"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Receipt Returns"
long_description: "Help documentation for Receipt Returns in the 4GL system."
---


Receipt Returns
===============

[merge Intercompany Receipt Returns into this topic]

[from old help, need to validate]

To reverse partial or full receipts and allow for return of material. Creates a document linking the original document. When preparing a Receipt Return, logs for the material cannot be committed or sold. Receipt Return interfaces with inventory and AP sub-ledgers. System automatically references Receipt Return to the Original accrual (Receipt Returns do not have to be selected/link in Accounts Payable Entry Maintenance – AP21B:

Choose Purchasing » PO Receipts » Receipt Returns [PO44].

The lists shows all receipts that [what is criteria to appear in this list?]. Select one of these to return or click New and then retrieve the related receipt.

On the Details tab, in the Select field, enter “Y” to select all receipt lines, “D” to duplicate, or leave blank [to what?].

If you enter “D”, the lines are created with returned weight and value populated. If any logs are picked or have a different cost price than what it was received at, you will receive a prompt stating some logs were not added; the returned quantity omits the weight of those logs. The BUM Qty Ret field shows all the valid logs added from the original receipt.

---
