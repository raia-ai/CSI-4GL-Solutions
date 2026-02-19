---
title: "Ar Cash Receipts Ar31"
source: "madcap.md"
tags: ["4GL", "AR", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Ar Cash Receipts Ar31 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Ar Cash Receipts Ar31 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the AR module."
---


Recording Cash Receipts
=======================

This function is used to process receipts (cash, check, wire transfer, credit card or any other inbound monetary transaction) from customers for payment of sales transactions. In event of an error, a posted deposit can be reversed.

1. Choose Accounts Receivable » Entry/Maintenance » Cash Receipt Entry [AR31].
3. To open an existing document, enter the Deposit Number on the left, or select from the list on the right.  
   To create a new deposit document, enter “N” in the Deposit Number field on the left, or click New.
4. On the Header tab, enter overall information about the document:
   * Select the Type of payment, e.g. check, wire, visa, etc1.
   * Enter or select Deposit Date (defaults to today's date). Note that back dating may not allowed depending on your security settings2. The fiscal period3 that the selected date belongs to is displayed.
   * The Deposit Amount may be enabled, allowing you to enter the total of the deposit. If an amount is entered here, the total deposits entered on the Details tab must equal this total or it cannot be processed4.
   * The Local Amt and Check Total will be updated once entered on the Details tab.
5. On the Details tab, enter details of the deposit. This can comprise multiple lines, e.g. multiple checks:

   Receipts can be imported from Excel; see Importing Receipts from Excel below.

   * Enter or select the Check Date (defaults to today's date).
   * The account Type defaults to Receivable; if no invoice was created for payment received, e.g. a freight claim or a utility rebate, enter General ledger.
     + If you entered “R”, enter the customer code in the Account field.
     + If you entered “G”, enter the GL account in the Account field.
   * Enter the Check Number (or other reference such as a wire number; up to 10 characters alphanumeric).
   * If the deposit is in your local currency, enter the amount in the Check Amt (Loc) field.   
     If the deposit is in a different currency, enter the amount in the Check Amt (Frgn) field, and press F4 in the C field to identify the currency of the deposit.  converts the amount and displays it in the Check Amt (Loc) field.
   * For R type payments: If the customer has outstanding AR documents, press F4 in the Apply field to select the documents that the check amount should be applied to. To filter the list of documents, select Type Of Entry code and indicate which balances to show: Plus, Minus or Zero (choosing Zero may result in a large list as it will include balances that may have been applied previously). As you select documents, the Open Amount shown at the top goes down accordingly. You can also choose how to automatically apply the check: click Select and then choose All (then select the entries in the window), Oldest (to apply the check to the oldest documents), or Month (to apply the check to documents in a specified month).  
     If there is not enough to cover a document (i.e. the Open Amount is a negative number), you can override the amount in the To Be Applied column for that document. When you close the window, the difference is shown as Open for that document; if you do not want it to remain as open on this account, press F4 in the Deductions field and enter the Reason Code, any remarks, and the amount as a negative number. For example, if a document for $1575 is outstanding, but the check amount is only $1550, you can choose to write off the $25 difference.
   * If the customer has no outstanding AR amounts, or if you do not want to apply this deposit against them, you may skip the Apply field. In this case, the customer will have an open cash receipt against their account that can be applied in the future.
   * For G type payments, you should enter a description in the Remarks field, e.g. the vendor or reason for the deposit.
6. Repeat as necessary to record additional payments for the same deposit.
7. * . You can view the deposit in Cash Receipt Inquiry.
   * , e.g. if you are waiting for further wire transactions, you can put the deposit on hold and return to it later

Importing Receipts from Excel
-----------------------------

Prepare your Excel file with the columns shown in the following example:

![](../Resources/Images/AR31_import.png)

Ensure that there isn't an empty row between the heading row and the first data row, and that each line is assigned one of the three application types:

* DOCUMENT – enter an invoice number to apply the check to
* OLDEST – the receipt will be applied to the oldest open documents
* MONTH – the application would be made for documents dated in the specified month. The format is MMM-YY (e.g. NOV-21). Ensure that the column is formatted as text.

To import the lines into SM3, on the Details tab of AR31 click Excel Import and retrieve your file.

Configuration


1 Deposit Types [AR19]

2 Options > Acc Receivable > Disallow Cash Rec Date in Past

3 Fiscal Period Dates [GL19]

4 > Balance Cash Receipts to a Deposit Total?

---
