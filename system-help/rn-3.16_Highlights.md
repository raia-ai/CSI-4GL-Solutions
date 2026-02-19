---
title: "Highlights"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Highlights"
long_description: "Help documentation for Highlights in the 4GL system."
---


Highlights
==========

Creating Outside Processing Documents from Sales Order Entry
------------------------------------------------------------

We have made several changes to streamline creating OP documents from a sales order:

* 37735 - A new price matrix (AP1B) allows you to store pricing for outside operations by vendor. 37735
* 37911 - On processing a sales order, all outside processes are presented for set allocation. An Auto Set button creates one document per vendor, even if their sets are split over different order lines. These documents will be linked and presented back-to-back for processing. In the resulting OP document(s), if the raw material will be the same as the finished goods for at least one line, the new Raw Mat button on the Set tab allows you to build both Details sections at the same time. You will be asked if the raw material is the same as the finished goods for all lines or selected lines. 37911
* A new switch (“Open Set Numbering Window”), when disabled, allows you to skip the Set Allocation screen entirely when automatically creating OP documents from sales orders. This performs the Auto Set allocation as described above and opens the resulting OP documents immediately for processing. 38031
* When creating an OP from a sales order, cost and price remarks are copied from the sales order to the finished goods. 38030

For more information, see Creating an OP Order from Sales Order Lines.

User-Defined Fields in Order/Quote Entry
----------------------------------------

Up to three user-defined fields can be added to quote/order details. The labels for these fields are defined in a new warehouse option (IN19>OE Options>UDF Descriptions). 37740

Any UDFs configured in IN19 will display beneath the Part Number field when adding a line to an order/quote.   
If there are no UDFs configured in IN19, a UDFs field will be visible but disabled in the order details. 38033

A form option on the sales forms (packing list, invoice, picking list, sales quotation, and sales order) allows any populated UDFs to be included when these forms are printed. 38062

Import Customer Parts into Order from Excel
-------------------------------------------

Customer parts can now be imported into an order from an Excel spreadsheet. The line type must be “Prt” and the SUM and PUM must be set to the part's pricing unit of measure. 37524

Custom Subject and Body for Emails
----------------------------------

When processing an order, quote, or PO, if a contact is specified to receive an email (on the Contacts tab), you can edit the default subject and message. This also applies to generating a customer statement. 37739

Task Notification for Purchase Price Changes
--------------------------------------------

If the price is updated on a purchase order line and material from that purchase order line has been allocated to sales order(s), a task notification will be generated to the sales people assigned to the sales orders. The sales people can then review the price change and decide whether they need to take action regarding the price change. 37737

37015 **Romac webservices**   
- as of Aug 9/2023, per Robin, “This one isn't ready to be rolled out to all customers yet. We are testing this with one or two customers.” He explained: “It's a linear nesting vendor software that exists as a windows program right now. The change is to connect to a web version of the same program. Only the web version of Romac will work with Open Client. So when we push open client to all of our customers, we would have to get them to use new web version of Romac. But there should be no noticeable difference in user experience when they nest in SM3. I don't know if we need to include this in the release notes.”  
I’m not sure if this is the same thing: https://romacsystems.com/length-nesting/  
Per 37015 testing notes, there’s a new whs switch to indicate whether to use web services or command line utility for Romac:  
New switches in MS33>System: Use Linear Nest Web Service, Romac Web Service Base URL, Romac Web Service Customer ID, Database Connection String  
New in MS32>Options>Inventory>Additional Options: Romac Web Service Application ID, Username, Password  
As of Nov 1/23 - the MS33 switches are hidden to non-dev users, and the MS32 switches will also be hidden as of 3.20, so this content should only go in internal documentation, not the online help

---
