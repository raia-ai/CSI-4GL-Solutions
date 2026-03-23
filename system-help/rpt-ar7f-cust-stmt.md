---
title: AR7F - Printing Customer Statements
source: madcap.md
version: '1.0'
last_updated: '2026-02-19'
short_description: AR7F - Printing Customer Statements
long_description: Help documentation for AR7F - Printing Customer Statements in the 4GL system.
---

# AR7F - Printing Customer Statements

This function allows you to print all customer statements, or send a statement electronically to one customer at a time. If you want to electronically send customer statements to a group of (or ALL) customers, use AR7E.

**NOTE:** Customer statements will always print portrait/condensed, regardless of the print window settings.

1. Choose Accounts Receivable » AR Reports » Customer Statement \[AR7F].
2. Enter or select the Warehouse code (defaults to the warehouse assigned to you).
3. Enter or select the Territory code (defaults to all).
4. Choose to Sort by Territory: Yes or No (blank).
5. Enter or select the Customer code (defaults to ALL).
6. To only print statements for customers who have requested them (as stored in the customer file)<sup>1</sup>, set Request Only? to “Y”. By default, a statement is printed for all customers.
7. By default, only Open documents (that is, do not have monies applied against them) are included. To include all documents, select ALL; you can then enter a from date to see all transactions on or after that date.
8. Select the Aging Date to include (defaults to today's date).
9. Enter the number of Past Due Days a document must be in order to be included in the report (by default, all documents are included).
10. Indicate the currency type: Functional (currency assigned to warehouse) or Source (customer’s currency).
11. Select whether to include only customer accounts with a balance over the credit limit : Yes or No (default).
12. Specify whether to age data by Invoice date (the default) or Due date.
13. By default, the report shows the Average Days to Pay for the customer (Yes): to change this, select No.
14. By default, the report shows the AR contact (Yes): to exclude this information, select No.
15. Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.

    If you open the Printer Code field and change the output Type to Fax/Email, you can edit the default subject and message for this statement.

Configuration

Customer Maintenance \[AR17] > Statement = “Y”

***
