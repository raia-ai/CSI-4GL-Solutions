---
title: "General Ledger Account Inquiry"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "General Ledger Account Inquiry"
long_description: "Help documentation for General Ledger Account Inquiry in the 4GL system."
---


General Ledger Account Inquiry
==============================

This function is used to inquire summaries (balances) or detail (transactions) information by GL accounts within a specific time period.

1. Choose General Ledger » GL Inquiry » Account Inquiry [GL64].
2. Enter or select Warehouse code, select check box to for all.
4. Enter or select Account Type, select check box for all.
5. Enter or select Account No.
6. Enter partial Account Name or leave blank for all.

What is the TOE?
----------------

All data posted to the GL references a source code1 that identifies the Type of Entry; this appears in the inquiry as “TOE”.

![](../Resources/Images/GL75_TOE.png)

The table below explains what the TOE is, and where you can view more information for the transaction (you can also view from GL inquiry by selecting the document): [missing xrefs]

| TOE | Generated From… | Online Inquiry | Reports |
| --- | --- | --- | --- |
| AC – Accruals \* | purchase order, outside processing order receipts | Accrual Inquiry [AP66] | Accrual Analysis [AP76] |
| CD – Cash Disbursements | payments of AP vouchers | Check Inquiry [AP67] | Check Listing [AP7B] |
| CR – Cash Receipts | AR deposits | Cash Receipt Inquiry [AR62] | Cash Receipt Register [AR71] |
| IC – Physical Inventory Count | variances posted from a physical inventory count | — | Variance Report [IN5G] |
| IN- Inventory Adjustments | inventory adjustments posted to adjust inventory | Inventory Adjustments [IN61] | Detailed Adjustments by Date [IN76] |
| JN – Journal Entries | posted journal entries (JE) | Journal Inquiry [GL63] Recurring Journal Inquiry [GL3A] | Journal Entry Report [GL78] |
| PR - Processing Inventory | outside processing entries | OP by Order Number [PP64] | Open OP Orders by Vendor [PP74] |
| SJ - Sales Journal | transactions from customer invoicing process | Invoice / Credit/Debit Memo Inquiry [OE62] | Invoice Summary by Document [OE74] |
| TI -Transfers in Inventory | inside production – finished goods | IP By Order Number [PR64] | Production Analysis Report [PR73] |
| TO – Transfer Out Inventory | inside production – raw material | IP By Order Number [PR64] | Production Analysis Report [PR73] |
| VR - Voucher Register | accounts payable vouchers | Accounts Payable Inquiry [AP68] | Vendor Invoice Listing [AP75] |
| YE – Year End Journals | postings from year end closing routine | Journal Inquiry [GL63] Recurring Journal Inquiry [GL3A] | Journal Entry Report [GL78] |

\* AC – Accruals can be documents starting with the following prefixes:

These would normally be a crediting accrual account:  
“R” – PO Receipts  
“F” – Outside Processing Receipts

These would normally debit accruals:  
“V” – Accounts Payable Vouchers  
“X” – Reversal of PO Receipt  
“U” – Reversal of OP Receipts

You could have a journal entry writing off an accrual:  
“J” – Journal Entry

You can view all document prefixes in Type of Entry Maintenance (MS31) [xref] – in the Pfx column.

Configuration


1 Source Codes [GL16]

---
