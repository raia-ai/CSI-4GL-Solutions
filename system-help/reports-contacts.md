---
title: "Contacts"
source: "madcap.md"
tags: ["4GL", "REPORTS", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Contacts - 4GL Help Documentation"
long_description: "This topic provides detailed information about Contacts in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the REPORTS module."
---
AR7V - Fax/Email Statement to Contacts
======================================

This function sends statements to customer contacts who have statement delivery options defined. If you want to send statements to the fax/email defined at the customer level, use AR7E.

The statement contains the same details as AR7E (assuming default selections).

Setting Up Contacts to Receive Statements
-----------------------------------------

1. Retrieve the customer maintenance form [AR17] and press F4 to open the Doc Delivery options (you’ll need to add the contact if they’re not already listed).
2. In the Doc Delivery options, indicate if the contact should receive statements by Fax and/or Email.
3. Specify the warehouse they should receive statements for (or ALL) and if the statements should only include Open (all documents which have a balance open) or Current documents (all Open or Closed documents in the month you are running the statement for).
4. Repeat for other contacts as necessary.

Generating Statements
---------------------

1. Choose Accounts Receivable » AR Reports » Fax/Email Statement to Contacts [AR7V].

4. Enter the Subject and Message to be used for the email. These default from MS33 the first time the function is run but then use the last value for each subsequent run.

---
