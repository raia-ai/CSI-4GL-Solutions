---
title: "Importing or Exporting Line Items or Parts"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Importing or Exporting Line Items or Parts"
long_description: "Help documentation for Importing or Exporting Line Items or Parts in the 4GL system."
---

Importing or Exporting Line Items or Parts
==========================================

There are several ways to use import/export with line items in a quote or sales order:

* Create an empty spreadsheet template that you can populate in Excel and then import into
* Export existing line items to Excel for use outside of  or for editing and reimporting into .

You can also export line items when viewing the order in the sales order inquiry [OE61].

Customer parts may also be imported from an Excel file.

Creating a Spreadsheet Template
-------------------------------

The spreadsheet template includes all the fields required for the line items. Once you complete the fields in Excel for each line item, you can import the spreadsheet into a quote or sales order in .

1. To generate the Excel template, choose Sales Order Entry » SO Entry/Maintenance » SQ/SO Lines Import Excel Template [OE3Q]. The template opens in Excel.
2. Populate the spreadsheet as much as required for each product you want to add to the quote. Of note:
   * Product Code or Pseudo Code is required (Pseudo Code is recommended as it is more intuitive). If both are populated,  will use the numerical Product Code.
   * Foreign/Domestic - used to filter, enter Foreign, Domestic or leave blank for either.
   * Enter the Width and/or Length as required (depending if it’s a long product or a plate product).
   * In the Line Type column, enter “A”.
   * The SUM must be valid for the product line.
   * In the PUM Quantity field, you can either enter a value, or enter “R” to have  recalculate the quantity based on the SUM Quantity and the dimensions entered.
   * In the Price field, enter the price or enter “P” to use the price from the  price book.
   * If applicable, enter the Process (machine, cutting or process) used for this line, along with the associated PUM, PUM Quantity and Price. You can enter up to fifteen processes.
   * Optionally enter the Delivery Date, line Group and Part Number.
   * Record any line-specific remarks.
3. Make note of the file name that  assigned to the spreadsheet, then save and close the spreadsheet.

If the “Is the Machine Code Mandatory During Order Entry” switch is enabled, you must enter a primary process, PUM and PUM Quantity. However, if the inventory item (or the first raw material of the customer part recipe) has its product line warehouse option “Disable Processing Options” set to “D”, a primary process will not be required for the line being imported.

Exporting Line Items to Excel
-----------------------------

Open the quote or sales order that you want to export lines from. On the Details tab, click Excel Export.

The spreadsheet opens in Excel where you can make any changes required.

Only “Inv” and “Prt” line types will be exported.

If you intend to reimport the line items into  at a later date, make note of the file name that  assigned to the spreadsheet, or save it with a different name.

OE7XW provides a more limited export of order lines to Excel; this includes the following information: Warehouse, Document, Customer Name, Document Line, Selling Qty, Line Description\,, and up to 10
remarks per line.   
Similarly, the Quote Export function exports a subset of the lines in a quote, particularly related to material and processing values: Part Number, Feed Material, Pieces, Width, Length, Gross Weight, IUM, Net Weight, IUM, Material Price, IUM, Material Value, Processing Value, Total $.  
Neither of these exports should be used to reimport items as described below.

Importing Items from Excel
--------------------------

Open the quote or sales order that you want to import the items into. On the Details tab, click Excel Import. Retrieve the appropriate spreadsheet and click Save. All the items from the spreadsheet are added to the quote/order Details.

Any errors are listed (e.g. “Row 7 Column G Invalid SUM (Selling Unit of Measure), Not Valid For This Product Line”). Resolve these and import the spreadsheet again.

Importing Customer Parts into an Order
--------------------------------------

Use the same functions as above to import customer parts into an order, with the following specifications:

* The customer part must already exist in 5PR17. If the part does not already exist in 5PR17, you can add it when entering a line item manually. (Parts may also be imported into 5PR17 from Excel; .)
* Create a spreadsheet either via OE3Q or Excel Export, as described above.
* Add a row in the spreadsheet for each part to be imported, with the following values:
  + Line Type = Prt
  + SUM and PUM = the pricing unit of measure of the part
  + Enter the Part Number and the SUM and PUM quantities
  + See note above re primary processing options.
