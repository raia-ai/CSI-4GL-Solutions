---
title: "Ip Op Import Rm Fg Lines Pr3Q Pp3Q"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Ip Op Import Rm Fg Lines Pr3Q Pp3Q - 4GL Help Documentation"
long_description: "This topic provides detailed information about Ip Op Import Rm Fg Lines Pr3Q Pp3Q in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Importing Raw Material and Finished Goods Lines
===============================================

The Import function allows you to import multiple raw material and finished goods lines into an in-house production document from an Excel spreadsheet. To do this, you will create a spreadsheet template, complete the fields in Excel for each line item, and then import the spreadsheet into the IP/OP document in .

This procedure also applies to importing into outside processing documents: use PP3Q to generate the template, populate the spreadsheet, then import it into the OP document.

1. To generate the Excel template, choose In-House Production » Production Document Controlled » IP Create Excel Import Template [PR3Q]. The template opens in Excel.
2. Populate the spreadsheet as much as required for each line you want to add to the IP document. Of note:
   * Product Code or Pseudo Code is required (Pseudo Code is recommended as it is more intuitive). If both are populated,  will use the numerical Product Code.
   * Optionally enter up to six specs; these must be variable and configured for the product line.
   * Enter the Width and/or Length as required (depending if it’s a long product or a plate product).  
     If the product line allows random dimensions, you can enter a random length/width in the form of min-max; e.g. 10-20.
   * Record any line-specific remarks.
3. Make note of the file name that  assigned to the spreadsheet, then save and close the spreadsheet.
4. Open the IP document that you want to import the lines into. On the Details tab, click the down arrow ![](../Resources/Images/i_arrow_down.png) in the bottom right of the screen to get to the Excel Import button. Retrieve the appropriate spreadsheet and click Save. All the line items from the spreadsheet are added to the document Details.

Any errors are listed; resolve these and import the spreadsheet again.

Excel Import Template Columns
-----------------------------

Column names in red are required always or based on the red Validation Rules description.

| Column | Column Name | Validation Rules |
| --- | --- | --- |
| A | Product Code | If not given then only look for Pseudo Code |
| B | Pseudo Code | If Product Code is given ignore Pseudo Code; Pseudo code must be prefixed with the Product Line code (i.e. SFL) |
| C | RM/FG | Mandatory. “RM” to indicate the line is a raw material, “FG” to indicate the line is a finished good. |
| D | Width | Mandatory for Square (SHAPE\_CATEGORY = 'S') products (if Width is Cut) |
| E | Length | Mandatory for Square (SHAPE\_CATEGORY = 'S') or Long (SHAPE\_CATEGORY = 'L') products (if Length is Cut) |
| F | UOM | Mandatory. For RM this is the used quantity unit of measure. For FG this is the produced quantity unit of measure. |
| G | Quantity | Mandatory. For RM this is the used quantity. For FG this is the produced quantity. |
| H | FG Freeze RM Alloc | **Y**es to freeze raw material allocation for a FG or blank. Not effective for RM lines. |
| I | Spec1 | A valid spec can only be included if the spec code is variable for the product. For a spec to be variable, it must be set as variable on the product line, and blank on the product. A spec is valid if it is defined for the product line. Applicable to RM or FG. |
| J | Spec2 |
| K | Spec3 |
| L | Spec4 |
| M | Spec5 |
| N | Spec6 |
| O...AK | Remark Type | Valid Comment Line Type for that document (TYPE\_OF\_ENTRY = IP or OP) - up to 12 times - alternate columns starting from column O |
| P...AL | Remark Desc | Remark details - up to 50 characters - up to 12 times - alternate columns starting from column P |
| AM | Dim 1 - Fin Size | A non-zero number can only be imported if the product line has the tolerance input option set and the dimension is a valid dimension; for example, if the product line only has two dimensions, non-zero numbers cannot be imported for Dim 3 fields. |
| AN | Dim 1 - Tol 1 |
| AO | Dim 1 - Tol 2 |
| AP | Dim 2 - Fin Size |
| AQ | Dim 2 - Tol 1 |
| AR | Dim 2 - Tol 2 |
| AS | Dim 3 - Fin Size |
| AT | Dim 3 - Tol 1 |
| AU | Dim 3 - Tol 2 |
| AV | Dim 4 - Fin Size |
| AW | Dim 4 - Tol 1 |
| AX | Dim 4 - Tol 2 |
| AY | Dim 5 - Fin Size |
| AZ | Dim 5 - Tol 1 |
| BA | Dim 5 - Tol 2 |

---
