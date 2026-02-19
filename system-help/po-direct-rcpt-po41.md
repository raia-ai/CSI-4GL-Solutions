---
title: "Direct Receipts"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Direct Receipts"
long_description: "Help documentation for Direct Receipts in the 4GL system."
---

Direct Receipts
===============

This function is used to receive inventory based on a purchase order.

1. Choose Purchasing » Receiving » Purchase Order Direct Receipts [PO41].
3. Enter or select Type Of Entry: BR = branch receipt, CS = consignment receipt, RC = receipt.
4. Enter or select Document number or New document.

When you the print labels it will either print one label per piece or one label for the bundle of pieces, depending on the product label configuration1.

On the Details tab, press F4 on the This Rcpt field to view details for a receipt log. Here you can print labels for the receipt log, or create one or more duplicates of the last created receipt log.

[not sure if this is the right place for this, but capturing it here for now anyway:]

BG 37817 - Two new switches are used when a sales order is reserved against an incoming PO or IP/OP:

* “Set Only Used Quantity When Allocating Incoming” – only sets the used quantities for logs that are allocated to the order when the PO/IP/OP is received
* “Release Orders When Allocating Incoming” – move the line(s) to PCK if they are in PBP status

A Receipt Confirmation task may be sent to the salesperson2.

BG 39074 - You can now close pre-receipts regardless of whether there are logs to be received. You can set the P/C field to “C” for any of the lines, even if the line has no cost.  
Pre-receipts will automatically close if:  
- all logs on the RP have been received, or  
- all lines on the RP are set as complete.

BG 39869 - If the exchange rate for a receipt is not defaulted from the purchase order3 and upon processing a newer rate is found, user will be asked if they want to refresh the rate.

BG 40536 - Auto-receive RP document - When creating a pre-receipt, a new processing option, “O” (one-step), allows you to process the document and automatically create and receive the receipt. “O” is not available for “RC” documents, only “RP” documents.

BG 40537 - Clone logs in receiving - The Duplicate button on the receipt log window has been enhanced with additional parameters:  
- MTR filename and case: duplicates the last log with the new MTR file name and case number.  
- Increment Case checkbox: duplicates the last log with a new case number that has been incremented by 1. If Copies is set to more than 1, the case number is incremented for each duplicated log.  
- Pieces  
- Length and Width fields are enabled if the dimensions exist for the product shape and the dimension is not fixed on the product. Fractional fields are enabled if the fractional dimension is set for the product line (e.g. if the length is in FT for the product line and the fractional UOM is in inches for the product line, the fractional field is enabled for inches).  
- BUM Quantity is updated according to the new pieces, length and width, but is editable.

40542 - When entering logs in PO41, you can now enter “P” in the MTR field to create an MTR name consisting of the PO number and PO line number. For the first receipt entered against a PO line the format will be P000001-001.PDF, and the - will change to A,B,C, etc. from the second receipt onwards(P00001A001.PDF, P00001B001.PDF, etc.).

Configuration


1 Product Label Piece / Bundle Flag [IN1ZA]

2  > Create Receipt Confirmation Task:  
- If set to blank, then no new receipt confirmation tasks will be created.  
- If set to "H" (hard allocation only), then new receipt confirmation tasks will be create for sales orders that are allocated to the received PO line.  
- If set to "S" (soft allocation only), then new receipt confirmation tasks will be created for sales orders that have committed out for the same product.  
If an open receipt confirmation task already exists for a sales order, it won't create a new task no matter what the switch is set to.

3  > Default Receipt Exchange Rate From Purchase Order

---