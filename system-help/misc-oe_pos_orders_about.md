---
title: "Oe Pos Orders About"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Oe Pos Orders About - 4GL Help Documentation"
long_description: "This topic provides detailed information about Oe Pos Orders About in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


About Point of Sale (POS) Orders
================================

A Point of Sale (POS) order is used for “walk-in customers” who will take the material with them. The order can be paid at the front counter or charged to an existing customer’s account.  applies any payment to the POS invoice, creating a cash receipt, and posts the payment to the bank.

Point of Sale orders are different from regular sales orders in the following ways:

* Payment information is entered during order entry
* Cash receipts are automatically applied against the POS sales invoice.

Process
-------

1. Enter the Point of Sale order in the regular sales order form (OE31).
2. Enter and process payments:

1. An order is identified as a POS order by the payment term selected. If a POS payment term is selected on the order, you can capture payments on the Payment tab. Payments can also be entered in the standalone Payment Entry form (OE5C).
2. At the end of the day, run the POS Payment Report (OE7XV) to view and reconcile unposted payments for all customers, then run the Payment Posting form (OE5D or OE5DA) to post the payments and process the cash receipts in AR31.

While the POS Payment Report allows you to report on payments from the stock warehouse (“I”) or the sales warehouse (“S”), payments must be posted by stocking warehouse. POS payments that are not linked to a sales order will have the same stock and sales warehouses.

Configuration


* AR19 > Indicate the deposit types that are valid for POS (select the “P” check box)
* OE11 > Indicate the payment terms that are valid for POS (More > Point of Sales)
* IN19 > Point of Sale options: you may have only have one Bank Code defined, or a separate Cash Code for POS transactions

---
