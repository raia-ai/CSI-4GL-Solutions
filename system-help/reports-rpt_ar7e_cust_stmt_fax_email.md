---
title: "Rpt Ar7E Cust Stmt Fax Email"
source: "madcap.md"
tags: ["4GL", "REPORTS", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rpt Ar7E Cust Stmt Fax Email - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rpt Ar7E Cust Stmt Fax Email in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the REPORTS module."
---


AR7E - Sending Customer Statements by Fax/Email
===============================================

This function produces customer statements for multiple customers at the same time. For each customer, you define if the statement will be sent by fax, email, both, or print a hard copy.

This function sends the statement to the fax/email defined at the customer level. If you want to send the statement to customer contacts who have statement delivery options defined, use AR7V.

1. Choose Accounts Receivable » AR Reports » Customer Statements Fax/Email [AR7E].
3. Enter or select the Customer category (defaults to all).
5. To restrict the report to a single salesperson, select a Salesperson code (by default, the report includes data related to all sales people).
6. To ensure that a statement is printed for any customers who are not set up for fax or email, select the Default Print check box.
7. To only produce statements for customers who have requested them (as stored in the customer file)1, set Request Only? to “Y”. By default, a statement is produced for all customers.
8. By default, only **O**pen documents (that is, do not have monies applied against them) are included. To include all documents, select **ALL**; you can then enter a from date to see all transactions on or after that date.

11. Indicate
12. In the Invoice or Due Date field, specify whether to age data by Invoice date or Due date.
13. Indicate if you want to  Show Avg Days to Pay for the customer.
14. Indicate if you want to Show the AR Contacts.


Customers will be included in the report even if they have no documents past due in the specified amount of days. However, such customers will not receive a statement by email or fax.

> Do not enter anything in the Reset field without the guidance of 4GL Support - if you enter D or N, any values previously changed in the table (Type, fax number, email address, Print flag) are wiped out (or restored to the values in the customer file) and you would have to set up your desired statement values again for all customers. The Reset field is used the first time the AR7E is run to pull the default information from the customer files, but subsequently you should only modify the customized statement settings in the AR7E table as described below. For these reasons, access to this function should be restricted.

Once you have cycled through all the input fields, the table shows matching customers.

1. The Grand Total is the dollar value of a customer’s outstanding receivables. Press F4 to open the Customer AR Inquiry screen to view further details.
2. Change the delivery method for a customer if required:
   * On initial setup, the Type flag is set depending if there is an email address and/or fax number in the customer file (Email, Fax or Both). Change this field as required, e.g. to change a B to an E.
   * If Type = B or F, confirm that the Fax Number is correct.
   * If Type = B or E, press F9 to confirm that the Email Address is correct.
   * If a customer prefers a hardcopy instead of an electronic statement, delete what is in the Type field (to set it to None) and select the Print checkbox.
3. Press F3 to process and generate the statements.
   * If you made any changes in the table, enter “H” to save the changes, then press F3 again to reopen the Process Options screen.
   * When you are ready to generate the statements, enter “P” to process them. A statement is sent (or printed) according to the settings in the table. Note that the electronic delivery will always use the fax number/email address set in this table, regardless of what is set in the customer file.

Configuration


1
Statement = “Y”; for first time setup, enter the email address for statements in the Web/Email field

---
