---
title: "Year End Process"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Year End Process"
long_description: "Help documentation for Year End Process in the 4GL system."
---


Year End Process
================

Year End Closing
----------------

When you close the current year,  will create year end closing entries (zero out all income and expense accounts and update retained earnings). All GL periods, for all warehouses,  must be closed prior to running Year End Closing. As well, all accounts payable periods must be closed. When starting the year end process,  will check to confirm all periods are closed.

Once a year is closed you cannot run reports written in the Financial Report Writer. You can run a Trial Balance but you would have to manually insert the period (instead of selecting the period) for years that have been closed.

Review GL accounts [GL12A] to ensure all P&L accounts are account type S (Sales), C (Cost of Sales) or X (Expense). Account Types S, C and X are cleared out at year end with the difference being posted to Retained Earnings.

To complete Year End Closing:

1. Choose General Ledger » GL Period End » Year End Closing [GLB].
3. After the GL Closing report is created, you will see the Year End Close window; leave default (“Y”) to confirm the action and close the year, or enter “/” to cancel request.

Final Year End Update
---------------------

Complete close current year process - system will post year end closing entries to the general ledger. This must be run after GLB.

You can close year end while users are logged into , but we would not recommend running a GL update to post transactions in other months while you are running the year end process. From start to finish (assuming all your periods are closed), the whole process takes 10-20 minutes (depending on your server, amount of data).

1. Choose General Ledger » GL Period End » Final Year End Update [GLC].
2. will open a window for dates for the months of the future year it will open. Enter the month end dates and press F3 to exit the window.

---
