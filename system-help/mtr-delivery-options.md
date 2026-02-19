---
title: "MTR Delivery Options"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "MTR Delivery Options"
long_description: "This topic provides detailed information about MTR Delivery Options in the 4GL system."
---


MTR Delivery Options
====================

When creating a sales order, you indicate if a mill test report (MTR) is required: **Y**es (include the original MTR), **O**verlayed (include the original with company header overlaid), **S**ys (system-generated MTR from company, not mill), **B**oth (original and system-generated), or blank for no. Regardless of the option selected, they all can print with the Packing Slip and, if required, be emailed to the customer.

The MTRs are emailed along with the delivery note if an email address is provided in the customer's Document Delivery Options; otherwise they are printed if the Print > MTRs check box is selected. [AR17].

The following settings determine how an MTR is generated:

If  > Print Scanned and Overlayed MTRs By = “Prod Code + Heat”:

* If two or more logs have the same heat number and are in the same product code (even if they are on different lines on the order), only one MTR will be produced.
* If multiple logs are delivered an MTR will print for each unique heat number and unique MTR file.
* For overlayed MTRs, the description is the product description with cut dimension omitted.

If  > Print Scanned and Overlayed MTRs By = “Prod Code + MTR”:

If two or more logs have the same MTR filename and they are in the same product code (or if an equivalent cut product code exists), only one MTR will be produced.

For example, there are two lines on the order, one is for the SRB 304 1" x 12' product code and the other is for the SRB 304 1" x 20' product code. If an SRB 304 1" x Cut product code exists, both lines will be grouped together using the cut code, and the product description that prints on the overlayed MTR will be from the cut code and the 'Lines' section of the MTR will show both line numbers from the invoice.  
If no cut code exists in this example, one MTR will be produced for the 12' product code and another for the 20' product code. The product description will come from each product code.

If  > Print Scanned and Overlayed MTRs By = “MTR + Doc Index”:

If printing scanned MTRs there will be one MTR for each unique MTR filename. If printing overlayed MTRs there will be one MTR for each unique MTR filename and document index combination.

For example:  
If you have one line with two logs that have the same MTR filename, you will get one MTR.   
If you have two lines that both have logs with the same MTR filename, you will get two MTRs and the product description will come from each invoice line.

If both system-generated and scanned MTRs are produced, the system-generated MTR will print for each log or heat per line, depending on  > Print System Generated MTRs By Heat Number.

Overlayed MTRs


To generate an Overlayed MTR, we take the scanned MTR, shrink it and in the white space enter:

* A barcode for the warehouse code, document number, and document index
* Your Company name, Address
* Customer PO
* Customer Contact
* Product Description belonging to the MTR
* Your Invoice #
* Heat #
* Date

The MTR field on the Customer file defaults to “O” to use an Overlay – instead of “Y” to use the scanned MTR.

### Sample

![](../Resources/Images/MTR_SampleOverlayed.png)



System-Generated MTRs


System-Generated MTRs require some setup at the product line, product, and alloy level.

At receipt of products, the user must record the chemistries of each heat #.

### Setup

1. Set up sets of min/max limits for each chemical element in the CVC field of the Alloy/Type [IN14]. Each set is assigned to a Chemical Validation Code.
2. Add the appropriate chemical validation code to each product code [in the Chem Val Code field in IN18].   
    can assist if all product codes in a product line will use the same CVC.
3. Define the product line to allow input of chemistries and physical properties [IN16 > F9 > Options].  
    can assist if all product lines will have the same options.

### Entering Chemistry During Receiving

During receiving, you may be prompted to enter the chemical composition of each heat # received, depending on the setup described above.

### Sample

The MTR includes a barcode for the warehouse code, document number, and document index.

![](../Resources/Images/MTR_SampleSysGen.png)

MTR Storage Location(s)
-----------------------

MTRs are stored in one of two locations, depending if you are using the Desktop version or the browser version of . An archive folder can also be defined to store older MTRs, to keep the main folder at a manageable size for efficient searching. When retrieving an MTR,  will look first in the main folder, then in the archive folder if the file is not found in the main folder.

These are configured in the “MTR” and “MTR Archive” switches respectively.

---
