---
title: "Recommended Monthly AR Procedures"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Recommended Monthly AR Procedures"
long_description: "Help documentation for Recommended Monthly AR Procedures in the 4GL system."
---

Recommended Monthly AR Procedures
=================================

* Review all unapplied $ amounts from posted cash receipts using AR Unapplied Document Inquiry [AR64]. The AR64 should contain no data. If there are any outstanding unapplied $ amounts, use the Document Application [AR33] function to apply the amounts.
* Ensure all cash receipts are posted to the General Ledger and Accounts Receivable subledger. There are two ways to view unposted cash receipts:
  + In Cash Receipt Entry [AR31], view any documents displayed that have not been posted.
  + In Cash Receipt Inquiry [AR62], a blank field in the PST/ABT column indicates the cash receipt has not been posted. For control purposes, you can also view all cash receipt journals which have been aborted (PST/ABT=A).

---