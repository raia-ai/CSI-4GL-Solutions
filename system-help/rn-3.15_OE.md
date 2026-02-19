---
title: "Order Entry"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Order Entry"
long_description: "This topic provides detailed information about Order Entry in the 4GL system."
---


Order Entry
===========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 28570 | Display bill-to name from order header, not from customer file | When the Bill-To name is overridden on a sales order, this name is reflected on order/invoice inquiries and reports so that “cash sale” orders are more informative. Screens that are not related to an order/invoice will continue to use the customer bill-to name from AR17. | OE42, OE62, OE64, OE74 |  |
| 37090 | Streamline direct delivery buyout process | Allow you to bypass picking confirmation for direct delivery shipments (when material is shipped directly from your supplier to your customer). To use this feature, select the new Direct Delivery check box when adding an order line. When the PO is received, logs will automatically allocate to the sale and the picking confirmation will automatically be processed.  Note: A packing slip will not be generated and these orders will go directly to Shipping Confirmation [OE42]. | OE31/OE32 |  |
| 37489 | Export detail lines from OE61 | When viewing the Details tab of an order from the Sales Order Inquiry, you can export the order lines to Excel in the same format as in order entry. | OE61 |  |
| 37504 | Add Remarks Description to Excel export | Sales order export includes remarks descriptions. | OE3Q, OE61, OE31/OE32 |  |
| 37516 | Use order writer as sender when emailing SO/SQ | New switch controls who an order/quote email is sent from: if the switch is enabled, the email is sent from the email address of the order writer. If not enabled, the email is sent from the salesperson. | > Email Orders/Quotes With Writer As Sender |  |
| 37578 | Add display window in OE61 to view header costs / revenue added to order during order entry | New Cst/Rev button added to sales order inquiry (details tab) to view header costs / revenue added to order during order entry. | OE61 |  |
| 37610 | Attach terms & conditions PDF to SO/SQ | A Terms & Conditions PDF can be attached to all order and quote emails. | The Terms PDF must be named “TERMS10107.pdf” for quotes and “TERMS10108.pdf” for sales orders. These must be added to the /usr/dev9/virtual\_machine/stm315/forms/ folder.  Please contact our office to load the form. | OE31/OE32 |
| 37663 | Ability to email OE743 from batch run | The Invoice Summary by Document report (by Detail Lines - OE743B) can be added to a batch run in BT92 | MS32 > Email Parameters - add the report and parameters to the operator  BT92 - add OE743B to a batch run |  |
| 37706 | Option to include cost lines in OE7G | New check box in the Open Order Report filters to include cost lines. | OE7G |  |
| 37759 | Suppress the ability to change pay term/taxes on invoices if they have been posted | On the Change Invoice Header Information form, you can no longer change pay terms or taxes if the invoice has been posted (i.e. status is END, POS, or INV). | OE9I |  |
| 37814 | Prevent user processing SO if Required Date in past | New switch controls what happens if a user changes the Required Date on an order to a past date: If set to “N” (no check) - the date will be changed as normal If set to “S” (soft warning) - a message will appear but user can choose to continue, the date will change If set to “H” (hard warning) - a message will appear and the date will not change. | > Check If Requested Date On Order Line Is Before Today | Editing an Order (changing the Req Date) |
| 37936 | Changes to operator access to PCK order details | The operator-level PCK Order Access now includes an option to warn or prevent changes to lines that have logs picked. | MS32 > Options > Order Entry > PCK Order Access > Picked/Delivered Lines |  |
| 38104 | Surcharges on OE7X can be printed in more detail. | The Sales by Customer By Product Line report parameters now allow surcharges to be printed individually on separate lines. | OE7X |  |

---
