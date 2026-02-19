---
title: "Cb32"
source: "madcap.md"
tags: ["4GL", "GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Cb32 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Cb32 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the GL module."
---
Importing Cash Book Entries
===========================

The Cash Book Import function allows you to import multiple cash book entries from an Excel spreadsheet. To do this, you will create a spreadsheet template, complete the fields in Excel for each entry, and then import the spreadsheet into .

1. To generate the Excel template, choose General Ledger » Cash Book/Bank Rec » Cash Book Entry/Maintenance » Cash Book Import Template [CB74]. The template opens in Excel.
2. In the spreadsheet, populate the header fields and a line for each entry.
3. Make note of the file name that  assigned to the spreadsheet, then save and close the spreadsheet.
4. To import these entries into :
   1. Choose General Ledger » Cash Book/Bank Rec » Cash Book Entry/Maintenance » Cash Book Import  [CB32].
   2. Retrieve the appropriate spreadsheet and click Save. All the entries from the spreadsheet are added to  and can be viewed and updated as usual.

Any errors (such as an invalid GL code) are listed; resolve these and import the spreadsheet again.

---
