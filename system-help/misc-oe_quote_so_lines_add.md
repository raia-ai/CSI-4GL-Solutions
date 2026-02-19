---
title: "Oe Quote So Lines Add"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Oe Quote So Lines Add - 4GL Help Documentation"
long_description: "This topic provides detailed information about Oe Quote So Lines Add in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Adding Line Items to an Order
=============================

The Details tab on a quote or sales order is where you identify the products the customer is ordering.

The order line can be driven from a product line or reserved directly from your logs/inventory.

You can import multiple lines, or existing customer part numbers, from an Excel spreadsheet.

Choosing From a Product Line
----------------------------

1. Click Add Line. If configured, you may see a Sales History window.1
2. On the Product tab:
   1. In the Product field, enter a product line or product pseudocode, or press F4 to select the product.2   
      If you selected a cut product, enter the desired dimensions either as a fraction or a decimal. Fractions may be entered with a space or a dash (e.g. 1 1/2 or 1-1/2) and will be converted to its decimal equivalent.
   2. The Remarks field displays the first remark associated with the product. Drill into the field to view all mandatory and default remarks associated with the product. You can edit or remove a default remark but not a mandatory remark. Click Sel Rmks to view all remarks including optional ones. Here you can select any remarks to add to this line item, including adding back a remark that you may have erroneously deleted or modified on the previous screen.
   3. Optionally enter a customer Part Number3. If you enter an existing part number, any revenue information associated with it is added to the order.   
      If this is a new part number that is not yet in the Customer Part Maintenance [5PR17], you can add it by selecting the check box beside the field. When the sales order is processed, the part will be added to 5PR17 with the product code assigned to the part. If you are entering a quote, the part number will not be added to 5PR17 until the quote is converted to a sales order and the order is processed. If the check box is not selected, the part number only prints on this order and is not saved in . [need more info about the use of part numbers]

      Up to three user-defined fields4 may be listed below the Part Number field.
   4. If you are processing the material, select the Primary Process2 and the Tolerance.  
      Notes re tolerances:
      * If the “Defaults Previous Product Code If A Cut Product” switch is enabled, the product code and tolerances entered for an order line are repeated for subsequent lines.
      * You can apply tolerances to multiple order lines; the lines must have the same product and the product must accept tolerances. On the Details tab of the order, click the down arrow ![](../Resources/Images/i_arrow_down.png) in the bottom right of the screen twice until you see the Tolerances button. If any of the lines already have tolerances defined, you will be asked if you want to overwrite them.
      * If the “Automatically Open Tolerance Window in Or Entry” switch is enabled, when you enter an order line for a product with tolerance input enabled and processing options enabled (Disable Processing Options set to “S” or blank), you will be prompted to apply tolerances.
   5. Select the Selling Quantity - the unit of measure and the quantity. The On Hand Reserve Qty weight is calculated automatically, including kerf; click ![](../Resources/Images/i_wrench.png) to see how it was calculated and adjust it if necessary (including overriding the billing weight, if applicable).
   6. Select the Pricing Quantity unit of measure. The price is calculated automatically; tab to enter a new price per selected UOM, or click Alt Prc if you want to set a price per lb, or to calculate the price according to a desired gross margin amount or percentage, or markup percentage. If the Process Breakout on the Header tab is set to “S”, in the pricing screen you can select which lines should appear on separate lines.
   7. If you want to use the actual cost of the logs that are picked on the order, even if the product is set to average costing, select the Freeze checkbox5.
   8. To exclude the order from the usage table (PO52), select the Ex Usg checkbox. This sets the flag against the invoice.
   9. Indicate if the material origin of this line item must be Domestic or Foreign. Corresponding text may print on the sales order/quote form6.
   10. If the material is sourced from multiple warehouses, select “Whse” in the Source field to create the branch transfer automatically. If you are doing an intercompany sale, select “Vendor”.[need info re other Source  options (Inventory/Vendor/Whse (+ OP in 3.14)) & related fields] 

       Warehouse Source orders may use the replacement cost of the product in the order warehouse rather than the average cost of the product in the sending warehouse7.
   11. Surcharge, Group/Freeze8 (if using Price Book pricing (from my notes:) “can assign a pricing group to override the system grouping to a different letter/number”; however, tooltip just refers to freezing the price for the order line); if Group/Freeze selected, the line cannot be edited in the customer portal)
   12. If material is being shipped directly from your supplier to your customer, select the Direct Delivery check box. When the PO is received, logs will automatically allocate to the sale and the picking confirmation will automatically be processed. When receiving direct delivery buy-ins, if the "Auto Pick Cost and Remark
       Lines" switch is enabled, the invoice will include both the inventory line and the cost line. Note that a packing slip will not be generated and these orders will go directly to Shipping Confirmation [OE42].
   13. If the order's Form Grouping (on the Header tab) = G and this line item is part of a group, enter the Form Group code. See Grouping Line Items below.
   14. If the order's Form Grouping = G or L, you may select the Hide check box to hide the line on the sales order, quote, invoice, and packing list forms. The value of the hidden line will be included in the lot charge for lot sales or group totals for groups. The weight of the hidden line will be excluded on the delivery note.

