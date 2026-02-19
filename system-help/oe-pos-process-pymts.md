---
title: "Processing POS Payments"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Processing POS Payments"
long_description: "Help documentation for Processing POS Payments in the 4GL system."
---


Processing POS Payments
=======================

You can enter payments directly in the sales order, or you can enter payments against a sales order or customer in a separate function as described below.

At the end of the day review all unposted payments, reconcile them against sales orders, then post the payments and process the cash receipts.

Recording Payments
------------------

1. Choose Sales Order Entry » Point of Sale » Payment Entry/Maintenance [OE5C].
2. Select the Document and/or Customer you are recording payment for.
3. Enter the amount of each payment type. You can split the payment across multiple payment methods (e.g. 25% cash, 30% Visa, 45% check).
   You can enter a negative payment when entering against a customer but not against an order.

   Depending on the definition of the payment type used1, the order may automatically go on credit hold unless the customer is identified as a member (trusted customer) in AR17 > More Info. Members must be account customers and cannot be “cash” customers.

Reviewing Payments
------------------

Run the POS Payment Report (OE7XV) to view and reconcile unposted payments. You can filter this report to all or a single customer, include posted payments or not, for a specified date range.

While the POS Payment Report allows you to report on payments from the stock warehouse (“I”) or the sales warehouse (“S”), payments must be posted by stocking warehouse. POS payments that are not linked to a sales order will have the same stock and sales warehouses.

Posting Payments
----------------

Run the Payment Posting form (OE5D to post all payments, or OE5DA to select individual payments) to post the payments and process the cash receipts in AR31.

This step will extract POS payments that have not already been extracted and where the order is in PBP status or later. Deposits will be created from these payments – one deposit per payment type.

If a payment was applied against a specific sales order:

* If invoice(s) exist for the sales order the payment will automatically apply against those invoices. Please note that when automatically applying against the invoices the invoice application could be spread over multiple deposits if there were multiple payment types.
* If invoices don’t exist, the deposit record will be created with the sales order reference. When invoices are eventually created from the sales order those invoices will auto apply against the payment.

If a payment was not applied against a specific sales order, the deposit record will be created with no sales order reference. Application of these transactions will need to be occur manually using the document application form (AR33).

When the deposits are created they will be put on hold. The deposits can then be reviewed and posted from the regular cash receipt form (AR31).

Payment details can be viewed in the Sales Order Inquiry.

Configuration


1 AR19 > Select the “C” check box if credit check applies to non-member customers

---
