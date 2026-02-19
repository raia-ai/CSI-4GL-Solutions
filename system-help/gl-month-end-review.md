---
title: "Month End Review"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Month End Review"
long_description: "This topic provides detailed information about Month End Review in the 4GL system."
---


Month End Review
================

Period End Closing
------------------

In order to close a GL period end, you must ensure that the following have been done:

* Sales Journal
* All transactions have been posted to the GL
* All periods have a [F]inal or [C]losed status
* [R]eopened periods are closed.

A period cannot be closed if there are open journal entries (not processed and updated). Periods must be closed in chronological order (oldest to most current).

To close a general ledger fiscal period:

1. Choose General Ledger » GL Period End » Period End Closing [GLA].
2. Enter or select the general ledger Fiscal Period To Be Closed in YY/MM format.
3. In the Process Period Closing field you must enter your authorized response in order for the period to be closed.

Reports
-------

It is not necessary to run reports at month-end; they can be run anytime for a date range.

There is no “Month End” routine that needs to be run – business continues as normal in the next month.

Balancing the GL to Subledger
-----------------------------

Run Trial Balance report (GL73) and look for the following GL accounts (you can find the GL codes in MS33 > GL Codes).

* Inventory
* Accounts Receivable
* Accounts Payable
* Accruals

The values in these accounts must match the value of the subledgers which can be determined by running the following reports:

* Inventory – IN75X or IN71
* Accounts Receivable – AR7D (for all customers)
* Accounts Payable – AP77(for all vendors)
* Accruals – AP7F (for all buyers)

[the following was in the original article as copied from the old help; GKW said to get rid of it but it’s here for posterity/inspiration]

Cash receipts

Bank deposits physically done in the current month to close, and have not yet created a cash receipt or posted a cash receipt in  must be addressed. You must back date the receipt to the month/day you physically made the deposit at the bank.

Material Receipts

If you have physically received items from a vendor or branch, you should date the receipt the day it entered your premises (as stated in a previous email). Therefore it is important all receipts are received correctly within xx working days after month-end.

POS Sales

All POS sales must be confirmed  - it is important this is complete xx (xx established by Controller / Sales Manager) working days after month end.

Sales Orders / Invoices

You need to be only concerned with sales orders which have been converted to packing slips and have been delivered to the customer. Be sure to date the packing slip the day the material has been delivered. Invoices must be created prior to sending out statements. Therefore, it is important all items shipped in the month are billed xx working days after month-end.

Statements

Once invoicing is complete for your location, and Automatic Interest Program has been executed, confirm GL entries for interest have been posted for your branch in the GL. Statements can then be created – be sure to date statements for the end of the month. Statements will not print for customers who have zero balance owing. Due to the amount of print time required, you should run statements at the end of the day because you will likely need to replenish the paper tray.

---
