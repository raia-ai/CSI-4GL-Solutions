---
title: "Creating an OP Order from Sales Order Lines"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Creating an OP Order from Sales Order Lines"
long_description: "Help documentation for Creating an OP Order from Sales Order Lines in the 4GL system."
---

Creating an OP Order from Sales Order Lines
===========================================

OP documents can be created automatically when the sales order is processed. Alternatively, the sales order lines can be converted into an OP order at a later date. Any cost and price remarks on the sales order are copied to the finished goods.

Creating OP Documents Automatically from a Sales Order
------------------------------------------------------

1. In a sales order, when you add a line that uses an external process1 you are prompted to enter the vendor. If costing is defined for the specified vendor and process2, the cost and selling prices are populated in the sales order. You can enter additional outside process lines as required, for the same or different vendors.
2. When the sales order is processed, all outside processes are presented for set allocation. Note that each index represents one sales line, and in each sales line there can be more than one process by the same or different vendor. Click Auto Set to create one set per line (1:1), or enter the Set ID manually for each line, e.g. 1:many — multiple lines will be processed from the same raw material. Sets are determined by vendor who might have different sets split over different lines. The object is to have one document per vendor with one or more sets. Where there is more than one vendor per sales line, these documents/sets will automatically be linked; where there is the same vendor per line these costs will be grouped.
3. Click Process to complete the sales order processing.
4. One OP document will be created per vendor, even if their sets are split over different order lines. These documents will be linked and presented back-to-back for processing3. In each OP document, review and complete the Sets and Details tabs. If the raw material will be the same as the finished goods for at least one line, on the Sets tab click Raw Mat. You will be prompted to indicate if the raw material is the same as the finished goods for all or selected sets, then select the raw material.
5. Continue processing through each document. At the end of a sales line you will see that the material is allocated to the sale. If multiple OP documents were generated for different vendors, they will be linked together and the last OP document will be linked to the sales order.

The purchase order(s) will be created at the order entry stage but will only be released if the order is released (i.e. if the order goes on pricing approval or credit approval the PO will not be released until the order is released).

When there is one or more machine lines on a sales order defined as an Outside process as well as machines lines defined as an Inside process, the resulting OP and IP documents are linked: the Committments tab for the FG in the OP show that it has been allocated to the new IP, and the Committed In tab for the RM in the IP shows that it is linked to the new OP. Once both are processed, the sales order will print.

Converting Sales Order Lines Into an Outside Processing Order
-------------------------------------------------------------

1. Choose In-House Production » Sales Order Controlled » Production Schedule [PR41B].
2. Select the Process machine (and optionally enter any other criteria to filter the data) to retrieve a list of documents.
3. Select the lines that you want to convert to an OP order, then click Create OP.
4. Select the vendor and click Save.
5. In the set allocation window, click Auto Set to create one set per line (1:1), or enter the Set ID manually for each line, e.g. 1:many — multiple lines will be processed from the same raw material.
6. Click Process. The OP order is created with the correct number of sets. The set process code is populated based on the process associated with the machine in Machine Maintenance.
7. In the OP document, review and complete the Sets and Details tabs. If the raw material will be the same as the finished goods for at least one line, on the Sets tab click Raw Mat. You will be prompted to indicate if the raw material is the same as the finished goods for all or selected sets, then select the raw material.
8. Complete the order's Header information and make any changes to the set details (e.g. raw material logs, finished goods costing, etc.), then process the order as described in Entering an Outside Processing Order.

   If you look at the Commitments tab of a finished good line, you will see that it is committed to the sales order line that was selected in the production schedule.

Configuration


1 A machine process may be identified as an outside process in the Machine Master [PR11].

2 Vendor Machine Pricing [AP1B]

3  > Open Set Numbering Window. If disabled, the Set Allocation screen is skipped entirely; this performs the Auto Set allocation as above and opens the resulting OP documents immediately for processing.

---