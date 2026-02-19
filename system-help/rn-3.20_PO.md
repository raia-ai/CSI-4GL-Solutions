---
title: "Purchasing"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Purchasing"
long_description: "Help documentation for Purchasing in the 4GL system."
---

Purchasing
==========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 37880 | PO7D generates PDF receipts | The Direct Receipts By Shipment Number report now prints a receipt PDF to screen for each receipt in the shipment. If the “Print Labels” check box is selected, it will print labels for those receipts. Note that the receipt PDF is the same form 11 that is used for receipt printing/reprinting. | PO7D |  |
| 38488 | Export to Excel from PO31 and PO61 | An Excel Export button has been added to the PO Inquiry and PO entry Details tab. This exports the PO lines in the same format as the Excel Import template (PO3D) with the exception of Rebate columns after the remark columns. | PO31, PO61 |  |
| 38514 39034 | EDI processing between SM3 customers | Fields have been added to the Vendor Maintenance, Warehouse options, and Customer Maintenance to allow  clients to record their own and their vendors’/customers’ EDI Mailbox IDs. This automates the process of sending a PO to a vendor and creating the sales order. POA (purchase order acknowledgement) and ASN (advanced shipment notification) EDI transaction types are now catered for, which completes the loop/cycle of purchasing/selling between SM3 customers. | PO11, IN19, AR17, TK1 (see Electronic Data Interchange (EDI)) |  |
| 38702 | Document tracking for PO receipts | Document tracking has been added for RC, BR, RR, and RP documents. | PO41, WF21, OE6J |  |
| 39033 | Identify which logs are picked for a receipt | A Reservations button has been added to the Header and Details tabs that allows you to view all documents reserving the logs on the receipt. | PO41 |  |
| 39052 | PO Delivery Date Change task for OP docs | If a PO is reserved against a sales and OP order and the delivery date is later changed, a PO Delivery Date Change task is created for both the sales order and OP document. | PO31, TK1 |  |
| 39074 | Close RP lines without receiving logs | You can now close pre-receipts regardless of whether there are logs to be received. You can set the P/C field to “C” for any of the lines, even if the line has no cost.  Pre-receipts will automatically close if:  - all logs on the RP have been received, or  - all lines on the RP are set as complete. | PO41 |  |
| 39448 | PO7K option to include all open statuses | The Open PO By Product - Excel report has a new option to include all open statuses.  If selected, the report will include open POs with ASG, CRD, POA statuses.  If not selected, open POs with these status will be excluded. | PO7K |  |
| 39641 | PO7N Excel output includes Mill Code and Mill Country | The Excel output of the Receipts/Sales by Log by Vendor report now include columns for the Mill Code and Mill Country. | PO7N |  |

---