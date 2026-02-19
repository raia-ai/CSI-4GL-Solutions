---
title: "Rg92 93 94 Resolving Acct Errors"
source: "madcap.md"
tags: ["4GL", "GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rg92 93 94 Resolving Acct Errors - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rg92 93 94 Resolving Acct Errors in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the GL module."
---


Resolving Account Errors
========================

Before troubleshooting financial report imbalances, update the GL (General Ledger » GL Period End » General Ledger Update). Run this for ALL warehouses and ALL periods.

Identifying Missing Accounts
----------------------------

This function is used to display GL accounts that are not included in selected financial reports but possibly should be (e.g. all assets and liabilities that do not appear on the balance sheet).

1. Choose General Ledger » Financial Report Writer » Report Missing Accounts [RG92].
2. Enter or select the Report Number.
3. Enter the Report Type:
   * **B**alance Sheet (default) – will list all Balance Sheet General Ledger accounts (Assets(A), Liabilities(L), Shareholder’s Equity(E)) not selected on report
   * **I**ncome Statement - will list all Income Statement General Ledger accounts (Sales(S), Cost of Sales(C), Expenses(X)) not selected on report.

If balances exist in Debits/Credits column, the report will be inaccurate.

If the report is for a single warehouse you can ignore all “missing” accounts that end in a warehouse code other than the selected warehouse statement. For example if you are running an income statement for warehouse 10, ignore missing accounts that do not end in -10 (-00 GL accounts will need to be added to at least one warehouse statement).

Identifying Duplicate Accounts
------------------------------

This function is used to display GL accounts duplicated on report lines.

1. Choose General Ledger » GL Reports » Financial Report Writer » Identifying Duplicate Accounts [RG93].
2. Enter or select the Report Number.

If duplicate lines exist in Debits/Credits column, the report will be inaccurate if a cash balance exists.

Identifying Invalid Accounts
----------------------------

This function is used to display GL accounts that may be on the report in error; for example, Income/Expense accounts should not be included on Balance Sheet reports.

1. Choose General Ledger » GL Reports » Financial Report Writer » Identifying Invalid Accounts [RG94].
2. Enter or select the Report Number.
3. Enter the Report Type:
   * **B**alance Sheet (default) – will list all Balance Sheet General Ledger accounts (Assets(A), Liabilities(L), Shareholder’s Equity(E)) that may be on the report in error
   * **I**ncome Statement - will list all Income Statement General Ledger accounts (Sales(S), Cost of Sales(C), Expenses(X)) that may be on the report in error as well as any balance sheet accounts.

If balances exist in Debits/Credits column, the report may be inaccurate.

---
