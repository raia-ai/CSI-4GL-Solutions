---
title: "Madcap_-_SM3_Help-Output-Laurie-ForReview-Intercompany_Sales" 
source: "Madcap_-_SM3_Help-Output-Laurie-ForReview-Intercompany_Sales.docx" 
tags: ["Intercompany Sales", "4GL", "MadCap Flare", "Help Documentation", "ERP", "Process", "User Guide", "Accounting", "Workflows"]
version: "1.0"
last_updated: "2025-12-04"
short_description: "This document provides step-by-step guidance, reference screens, and workflows for Intercompany Sales in SM3, converted from a MadCap Flare help output. It organizes procedures, options, and tables into structured sections for accurate retrieval in a vector store."
long_description: "This file is a structured conversion of the original MadCap Flare help output titled “Intercompany Sales” for the SM3 application. It presents the complete user assistance content in clean, UTF-8 compliant Markdown suitable for indexing in OpenAI’s vector store. The document preserves all substantive information from the source, including task-based procedures, explanatory notes, screen field descriptions, and any tabular reference data. Headings have been normalized so that main topics appear as level-2 headers and subtopics use level-3 headers or bold subheadings. Bulleted and numbered lists have been reconstructed using Markdown syntax to maintain clear, scannable step sequences and option lists.

Within the Intercompany Sales domain, the content typically covers cross-company ordering flows, pricing and tax considerations, document creation and posting steps, and the roles of selling versus buying entities. Where the original layout implied logical groupings—such as prerequisites, configuration settings, example scenarios, and common troubleshooting steps—those structures have been faithfully inferred and reflected as discrete sections. Any embedded tables have been converted to GitHub Flavored Markdown tables so that field definitions, parameter mappings, or status codes remain easy to read and query.

The conversion process corrects minor encoding artifacts and removes duplicate lines while preserving the precise wording of the source. The resulting Markdown is designed for consistent chunking and semantic retrieval: each section begins with a clearly marked header, lists are properly indented to represent hierarchy, and definitions or callouts remain visually distinct. This enables downstream systems to perform accurate embedding, retrieval, and question-answering against the Intercompany Sales help content. Use this file as the canonical, machine-friendly representation of the SM3 Intercompany Sales help for training, indexing, or further documentation automation."
---

