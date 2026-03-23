---
title: Setting Up Form Print Options
source: madcap.md
version: '1.0'
last_updated: '2026-02-19'
short_description: Setting Up Form Print Options
long_description: Help documentation for Setting Up Form Print Options in the 4GL system.
---

# Setting Up Form Print Options

Print options are defined for each warehouse in IN19 > Forms.

Each form type is listed, and you can control the print options, form options, fine print, and remark line types for each form separately. A + in the column indicates that there are applicable options for that form.

## Changing the Header Information

The header information that prints on each form includes the company name, address, logo, tax code, and remittance information. To define or change any of this information, click Change Logo/Address.

Enter or change any of the information. For the company name and address lines, select any combination of the check boxes to format it as **B**old, _I\*\*talic_, and/or Underlined. For the company name, select the Font Size for landscape and portrait forms.

To enter a translation of a line, click the … beside the line. The language options are defined for your implementation in MS44. \[xref to where languages are further discussed]

## Print Options

A form's print options allow you to control which printer or which printer tray to send different form types to, the number of copies to print, if it should print in landscape orientation, etc. For example, you may want to print regular sales orders from tray 1 with white paper but print backorders from tray 2 with yellow paper.

To access the print options, click … or press F4 on the P column.

The C column (Customer Copy) controls if a copy of the form (sales orders, quotes, invoices, MTRs, delivery notes/packing lists) prints for the customer. This works in conjunction with the Document Delivery options set for in the customer maintenance file (AR17): the form will print when the Customer Copy (“C”) checkbox is not selected in the IN19 print options; however if the Customer Copy checkbox is selected in the IN19 print options, then the form will only print if the checkbox in AR17 is also selected.

On the print options screen, create an entry for each type of document that you print the form for, using the W column to specify the document type, as shown in the image above. The options available in the W column are shown at the bottom of the screen and are applicable for form types as follows:

| Form Code                      | B - BT | D - Diff | I - Invoice | K - Backorder | M - Manifest | O - OP | P - POS | R - Pre-Inv | S - Same |
| ------------------------------ | ------ | -------- | ----------- | ------------- | ------------ | ------ | ------- | ----------- | -------- |
| 01 Credit Note                 |        |          | ü           |               |              |        | ü       | ü           |          |
| 02 Debit Note                  |        |          | ü           |               |              |        | ü       | ü           |          |
| 03 Delivery Note               |        |          |             |               |              |        | ü       |             |          |
| 04 Invoice                     |        |          | ü           |               |              |        | ü       | ü           |          |
| 05 Picking List \*             |        |          |             | ü             |              | ü      | ü       |             | ü        |
| 07 Sales Quote                 |        |          |             | ü             |              |        |         |             |          |
| 08 Sales Order                 | ü      |          |             |               |              | ü      | ü       |             | ü        |
| 11 Receiving Report            | ü      |          |             |               |              |        |         |             |          |
| 16 Machine Production Schedule | ü      |          |             |               |              |        | ü       |             |          |
| 17 Blind Shipment              |        |          |             |               |              |        | ü       |             |          |
| 18 Bill Of Lading              | ü      |          |             |               |              |        | ü       |             |          |
| 25 PO Pick-Up                  | ü      |          |             |               | ü            |        |         |             |          |
| 31 OP Pick Slip                |        |          |             |               | ü            |        |         |             |          |
| 55 BT Pick Slip                |        |          |             | ü             |              | ü      | ü       |             | ü        |
| 56 CC Pick Slip                |        |          |             | ü             |              | ü      | ü       |             | ü        |
| 58 CC Delivery Note            |        |          |             |               |              |        | ü       |             |          |

Print options set at the Operator, Machine or Bin levels take precedence over warehouse printers.

Pick slips have more involved print options; see Setting Up Pick Slip Print Options.

## Form Options

You may be able to control how various elements of a form are handled; for example, should a document number be aligned left or right, should the fax number be displayed, should the data be sorted by product line, etc. This allows you to include or format common elements differently between form types.

To access the form options, click … or press F4 on the O column. When viewing the options, you can press F9 to see the possible values for each option.

## Fine Print

Most of the forms allow for up to three lines of fine print to be printed at the bottom of the form.

To access the fine print, click … or press F4 on the F column.

Enter the desired text on one or more of the lines, then use the check boxes to format each line. The first check box controls the alignment: enter “L” for left, “C” for centered, or “R” for right. Select any combination of the other check boxes to format the line as **B**old, _I\*\*talic_, and/or Underlined.

To enter a translation of a line, click the … beside the line. The language options are defined for your implementation in MS44. \[xref to where languages are further discussed]

## Setting the Order of Remarks

To access form remark options, click … or press F4 on the R column.

If not already defined for the form, create an entry for each type of remark you want to print on the form. For each entry, select the type from the remarks defined in MS12.

Enter a number in the Ord field to indicate the sequence that the remark types will print. Top, Header, Footer, and Detail remarks will all follow this sequence. A number is required for each entry, and repeating numbers are not allowed. To delete a line, select it and press F7.

Valid remark types are set in MS12. These are the same types of remarks that can be entered in the Remarks tab of the maintenance screen for that document (e.g. OE31, PO31, etc.).

## Controlling the Email Address That Forms Are Sent From

Forms are sent by email according to the following hierarchy:

1. The name and email defined for the form in the warehouse Form Options (IN19 > Forms > press F9 to display the Name and Email fields for each form) takes precedence.
2. If the name and email are not defined for the form, then the entry operator's email address (MS32) is used.
3. If the operator's email is not defined, then it will use the warehouse email defined in the main screen of IN19.

***
