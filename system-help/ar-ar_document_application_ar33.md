---
title: "Ar Document Application Ar33"
source: "madcap.md"
tags: ["4GL", "AR", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Ar Document Application Ar33 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Ar Document Application Ar33 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the AR module."
---
Applying Unapplied Amounts
==========================

This function is used to apply unapplied amounts to documents in the same customer sub account ledger so that they no longer appear open. For example, you may have an open invoice and a corresponding credit memo, but they will remain open until they are applied to each other. You can apply a credit memo or a prepaid cash receipt to an invoice, or conversely apply the invoice to the credit memo/cash receipt.

This function does not allow you to write-off amounts or move them to a different account; if you need to move the amount to a different AR account, do a negative deposit to the account you are taking monies from, and a positive deposit to the account where it should be.

If you are using system credit checks, it's important to view this screen on a daily basis.

1. Choose Accounts Receivable » Entry/Maintenance » Document Application [AR33].
2. Enter the criteria to find a list of unapplied amounts:

   * Enter or select the Customer.
   * Enter or select the Type Of Entry or default to “ALL” types.
   * Enter the Date range or leave the dates blank to include all documents.
   * Indicate if you want to include Plus, Minus, and/or Zero balance amounts.
3. In the table, locate the document that includes the unapplied amount that you want to apply.
4. Optionally record any Remarks.
5. In the Appl Amt field, press F4.
   * Press F4 in the TOE field to retrieve the document that you are applying the amount to.
   * Once you've retrieved the document, in the This Appl field enter the amount you are applying \*with the opposite sign to what is shown in the Document Amt field.\*
   * If there is still an Open Amount, you can press F5 and retrieve another document to apply it to, until the Open Amount is nil.
   * When you are finished, click Close.

**Example** In step 3 you opened a credit memo document with an open amount of $334.22. In step 5, retrieve an invoice that the amount should be applied to. The invoice's Document Amt is 79.91, so you enter -79.91 in This Appl. The Open Amount of the original document (the credit memo) is reduced by that amount. In another line, you retrieve another invoice to apply all or some of the Open Amount to.

![](../Resources/Images/AR33_apply_multiple.png)

If you did not apply the full open amount of the original document (the credit memo, in our example), it will remain in the list with the updated open amount. If you applied the full amount, it will be removed from the list, along with the documents that you applied the balance to (the invoices, in our example), provided you applied their full balance.

To unapply an amount: show Zero balance documents, press F4 in the Appl Amt field, then delete the This Appl amount.

You can press F9 to display and change the PO number if necessary.

---
