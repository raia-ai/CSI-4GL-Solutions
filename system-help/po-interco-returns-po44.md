---
title: "Intercompany Receipt Returns"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Intercompany Receipt Returns"
long_description: "Help documentation for Intercompany Receipt Returns in the 4GL system."
---


Intercompany Receipt Returns
============================

[merge into Receipt Returns when that topic is done]

For intercompany receipts, you will need to do a receipt return in the receiving warehouse (e.g. warehouse 20) and a credit in the selling warehouse (e.g. warehouse 10).

1. Find the invoice number:
   1. Choose Sales Order Entry » Order Entry Inquiries » Sales Orders By Customer PO [OE66].
   2. Enter the receiving warehouse (e.g. 20) purchase order number.
   3. Press F4 in the + field to display the order details.
   4. On the Header tab, click Invoices to display the invoice number.
2. Process the receipt return to remove the material from the receiving warehouse (20): choose Purchasing » PO Receipts » Receipt Returns [PO44].
3. Issue a credit note in the selling warehouse (10) for the invoice number you noted in step 1 to return the material to the selling warehouse.

---
