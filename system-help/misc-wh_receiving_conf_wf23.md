---
title: "Wh Receiving Conf Wf23"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Wh Receiving Conf Wf23 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Wh Receiving Conf Wf23 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Receiving Confirmation
======================

Used to receive stock where a pre-receipt exists.

1. In the Doc field, enter or select an existing Receiving Confirmation #, or enter N to create a new one.
2. Optionally, in the Ref field enter a supplier reference number for the material, e.g. a barcode from the packing list.
3. Optionally, select the Mill to help identify barcodes in the event of a conflict between two or more.
4. In the Case field, scan the barcode on the tag you are receiving. The system will look for a pre-received log where the value of the tag scanned is equal to the value of the case number field on the pre-received log. The scanned value can be parsed through the Barcode Query Maintenance (PO1K) prior to trying to match the fields.   
    The complete value of the barcode scanned (prior to barcode query) will be stored on the logs.   
   You can also enter a log number to retrieve the case number.   
   The corresponding PO number is populated. If there are any allocations against this material, you will see the sales order and required date and amount.
5. Repeat step 4 to receive additional materials as applicable.

As you scan barcodes, the case numbers are added to the table along with one of the following Status codes:

* 1=success (bundle was found on a pre-receipt)
* 2=case # was previously scanned on a different receipt but not processed
* 3=case # has already been received
* 4=case # cannot be found on any receipt or pre-receipt.

When you process, lines with status 1 will set the received flag to “Y” and the processed receipt will be sent to Task Manager for approval. Any lines with error status 2-4 will generate a receipt confirmation error and an investigation task will be created in
Task Manager.

At any point you can press F3 to see the action options:

1 - Process  
2 - Abort - this deletes all scanned case numbers  
3 - Hold - this retains the scanned case numbers and exits the screen; you can enter the Doc number at a later date to resume  
4 - Scan - resume scanning   
5 - Inquire/Delete - go into the table to review or delete any lines

Upon processing:

* The Receipt Confirmation # (RF) is printed on the Receipt Report and
  displayed on the Receipt Inquiry screen (PO62).
* If you received all logs on an RP (pre-receipt) line, the RP will be closed automatically.
* Labels are printed:
  + If the mill on the receipt log is blank, or the mill is not identified as a mill exception (in IN1ZA):
    - if the product's receipt label type (in IN1ZA) = bundle, it will print one label
    - if the receipt label type = piece, it will print the same number of labels as the number of pieces.
  + If the mill on the receipt log matches one of the mill exceptions for the product (in IN1ZA), the opposite will occur:
    - if the product's receipt label type = bundle, it will print the same number of labels as the number of pieces
    - if the receipt label type = piece, it will print one label.
* A Receipt Confirmation task may be sent to the salesperson1.

Configuration


1  > Create Receipt Confirmation Task:  
- If set to blank, then no new receipt confirmation tasks will be created.  
- If set to "H" (hard allocation only), then new receipt confirmation tasks will be create for sales orders that are allocated to the received PO line.  
- If set to "S" (soft allocation only), then new receipt confirmation tasks will be created for sales orders that have committed out for the same product.  
If an open receipt confirmation task already exists for a sales order, it won't create a new task no matter what the switch is set to.

---
