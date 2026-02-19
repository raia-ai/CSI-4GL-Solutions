---
title: "Bank Reconciliation in Bulk via Excel"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Bank Reconciliation in Bulk via Excel"
long_description: "Help documentation for Bank Reconciliation in Bulk via Excel in the 4GL system."
---

Bank Reconciliation in Bulk via Excel
=====================================

The Bank Reconciliation Import function allows you to reconcile multiple transactions at once. To do this, you will generate a spreadsheet of all unreconciled transactions at all banks, mark the ones that should be reconciled, and then reimport them into .

You can also use this spreadsheet to unreconcile a transaction that was previously reconciled: manually enter the reconciled transaction on the spreadsheet and enter “2” in the Reconciled column.

1. To generate the list of transactions, choose General Ledger » Cash Book/Bank Rec » Bank Reconciliation » Bank Reconciliation Import Template [CB75] and enter “Y”.

The data is compiled and the corresponding spreadsheet opens. The spreadsheet includes three sheets – Report contains the transactions you may mark for reconciliation; Parameters identifies who generated the template and when; Instructions describes how to complete the import.

2. Select column I and change its formatting to text (click the I column head, right-click and choose Format Cells, then on the Number tab select “Text” and click OK).
3. For each transaction that has cleared the bank, enter “1” in the Reconciled column (column H) and enter the Reconciliation Period (column I), i.e. the fiscal period it should be reconciled in.
4. Make sure you are on the Reports sheet, then save the file as a “Text (Tab Delimited) (\*txt)” file (**Tip** Type “T” to quickly get to that option.).
   1. Change the location to where you will be able to find it in the next step.
   2. Make note of the generated file name or change it if desired.
   3. Click Save.
   4. You will be alerted that the selected file type does not support workbooks that contain multiple sheets; click OK to save just the sheet you are on, then click Yes to the formatting prompt. You can then close the spreadsheet.
5. To import these reconciliations into :
   1. Choose General Ledger » Cash Book/Bank Rec » Bank Reconciliation » Bank Reconciliation Import [CB56].
   2. Click and retrieve the .txt file you saved, then click OK.
   3. validates the entries in the spreadsheet by comparing the Bank, Cheque No, Cheque Type, and Cheque Period against the data in SM3. All matches that are marked as “1” are then reconciled in .
6. Any errors are presented in the Bank Reconciliation Takeon Errors report – resolve these and rerun the import.

---