---
title: "Entering an Outside Processing Order"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Entering an Outside Processing Order"
long_description: "Help documentation for Entering an Outside Processing Order in the 4GL system."
---

Entering an Outside Processing Order
====================================

An OP order can manage multiple forms of processing (sets) on one document. The set type depends on the Process code selected:

* One-to-Many — one RM (e.g a coil) producing many FG items (e.g. sheets of different sizes)
* Many-to-One — several different RM items produce one FG item (e.g. a recipe or fabrication)
* Many-to-Many — many RM items producing many FG items (this process does not have any traceability).

You must decide how many sets are required in a processing document. For example, if a number of different sheet sizes are being cut from one coil, this will constitute one set; but if different sheet sizes are being cut from different coils, that would require multiple sets.

1. Choose Outside Processing » OP Entry/Maintenance » OP Entry/Maintenance [PP34].

   All open OP orders are listed. You can use the filters on the left to locate an existing document to modify or copy (e.g. a repeat order). Using the Link button, documents representing inbound material (e.g. purchase orders) can be linked to the raw material of the OP document that you are creating, and lines will automatically be created in the OP document from the document that you are linking from. For example you can link an OP document to a purchase order to send all the line items on that PO out for processing, or you can link to another OP document. Similarly, a sales order can be linked to an OP document. When creating the finished goods you will be able to link them to documents representing outbound material.

   You can create OP orders from sales order lines in the machine production schedule.  
   You can also create an OP document by linking to a linear nest document: from the OP entry window, click Nest and retrieve the nest document. The system will create an OP document with one set per pattern; each set will have one raw material, one log and a number of finished goods.
2. Click New.
3. On the Header tab:
   * Select the Vendor that you are sending the material to for processing, and the vendor's location that they will Ship From when finished processing.
   * Enter the Due Date when the order is required to be either returned to your warehouse or shipped elsewhere.
   * The vendor's Contact name, Currency and Pay Terms default to those defined in the vendor's file but may be overridden.
   * Enter or change the shipping information as required, including how you are going to send the material to the vendor (To Ship Via) and how it will be returned from the vendor (From Ship Via).
   * The Shipping Costs entered here are termed “header costs” and should only be used if the exact same cost applies to all sets in the document. The costs default to those defined in the vendor's file but may be overridden.
   > * enter the number of Packages defined in the document's sets; this information will print on the packing slip to tell the warehouse what will be loaded on the truck
4. Click the Sets tab.
   1. You may be prompted1 to confirm or enter any header costs, e.g. third party freight, packaging, etc., that apply to the entire document. These costs are converted to the price per CUM and included in the cost of each finished good. Close the window when you are finished to continue to the Sets tab.  
      You can also click Hdr/Lot Costs to enter a header or “M” line lot charge to be distributed proportionally by weight across all finished goods lines in the set.
   2. Click New Set, select the machine Process Code and change any of the default settings if required, then click Save. Repeat if necessary to record additional sets.
