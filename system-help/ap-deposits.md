---
title: "Deposits"
source: "madcap.md"
tags: ["4GL", "AP", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Deposits - 4GL Help Documentation"
long_description: "This topic provides detailed information about Deposits in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the AP module."
---


Managing Prepayments/Deposits
=============================

There are two ways you can handle a prepayment/deposit – it depends on how you want the open prepayments to display on your balance sheet.

Example:  
Let’s assume you are buying $10,000 and have to prepay $2,000 before you receive the inventory. In both cases below the PO should already be prepared.

Method 1 – Display Open Prepayment(s) as an Asset on Your Balance Sheet
-----------------------------------------------------------------------

**Pros** – Any prepayments which prolong over an accounting period will display as an Asset (Prepaid Inventory) on your balance sheet.  
**Cons** – Someone should manually reconcile open prepayments in the Prepaid Inventory GL account each month.

1. Enter an A/P voucher in the amount of $2,000 – your GL account distribution should be a Prepaid Inventory account (no sub-ledger).  
   \*\*Recommendation\*\* If you do not have an invoice, enter the PO# as the invoice. If there is more than one prepayment, just add “-A”, “-B” etc. to the end of the PO number – this may be useful in the future for tracking purposes.
2. When the inventory is received and you have received the invoice from the vendor, enter an A/P voucher in the amount of $8,000 ($10,000 – 2,000). Your GL account distribution will include the A/P accrual of $10,000 from the Material Receipt. To balance to the voucher header, you need to add another line crediting your Inventory Prepayment account – in this example $2,000.

Method 2 – Display Open Prepayment(s) as a Reduction of A/P on Your Balance Sheet
---------------------------------------------------------------------------------

**Pros** - Prepayments will display as an open credit in your A/P sub-ledger.  
**Cons** – The Prepaid Inventory will not display as an asset. Zero A/P voucher appears as closed on your disbursement screen (have to display open/closed vouchers to pay).

1. Enter an A/P voucher in the amount of $0 – your GL account distribution will be blank as there is $0 in the header.  
   \*\*Recommendation\*\* If you do not have an invoice, enter the PO# as the invoice. If there is more than one prepayment, just add “-A”, “-B” etc. to the end of the PO number – this may be useful in the future for tracking purposes.
2. When selecting voucher for payment, ensure you display “closed” vouchers. When you select the voucher,  opens a window you to state what you want to pay – the default is the amount of the voucher, in this scenario it would be changed. Change the dollar amount on the closed voucher to the amount of the deposit – in this example $2,000.
3. When the inventory is received and you have received the invoice from the vendor, enter an A/P voucher in the amount of $10,000. Your GL account distribution will include the A/P accrual of $10,000 from the Material Receipt .
4. When you are ready to pay the vendor, select the deposit voucher which will have a credit balance of $2,000 and the full voucher of $10,000 –  will create a check for the net amount of $8,000.

---
