---
title: "Setting Up Automatic Interest Charges"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Setting Up Automatic Interest Charges"
long_description: "This topic provides detailed information about Setting Up Automatic Interest Charges in the 4GL system."
---


Setting Up Automatic Interest Charges
=====================================

This function is used to charge interest1 on outstanding AR balances. This function will create a journal entry for each interest amount to be charged. When the journal entries are posted, they are charged to the GL account2 and the transaction will display as “JN” in the AR customer account.

Interest is only charged to customers that are flagged to be charged interest3.

1. Choose Accounts Receivable » Entry/Maintenance » Automatic Interest Maintenance [AR35].
3. Enter or select the fiscal Period for which to charge interest.
4. If you want to apply interest to all customers with overdue balances, enter “Y” in the Set Default? field.

If you want to select which customers with overdue balances to apply interest to, leave Set Default blank and:

1. Enter the Search Parameters to retrieve a list of customers with overdue balances:
2. To view a customer's past interest charges, press F4 in the D field.  
   To view their credit information, press F4 in the C field.
3. For each customer that you want to charge interest, select the S check box.

5. When you exit the window, creates a journal entry for each charge.

Configuration


1  > Interest Rate Charged on Overdue Accounts

2 GL Codes > Interest Income

3 Customer File [AR17] > More Info > Charge Interest?

---
