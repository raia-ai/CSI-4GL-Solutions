---
title: "Processing a POS Order"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Processing a POS Order"
long_description: "Help documentation for Processing a POS Order in the 4GL system."
---


Processing a POS Order
======================

OLD PROCESS, UNPUBLISHED, KEPT IN PROJECT FOR POSTERITY (FOR NOW)

In order to enter a POS order,  must be configured properly and a shift must be started.

Entering the order in :

1. Choose Sales Order Entry » Point of Sale » POS Entry [POS].
2. Click New to create the order. You cannot copy or link POS orders.
3. Complete the Header and Details similar to a regular sales order. On the Billing/Shipping tab:

   * The Bill To may default to a standard “Cash” customer code assigned to the stock warehouse1; if the customer will be charging to their account, select the proper customer account.
   * Optionally enter or change the Contact name, which will appear on the invoice.
   * Change the Ship Via to “PU” for customer pickup.
4. Process the order. The Payment Processing window opens. Enter the payment details:
   * If the customer is paying for the order, enter the amount paid in the appropriate payment type field: Cash Payment, Check Payment, Card Payment (debit or credit).
   * If the customer is charging the order to their account, enter the $ amount in the On Account field.
   * You can split the payment across multiple payment methods (e.g. 25% cash, 30% Visa, 45% on account).
   * Enter through all fields to enable the Process button.

   You will not be able to process the payment until the Balance field is zero.
5. When you click Process, two copies of the invoice will print.

Fulfilling the order:

1. Customer will take both copies of the invoice to the warehouse.
2. Warehouse will write on one copy of the invoice the log picked for the order (cannot use Handheld at present time) and have the customer sign this copy confirming they have picked up the material.
3. Customer will return both copies of the invoice to the office.
4. Office will retain the signed copy, and mark “Picked Up” on the second copy and give it to the customer for their records.

At the end of the day orders must be confirmed to assign the logs to the invoices, and the Close/End of Shift processes must be run.

Configuration


1 IN19 > OE Options > Additional Options > Cash Sales Account

---
