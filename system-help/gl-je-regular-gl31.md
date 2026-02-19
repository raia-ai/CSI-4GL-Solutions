---
title: "Creating a Journal Entry"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Creating a Journal Entry"
long_description: "Help documentation for Creating a Journal Entry in the 4GL system."
---


Creating a Journal Entry
========================

This screen is used to create a regular (one-time only) journal entry. To create recurring journal entries, see Creating a Recurring Journal Entry.

If you know that [what? why would you create a JE and reversal at the same time?],  you can create a reversal entry at the same time by selecting the Create Reversal? check box and entering the Reversal Date on the Header tab.  will create two journal entries: the original and the reversal.

1. Choose General Ledger » Journal Entry » Journal Entry/Maintenance [GL31].
2. To create a new journal entry, change the Warehouse code if necessary, then click New.

   To edit an existing journal entry, enter the Document number and press Enter, or located it in the list and click Select.
3. On the Header tab:
   * Change the Document Date if necessary; the date must fall within an open fiscal period.
   * Change the Journal Currency and/or Currency Rate, if necessary.
   * Enter a Description of this journal entry; use the adjacent field to add any further Remarks. Both of these can be edited later in GL3C.
4. On the Details tab, click Add Line and then:
   1. Enter or select the GL Account Number.
   2. If the account selected is controlled by sub accounts (as defined in the GL Chart of Accounts [xref]), you will be prompted to select a sub account depending on the account type:
      * B (Bank) - select transaction type; entry will be added to Cash Book transactions [xref]
      * R (Accounts Receivable) - select the customer and AR document
      * P (Accounts Payable) - select the vendor and voucher
      * A (Accruals) - select the vendor and receipt
   3. Enter the $ amount to be applied in Journal currency (debits are positive, credits are negative; for credits, the minus sign can precede or follow the number). The amount entered in the Journal field is displayed in the Source currency.
   4. Enter a Description for this line entry.
   5. Enter theQuantity associated with this entry.
   6. Click Save.

   [What is purpose of E Applications button? Seems to be mandatory next step but has wrench icon like for settings ?? It opens the same screen as in 4b - is the button just to later get back to that screen to make changes?]

   7. Repeat steps a-f to add a new line, or click Cancel to return to the Details tab.

When you are finished, click Process.

[the following is from the old help but I'm not sure what it means, if it's still correct, where it goes]

When complete, and Journal control = zero, press <F3>. System will open Process Options window

If Journal Control does not equal zero the following window will open: [msg “TO PROCESS THIS DOCUMENT THE CONTROL MUST BE ZERO”]

Cannot process Journal Entry – options are to Abort or Hold in Process Options window

These journal entries are posted to the general ledger in GL32.

---
