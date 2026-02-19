---
title: "AR7F - Printing Customer Statements"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "AR7F - Printing Customer Statements"
long_description: "This topic provides detailed information about AR7F - Printing Customer Statements in the 4GL system."
---


AR7F - Printing Customer Statements
===================================

This function allows you to print all customer statements, or send a statement electronically to one customer at a time. If you want to electronically send customer statements to a group of (or ALL) customers, use AR7E.

Customer statements will always print portrait/condensed, regardless of the print window settings.

1. Choose Accounts Receivable » AR Reports » Customer Statement  [AR7F].

4. Choose to Sort by Territory: Yes or No (blank).
6. To only print statements for customers who have requested them (as stored in the customer file)1, set Request Only? to “Y”. By default, a statement is printed for all customers.
7. By default, only **O**pen documents (that is, do not have monies applied against them) are included. To include all documents, select ALL; you can then enter a from date to see all transactions on or after that date.

10. Indicate
12. Specify whether to age data by Invoice date (the default) or Due date.
13. By default, the report shows the Average Days to Pay for the customer (Yes): to change this, select No.
14. By default, the report shows the AR contact (Yes): to exclude this information, select No.
15. If you open the Printer Code field and change the output Type to Fax/Email, you can edit the default subject and message for this statement.

Configuration


1 
Statement = “Y”

Output
------

|  |  |  |  |
| --- | --- | --- | --- |
| column heading | needs description? (if yes, populate one of the next two columns only) | glossary description | report-specific description |
| Grand Total |  |  |  |
| Current |  |  |  |
| 1-30 Days |  |  |  |
| 31-60 Days |  |  |  |
| 61-90 Days |  |  |  |
| 91-120 days |  |  |  |
| Over 120 |  |  |  |
| Seq |  |  |  |
| TOE |  |  |  |
| Document Number |  |  |  |
| Customer PO |  |  |  |
| Doc Date |  |  |  |
| Due Date |  |  |  |
| Amount |  |  |  |
| Applied |  |  |  |
| Due |  |  |  |

---
