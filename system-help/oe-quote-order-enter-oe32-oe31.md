---
title: "Entering Quotes and Orders"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Entering Quotes and Orders"
long_description: "This topic provides detailed information about Entering Quotes and Orders in the 4GL system."
---


Entering Quotes and Orders
==========================

The forms for creating quotes and orders are almost identical: a sales order has additional fields to capture a PO # and an Invoice Date. In the respective forms you can:

* Create a new quote, or edit an existing quote that is still open, or convert an existing quote to a sales order. If you wish to reinstate an expired quote with the original quote date, you must change the Expiry Date (on the Header tab); to re-issue an expired quote with the current date, you must copy it to a new quote number. [xref to Copying a Sales Order?]
* Create a new sales order, or edit an existing sales order that is still open.

There are operator and warehouse options that control what you can edit on an order, based on its status, and whether the status reverts to ASG/OPN.

[... explain why/when they might want to copy a previous order or link to other documents instead.]

1. Choose Sales Order Entry » SO Entry/Maintenance » Quote Entry/Maintenance [OE32] or Sales Order Entry/Maintenance [OE31].
2. Click New.
3. On the Billing/Shipping tab:
   * If necessary, change the Sale Whse (the warehouse that the sale would be credited to).
   * In the Bill To field, select the customer. If the customer has a credit hold, the reason will display but it will not affect the quote.  
     The remaining fields may be populated with default values set in the customer file. Depending on your permissions, you may be able to edit some of these fields.
   * The exchange Rate defaults to the current rate (set in MS34) according to the Currency selected; if you want to freeze the rate for this quote so that it is not changed to a different rate in effect when the order is invoiced, select the Freeze check box.
   * Select the appropriate Ship To address, if there are multiple defined for the customer, or enter Same as Bill To, Manually enter a one-off address that will not be saved in the database for the customer, or P if the customer will pickup at the stocking warehouse. Sales Taxes are based on the Ship To (or Picked Up from) address.   
     If you select “P”, the Ship Via will change to the Ship Via that has the Pickup flag set in PO13.
   * Optionally enter or change the shipping information as required.
   * *Orders:* Optionally enter an Invoice Date if agreed upon with the customer.

   The top right corner of the Shipping section displays a count of any open orders for the same customer and ship-to as the current order. The count displays in red text if there are orders with the same required date.   
   Click the binoculars beside the count to view a list of these orders. It displays one record for each sales order and required date on the order line. A red icon highlights those that match the required date on the current sales order. If there are order lines with different required dates on a sales order, it displays once for each required date.   
   In this list you can inquire on an order, or print the order lines with the same required date as the current order to Excel.

   > * modify a manually-entered Bill To address (**Modify Address**) if enabled in the customer file