5. Click on the set in the table to go to the Details tab for that set. Here you define the raw material(s) involved and the finished good(s) that will be created in that set.
   1. Add the raw materials:
      * If you know the log number you want to send, click Add Logs. Enter or select the Log Number. Add another log or click Close.
      * If you don't know the log number, click Add RM to select from your product list.
        + Select the product and then enter the Unit and Quantity to use. If necessary, click Size to enter the size. For example, if you are cutting pipe in house before sending out to the processor enter the size of the cut pieces. For inches only, enter a 0 in the FT field. If the log has variable specs, click Specs to capture these.
        + On the Logs tab, select the log. To change the raw material log without having to remove the lift records from the finished goods, click Swap. The system will check to ensure that the available quantity is greater than or equal to the usage of the original log. The system will update the properties of existing lift records (baby log numbers, heat, case, etc.) with the properties of the new log selected.  
          If necessary, you can split a log that has already been assigned to the order—in effect this removes the log, splits it, and then allocates the cut piece.
        + Use the Committed tab to reserve the raw material against incoming stock. You can reserve against more than one incoming document.
      * If the selected product code does not have a theoretical weight, you will be prompted to enter the weight.
   2. Add the finished goods:
      * Click Add FG. On the New tab select from your product list.
      * The Produce Unit Qty fields default to the theoretical piece count that can be produced from the selected raw material. This number will be superseded once actual logs are selected.
      * Click the … beside the Produce Unit Qty field to enter the lift details for the pre-receipt logs that will be created. Each line represents a finished good log; the log # generated will be the same as the raw materials log with an incremented prefix. For example, if the RM log is LA05292, the FG logs will be AA05292, BA05292, CA05292, etc. The sum of the pieces in this window is updated to the Produce Unit Qty field.

        If you are going to bundle pieces together, e.g. three pieces per skid, click Bndl/Pcs and enter the number of Packages and Pcs/Pck (and select the log if there is more than one identified for the set), then click Gen Lifts. This creates the number of lift records in one step, rather than creating them individually.
      * Click the … beside the Cost Price field to review the cost breakdown of the finished goods: the raw materials cost, yield/loss, machine cost, and any header costs such as freight. You must enter the charge from the outside processor against the appropriate machine cost. Raw materials on OP orders may be costed using average cost or replacement cost2.

        If you have any lines with Pricing UOM=PCT, if you change the value of another line you must click the refresh button ![](../Resources/Images/i_refresh.png) to recalculate the PCT items.
      * Click Save. The window changes to the Commitments tab that displays the outbound documents. Here you can allocate the finished goods to an open sales order or other documents that represent outbound material. Click Save to close the window.
   3. Optionally repeat step b to create additional finished goods .
   4. If you want to change the order of the detail lines in the Raw Materials or Finished Goods section, click Resequence RM or Resequence FG as applicable. Enter new line numbers in the New column, or click Same to populate the New column with the current sequence and change the ones required.
   5. All sets must be balanced (all of the raw material weight must be allocated against the finished goods; a difference between raw material allocated and finished goods produced will result in a yield loss/gain).  will attempt to do this when you process the document. However, there are times when you may want to control the allocation manually for a set; see below for an explanation of automatic and manual balancing.
6. If necessary, return to the Sets tab to create another set.
7. * \* - Select the documents to print. Note that a Packing Slip can only be selected if you selected logs for a set; some other options are produced at the confirmation step [xref]. The Subcontract may3 list the quantity and pieces beside the raw material logs, and the quantity, pieces and case number next to the lifts.

   * .

Balancing Sets
--------------

All sets must be balanced (all of the raw material weight must be allocated against the finished goods). If the FG Allocation in the Raw Materials section of a set is greater than the sum of the RM Allocation in the Finished Goods section, i.e. you are not using 100% of the raw material, the allocation process will allocate the full weight to the finished goods lines based on a weight proportion of the finished goods. For example, if the weight of the RM was 120lb and there are two FG of 60lb and 40lb, the allocation would be 72lb and 48lb respectively.

Allocation may result in a Yield/Loss (if RM Allocation>Produce IUM) or Yield/Gain (if RM Allocation>Produce IUM), and this change in weight changes the cost of the FG. To see the Yield/Loss (or Gain), open the FG record and then open the cost screen.

### Automatic Allocation

During processing,  attempts to allocate and balance open sets. If the variance between the raw material and finished goods quantity exceeds the percentage defined for the warehouse4, the allocation is aborted and the set remains open to allow you to make changes.

If a set is balanced and closed, you will see a green checkmark in the Bal column on the Sets tab. If you see a red x instead, click Set Status to view information about the set and the reason it may not have been balanced and closed.

### Manual Allocation

If you have multiple FG lines you may want to allocate all of a Yield Loss to a particular line; for example, if you are shipping one line to a customer and returning the other line to stock, you want to allocate the Yield Loss to the customer order. Similarly, you may require that a specific FG has a fixed allocation. To handle these, enter the required allocation and then “freeze” that quantity. The allocation ignores the frozen line and allocates the remainder to the “non-frozen” lines.

1. Open the FG record you want to remain unchanged and select the Freeze check box.
2. Click Allocate RM.

   If you have already run the allocation, open the FG record to change the RM Allocations value to match the value in the Produce IUM Qty field, select the Freeze check box, and then click Allocate RM again.

Configuration


1 PO15 > The header costs window will automatically open if a header cost is defined on the OWPRO shipping term

2  > Processing Raw Material Costing Method

3 IN19 > Forms: for forms 23 and 32 set Options 7 and 8 = “Y”

4  > Variance Pct For Raw Mat vs Fin Gds Alloc

---