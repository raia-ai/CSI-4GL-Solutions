---
title: "About"
source: "madcap.md"
tags: ["4GL", "GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "About - 4GL Help Documentation"
long_description: "This topic provides detailed information about About in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the GL module."
---


About Cash Book / Bank Reconciliation
=====================================

Cash Book entries in  are the subledger entries for the associated GL bank code. The bank’s Cash Book report (CB71) and the bank’s GL Account on a Trial Balance report (GL73) should balance.

Transactions are posted to the  Cash Book in any of the following manners:

* Accounts receivable cash receipts
* Vendor payment/cheque processing
* Journal entries
* Cash Book direct manual entries

The purpose of the Cash Book / Bank Rec menu is to balance the Cash Book to statement(s) received from bank(s). At any point, they generally do not balance due to timing of transactions and transactions which happen at the bank prior to happening at the company -- bank(s) would have items, such as service charges, which the Cash Book would not have and the Cash Book might have check payments which may not have been processed by the bank(s).

Procedure:

* Ensure the previous fiscal period (month) has been reconciled. For example, when reconciling a July bank statement ensure the corresponding fiscal period for June has been closed out. Do not proceed if it has not.
* Ensure manual entries that have been left out of the system are entered into the cash book (in CB31).
* Post to GL (CB41). Only posted entries can be reconciled.
  You cannot make changes to posted entries.

Configuration


Set up the following files:

* AR11 - banks file
* CB11 - cash book transaction types
* CB12 - bank transaction types
* CB13 - recurring bank transactions
* CB14 - EFT bank formats

---
