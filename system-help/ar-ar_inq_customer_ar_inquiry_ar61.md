---
title: "Ar Inq Customer Ar Inquiry Ar61"
source: "madcap.md"
tags: ["4GL", "AR", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Ar Inq Customer Ar Inquiry Ar61 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Ar Inq Customer Ar Inquiry Ar61 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the AR module."
---
Customer AR Inquiry
===================

This function is used to find customers with outstanding credit balances.

1. Choose Accounts Receivable » AR Inquiry » Customer AR Inquiry [AR61].
2. Enter or select a Warehouse code, or select the check box to search All warehouses.
3. To filter the customers, do one of the following:
   * Select the All check box to search all customers.
   * Retrieve a particular customer.
   * Enter partial text in one or more of the Alpha Search (first couple characters of name), Search String (characters within name), Phone Search, and/or Post/Zip fields to filter the list of customers.
4. If you want to search for customers with a credit hold1, select the Credit Hold type.
5. If Credit Hold = **A**ny or **P**ast Due, enter the minimum number of days Past Due to search. For example, you may want to search for customers who have at least one transaction more than 90 days past due.

If you want your Collections staff to concentrate on customers who have the most days past due, enter 100 (or any other high number), then when complete search again with a lower number, e.g. 80.

The lower section displays the Grand Total for all outstanding receivables for the selected warehouse, as well as the total receivables for the customers that match the selection filters above (i.e. those listed in the table).

Press F9 to view the total $ value of sales orders awaiting credit approval and those credit approved but not yet picked (Release and Open Order fields respectively) for each customer.

To view all open documents on a customer’s account, press F4 on the Grand Total field for that customer. The resulting window displays relevant dates, credit and aging amounts, and a table that allows you to view the AR documents by Doc Type and Type of Entry, or locate a specific document number.

Configuration


1 Credit hold codes are maintained in AR18, and applied to a customer in AR17 or AR1D

---
