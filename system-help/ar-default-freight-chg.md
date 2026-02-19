---
title: "Setting Up a Default Freight Charge for a Customer"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Setting Up a Default Freight Charge for a Customer"
long_description: "This topic provides detailed information about Setting Up a Default Freight Charge for a Customer in the 4GL system."
---


Setting Up a Default Freight Charge for a Customer
==================================================

You can set up a default charge, e.g. a freight charge, for a customer. This charge is associated with the Ship Via code that would be selected on the Billing tab of a quote or sales order. This charge may be added to the Details tab by default (but can be removed), or it may be mandatory and not removable.

To set up a default charge for a customer:

1. Set up the charge associated with the Ship Via code:
   1. Choose Sales Order Entry » File Maintenance » Ship Via [PO13].
   2. Add the record first, then go back into the line and go to the Revenue field.
   3. Create a “C” line and enter a Code and Description, then the Value of the charge. Select the E check box to make the charge active. In the D column, enter “Y” to indicate that the charge should be added to a quote or order by default (but can be removed), or “M” if the charge is mandatory (not removable), or leave blank to allow a user to manually add the charge to a quote or order.
2. Assign the Ship Via code to the customer:
   1. Choose Accounts Receivable » File Maintenance » Customer Maintenance [AR17].
   2. Retrieve the customer, then go into the Ship To field.
   3. Press F4 in the M field, then select the Ship Via code you defined in step 1.
   4. Repeat if necessary for other Ship To entries for this customer.

When you create a quote or sales order for this customer, the Ship Via is populated on the Billing tab, and the charge is added to the Details tab. If a global default charge is also listed you should delete that line.

If the Ship Via in the customer's Ship To is one that does not have an associated charge, then that Ship Via will be listed by default on the Billing tab of a quote or order and the customer-specific charge will not be applied. However, if you change the Ship Via on the Billing tab to the one with the charge, then the charge will be added to the Details tab.

If you set the Ship To for an order or quote to “P”, the Ship Via will change to the Ship Via that has the Pickup flag set in PO13, but this can be changed to a different Ship Via.

---
