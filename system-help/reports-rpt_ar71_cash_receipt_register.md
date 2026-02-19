---
title: "Rpt Ar71 Cash Receipt Register"
source: "madcap.md"
tags: ["4GL", "REPORTS", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rpt Ar71 Cash Receipt Register - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rpt Ar71 Cash Receipt Register in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the REPORTS module."
---


AR71 - Printing Cash Receipt
============================

This function prints posted or unposted cash receipts for a specified period.

1. Choose Accounts Receivable » AR Reports » Cash Receipt Register  [AR71].

4. Enter or select Deposit Number (defaults to all).
5. Enter or select Fiscal Period (defaults to all).
6. Enter the Start Date and Ending Date for the deposit transactions to be included in the report.
7. Select the Payment Type (defaults to all types).
8. Indicate if you want to include Only Posted receipts or leave blank to exclude them.

If you generate a Detailed report output to Excel, the worksheet will have an "Applications" sheet that contains each applied document with the same columns as the "Report" sheet plus additional columns for sequence, type, document #, applied amount, deduction amount, currency, and reason code.

Output
------

|  |  |  |  |
| --- | --- | --- | --- |
| column heading | needs description? (if yes, populate one of the next two columns only) | glossary description | report-specific description |
| Bank |  |  |  |
| Dep |  |  |  |
| Cheque # |  |  |  |
| Cheque Date |  |  |  |
| Payee/Account |  |  |  |
| T |  |  |  |
| Account |  |  |  |
| ChequAmount |  |  |  |
| Cur |  |  |  |
| Remarks |  |  |  |
| Posted |  |  |  |

---
