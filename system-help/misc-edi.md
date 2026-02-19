---
title: "Edi"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Edi - 4GL Help Documentation"
long_description: "This topic provides detailed information about Edi in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Electronic Data Interchange (EDI)
=================================

Electronic Data Interchange (EDI) is the electronic interchange of business information using a standardized format, a process which allows one company to send information to another company electronically rather than with paper.

Transactions like purchase orders, PO Acknowledgments, Advanced Shipment Notifications and Material Test Reports (MTRs/Certifications) often involve a series of steps to process with human intervention, which makes them prone to mistakes and human errors. But with the use of EDI, paper documents are eliminated and human intervention is minimized.

[EDI is only used by SSG, so related functions are not documented]

EDI Integration
---------------

The following RESTful (JSON) web services are currently integrated with :

* Purchase Order Transfer – Once a purchase order is processed in , the PO information is transferred to the supplier electronically by calling the supplier’s specific web service.
* Purchase Order Acknowledgment – When the supplier receives the  purchase order electronically, the supplier’s software calls our  Hosted Web Service to acknowledge the purchase order.
* Advance Shipment Notification – When the supplier creates the shipment, the supplier’s software calls our  Hosted Web Service to transfer that information electronically to .
* AP Goods Receipts – Once invoices are paid, a payment voucher is created in .
* Test Certificate Transmission – When the supplier uploads the MTR document to the  Server (via FTP or shared drive), a call is made to the  Hosted Web Service to store that Test Certificate Information in  and automatically attach to receipts based on case/heat number.

If both parties are  clients, the process of PO and sales order creation can be automated (see below).

EDI Process Flow Diagram
------------------------

The following schematic shows the process flow of EDI documents to and from suppliers:

![](../Resources/Images/EDI-process-flow.png)

Automatic Processing Between Two  Clients
-----------------------------------------

Both parties must enter the mailbox IDs as indicated.

If you are the customer/purchaser:

* Set up the vendor record for EDI:
  + Enter the vendor’s EDI Mailbox ID (PO11 > Ship-From details)
  + Enable sending EDI transactions to IBM Sterling when processing POs (PO11 > Doc Delivery > EDI Details > EDI Type = "2")
* Enter your own EDI Mailbox ID in your warehouse options (IN19>Additional Options)
* Create and process a PO for the vendor.

If you are the supplier:

* Obtain the customer’s EDI Mailbox ID and enter it in the customer record (AR17>Ship-To)
* Enter your own EDI Mailbox ID in your warehouse options (IN19>Additional Options)
* When the customer processes the PO, you will get a new EDI Incoming PO task in your Task Manager
  + Edit the task — edit the customer, warehouse, or ship-to fields, and select a  product for any PO line that is not already linked.
  + Approve the task.  creates the sales order. Finalize and process as usual.

---
