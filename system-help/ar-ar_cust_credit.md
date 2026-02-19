---
title: "Ar Cust Credit"
source: "madcap.md"
tags: ["4GL", "AR", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Ar Cust Credit - 4GL Help Documentation"
long_description: "This topic provides detailed information about Ar Cust Credit in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the AR module."
---
Understanding Credit Checks
===========================

Credit Settings
---------------

Credit checks take into account credit settings configured at three levels:

### Customer Level [AR17]

* Credit Group - If the customer belongs to a Customer Credit Group, one credit limit is assigned to the group for all members to draw upon. This overrides any credit line set for the customer.
* Credit Hold? - Enter “Y” if this customer is on credit hold. If credit check is turned on for the warehouse (see below), all sales orders for this customer will be held.
* Credit Line - Enter the credit limit assigned to the customer. If system credit check is turned on, all sales orders will be held if the customer credit balance is less than the credit line. If the customer belongs to a Customer Credit Group, the credit limit assigned to the customer is not used.

### Warehouse Level [IN19]

* Perform Credit Check - can be set to Do Not Perform (blank), Perform Credit Check (Y), or Warning Only (W).

### System Level [MS33]

* Number of Days of No Customer Activity Before Credit Check Required
* Past Due Days Above Which a Credit Hold Will Apply
* Check Past Due Days (indicate if calculated on Invoice Due Date or Document Date).

How is Credit Checked and What Happens to a Quote or Sales Order?
-----------------------------------------------------------------

There are operator and warehouse options that control who can edit an order in CRD status and whether the status will revert to ASG.

**If the Perform Credit Check switch is set to “Do Not Perform”**, quotes and sales orders may be processed as usual, even if the customer is on credit hold.

**If the switch is set to “Perform Credit Check”**:

The credit check looks at the following questions:

* After the quote/sales order, will the customer be $0.01 or more over their credit limit (or the customer group's limit)?
* Does the customer have outstanding documents over xx days (per system level switch described above)
* Has the customer not done business with you in the last xx days (per system level switch described above)

Quotes: If the customer file is set to credit hold, or if any of the above are true, the quote will receive a warning but can be printed or emailed.

Sales Orders: If the customer file is set to credit hold, or if any of the above are true, the order is placed on hold and must be approved before it can be processed (see note below).

**If the switch is set to “Warning Only”**:

The credit check looks at the same questions as above. If the customer file is set to credit hold, or if any of the above are true, the quote/order will receive a warning but can be printed or emailed.

Checks are done twice: when the customer is selected, and when the document is processed (for example, the customer can be below the credit limit prior to entering the order, but the value of the order puts them over the credit limit).

If an order is disapproved after the credit check, its status will be set to “BAD”; the order cannot be copied and must be re-entered.

---
