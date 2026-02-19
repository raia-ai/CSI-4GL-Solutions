---
title: "Importing Line Items from Excel"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Importing Line Items from Excel"
long_description: "Help documentation for Importing Line Items from Excel in the 4GL system."
---


Importing Line Items from Excel
===============================

The Import function allows you to import multiple product lines into a purchase order from an Excel spreadsheet. To do this, you will create a spreadsheet template, complete the fields in Excel for each line item, and then import the spreadsheet into a purchase order in .

If you are using the Material Requirements Planning report (IN7YR) or the Inventory Sales Usage Report (IN7ZI), you can enter order quantities and prices into the resulting spreadsheet, then run a utility (PO3E or PO3F, respectively) to convert it into another Excel file formatted for import into a purchase order.  
In either case, skip to step 4 below.

1. To generate the Excel template, choose Purchasing » Entry/Maintenance » PO Lines Import Excel Template [PO3D]. The template opens in Excel.
2. Populate the spreadsheet as much as required for each product you want to add to the purchase order. Of note:
   * Product Code or Pseudo Code is required (Pseudo Code is recommended as it is more intuitive). If both are populated,  will use the numerical Product Code.
   * Enter the Width and/or Length as required (depending if it’s a long product or a plate product).  
     If the product line allows random dimensions, you can enter a random length/width in the form of min-max; e.g. 10-20.
   * In the Line Type column, enter “I” - this is currently the only line type supported.
   * The BUM must be valid for the product line.
   * In the PUM Quantity field, you can either enter a value, or enter “R” to have  recalculate the quantity based on the BUM Quanity and the dimensions entered.
   * In the Price field, enter the price or enter “P” to use the price from the  price book.
   * If the Delivery Date is not defined in the spreadsheet, the import will assign the document date plus the lead time as set for the vendor. The delivery date on the template cannot be before the document date.
   * Record any line-specific remarks.
3. Make note of the file name that  assigned to the spreadsheet, then save and close the spreadsheet.
4. Open the purchase order that you want to import the lines into. On the Details tab, click Excel Import. Retrieve the appropriate spreadsheet and click Save. All the line items from the spreadsheet are added to the purchase order Details.

Any errors are listed (e.g. “Row 7 Column G Invalid SUM (Selling Unit of Measure), Not Valid For This Product Line”). Resolve these and import the spreadsheet again.

Excel Import Template Column Values
-----------------------------------

Column names in red are required always or based on the red Validation Rules description.

| Column # | Column Name | Validation Rules |
| --- | --- | --- |
| 01 - A | Product Code | If not given then only look for Pseudo Code |
| 02 - B | Pseudo Code | If Product Code is given ignore Pseudo Code; Pseudo code must be prefixed with the Product Line code (i.e. SFL) |
| 03 - C | Width | Mandatory for Square (SHAPE\_CATEGORY = 'S') Products (If Width is Cut) |
| 04 - D | Length | Mandatory for Square (SHAPE\_CATEGORY = 'S') or Long (SHAPE\_CATEGORY = 'L') Products (If Length is Cut); Length unit of measure depends on setting in IN16 > Options > Search Unit. For example, if Search Unit=“IN”, then for 12' lengths you must enter 144. |
| 05 - E | Line Type | Always be 'I' |
| 06 - F | BUM | Buying Unit Of Measure |
| 07 - G | BUM Quantity | Buying Quantity |
| 08 -H | PUM | Pricing Unit Of Measure |
| 09 - I | PUM Quantity | Pricing Quantity (Valid Values: Blank/0 or 'S' to recalculate); if PUM and BUM are same then BUM Quantity and PUM Quantity must be same too. |
| 10 - J | Price | Purchase Price (Valid Values: Blank/0 or 'P' for Price Book); Purchasing Price Book is maintained in Vendor Pricing Maintenance [PO4F] |
| 11 - K | Remark Type | Valid Comment Line Type for that document  (TYPE\_OF\_ENTRY = SQ or SO) - Up to 12 Times |
| 12 - L | Remark - OEDRM\_REMARK | Remark Details - Up to 50 Characters Long - Up to 12 Times |

---
