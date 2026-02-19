---
title: "Intercompany Sales"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Intercompany Sales"
long_description: "This topic provides detailed information about Intercompany Sales in the 4GL system."
---


Intercompany Sales
==================

**Branch Transfer vs Intercompany Sale?**
  
If the branches/warehouses are separate legal entities in a financial sense, use an intercompany sale.   
If the branches keep the same accounting books, use a branch transfer.

There are two scenarios:

* The purchasing warehouse requests material from the selling warehouse.  
  or
* The purchasing warehouse requests material to fulfill individual line items in a customer sales order.

Requesting Material Directly from the Selling Warehouse
-------------------------------------------------------

1. Create a PO Quotation to request the material:
   1. Choose Purchasing » Entry/Maintenance » Purchase Order Entry/Maintenance [PO31].
   2. On the Search page, change the Type of Entry to “PQ” and click New.
   3. On the Header tab, in the Vendor field, enter or select the intercompany vendor (the selling warehouse).
   4. Complete fields on the Header and Contact tabs as required.
   5. On the Detail tab, add lines for the product you are requesting from the other warehouse.  
      For intercompany sales, the receiving weight is based on the weight that is “billed”. The Price field will be populated with the average cost of the product’s inventory in the selling warehouse, including any markup1.
2. Process the PQ. The quote document (Q######) has a status of “END” and the new order document (W######) has a status of “ICA”.   
   An Intercompany Approval task is created at the selling warehouse.
3. In the order document:
   * If you want to request specific logs, this should be done immediately, before it is approved and the pick slip is printed.
   * On the Billing/Shipping tab, the Customer PO field references the quote document (Q######). When approved it will change to reference the PO# for the purchasing warehouse.
   * On the Header tab, enter a note in the Ship Inst field to indicate if this intercompany sale is for “stock” or for a “customer order”.
   * Click Exit.
4. The order document status remains as “ICA”, awaiting approval in the selling warehouse.

Requesting Material to Fulfill Line Items in a Customer Sales Order
-------------------------------------------------------------------

1. Create the customer sales order as usual:
   1. Choose Sales Order Entry » SO Entry/Maintenance » Sales Order Entry/Maintenance [OE31].
   2. For any line item that you are requesting from the selling warehouse, select Source =“Vendor”, and in the Vendor field enter or select the intercompany vendor (the selling warehouse).  
      For intercompany sales, the receiving weight is based on the weight that is “billed”. The Price field will be populated with the average cost of the product’s inventory in the selling warehouse, including any markup1. The price value will also be populated in the Cost Price field.
2. Process the sales order.
3. A PO Quotation is created for all items marked as Source=”Vendor” (where the vendor code is the intercompany vendor code of the selling warehouse). Verify all information and process the quote document. The quote document (Q######) has a status of “END” and the new order document (W######) has a status of “ICA”.   
   An Intercompany Approval task is created at the selling warehouse.
4. In the order document:
   * If you want to request specific logs, this should be done immediately, before it is approved and the pick slip is printed.
   * On the Billing/Shipping tab, the Customer PO field references the quote document (Q######). When approved it will change to reference the PO# for the purchasing warehouse.
   * On the Header tab, enter a note in the Ship Inst field to indicate if this intercompany sale is for “stock” or for a “customer order”.
   * Click Exit.
5. The order document status remains as “ICA”, awaiting approval in the selling warehouse. The customer sales order is printed, and any line item that is sourced from intercompany will reference the material incoming from Q#######.
6. When the order is approved at the selling warehouse, a PO document (P######) is created in the purchasing warehouse.  
   When the order is picked, packed and invoiced, a Receipt Document is created in warehouse for the PO document. The receipt must be processed in Purchase Order Direct Receipts (PO41).

Picking, Confirming, Shipping and Invoicing Intercompany Sales
--------------------------------------------------------------

1. Intercompany Sales Picking Slips are printed for the selling warehouse to pick.
2. Confirm the intercompany sale in Sales Order Picking Confirmation (OE41), the same as any other sale.
3. After the intercompany sale is confirmed, it must be marked “OK” on the Shipping Confirmation (OE42) [xref].
4. Once invoicing is run, a RC Receipt is created for the PO document (P######) in the purchasing warehouse; process this RC Receipt (in PO41).

Configuration


For each warehouse (purchasing and selling):

* AR17 - set up the warehouse as a customer, and define the sales shipping terms (Ship To>More options)
* PO11 - set up the warehouse as a vendor, and define the purchase shipping terms (Prch Shp Trm)
* IN19:
  + select the Customer code and Vendor code and select the checkbox beside each
  + in More Options, select the default GL codes for Intercompany AR and Intercompany AP

A system switch, "Whs To Be Changed Only to a Parent/Child/Sibling", must be set (in MS33) to prevent branch transfers from being processed, unless the warehouse relationship is parent/child.

1  > Pct to Markup Avg Cost of Sending Whs in Calc Sales Price for Intercompany

Set Up the GL Codes:

In the following examples, “warehouse 10” is the selling warehouse and “warehouse 20” is the purchasing warehouse.

On warehouse 10 the codes should be named as follows:

* Intercompany AR: 1000-00 Interco AR from XXX (where “XXX” is the name of warehouse 10)
* Intercompany AP: 2000-00 Interco AP to XXX (where “XXX” is the name of warehouse 10)

On warehouse 20 the codes should be named as follows:

* Intercompany AR: 1001-00 Interco AR from YYY (where “YYY” is the name of warehouse 20)
* Intercompany AP: 2001-00 Interco AP to YYY (where “YYY” is the name of warehouse 20)

If the company’s GL codes are set up as not-consolidated, the same GL code can be entered for all warehouses; if they are set up as consolidated, then unique GL codes must be entered for each warehouse. In either case, the intercompany AP and AR would show as a unique GL code per warehouse on their financial reports.



GL Entries

In the following examples, “warehouse 10” is the selling warehouse and “warehouse 20” is the purchasing warehouse.

**At time of invoicing (Shipping Confirmation)**

Cr Warehouse 10 Inventory  
Dr Warehouse 10 COGS

Cr Warehouse 10 Sales  
Dr 1001-10 Interco AR from warehouse 20

Cr 2000-20 Interco AP to warehouse 10  
Dr Warehouse 20 Goods In Transit

**At time of receiving**

Cr Warehouse 20 Goods In Transit  
Dr Warehouse 20 Inventory

Journal entries will be required to clear out the Intercompany AR from WH20 and Intercompany AP from WH10 accounts.

---
