---
title: "Ap Scanning Vendor Invoices"
source: "madcap.md"
tags: ["4GL", "AP", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Ap Scanning Vendor Invoices - 4GL Help Documentation"
long_description: "This topic provides detailed information about Ap Scanning Vendor Invoices in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the AP module."
---


Scanning Vendor Invoices
========================

If you have enabled the voucher label1, when a voucher is processed from Vendor Invoice Entry a label will print that contains a barcode representing the voucher number.

Affix the label on the vendor invoice (on the first page if it is a multi-page invoice).

Use a scanning program (e.g. 's integrated Scan2PDF) to scan the vendor invoices and save them to the defined network location2. The scanning program autonames the images based on the barcode value (i.e. the voucher number), e.g. the vendor invoice for 10v000123 is scanned as 10v000123.pdf.

adds each scanned image as an attachment to its corresponding voucher. You can view a scanned invoice in the I column of the AP Inquiry.

Configuration


1 
Label Options > Label Printer Defaults > VO01 Voucher Label = LRVOHLB1

2  > Vendor Invoice

---
