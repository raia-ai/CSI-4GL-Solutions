---
title: "Order Entry"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Order Entry"
long_description: "Help documentation for Order Entry in the 4GL system."
---

Order Entry
===========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 34345 | Enter trip times for each drop on a manifest | A new screen allows you to go into a manifest run after it has been processed to enter trip times for each customer delivery. | MN32 |  |
| 38164 | Reprint delivery notes from manifest | When processing a manifest, if you select a previously processed run, the prompt to reprint reports now includes delivery notes. | MN31 |  |
| 38221 | Customer filter added to AR7N | The Salesperson Call Report can now be run by a single customer or All. | AR7N |  |
| 38378 | Change to status indicators for quotes on Inventory Inquiry | When a quote has been converted to a sales order, its status (“S” column) = “P”. When a quote has been closed, its status now shows as “C” to more easily differentiate. | Inventory>Detailed Inquiry>Quotes |  |
| 38388 | Display operator in Scheduled tab of OE61 | The Scheduled tab of the Order Inquiry now displays the operator who completed the job. | OE61 |  |
| 38414 | “Government Approved” mills | The Mills form (IN1F) now includes an “Approved” check box to identify if the mill is approved for government projects.  The Material Origin field on a sales order Header tab now includes a “Government Approved” option. If this is selected, only logs from mills identified as Approved can be picked for that order. | IN1F |  |
| 38453 | Display Assigned and Picked/Loaded in Run inquiry from OE61 | The Manifest Run Assignment Inquiry screen accessed from OE61 now displays the line items assigned to the run as well as the logs picked for the run. | OE61 |  |
| 38520 | Manifest information visible in CM Inquiry | If a credit memo is added to a manifest, when you select it and click Inquire on the Documents tab the CM Inquiry that appears now includes a Run button and Manifest tab. | MN31, OE62 |  |
| 38586 | UDF fields added to sales order import/export | The three user defined fields that appear to the right of remarks have been added to the Excel export/import functionality. | OE3Q |  |
| 38595 | Estimated times displayed in repricing window | If an estimated time was entered against multiple processing lines in the pricing window, the summary section at the top of the repricing window will display the total estimated processing time. The estimated time is also displayed when modifying a process line in the repricing window. | OE31 |  |
| 38617 | Upload compressed file with OE9XA | The Customer Pricing Import function can import a compressed Excel file (in zip or rar format) as long as the compressed file only contains one file, that file is an xls or xlsx file, and the spreadsheet is filled out correctly. | OE9XA |  |
| 38635 | Primary process displayed on Details tab | The Details tab on a sales order, quote, or inquiry now displays the primary process if entered for a line. | OE31/OE32, OE61 |  |
| 38764 | Clone random length lines | Random length products can now be cloned in an order. The dimension will be copied from the source line; you cannot change the size. | OE31/OE32 |  |
| 38766 | Modify price/value of processes and apply to selected lines | A Processing button has been added to the mass Reprice window where you can modify the price/value of processes for selected lines. You can also add new codes for lot charges that would be distributed across the selected lines. Related, the Summary tab of the order now includes two new columns (Stock Value and Proc Value) and a Processing button that shows a summary of the processes for the whole order. | OE31 |  |
| 38767 39121 | Preview pick slips in Order Inquiry | A new Pick Slip button on the sales order inquiry for BT, CC and SO documents allows you to view a PDF of the pick slip. The PDF includes “Preview” as a watermark (as well as “Backorder” if applicable). | OE61 |  |
| 38768 | Prevent processing if log reservations but zero picked | New operator switch controls what happens if a user tries to process an order containing log reservations with no picked quantity in OE41, MN31, and WF11: If set to “N” (no warning) - the order is processed without any warning If set to “S” (soft warning) - a message will appear but the order can be processed. If set to “H” (hard warning) - a message will appear and the order cannot be processed. | MS32>Options>OE>Additional Options>Warning If Used Logs Not Picked OE41, MN31, WF11 |  |
| 38791 | Option to include “Reprint” on OE7B | The Sales Order Reprint now has an option to print the word “Reprint” in the top right corner. | OE7B |  |
| 38881 | Print UDF fields on return slip | A new Forms option allows any UDF entered on an order line to be printed on the return slip. | IN19>Forms>Return Slip>Display UDF |  |
| 38899 | View scanned order documents in Order Inquiry and Invoice Inquiry | A new Order Docs button on the Billing/Shipping tab of the order /invoice inquiry allows you to view any scanned documents attached to the order. The storage location for such scanned documents must be defined in one of two new switches (“Order Documents Linux Directory” and “Order Documents Windows Directory”) to allow for them to be retrieved.  Scanned files must be named the sales warehouse of the order + document number.pdf (e.g. 10W012345.pdf). | OE61, OE62 |  |
| 38907 | OPs in PAR status can be added to a manifest | OP documents in PAR status can now be added to a manifest. You can only add RM and FG for sets that have not been received or completely assigned to any runs. | MN31 |  |
| 38914 | Switch to control ScantoInvoice task | A new switch (“Create Scan to Invoice Task From Manifest”) controls whether a ScantoInvoice task is generated (resulting in a release status of “OK” in OE42) when a delivery note is generated from a manifest. |  |  |
| 38948  39128 | UDF fields added to OE61 and OE62; columns added to OE31 Details | The UDF fields on a sales order are now visible on the Sales Order Inquiry and Invoice Inquiry, as well as the Details tab of the sales order. Note that the column headings will be UDF1, UDF2 and UDF3, not the headings assigned to those fields in OE31 (i.e. Job Number, Detail Number, Nest). | OE61, OE62, OE31 |  |
| 38979 | Display SO and IV numbers on credit note header | The sales order and invoice numbers are now displayed in the header of the credit note and debit memo forms. |  |  |
| 39002 | Fin Size and Tolerance can be imported into a sales order for up to five dimensions | Fields have been added to the export/import Excel file for five dimensions (Dim 1-Fin Size, Dim 1-Tol 1, Dim 1-Tol 2, Dim 2-Fin Size, Dim 2-Tol 1, Dim 2-Tol 2, etc.).  A non-zero number can only be imported if the product line has the tolerance input option set and the dimension is a valid dimension; for example, if the product line only has two dimensions, non-zero numbers cannot be imported for Dim 3 fields). | OE3Q |  |
| 39127 | LRSHPLBN displays warehouse name instead of company name | The shipping label now displays the warehouse name (from IN19) instead of the company name (from MS33). | IN19, LRSHPLBN |  |
| 39134 | Display machine pricing remarks on pick slip and OE61 | A new form option has been added to the Pick Slip form to include any remarks entered on an order for machine price lines. When enabled, the remarks print below each machine line. These remarks are also visible in the Sales Order Inquiry: a new “Proc Rmks” button has been added to the Scheduled tab. | IN19>Forms>05>Form Options>Display Machine Remarks OE61 |  |
| 39208 | New columns added to OE74 | The following new columns have been added to the Excel output of the Invoice Summary by Document report: Replacement Cost (for products only), UDF fields, Currency, Currency Rate, Sales Value, and Tax Value. | OE74 |  |
| 39295 | Numeric Run ID added to run sheet | The Run Sheet produced from a manifest includes a numeric run ID prefixed with “MN”. | MN31 |  |
| 39316 | Changes to OE74 | Changes have been made to the Excel output of the Invoice Summary by Document report: - Some column names changed to reflect that their values are in local currency (e.g. Loc Sale Price, Loc Sales Value, etc.). - New column (Price Qty \* Rep cost) displays the pricing quantity multiplied by the replacement cost for the product. | OE74 |  |
| 39340 | Changes to OE74A | The Customer Detailed Invoice Report can now be filtered to all or select machines. Columns have been added to the Excel output for the sales and stocking warehouses as well as physical machine (this corresponds to the physical machine on the first machine cost line). | OE74A |  |
| 39364 | “Use Second Base Price” added to OE1N and OE1M | The field "Second base price" has been added to OE1N (export customer pricing) and OE1M (import customer pricing). | OE1N, OE1M |  |
| 39534 | Payment terms added to OE74 | A new field allows you to filter the Invoice Summary by Document report to a specific payment term (or leave ALL). Excel output now includes a Payment Term column. | OE74 |  |
| 39714 | FG Product Code added to OE74 | Excel output of the Invoice Summary by Document report now includes an FG Product Code column. | OE74 |  |

---