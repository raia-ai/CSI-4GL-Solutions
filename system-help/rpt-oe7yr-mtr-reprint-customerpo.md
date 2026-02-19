---
title: "OE7YR - MTR by Customer PO/SO/Invoice"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "OE7YR - MTR by Customer PO/SO/Invoice"
long_description: "Help documentation for OE7YR - MTR by Customer PO/SO/Invoice in the 4GL system."
---

OE7YR - MTR by Customer PO/SO/Invoice
=====================================

This function is used to reprint/fax/email the MTRs for a given customer purchase order.

If any logs are missing MTRs, an Excel report is generated that shows the log information and a Status column: if there is no MTR for a log, the Status column indicates “No MTR Defined”. If the MTR is invalid, the Status column indicates “MTR Not Found” and includes the filename specified in IN1E.

1. Choose Sales Order Entry » Order Entry Reprints » MTR by Cust PO/SO/Invoice [OE7YR].

4. If you selected a Customer:
   1. Enter the PO Number.
   2. Select the Sales Order number associated with the PO.
   3. Select the Invoice Number associated with the selected Sales Order.

If you did not select a Customer, you must manually enter a Sales Order number and an Invoice Number.

You do not have to enter preceding alpha or leading zeros for the Sales Order or Invoice Number fields.

5. Indicate the MTR Type required: Yes (include the original MTR), Overlayed (include the original with company header overlaid), Sys (system-generated MTR from company, not mill), or Both (original and system-generated).
6. Select where the MTRs should be printed (press F4 to choose from a list) and press Enter.

Output - cant generate output
-----------------------------

|  |  |  |  |
| --- | --- | --- | --- |
| column heading | needs description? (if yes, populate one of the next two columns only) | glossary description | report-specific description |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

---