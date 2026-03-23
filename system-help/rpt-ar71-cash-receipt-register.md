---
title: AR71 - Printing Cash Receipt
source: madcap.md
version: '1.0'
last_updated: '2026-02-19'
short_description: AR71 - Printing Cash Receipt
long_description: Help documentation for AR71 - Printing Cash Receipt in the 4GL system.
---

# AR71 - Printing Cash Receipt

This function prints posted or unposted cash receipts for a specified period.

1. Choose Accounts Receivable » AR Reports » Cash Receipt Register \[AR71].
2. Enter or select Warehouse code (defaults to all warehouses).
3. Select the Bank Code.&#x20;
4. Enter or select Deposit Number (defaults to all).
5. Enter or select Fiscal Period (defaults to all).
6. Enter the Start Date and Ending Date for the deposit transactions to be included in the report.
7. Select the Payment Type (defaults to all types).
8. Indicate if you want to include Only Posted receipts or leave blank to exclude them.
9. Select whether to produce a **D**etailed or **S**ummary report.
10. Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.

**NOTE:** If you generate a Detailed report output to Excel, the worksheet will have an "Applications" sheet that contains each applied document with the same columns as the "Report" sheet plus additional columns for sequence, type, document #, applied amount, deduction amount, currency, and reason code.

***
