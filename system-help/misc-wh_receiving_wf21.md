---
title: "Wh Receiving Wf21"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Wh Receiving Wf21 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Wh Receiving Wf21 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Receiving
=========

Create or modify PO receipts. Depending on your configuration, you may be able to create a new receipt against an existing PO that already has one or more receipts.1

![](../Resources/Images/WH_receiving.png)

1. Enter the Action to be performed:   
   1=New  
   2=Modify  
   3=Exit
2. Scan or enter the PO number to receive.
3. A confirmation screen displays. [presumably they have to do some action in the box?]

![](../Resources/Images/WH_receiving_conf.png)

4. Optionally enter a supplier reference number (Ref).
5. Scan or enter the Vendor Product Code (VCd).
6. If this vendor product code has never been cross-referenced in the past, you will see the Purchase Order Details and you must select the Product Code listed on the PO.  [how to select and return?]  
    will cross-reference the Vendor Product Code with the  Product Code for future reference. This vendor-to- product code record can also be created through a maintenance function [xref PO1C].

![](../Resources/Images/WH_receiving_PO_selection.png)

7. Enter the vendor barcode (BCd) . This will be associated with the log so that during the Picking Confirmation you can retrieve all logs associated with the same barcode.

The barcodes on each log can also be maintained in IN1BC [xref] and IN1E.

If the product is set to auto-receive one piece2:

* If the heat number is extracted from the barcode, the log is immediately received as one piece, and you will be returned to the BCd field.
* If the heat number is not extracted from the barcode, you will be taken to the Ht field. Once you enter a heat number, the log will immediately be received as one piece and you will be returned to the BCd field.
* If the barcode is not recognized, you will have to go through all the required fields.

8. Enter the log information (Case, heat number (Ht) and bin location (Loc)).
9. Optionally enter any log remarks (Rmk). You can input remark 1 directly and window in to add any additional remarks.
10. Enter the total amount received in the PO Buying Unit of Measure (Bum) as well a the Inventory Unit of Measure (Inv).
11. Enter the number of log Tags required to print on the barcode printer.
12. [then what?]

Configuration


1  > Allow Multiple Receipts in HH Receiving

2 Product Label Piece / Bundle Flag [IN1ZA]

---
