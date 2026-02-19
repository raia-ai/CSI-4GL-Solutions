---
title: "Ip Sigmanest Pr44B Pr34"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Ip Sigmanest Pr44B Pr34 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Ip Sigmanest Pr44B Pr34 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Plate Nesting with SigmaNEST
============================

An order line requires the following to be exported to SigmaNEST:

* A primary machine that has Plate Nest Integration enabled1.
* The product must be a product line with Plate Nest Integration enabled1.
* The order line must have a Customer Part Number.

Once the order has been processed and is in PCK or PBP status, the line will be available in PR44B. When the order is processed, a directory for the customer will be created in the Part Drawing directory2 (if not already created), and a subdirectory for the order will be created. This sales order directory will contain a Sales directory and a Production directory. The customer directory is also created when a CAD file is attached to a line in PR44B or when a sales order is approved from credit approval or quality control.

The work order and parts are now ready to be uploaded to SigmaNEST.

In SigmaNEST, the order lines are nested and the remnant created. When the job is posted, the IP document is created in  where it can be processed and tracked. When the IP document is processed, any sales order lines reserved against the IP are released from PBP status. If the log used on the nest is the same as the log that was originally allocated to the order,  will deallocate the log from the sales order and allocate it to the IP; the finished goods of the IP will be allocated to the sales order.

A SigmaNEST program may contain a work order that is not in , e.g. for a test piece cut from the plate. In the generated IP document, the test piece does not appear as a finished good, but its weight is allocated to the finished goods for the  order(s).

Whenever a full plate is moved in or out of inventory without being processed, it will be automatically updated in SigmaNEST stock (provided the plate is a product line with Plate Nest Integration enabled).  
Plates may be marked3 as reserved in SigmaNEST (stamped with customer name) whenever a log is fully used in  for a sales
order, BT or CC.
Partially picking a log (either initially, or changing it from being fully
picked) for an order, closing the picked sales order line, or aborting the sales order will
remove the reservation.

Exporting Orders to SigmaNEST
-----------------------------

1. Choose In-House Production » Nesting » Export Work Orders to SigmaNest [PR44B].
2. This window displays all work orders that are ready to be exported to SigmaNEST; these are indicated by ![](../Resources/Images/i_round_red_x.png) in the Exp field. If your line does not show up in the list, check to ensure that it has a primary process that has plate nesting enabled, the part number field is populated, the product line has plate nesting enabled, and the line is in either PCK or PBP status.  
   Use the fields at the top to filter the list as required. If you choose to Show Exported, you will see the exported work orders indicated by ![](../Resources/Images/i_round_green_check.png).

To view details about an order, select it and click Inquire to view the Sales Order Inquiry window.

3. To attach a part file (.dxf, .dwg, or NC1 file) to an order, select the order and click Attach CAD and retrieve the file.

Alternatively, if the files are stored in the designated folder4, click Auto-Attach CAD.  will scan the Sales folder in the Workorder folder for any .dxf or .dwg files named with the part number (*partnumber*.dxf or *partnumber*.dwg). If found, the drawing will be attached to the work order line and will be copied to the Production folder.

4. When you are ready to export, select the line(s) and click Export Lines.

If a file was attached to the order line, a SimTrans transaction will be generated that will create a new SigmaNEST part based on the customer part number and file (as the drawing). It will automatically be attached to the SigmaNEST work order. This is considered a SimTrans SN85 transaction.

In the above, if the part already exists in SigmaNEST it will be overwritten.

If a file was not attached to the order line, a SimTrans transaction will be generated that will look for an existing SigmaNEST part with a name that matches the customer part number. If it finds one, the part will be attached to the SigmaNEST work order. If it does not, the work order line will be created in SigmaNEST with no part attached. This is considered a SimTrans SN84 transaction.

The files transferred can be viewed in the SimTrans dashboard.

5. Click Sync to check with the SigmaNEST database to confirm and refresh the icons in the Exp field.

