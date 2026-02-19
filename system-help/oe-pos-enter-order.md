---
title: "Entering a POS Order"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Entering a POS Order"
long_description: "This topic provides detailed information about Entering a POS Order in the 4GL system."
---


Entering a POS Order
====================

In order to enter a POS order,  must be configured properly (see below).

Entering the order in :

1. Choose Sales Order Entry » SO Entry/Maintenance » Sales Order Entry/Maintenance [OE31].
2. Click New to create a new sales order.
3. Complete the order the same as a regular sales order. On the Billing/Shipping tab, you must select a payment term (Pay Terms) that has been defined for POS1.
4. Payments can be recorded as part of the order entry, or in a separate process at a later time.
   * If the customer is paying for the order now, enter the payment on the Payment tab. This tab is only accessible if the Pay Term selected on the Billing/Shipping tab is defined as a POS payment term1. Enter the amount of each payment type. You can split the payment across multiple payment methods (e.g. 25% cash, 30% Visa, 45% check).

     Depending on the payment type2, the order may go on credit hold unless the customer is a identified as a member (trusted customer) in AR17 > More Info. Members must be account customers and cannot be “cash” customers.
   * If the customer is not paying now, you can either place the order on hold or process it with the amount outstanding.
5. When you click Process, a POS Sales Order will print which is the same as a regular sales order but will show the payment and balance owing. POS sales orders may have a different heading (e.g. Invoice/Tax Invoice)3.

Configuration


1 OE11 > Indicate the payment terms that are valid for POS (More > Point of Sales)

2 AR19 > Select the “P” check box to indicate if the payment type is valid for POS; select the “C” check box if credit check applies to non-member customers

3 OE1Q > heading marked as “P”

IN19 > Point of Sale options: you may have only have one Bank Code defined, or a separate Cash Code for POS transactions

---
