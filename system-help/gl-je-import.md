---
title: "Importing Journal Entries"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Importing Journal Entries"
long_description: "This topic provides detailed information about Importing Journal Entries in the 4GL system."
---


Importing Journal Entries
=========================

The Journal Entry Import function allows you to import multiple journal entries from an Excel spreadsheet. To do this, you will create a spreadsheet template, complete the fields in Excel for each journal entry, and then import the spreadsheet into .

1. To generate the Excel template, choose General Ledger » Journal Entry » Journal Entry Import Template [GL7B]. The template opens in Excel.
2. In the spreadsheet, populate the header fields and a line for each journal entry (account no., amount, description, quantity).

   Ensure that there are no blank rows between journal entries. Do not include any commas or $ signs.
3. Make note of the file name that  assigned to the spreadsheet, then save and close the spreadsheet.
4. To import these journal entries into :
   1. Choose General Ledger » Journal Entry » Journal Entry Import [GL3B].
   2. Retrieve the appropriate spreadsheet and click Save. All the journal entries from the spreadsheet are added to .

Any errors (such as an invalid account number) are listed; resolve these and import the spreadsheet again.

These journal entries must be processed in GL31 and posted to the general ledger in GL32 as usual.

---
