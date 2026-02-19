---
title: "Creating Recurring Journal Entries"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Creating Recurring Journal Entries"
long_description: "Help documentation for Creating Recurring Journal Entries in the 4GL system."
---


Creating Recurring Journal Entries
==================================

Recurring journals allow you to process journals to the same account code(s) on a regular basis within a fiscal year. Recurring journals are useful for:

* Distributing expenses among a variety of accounts
* Creating accruals for non-inventory items, such as rent in future months (useful when preparing Estimated Actual reports).

There are two types of recurring journals:

* *Standard* recurring journals allow you to create a journal template that includes all chart of account values and same dollar amounts for the journal. Example: allocating rent expenses since the same amount is charged each month for rent.
* *Skeleton* recurring journals allow you to create a journal template that includes all chart of account values, but does not include any dollar amounts for the journal. Accounts can be modified, added or deleted before the entry is posted. Example: allocating phone expenses to a number of code combinations since the phone bill changes each month.

For regular (one-time) journal entries, see Creating a Journal Entry.

[complete the procedure below after Creating a Journal Entry is finalized; it seems to have the same fields/functions except #3/4 below in place of the Reversal fields, and no E Applications button; possibly combine the articles?]

1. Choose General Ledger » Journal Entry » Recurring J/E Maintenance [GL35].
2. In the Select Voucher window, you can optionally select the Open check box to filtered the list to only display open (non-zero) vouchers.
3. Enter the recurrence Frequency (1- 6), i.e. journal occurs every “x” fiscal periods.
4. In the Occurrence field, enter the number of times the journal entry should occur. For example, a recurring journal entry created in the first period of a fiscal year, with Frequency=“1”, there can be maximum 12 occurrences. Recurring journal entries cannot carry over into next fiscal year.

[the following is from the old help but I'm not sure what it means, if it's still correct, where it goes]

When complete, and Journal control = zero, press <F3>. If “Process” is selected, system will create duplicate Journal Entries for periods/frequency selected. Journal Entries are not posted – user has option to change entry lines/amounts. View Journal Entries created in Recurring Journal Inquiry screen

If Journal Control does not equal zero the following window will open: [msg “TO PROCESS THIS DOCUMENT THE CONTROL MUST BE ZERO”] Cannot process Journal Entry – options are to Abort or Hold in Process Options window

These journal entries are posted to the general ledger in GL36.

---