Use PR57 to identify and export any logs (including customer part logs) that have not been exported to SigmaNEST. When exporting a log to SigmaNEST, the first three specifications on the log are stamped on the SigmaNEST stock item as SheetData2, SheetData3 and SheetData4.  
When a credit memo for a SigmaNEST IP containing a customer part log is processed, the customer part log is automatically exported to SigmaNEST.

Setting Up the Job in SigmaNEST
-------------------------------

Refer to the SigmaNEST documentation.

1. Set up your workspace: create a new workspace, create a new task, retrieve the work order lines to add to the workspace, select the sheet.
2. Create the remnant: choose Nesting » Auto Nest, then choose Nesting NC » Crop Sheet (example: Min % Used = 100, select Create Remnant, Crop Type=Crop Step 1, Part Offset 0.5).

The remnant directory set in SigmaNEST must be mounted to allow users to view remnant images in . If the directory is invalid, remnants will NOT be saved when posting SigmaNEST programs.

3. Post the job (Nesting NC » Post).

Tracking the Job in
-------------------

### Viewing the IP Document

When the job is posted in SigmaNEST, a corresponding IP document is created in  for each layout. To view an IP document:

1. Choose In-House Production » Production Document Controlled » IP Entry / Maintenance [PR34].
2. Locate and open the new document.
3. On the Header tab, select a Due Date.

you will see the SigmaNEST program number associated with the IP in the search list as well as on the Header tab.

1. The Details tab displays the raw material sheet and the finished goods line items, including the remnant that will go back into inventory. Modify as required.

   In the case of remnants, a corresponding dog leg record is created that can be viewed from Inventory Inquiry or from the IN1E Shape field.

   You can change the raw material log without having to remove the lift records from the finished goods: click Swap in the Logs tab of the raw material window. The system will check to ensure that the available quantity is greater than or equal to the usage of the original log. The system will update the properties of existing lift records (baby log numbers, heat, case, etc.) with the properties of the new log selected. When performing a log swap,  will attempt to submit the transaction to SimTrans every five seconds; if the maximum defined attempts5 is reached, you will be prompted to resubmit or cancel the swap.

The -Sigma Cron Activity Log [PR59] captures cron activity when validating work orders and programs pulled from SigmaNEST, and when an IP is generated. When viewing this log, you will see one or more entries for the program you posted; these may indicate that there are parts missing, or the IP was generated, or it was generated but with an allocation code, or it was generated but has non-WO parts, or there were incompatible material origins among the order lines or between the order lines and plate’s mill code.

If the nested area on a program does not equate to the total nested area from the work orders, the -Sigma cron will make a second attempt to confirm there are no missing work order parts. The IP will be generated after the second attempt regardless of whether the areas equate, under the assumption non-work order parts are part of the nest. In the IP document, the Special Instructions field on the Header tab will include a note indicating that the nest may contain non-work order parts.

A production order will only be generated if all order lines have the same specified material origin AND the plate has a mill code for the same origin.

If you find that parts are missing from the generated IP, set a buffer6 that prevents  from processing a program while SigmaNEST is still processing it.

### Processing and Tracking the Job

Shop operators use the following wireless handheld functions to finish processing the job:

* Conf Production & SigmaNEST Program  [WF1L] is used to pick and validate the log used for the production job: scan the document, which brings up the plate assigned to the job. If the operator used a different plate, scan the different log (must be same material and dimensions). If they chose a different size plate, the remnant will be different and the job must go back to the CAD department to be renested on the new plate.
* Update SigmaNEST IP  [WF1M] is used to confirm and update the IP and the SigmaNEST job.

Once the job has been processed, the IP document will be updated and materials allocated to the order(s) that made up the IP.

Configuration


1 Product lines and machines (primary process) in sales orders must have plate nest integration enabled (in IN16 > Warehouse and  respectively) in order to be included in PR44B.

2  > Part Drawing

3  > Allow SigmaNEST Plate Reservations

4  > Part Drawing

5  > SimTrans Transaction Check Max Attempts

6  > SigmaNEST Post Buffer Period

Refer to SigmaNEST Integration for full installation and configuration instructions.

---
