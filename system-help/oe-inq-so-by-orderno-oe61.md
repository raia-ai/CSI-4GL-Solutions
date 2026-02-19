---
title: "Sales Orders By Order Number"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Sales Orders By Order Number"
long_description: "This topic provides detailed information about Sales Orders By Order Number in the 4GL system."
---


Sales Orders By Order Number
============================

This function is used to look up branch transfers, processing, production, sales orders and quote information.

1. Choose Sales Order Entry » Order Entry Inquiries » Sales Orders By Order Number [OE61].
2. Use the fields at the top to filter your search. All documents that match your criteria are listed in the table.

   If a cash customer is set to allow the address to be modified (AR17>Mod Addr), and the billing information was changed in an order, then the Customer Name can be searched or edited in OE61 and OE62.
3. Open a document to view the sales order. In addition to the information recorded on the sales order:
   * On the Billing/Shipping or Header tab:


     + view any external documents (e.g. working papers) that were attached to the sales order (Document).
     + view any proof of delivery documents generated for this order (POD).
     + view any scanned documents attached to the order (Order Docs)1.
     + view changes made to the document after the order was processed (e.g. change to selling price or delivery date, deleting or closing an order line, etc.) (Revision). These changes can be exported to Excel in Document Changes Tracking to Excel (MS73).
   * On the Header tab, view any invoices generated for this sales order (Invoices).
   * On the Details tab:
     + click Inquire to view line level details (costing/pricing, reserves, invoices, scheduled production, packages); if the order line has reserves on an IP or OP document, you can further inquire on those from the Reserves tab.
     + click Run to view details about the manifest and run the line is assigned to (if the line has been assigned to a manifest but not a run, the window will not open)
     + click Excel Export to export line items in the sales order
     + click Cst/Rev to view any header costs or revenue added to the order during order entry
   * On the Manifest tab, view the manifest runs related to the order delivery. Optionally select a run and click Inquire to open the Manifest Inquiry.
   * At the top of the sales order inquiry window for the sales order, click Preview to view a PDF of the sales order, or click Pick Slip to view a PDF of the pick slip (there will be one pick slip PDF for "ALL"; other pick slip PDFs will be generated if the "Print Separate Pickslip for Each Unique Machine/Bin on Order" switch is enabled).

Configuration


1 The storage location for such scanned documents must be defined in the “Order Documents” switch to allow for them to be retrieved.   
Scanned files must be named the sales warehouse of the order + document number.pdf (e.g. 10W012345.pdf).

---
