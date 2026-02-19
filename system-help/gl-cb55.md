---
title: "Cb55"
source: "madcap.md"
tags: ["4GL", "GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Cb55 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Cb55 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the GL module."
---


Manual Bank Reconciliation
==========================

This screen is used to manually reconcile the Cash Book to the bank statement. Ensure Recon Type is set to Manual in AR11.

1. Choose General Ledger » Cash Book/Bank Rec » Bank Reconciliation » Bank Reconciliation [CB55].

4. Enter the Latest Bank balance from your bank statement.
5. Select the action to be applied to all current transactions: Tick, Untick or None.
6. To filter the list to only see unreconciled transactions, select the Open? checkbox (leave cleared to list all).
7. In the table, verify the Bank Statement amount, and indicate (in the R field) whether to show all transaction types listed on the bank statement.
8. Look for double entries. There could be two or more Cash Book entries for one bank statement or vice versa. Tick items accordingly.  errors must be corrected. Bank errors must be noted and the imbalance carried forward. Once error has been rectified this should automatically correct the situation in the next statement.
9. Review any unreconciled items on the bank statement. They should either be bank fees, or manual deposits or withdrawals that have not been entered in the Cash Book, or an error entry by the bank.   
   After these are investigated, the legitimate ones should be entered into the Cash Book (either manually or imported). Once these items have been entered you must Post Cash Book to GL (CB41) again (DO NOT close the Bank).   
   Open the Bank Reconciliation (CB55) again to see the newly entered transactions. Tick these items off and highlight the corresponding items on the bank statement. At this point the Latest Bank and Expected Bank balances should balance.
10. Post Cash Book to GL (CB41) again and set the Close Bank field to **Y**es. Closing the bank will freeze the fiscal period and no more entries will be allowed in the Cash Book for that period.

It might be necessary to “un-tick” the entries and start again. Sometime you may “un-tick” items by clicking on the item again, however the item will disappear once the transaction section gets refreshed. To reinstate any item that has previously been ticked, clear the Open flag in the header. All transactions will be displayed. Locate the transaction you wish to review and “un-tick” it.

Recommendation: Run the Bank Reconciliation report and file it with the bank statement.

---
