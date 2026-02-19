---
title: "Rn 3.24 Po"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rn 3.24 Po - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rn 3.24 Po in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Purchasing
==========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 40536 | Auto-receive RP document | When creating a pre-receipt, a new processing option, “O” (one-step), allows you to process the document and automatically create and receive the receipt. “O” is not available for “RC” documents, only “RP” documents. | PO41 |  |
| 40537 | Clone logs in receiving | The Duplicate button on the receipt log window has been enhanced with additional parameters: - MTR filename and case: duplicates the last log with the new MTR file name and case number. - Increment Case checkbox: duplicates the last log with a new case number that has been incremented by 1. If Copies is set to more than 1, the case number is incremented for each duplicated log. - Pieces - Length and Width fields are enabled if the dimensions exist for the product shape and the dimension is not fixed on the product. Fractional fields are enabled if the fractional dimension is set for the product line (e.g. if the length is in FT for the product line and the fractional UOM is in inches for the product line, the fractional field is enabled for inches). - BUM Quantity is updated according to the new pieces, length and width, but is editable. | PO41 |  |
| 40542 | Automatic MTR naming, missing MTR task | - When entering logs in PO41, you can now enter “P” in the MTR field to create an MTR name consisting of the PO number and PO line number. For the first receipt entered against a PO line the format will be P000001-001.PDF, and the - will change to A,B,C, etc. from the second receipt onwards(P00001A001.PDF, P00001B001.PDF, etc.).  - If you pick a log with an invalid MTR filename, an MTR Missing task is created. In the Task Manager comment field, if there is only one log with missing MTR the product description is shown and you can inquire on the log using the Inventory>Log Inquiry dropdown. | PO41  TK1 |  |

---
