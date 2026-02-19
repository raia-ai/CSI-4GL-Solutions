---
title: "Issuing Credit or Debit Memos"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Issuing Credit or Debit Memos"
long_description: "Help documentation for Issuing Credit or Debit Memos in the 4GL system."
---


Issuing Credit or Debit Memos
=============================

There are several scenarios where you may need to issue a credit to a customer, such as:

* The customer wants to return a product (e.g. if it was damaged or an incorrect item)
* The invoice was incorrect (overcharged due to the wrong amount or wrong price)
* The invoice included tax and the customer has a tax exemption.

If you are creating a credit memo related to an invoice, the invoice must have already been posted.

Conversely, a debit memo allows you to bill the customer for an amount without going through the normal order process. Debit memos work the same as credit memos—the only difference is you select “DM” instead of “CM” (which is default) at time of creating the document. This topic will focus on credit memos.

Credit memo document numbers start with a “K”, debit memo document numbers start with a “D”.1

Typical Workflow
----------------

The workflow hinges on whether return slips are enabled for the warehouse2. Ideally they should be, because that is the only way to get a list of the goods to be picked up and returned to the warehouse.

1. Salesperson with appropriate permission3 enters the credit memo and sends for authorization.
2. Approval manager reviews and authorizes the credit memo.

If return slips are not enabled for the warehouse, the credit memo is issued to the customer at this point and applied to AR4.  
If return slips are enabled for the warehouse:

1. A return slip is generated that lists the goods to be returned; the driver uses this to go pickup the goods.
2. Once the goods are marked as received in , the credit memo is issued to the customer and applied to AR.

   The Received check box will automatically be selected for non-inventory lines (Line Type “C”, “O”, “P”), but can be set manually by any user with “Authorize” permission3.

While credit figures appear positive in the entry form,  can be configured to show negative amounts on the credit note document sent to the customer.5

To create a credit note to reverse an entire invoice and return all products to the warehouse where they were shipped from, use the Quick Credit Note [OE45A] instead. A Quick Credit Note is processed immediately: no authorization is required and no return slip is generated.

Creating a Credit Memo


1. Choose Sales Order Entry » Invoicing » Credit and Debit Note Entry/Maintenance [OE45].
2. In the Search pane on the left, select the Type of Entry (CM or DM), then click New.
3. In the Select Reference Document prompt:
   * Select the Type of document that the credit memo refers to, then select the Document number. Typically this will be an invoice, but you could also create a credit memo to counter a previous debit memo (or vice versa). You cannot have two unauthorized credit memos in process against the same invoice at the same time. If you don’t want to reference any document, enter \*\* in the Type field.
   * Generate Lines? - include all the lines from the reference document on the credit memo (select this if you are crediting most of the document). If you select “Y”, then in the Return Log As field indicate whether the goods should be returned to the Same or a New log number (this may be selected by default6). Any S lines on the order are converted to C lines on the credit note.

   If Return Log As = N,  will create the same log number with a different prefix; e.g. if original log # = L000058, the new log number for the returned goods will be A000058. All characteristics (Case, MTR, Mill etc.) of the original log are retained.
   * Select a Reason Code. If you also selected Generate Lines, all lines will have this reason code. If you did not select Generate Lines, when you add the lines manually the reason code defaults to this reason code; if you change the reason code for a line, it becomes the new default reason code for subsequent lines.
   * Click Save. The Credit/Demo Entry screen opens.

     If you attempt to create a credit note with a different sales warehouse than the one on the invoice, you may see a warning7.
4. On the Billing/Shipping tab, change the Terms or Currency if necessary. The Shipping Information section reflects where the goods are to be picked up. To see where the goods should be returned (or sent) to, click Ship To.
5. On the Header tab, enter or change the Memo Date8. Enter a Memo Description (this may be mandatory9), and optionally enter the Financial Impact and Description (these can be reviewed on the Financial Impact report).   
   If this is a non-inventory credit memo, select the Received? check box so it can automatically be finalized after authorization.

   If the warehouse is set up to require Non-Conformance Reporting10, you must enter the Error Track ID, Operator, Department, Error, and Description. See Non-Conformance Reporting and Error Tracking.