* Use the Excel Import as described above to import the spreadsheet.

Excel SQ/SO Import Template Column Values for Importing Line Items
------------------------------------------------------------------

The following values relate to importing line items; see the section above for values required when importing customer parts.

Column names in red are required always or based on the red Validation Rules description.

| Column | Column Name | Validation Rules |
| --- | --- | --- |
| A | Product Code | If not given then only look for Pseudo Code |
| B | Pseudo Code | If Product Code is given ignore Pseudo Code |
| C | Foreign/Domestic | Valid values: 'D'omestic, 'F'oreign or blank |
| D | Width | Mandatory for Square (SHAPE\_CATEGORY = 'S') products (if Width is Cut) |
| E | Length | Mandatory for Square (SHAPE\_CATEGORY = 'S') or Long (SHAPE\_CATEGORY = 'L') products (if Length is Cut) |
| F | Line Type | Always be 'A' (Inventory Reserve Against PO) |
| G | SUM | Selling Unit of Measure |
| H | SUM Quantity | Selling Quantity |
| I | PUM | Pricing Unit of Measure |
| J | PUM Quantity | Pricing Quantity (valid values: blank/0/>0, 'R' or “Gross Multiplier with P Suffix, e.g. 50P for 50 Percent” to Recalculate)  If PUM and SUM are same then SUM Quantity and PUM Quantity must be same too |
| K | Price | Selling Price (valid values: blank/0/>0 or 'P' for Pricebook) |
| L | Primary Process | If Machines are mandatory at least Primary Process must be populated |
| M | PUM (Primary Process) | Pricing Unit of Measure If Price is not given as ‘P’ then PUM is always required, otherwise must be blank for Pricebook |
| N | PUM Quantity (Primary Process) | Pricing Quantity (valid values: blank/>0 or 'R' to Recalculate) If Price is not given as ‘P’ then Quantity is always required, otherwise must be blank for Pricebook For Regular (not 'E') lines, if Price is not given as ‘P’ then Quantity is always optional, otherwise must be blank for Pricebook Quantity is always required and must be > 0 positive number for 'E' and 'D' lines, even when Price is 'P' |
| O | Price (Primary Process) | Price (valid values: blank/0/>0 or 'P' for Pricebook) |
| P...BS | additional process columns including PUM, PUM Quantity, and Price | Up to fifteen processes can be entered provided prior process fields are entered; for example, the fields for Seventh Process cannot be entered unless Primary, Second, Third, Fourth, Fifth, and Sixth Process are entered. See M, N, O descriptions above. |
| BT | Delivery Date | Optional, in system Delivery Date format |
| BU | Group | optional, max 3 characters |
| BV | Part Number | optional, max 84 characters |
| BW…CS | Remark Type | Valid Comment Line Type for that document (TYPE\_OF\_ENTRY = SQ or SO) - up to 12 times - alternate columns starting from column BW |
| BX…CT | Remark Desc | Remark details - up to 50 characters - up to 12 times - alternate columns starting from column BX |
| CU…CW | UDF (1-3) | User defined fields if configured to be included in a sales order |
| CX | Dim 1 - Fin Size | A non-zero number can only be imported if the product line has the tolerance input option set and the dimension is a valid dimension; for example, if the product line only has two dimensions, non-zero numbers cannot be imported for Dim 3 fields. |
| CY | Dim 1 - Tol 1 |
| CZ | Dim 1 - Tol 2 |
| DA | Dim 2 - Fin Size |
| DB | Dim 2 - Tol 1 |
| DC | Dim 2 - Tol 2 |
| DD | Dim 3 - Fin Size |
| DE | Dim 3 - Tol 1 |
| DF | Dim 3 - Tol 2 |
| DG | Dim 4 - Fin Size |
| DH | Dim 4 - Tol 1 |
| DI | Dim 4 - Tol 2 |
| DJ | Dim 5 - Fin Size |
| DK | Dim 5 - Tol 1 |
| DL | Dim 5 - Tol 2 |

---