---
title: "About"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "About - 4GL Help Documentation"
long_description: "This topic provides detailed information about About in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


About Pre Receipts
==================

[all of this is from old help]

##### **Definition**

A Pre Receipt is a Receipt prepared by paperwork received from the supplier with the Physical Inventory in-transit. If supplier has forwarded copy of Bills of Lading, packing slips and/or Mill Test reports (MTR’s) at time of shipment, Receiving staff can execute pre-Receiving procedures.

##### **Purpose**

Two main reasons for using Pre Receipts

Receiving staff can create a Pre Receipt early, which will eliminate the administrative “paperwork backlog” for Receiving staff when receiving Mill Shipments

Staff can view Inventory In-transit details, providing them with Product code and quantities to be physically received, as well as realistic delivery dates (Information is better updated than Committed In quantities on Purchase Order)

##### **Creating a Pre Receipt**

Pre Receipts are entered, similar to a Material Receipt

Pre-Receipts are created when the Receipt is processed using “R” (print Receiving Report) or “H” (Hold). There is an option (click to select (Yes) in “Received” field in screen PO41) to make Logs available to select for creation of Delivery note (Stock has arrived, but Receiving has not finished receiving all line items on Receipt).

When the Receipt is complete, and material has been fully received, the Receiver is posted. At that time, Average costs for product will be updated and entries will be made to Inventory and AP Sub files

##### **Transient Tags**

Upon creation of Pre-Receipt, Steel Manager III will generate relevant tag numbers (known as Transient tags) and Inventory labels. If MTR’s are available, they can be scanned and indexed to the Log numbers, if not, MTR’s can be indexed at a later date using MTR Image Indexing – PO45.

##### **Viewing Pre Receipts**

Pre-Receipts by Purchase Order can be viewed using the Purchase Order Inquiry – Committed In Quantities|group=ViewCommitedInForProductInquiry. Pre-Receipts are displayed in Red. Transient Tag numbers can be viewed in the Inventory on Hand|group=InventoryOnHand screen. Transient Tag Logs are displayed in Red (Exhibit A)

Exhibit “A”

Pre Receipt Logs cannot be selected at time of Work Order creation, however, Logs can be selected by Shipping clerk when preparing a Delivery note (assuming Received field in PO 41 is selected) – a delivery note can be created, however an Invoice cannot be completed until the Receipt document is completed.

---