6. On the Details tab:
   * If Generate Lines was selected in step 3 above, this screen displays all the lines from the referenced document. Double-click on a line (or select it and click Modify Line), then select the Reason Code for the credit, and change the Invoice Quantity affected if necessary.
   * If Generate Lines was not selected, click Add Line to enter a credit line:
     + Select the Line Type:
       - Cost - revenue only line, used for non-inventory credits (e.g. perhaps goods were slightly damaged but the customer will keep them and be given a discount). Enter the total Value that you want to credit — you cannot credit more than the total amount on the original invoice.  
         Select the Sales Cost category that defines the G/L codes that will be affected.
       - Inventory - return of shipped goods to inventory.   
         Select the line number from the invoice. You are then prompted to Select whether the Same or a New log number will be used for the returned goods; change the details of the goods or log as required. You could also leave the Select field blank and manually select the log.
       - Over Invoice - used when the customer was overcharged for material (e.g. the actual weight of goods received was less than the weight charged); enter the selling and pricing quantities that should have been invoiced (not the difference that you are crediting).  does not expect it to be returned to inventory.
       - Price Adjustment - invoice price was incorrect - enter the price that should have been charged (not the difference that you are crediting).
     + Select the Reason Code for the credit, and change the Invoice Quantity and/or Invoice Value affected if necessary.

     To return a log to multiple baby logs: Do not select Generate Lines and clear the Select field to add a new log manually. When you return it, you can select the same log and return it to multiple baby logs.
7. On the Remarks tab, enter any remarks as required.
8. * - submit the credit note for authorization


   * Report - If return slips are enabled, depending on your permissions3 you will either get an authorization report (if your CM/DM Security flag=“A”) or a return slip (if your CM/DM Security flag =“M”). If your CM/DM Security flag=blank, you will not see the “R” option at all. If the credit memo has not yet been processed, it will be placed on Hold.  
     If return slips are not enabled for this warehouse, an authorization report is generated.


Authorizing a Credit/Debit Memo


If return slips are enabled for the warehouse, credit memos must be approved via the Task Manager. A “CM/DM Approval” Diary Group must be defined and assigned to the CMDMAPPROVAL Task Type.

If return slips are not enabled for the warehouse, the credit memo must be authorized as follows:

1. Choose Sales Order Entry » Invoicing » Credit and Debit Authorization [OE46].
2. Retrieve the list of unauthorized memos. Review the list; press F4 on the Total Value field to drill down to the memo details and further to the log details.
3. To authorize a memo, enter “OK” in the Auth column. A credit/debit note will print, inventory will be returned to stock (if applicable), and the credit/debit will be applied against the customer’s account. An email may be sent to the order writer11.


Finalizing/Issuing the Credit Memo


If return slips are enabled for the warehouse, the credit memo is not issued until the goods have been returned and marked as received.

1. If you have the appropriate security3, open the credit memo.
2. If the credit note contains “I” inventory lines, enter into the inventory line and adjust the log details as necessary to reflect exactly the material that has been returned.
3. On the Header tab select the Received? check box and click Process.
4. Enter “H” to put the credit memo on hold.
5. Go into the Shipping Confirmation [OE42] [xref] and change the status to “OK”.

The credit memo will be emailed to the customer and routed to Accounts Receivable4.

When a credit memo for a SigmaNEST IP containing a customer part log is processed, the customer part log is automatically exported to SigmaNEST.



Creating a Quick Credit Note


Use this to create a credit note to reverse an entire invoice and return all products to the warehouse where they were shipped from. A Quick Credit Note is processed immediately: no authorization is required and no return slip is generated. The invoice must have already been posted.

If you need to credit/debit a partial amount of the original invoice, or to assign log remarks at time of return, use the more detailed Credit/Debit Note Entry Maintenance [OE45] as described above.

1. Choose Sales Order Entry » Invoicing » Quick Credit Note [OE45A].
2. Change the Warehouse if necessary, and select the Invoice you are reversing.
3. Change the Credit Note Date if necessary.
4. In the Return Log As field, indicate if inventory should be returned to the Same or a New log number (this may be selected by default6).
5. In the Financial Impact field, press F4 or click … to record the financial impact or cost for this transaction, such as packing/unpacking, shipping etc. These can be reviewed on the Financial Impact report.
6. Enter “Y” in the Create? field.

Configuration


1 If  > Assign Invoice/CM/DM Number By Whs = Y, credit/debit document numbers are incremented at the warehouse level.

2  > Issue Return Slips for CM/DM

3 Credit Note security involves several permission settings:  
- in Options > Order Entry,  the CM/DM Security flag may be set to allow the operator to Modify, Authorize, or only enter credit notes (blank); a user with Authorize permission can enter or modify credit notes, and mark a credit note as Received.  
- a limit may be set that requires higher approval in  > CM/DM Approval Manager Override Limit for Non-Inventory Limits  
- if such a limit is set, only operators who also have the CM/DM Manager flag set in Options > Order Entry can authorize credit notes above those limits.

4 If  > Do Not Apply CM/DM to Invoices = Y, credit notes are not automatically applied to their corresponding invoices in the AR subledger but instead will show as a separate credit. They would have to be manually applied via Document Application [AR33].

5  > Show Negatives on Credit Note

6  > Default Credit Note to Same Log Number

7  > Display Warning For CM/DM Different Warehouses

8  > Default Credit/Debit Memo Date to Today

9  > Is Credit/Debit Memo Desc Mandatory

10  > Mandatory Non-Conformance Reporting

11  > Email Body for CM/DM Approval Email

---
