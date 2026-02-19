---
title: "In Inv Count Checklist"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "In Inv Count Checklist - 4GL Help Documentation"
long_description: "This topic provides detailed information about In Inv Count Checklist in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Inventory Count - Checklist
===========================

Physical inventory counting can be a tedious chore. Perform the following procedures prior to the count to ensure a smooth and accurate physical inventory count:

**In the warehouse:**

* CLEAN UP THE WAREHOUSE!!! If you have scrap inventory toss it out now! You don’t want to slow down the count trying to determine what a product is. Ensure product in racks can be easily counted (sort those junk piles!). If some items are not standard lengths, measure them and write the length on the metal to save time during the count. Try to ensure inventory tags exist on all products.
* Draw a floor plan of the warehouse displaying all racks / bin locations – this floor plan will be posted for all to see. As counts are complete for each location they are marked complete on the floor plan.
* Are there any products in the warehouse that do not have a product code?

**In** **,** check the following screens to ensure accuracy of system data:

* Confirm: Open Orders (OE61), Inside/Outside Processing orders, Pick Slips (OE41), Packing Slips (OE42), Invoices (OE42), any outstanding credit notes.
* Receivers [PO62] - Open receivers should be checked and posted, or deleted. Pre-receivers must be checked to ensure who owns title of goods; any whose title belongs to purchaser must be counted.
* Open Purchase orders [PO61] - purchase orders with past due delivery dates must be checked to ensure they were not received and updated with an accurate expected delivery date.
* Open Sales Orders with Past Due delivery dates [OE6H] must be checked to ensure they should still be open. If not, locate the paperwork (picking slips) cancel the sales order.
* Open Delivery Notes not yet posted to GL [OE62] - review any delivery notes that were created but not yet shipped to determine if they are to be counted during physical count; e.g. orders may ship on day of count and may not need to be counted (depends on invoice date).
* Log items without MTRs [IN7G] - If not done on a regular basis, this is a good time to ensure that logs have MTRs attached (if using Electronic MTR control)
* Product weights [IN1I] - Ensure product weights are correct (especially important if you are planning to count by pieces).   
  Products with negative theoretical weight [IN7N] - If not done on a regular basis, products should be reviewed to ensure correct theoretical weight.
* Ensure you have no open Branch Transfers that have been picked but not received by the Receiving location (if you have multiple warehouse locations).
* Ensure there are no open Inside Production orders where work has been started - you will have to count the original raw material used.
* Review your Miscellaneous Product Codes… there should be no stock. If there is, create an adjustment transferring stock to a product code (IN31).
* Outside Processing – will your stock be at a vendor during the physical inventory count? If so, you will have to count/enter the original raw material manually using the count sheets.
* Ensure all invoicing is posted prior to starting the count – you cannot start entering tickets until all invoices are posted. Items that are picked, to be shipped/picked up after inventory, must be put in one area in order to identify items that have already been invoiced.
* Staff who will be entering the inventory count manually will require screen IN5E on their menus.
* If using Bin Locations, ensure all Bin Locations exist and counters are aware of the Bin Location codes in the warehouse.

If you are not using  handheld devices, download this sample Excel spreadsheet for counting inventory on paper before transferring to .

Configuration


If using handheld, ensure the Physical Inventory  function [WF15] is available on each device's menu.

The following switches (in ) affect physical inventory counting:

At the system level:

* Hide Inventory Pieces on Inventory Count? - if “Yes” you will be unable to count pieces for your inventory count
* Hide System Quantities on Inventory Count? - if “Yes”, system quantities for each log will not display at data entry time, but will allow operator to input physically counted pieces of the log
* Provide Additional Options on Inventory Count? - if “Yes”, enables a “More Options” window in Inventory data entry window to allows change to average cost for the selected log
* Default Cost on Inventory Count - Indicates the default cost price for each log in the inventory count entry window:  
  **Z**ero cost
  \*\* Setting the cost to zero will set all the log costs to zero and is NOT recommended – call 4GL to clarify
  \*\*
    
  **A**verage cost
    
  Blank = system cost will be used (default/recommended option)
* Sort Inventory Count Logs by Length? - if “Yes”, sorts logs on the data entry screen and reports by length
* Use Tags on Inventory Count? - set to “Yes” if using tag numbers as part of physical inventory count

This switch can be set at the system level to apply to all warehouses, or left blank at the system level and set at the warehouse level instead if you will be counting warehouses separately.

At the warehouse level:

* Use Tags During Inventory Count? - see above
* Print A Label For All Logs?
* Only Floor Bin Locations Types?
* Is Variable Spec Mandatory?
* Show Prod with Compatible Specs Only in Picking Conf?
* Allow Zero Pieces On Logs?
* Keep the Same Numeric Log Number for Spawned Logs?
* Exclude Neg Adjustments from E&O Calc?
* Days Without Stock Back

---
