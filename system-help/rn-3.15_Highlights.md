---
title: "Highlights"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Highlights"
long_description: "This topic provides detailed information about Highlights in the 4GL system."
---


Highlights
==========

* is now running on PROIV v9 and Oracle v19c. If you are using the Windows client, it will need to be upgraded (download it here).
* Open Client issue with the Customer, Inventory and Vendor dropdowns has been fixed.
* Customer and vendor contact names now allow 40 characters.
* Communication between  and SigmaNEST now requires TLS 1.2 support; in order for SigmaNEST to work with that, you must install Microsoft SQL Server 2014 Service Pack 3 (assuming you are using SQL Server 2014) which can be found here.

Mass Price Adjustment
---------------------

A new switch (“Mass Price Adjustment Option on Reprice”) changes the functionality of the RePrice button on a sales order, providing a streamlined, efficient way to perform mass price/unit adjustments on quotes and orders.

When the switch is enabled, the Reprice window lists all line items on the quote or order with an option to filter them by grade. You can select all or some of the lines and then apply any of the following changes to the selected lines:

* Enter a selling price in whichever unit you choose — the entered price will apply to all selected lines on the order but the actual unit on the order is not changed. In other words, you could enter a price of $2/lb but the price the customers sees could be $4/FT.
* Apply a markup and/or margin percentage — the number entered in either of these fields will be applied to the replacement cost of the item on each individual line in order to arrive at a selling price.
* Change the unit — this will change the PUM on the selected order lines while keeping the same value and quantity.

All price changes will affect the material portion of the price only – additional operation charges will remain unchanged.

---
