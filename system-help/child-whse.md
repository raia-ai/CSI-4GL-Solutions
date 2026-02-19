---
title: "Setting Up Parent/Child Warehouses"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Setting Up Parent/Child Warehouses"
long_description: "This topic provides detailed information about Setting Up Parent/Child Warehouses in the 4GL system."
---


Setting Up Parent/Child Warehouses
==================================

Parent/child warehouses are generally set up when more than one stocking/sales location belong to a single legal entity.

Setting Up the Relationship
---------------------------

To set up a parent/child warehouse relationship, retrieve the child warehouse in the Warehouse Controls form [IN19], and enter the Parent Whse.

Controlling Where GL Activity is Posted
---------------------------------------

Once the relationship has been established, you can choose to post GL activity to the parent warehouse instead of the child warehouse. In the Chart of Accounts [GL12A], select the Prt Whse (post to parent warehouse) flag against selected GL codes. For example, if you want to post AR activity for warehouse 11 to its parent (warehouse 10) you would set the post to parent flag against the AR GL code. With this flag set, whenever a warehouse 11 invoice is posted it will hit the warehouse 10 AR GL instead of the warehouse 11 GL code.

If you choose to have different sales and stocking warehouses. In this case, you can choose to post GL activity to the sales warehouse by selecting the Sales Whs flag in the Chart of Accounts.

Moving Inventory
----------------

When warehouses are set up with a parent/child relationship (i.e. they keep the same accounting books), you would typically use the Branch Transfer module to move inventory from one warehouse to another. If they are not set up with this relationship (i.e. they are separate legal entities in a financial sense), you would typically use intercompany sales transactions.

Reporting
---------

There are many reports and inquiries in the system that provide the option to include children in the output. Some examples:

AR Aging Report [AR7R]:

![](../Resources/Images/parent-child-include-AR7R.png)

Detailed Inventory Inquiry > Sales:

![](../Resources/Images/parent-child-include-det-inquiry-sales.png)

---