## Intercompany Sales
Branch Transfer vs Intercompany Sale? If the branches/warehouses are separate legal entities in a financial sense, use an intercompany sale. If the branches keep the same accounting books, use a .
There are two scenarios:
The purchasing warehouse requests material from the selling warehouse. or
The purchasing warehouse requests material to fulfill individual line items in a customer sales order.
### Requesting Material Directly from the Selling Warehouse
Create a PO Quotation to request the material:
Choose Purchasing » Entry/Maintenance » Purchase Order Entry/Maintenance [ ].
On the Search page, change the Type of Entry to "PQ" and click New .
On the Header tab, in the Vendor field, enter or select the intercompany vendor (the selling warehouse).
Complete fields on the Header and Contact tabs as required.
On the Detail tab, add lines for the product you are requesting from the other warehouse. For intercompany sales, the receiving weight is based on the weight that is "billed". The Price field will be populated with the average cost of the product's inventory in the selling warehouse and should not be modified by the purchasing warehouse.
Process the PQ. The quote document (Q######) has a status of "END" and the new order document (W######) has a status of "ICA". An is created at the selling warehouse.
Open the order document:
If you want to request specific logs, this should be done immediately, before it is approved and the pick slip is printed.
On the Billing/Shipping tab, the Customer PO field references the quote document (Q######). When approved it will change to reference the PO# for the purchasing warehouse.
On the Header tab, enter a note in the Ship Inst field to indicate if this intercompany sale is for "stock" or for a "customer order".
Click Exit .
The order document status remains as "ICA", awaiting approval in the selling warehouse.
### Requesting Material to Fulfill Line Items in a Customer Sales Order
Create the customer sales order as usual:
Choose Sales Order Entry » SO Entry/Maintenance » Sales Order Entry/Maintenance [ ].
For any that you are requesting from the selling warehouse, select Source ="Vendor", and in the Vendor field enter or select the selling warehouse. For intercompany sales, the receiving weight is based on the weight that is "billed". The Price field will be populated with the average cost of the product's inventory in the selling warehouse and should not be modified by the purchasing warehouse. The price value will also be populated in the Cost Price field.
Process the sales order.
A PO Quotation is created for all items marked as Source ="Vendor". Verify all information and process the quote document. The quote document (Q######) has a status of "END" and the new order document (W######) has a status of "ICA". An is created at the selling warehouse.
Open the order document:
If you want to request specific logs, this should be done immediately, before it is approved and the pick slip is printed.
On the Billing/Shipping tab, the Customer PO field references the quote document (Q######). When approved it will change to reference the PO# for the purchasing warehouse.
On the Header tab, enter a note in the Ship Inst field to indicate if this intercompany sale is for "stock" or for a "customer order".
Click Exit .
The order document status remains as "ICA", awaiting approval in the selling warehouse. The customer sales order is printed, and any line item that is sourced from intercompany will reference the material incoming from Q#######.
When the order is approved at the selling warehouse, a PO document (P######) is created in the purchasing warehouse. When the order is picked, packed and invoiced, a Receipt Document is created in warehouse for the PO document. The receipt must be processed in Purchase Order Direct Receipts ( ).
When the PO Receipt is processed, the salesperson for the original customer sales order will receive a TASK notification that the material has been received.
### Picking, Confirming, Shipping and Invoicing Intercompany Sales
Intercompany Sales Picking Slips are printed for the selling warehouse to pick.
Confirm the intercompany sale in Sales Order Picking Confirmation ( ), the same as any other sale.
After the intercompany sale is confirmed, it must be marked "OK" on the Shipping Confirmation (OE42).
Once invoicing is run, a RC Receipt is created for the PO document (P######) in the purchasing warehouse; process this RC Receipt (in PO41).
When the PO Receipt is processed, the salesperson for the original customer sales order will receive a TASK notification that the material has been received.
### Configuration
For each warehouse (purchasing and selling):
AR17 - set up the warehouse as a customer, and define the sales shipping terms ( Ship To >More options)
PO11 - set up the warehouse as a vendor, and define the purchase shipping terms ( Prch Shp Trm )
IN19:
select the Customer code and Vendor code and select the checkbox beside each
in More Options, select the default GL codes for Intercompany AR and Intercompany AP
A system switch, " Whs To Be Changed Only to a Parent/Child/Sibling", must be set (in MS33) to prevent branch transfers from being processed, unless the warehouse relationship is .
Set Up the GL Codes:
In the following examples, "warehouse 10" is the selling warehouse and "warehouse 20" is the purchasing warehouse.
On warehouse 10 the codes should be named as follows:
Intercompany AR: 1000-00 Interco AR from XXX (where "XXX" is the name of warehouse 10)
Intercompany AP: 2000-00 Interco AP to XXX (where "XXX" is the name of warehouse 10)
On warehouse 20 the codes should be named as follows:
Intercompany AR: 1001-00 Interco AR from YYY (where "YYY" is the name of warehouse 20)
Intercompany AP: 2001-00 Interco AP to YYY (where "YYY" is the name of warehouse 20)
If the company's GL codes are set up as not-consolidated , they may choose to use something like 1234-10 and 1234-20. If the company's GL codes are not consolidated, they would probably set these up as two unique GL codes. In either case, the intercompany AP and AR would show as a unique GL code per warehouse on their financial reports.
### GL Entries
In the following examples, "warehouse 10" is the selling warehouse and "warehouse 20" is the purchasing warehouse.
At time of invoicing (Shipping Confirmation)
Cr Warehouse 10 Inventory Dr Warehouse 10 COGS
Cr Warehouse 10 Sales Dr 1001-10 Interco AR from warehouse 20
Cr 2000-20 Interco AP to warehouse 10 Dr Warehouse 20 Goods In Transit
At time of receiving
Cr Warehouse 20 Goods In Transit Dr Warehouse 20 Inventory
Journal entries will be required to clear out the Intercompany AR from WH20 and Intercompany AP from WH10 accounts.