4. On the Header tab, enter overall information about the quote document:
   * the quote/order date, if other than today; change the default follow-up and expiry dates1 if necessary
   * sales personnel
   * . See also MTR Delivery Options.
   * shipping instructions (which print on the top right corner of all related documents (quotation/order, picking slip, packing slip, invoice)
   * if the selling price and pricing quantity should be hidden on the printed quote (only the final sales value will be printed); these may be set by default2
   * the form grouping (invoice type)
   * whether machine processing costs should be broken out and shown in the **F**ooter, at the end of each **G**roup, **S**elected lines only, or **N**ot broken out at all3.
   * if enabled4, you can specify whether all material must be Domestic or Foreign origin (this can also be set at the individual line level); if Domestic is selected, when picking logs you will not be able to pick a log that has a foreign mill assigned to it (in IN1F), and conversely if Foreign is selected for an order or order line, you cannot pick a log associated with a domestic mill. If the Material Origin is set to “Government Approved”, only logs from mills identified as Approved can be picked for the order. A default Material Origin may have been set for the customer (in AR17) but can be overwritten.
   * the Order Description is normally only used as an internal description but may be printed on forms5. This Order Description can also be used as a criterion when searching for a quote/order for copying.
5. The Contacts tab is populated from the customer file. Indicate which contact(s) you wish to send documents to, by fax or email6. You can also do the following:
   * add a new one-off contact (which will not be saved in the customer file)
   * change an existing contact
   * set a contact as primary for this order (Primary is printed on the order documents)
   * view and manage the customer’s contacts list.
6. The Details tab is where you identify what is included on the order. Here you can:
   * Add Line, From Logs, Invoice Logs - add a line item from a product line, from inventory, or from entire logs
   * Add Part [need info (should this be included in the Add a Line topic?)]; [the part number for the selected customer part is shown in the part number field; when using customer parts in an order the revenue will come directly from the customer part recipe – no price books for material or processing will be used]
   * Add Cost - add a charge that is not related to inventory that will be shown on the order  
     Cst/Rev - add a charge that is not related to inventory that will be hidden from the customer
   * Modify Line - modify the selected line
   * Delete Line - delete the selected line(s)
   * Lines - copy detail lines from another quote or order
   * Clone - clone a line on the order, e.g. for different lengths of the same product
   * Resequence - change the order of the detail lines (either enter all new line numbers in the New column, or enter a new line number for one or more lines and click AutoFill to populate the remaining lines in order; for example, if there are four lines and you change line 4 to “2” and click AutoFill, the lines will be renumbered as 1,3,4,2)
   * Surcharges - automatically add the alloy surcharge to the order (only applies when you have the Auto Surcharge feature enabled) [will be documented later]
   * Prices - recalculate the sales prices based on the price book tables, e.g. to combine lines for quantity breaks (only applicable for Price Book pricing); this button may be configured7 to refresh all individual price lines rather than grouping them.
   * Re-Price - price adjustments against one or more lines
   * Excel Import, Excel Export, Quote Export - import line items from, or export to, a spreadsheet
   * Nest - nest selected line items, or import line items into a new sales order and nest them at the same time.

   Click ![](../Resources/Images/i_arrow_down.png) to access additional buttons.
7. The Remarks tab displays any optional remarks that apply to this customer and order. You can edit, delete, or add new remarks here, or click Template to add a predefined remark template that you can further edit. Click Mandatory to view any mandatory remarks; these cannot be edited or removed.
8. The Summary tab displays a summary of the order; select a line and click Qty Ordered to view the logs picked for that order line.
9. The Payment tab is for use with Point of Sale orders only.
10. * If a contact is specified to receive an email (on the Contacts tab), you can edit the subject and message for this order.
    * - It will print and may also be sent to the customer depending on settings in the customer file8. For a quote, you may receive an alert if the customer has credit issues to consider if the quote is later converted to a sales order.   
      If there are other orders with the same ship-to address, customer and stocking warehouse with lines that have the same delivery date, a report may print9 displaying the lines on other sales orders along with the delivery date. MTRs may be included with an emailed quote10. The salesperson may be BCC'd on the confirmation email11. A “Terms & Conditions” PDF may be attached to the email.12
    * **O**ne-Step Invoicing - if you have appropriate permission13 and the sales order meets the required criteria, you may choose this option to finalize the sales order and print the packing slip (option not available if criteria not met)
    * ConVert the quote to a sales order

When the order is processed:

* If the customer file is set to credit hold, or the order meets any of the other credit hold criteria, the order is placed on hold and must be approved in the Task Manager before it can be processed.
* If the order is not placed on credit hold and the warehouse options are not set to batch print pick slips, the pick slip is printed and the warehouse can continue with the picking confirmation.
* If the warehouse options are set to batch print pick slips, the pick slip must be released from the queue.

If the order is a blanket order, add a note or remark on the order to tell the warehouse to ignore the pick slip. When ready to send partial quantities to the customer, use the Blanket Order Pick Slip Release [OE72C] to create a pick slip for the partial quantity.

[CHM: “Quotation is sent to the Purchasing department for approval, if there are buyouts or outside processing orders present (based on Company Purchasing policies in System Control Maintenance).” - still accurate/relevant?]

Configuration


1  > Follow Up Days for Sales Quotations, Quote Expiry Days for Sales Quotations

2  > Hide Quote Price by Default, Hide Quote Pricing Quantity by Default

3  > Break Out Processing Revenue

4  > Enable Material Origin Selection at Order Entry

5  > Print Order Description on Forms

6 If MS33 > Order Entry - Auto fax/email sales order = ”No”, the fax sales order and email sales order fields will be disabled even if there is a fax/email set up on the contact.

7  > Refresh Order Prices to Default

8  > Email Orders/Quotes With Writer As Sender; Email Packing Lists With Writer As Sender — if enabled, the email sent to the contacts is sent from the email address of the order writer. If not enabled, the email is sent from the salesperson.

9  > Print Delivery Date Report

10  > Email MTRs with Quote

11 Salesperson's email must be defined in MS32, and Salesperson Maintenance [OE13] must be set to email the quote and SO to the salesperson.

12 The Terms PDF must be named “TERMS10107.pdf” for quotes and “TERMS10108.pdf” for sales orders. These must be added to the /usr/dev9/virtual\_machine/stm315/forms/ folder.

13 MS32 > Options > Order Entry > One-Step Invoicing

---
