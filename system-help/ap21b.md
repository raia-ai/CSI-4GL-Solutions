---
title: "Copying a Voucher"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Copying a Voucher"
long_description: "This topic provides detailed information about Copying a Voucher in the 4GL system."
---


Copying a Voucher
=================

Create a new voucher based on a previous voucher for the same vendor.

1. Choose Accounts Payable » Vendor Invoice Processing » Voucher Entry Maintenance [AP21B].
2. Click Copy.
3. Select the Vendor.
4. To filter the list, select a Status or leave it as “ALL”.
5. Optionally enter the Invoice number to search for.
6. All matching vouchers are listed; select the one you want to copy and click Select. Note that you cannot copy a voucher that has an accrual line.

A new voucher is created with a new Document #. On the Header tab, the invoice, effective and due dates are based on the current date. If the currency differs from the system currency, the exchange rate reflects the effective date of the voucher. The Details tab includes the same information as the original voucher -- materials ordered, remark lines, pricing breakdowns, etc. Make any changes to the new voucher as required.[anything else to note about what is/is not copied over?]

---