Click Sales or Quotes to view the history of sales (or quotes) of this product to this or all customers.

3. Optionally, on the Log Reservation tab, select specific log(s) that you want to sell from.

Click Filters to located logs with a specified minimum or maximum width or length.

4. [purpose of PO Allocation, Cut Details tabs?]
5. Click Save to return to the quote or sales order. Repeat as needed for additional products.

Grouping Line Items


If a product should be considered the “master” or fabrication product, to the right of the Form Group field select if **A**ll other lines in the group will be printed, or just the **M**aster product. Each group can only have one master product; this line will have a pricing quantity, a value, but no weight.

If there is no master product, the lines will print normally on the sales order by group. The quantity and value at the end of each group will be the sum from each line of the group, and the price is the value divided by the quantity.

If there is a master product and it is set to “A”, then it will still print the lines in the group.  
If there is a master product and it is set to “M”, then it will only print the master product line.  
In both cases, the value will still be the sum from each line of that group. The quantity will be the quantity on the master product, and the price is the value divided by the quantity.

Choosing From Logs/Inventory
----------------------------

Use this function if you are selling items from logs; if you are selling an entire log, use the Invoice Logs function described below.

1. Click From Logs.
2. Select the product. The Modify Line Item window opens on the Log Reservation tab, displaying all logs and their available inventory.
3. For each log that you want to sell from, select the S checkbox. The full available quantity is selected; change the number of Pcs if necessary. When you are finished, click Save to reserve the items.
4. The window changes to the Product tab. If you selected items of different lengths, the Line Description reflects the range selected. The Selling Quantity is calculated from the total quantities selected in the previous step. Change any other fields as required (see above).
5. [purpose of PO Allocation, Cut Details tabs?]
6. Click Save to return to the quote or sales order. Repeat as needed for additional products.

Choosing Entire Logs
--------------------

Use this function if you are selling full bundles/logs; if you need to select partial quantities from a log, use the From Logs function described above.

1. Click Invoice Logs.
2. Indicate how you want the logs to appear on the order - individual line items for each Log, or grouped by Product/PUM.
3. Enter the Log Number or click … to find it. You can select logs from different product lines.
4. Enter the PUM and Sales Price for each log.
5. Click Save. The lines are added to the order according to your Group By selection.

Configuration


1  > Sales History Popup=”Y”

2 If the order is destined for SigmaNEST, product lines and machines (primary process) must have plate nest integration enabled (in IN16 > Warehouse and  respectively) in order to be included in the export to SigmaNEST (PR44B)

3  > Enable Customer Parts Field in Order Details

4 IN19 > OE Options > UDF Descriptions; any UDFs configured in IN19 will display beneath the Part Number field when adding a line to an order/quote; if there are no UDFs configured in IN19, a UDFs field will be visible but disabled. UDF fields must be configured (in IN19 > Form Options) to be included on individual forms. If the check box beside the UDF Description (in IN19) is selected, the field value will be copied to subsequent lines in the sales order.

5  > Skip/Disable Freeze Cost (controls if the Freeze flag is skipped in tagging or not selectable at all)

6 IN19 > Forms > Sales Order/Sales Quotation > Form Options

7  > Use Replacement Cost for Warehouse Source Orders

8  > Disable Pricing Group (controls if the Group/Freeze check box is enabled); and Default Order Freeze Flag (defaults the flag to Y)

---
