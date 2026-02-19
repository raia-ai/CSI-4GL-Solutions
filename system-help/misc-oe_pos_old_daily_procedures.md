---
title: "Oe Pos Old Daily Procedures"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Oe Pos Old Daily Procedures - 4GL Help Documentation"
long_description: "This topic provides detailed information about Oe Pos Old Daily Procedures in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Daily Procedures
================

OLD PROCESS, UNPUBLISHED, KEPT IN PROJECT FOR POSTERITY (FOR NOW)

Your warehouse may have multiple shifts in a day. For each shift, run Start of Shift and later Close of Shift. At the end of the day you must run End of Shift (End of Day) to close the day and allow for a new shift to be started the next day.

It is assumed that there is a safe which has limited access, together with an accessible till for cash transactions. We recommend that a “Cash” pseudo bank code is set up to keep track of the total cash in the till and the safe.1

Start of Shift
--------------

At the beginning of a day where there will be POS orders, someone must “Start” the POS shift. If this is not done, POS users will receive an error “Shift not open” when they try to create a new POS order.

1. Choose Sales Order Entry » Point of Sale » Start Of Shift [OE5S]
3. Change the Next Shift Date if necessary.

   The starting amounts in the safe and the till are populated based on the previously closed shift's balances.
4. Click Process.

Close of Shift
--------------

At the end of the shift, run this function to balance the POS transactions processed in the shift. This function balances the safe and till cash amounts, reconciles the various forms of payment received as well as bank deposit slip, and posts the payments to the Accounts Receivable system.

All POS invoices must be confirmed before running this function.

Choose Sales Order Entry » Point of Sale » Close Of Shift [OE5E] and record the total value of payments collected during the shift. Each of these fields opens a separate window. Some may not be applicable to you/this shift; if all sales were “On Account”, just press Enter through the fields.

| Field | Description |
| --- | --- |
| Safe Count | Cash amount in the safe. Use only if you have a float separate from Till Float (petty cash).  If the safe has not been accessed during the day, the entered amount should balance to the B/Forward amount. The only time there would be a difference is if the safe was accessed during the day either to borrow or top up the cash in the till. For example: Safe Count : $1,000 B/Forward : $800 Adjustment: $200  In this example we started off with $800 and ended up with $1,000. This means that an additional $200 was placed in the safe and this should reflect as a positive adjustment. Conversely we could have a negative adjustment which reflects that some cash was withdrawn from the safe. In both cases the contra entry will appear in the Till reconciliation. |
| Till Count | Total cash amount (excluding credit card/check amounts) in the till. This amount should balance to the B/Forward Till amount plus/minus any Adjustment amount (see above) plus any Cash sales during this shift. If it does not, a difference will be reflected and should be investigated. |
| Check Payments | Total amount of check payments. This should balance to the sum of all the check sales. If it does not, a difference will be reflected and should be investigated. |
| Credit Card Pmnts | Total amount of credit card payments. This should balance to the sum of all the credit card sales. If it does not, a difference will be reflected and should be investigated. |
| Debit Card Pmnts | Total amount of debit card payments. This should balance to the sum of all the debit card sales. If it does not, a difference will be reflected and should be investigated. |
| Cash On Hand | The total of all cash in both the safe and the till (will be used as Carry Forward $ amount for the next POS shift). This will be the sum of both B/Forward amounts plus Cash sales for the shift.  C/F Safe Amount: Enter the amount of cash that you want to hold in the safe.  C/F Till Amount: Enter the amount of cash that you want to hold in the till.  To be Banked: This is the total cash on hand minus the two C/F amounts. This amount will be reflected below. |
| Deposit Slip | Amount to be deposited in the bank, based on data enter above. Difference must be zero to close shift.  Cash Code: The default bank code set up for the warehouse1.  Deposit Bank Code: Displays the same bank code as the Cash Code above but can be overridden by selecting a new bank.  Deposit Slip: Enter the amount to be deposited. This should be equal to the sum of the Cash On Hand and Checks above.  These latter two fields plus any difference will be displayed. If there is a difference, this should be investigated. |
| Total Receipts | Display only totals for cash+checks, credit card receipts, and debit card receipts. |
| Turnover | Total Receipts: Displays the total receipts (same as Total Receipts field above)  Sales on Account: Enter the total of any sales where no payment was received.  Store Credits: Enter the total of any sales where a credit was used to offset the invoice.  Invoice Totals: Displays the total of all invoices.  Difference: This is the result of Invoice Totals minus Total Receipts minus Sales on Accounts minus Store Credits. This should be zero. If there is a difference this should be investigated. |

Once you go through all the fields, click Process.

If all totals are correct (no differences) all receipts are posted to Accounts Receivable and the POS shift is closed off. All Cash transactions will be posted to the “Cash” pseudo bank code. In actuality, if you are depositing any cash into your current bank account (see “To Be Banked” above), this will have to be done via a journal entry.

If there was payment collected “On Account” the Customer AR Inquiry window will open. The invoice would be emailed to the customer or printed (depending on their Customer file delivery options). The POS invoice will be posted to the customer’s account at this time.

If there is another shift today, run Start of Shift to open it for orders (and Close of Shift again when it's finished).   
If there are no more shifts today, run the End of Shift function next to close the day.

End of Shift (End of Day)
-------------------------

This is the final step of the day, to be run when there are no more POS invoices for the day. This must be run in order to be able to start a new shift on the next business day.

Choose Sales Order Entry » Point of Sale » End Of Shift [OE5F].

Configuration


1 IN19 > OE Options > Additional Options > Cash Sales Account

---
