---
title: "Setup"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Setup"
long_description: "Help documentation for Setup in the 4GL system."
---


Setup
=====

Purchase Shipping Terms
-----------------------

Purchase Shipping Terms are defined in PO15 and assigned to a vendor in Vendor File Maintenance (PO11). Purchase Shipping Terms determine what type of costs can be used for a Purchase Order issued to a vendor.

System Controls - MS33
----------------------

### AP Options

1. Auto Accrual? “Y” or blank (default).

   If auto accrual is set to “Y” system will automatically accrue purchase at time receipt is processed. E.g. Purchase Order (P000179) is issued and receipt is processed (Receipt R000134).
2. Accrual Date Check? “Y” or blank (default).
3. Purch Var Percent. Enter up to 3 digits.
4. Auto Reverse Accrual? “Y” or blank (default).
5. Enter “Y” to confirm changes or type “/” to exit.

### GL Options

1. Type “Y” to use Default Fiscal Period (earliest fiscal open) or leave blank for no.
2. Type “C” to display container and supplier reference in GL or leave blank for no.

### GL Codes

Enter the default GL Codes specific to your company, especially pay attention to Purchase Variance field (difference between purchase order and invoice costs).

---
