---
title: "Handling Checks Returned from Bank"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Handling Checks Returned from Bank"
long_description: "This topic provides detailed information about Handling Checks Returned from Bank in the 4GL system."
---


Handling Checks Returned from Bank
==================================

The procedure for handling a returned (NSF) check is the same as for depositing a check, except reversing the signs. We recommend entering returned checks on a separate cash receipt document, and not including them on a daily cash receipt to be deposited at the bank.

1. Create a new cash receipt - be sure to select same Bank / Warehouse Check was originally deposited in.
2. Record the check in the cash receipt entry but instead of a positive number, replace the Check Amount with a negative number (negative sign precedes number when entering).  will display a warning as a result of using a negative sign, but when handling a returned check this is OK.
3. Apply the amount against the original cash receipt document that the check was deposited with. Again, the system will display a warning as it normally expects a negative application amount for cash receipts.
4. At this point, you can optionally apply a bank charge to the customer’s account to cover the administration costs of handling returned check. Press F4 in the Other Amount field to record the charge along with a reason and remarks. Again the system will display a warning as it expects a negative amount in this field.

Charges can be applied to a customer's account via GL journal entry.

5. Process the cash receipt as normal. Once again the system will display a warning as normally deposit totals are > zero.

The customer account detail activity will display the reversal as a separate line item. Any additional bank charge entered will also be displayed as a separate line item.

---
