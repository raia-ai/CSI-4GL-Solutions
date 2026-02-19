---
title: "Initiating an Inventory Count"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Initiating an Inventory Count"
long_description: "Help documentation for Initiating an Inventory Count in the 4GL system."
---

Initiating an Inventory Count
=============================

This function is used to initiate a physical inventory count.

This screen should have limited access:
Running will freeze product quantities for the product lines selected for the physical inventory count. ALL inventory logs are reduced to zero. Entering
the count tags puts inventory back into stock. DO NOT post your inventory until all inventory
count tags are entered.

1. Choose Inventory Control » Physical Inventory » Inventory Count Initialization [IN5B].
2. Enter or select Warehouse code.
3. If you are not counting all product lines at this time, select one or more Product Lines to be counted.
4. Optionally, if you want to filter by bin location, select the Count By Location checkbox, then select the Location type and the location(s) within that type. The inventory count pre-stock report will only show logs that belong to the product lines and bin location selected.
5. Enter or select Document Date.

This is the GL Date used for posting adjusting entries for Physical Inventory Variances – your Accounting staff should supply you with this date.

6. Enter a Count Description. The first line displays on the header of Physical Inventory Count reports; we recommend including the date (e.g. Oct 21, 2020 Physical Count) in the Description.
7. Enter the Start Tag Number. This is the starting number of Physical Inventory Count Ticket or starting Tag number on Inventory Count page.
8. Enter the End Tag Number. This is the ending number of Physical Inventory Count Ticket or ending Tag number on Inventory Count page. To determine how many active logs you have in the system, run the Active Logs inquiry [IN69].[xref]

If more tags are later required in order to complete the physical inventory count, use the Expand Tag Allocation utility [IN5J].

9. Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate. If you output to Excel, there will be two Excel reports: one for non-committed inventory and one for committed inventory.

Once a physical inventory count has been initiated, two reports will print that display all inventory that is currently committed
and all inventory that is currently not committed.

Before continuing with the physical inventory count, all committed inventory must be uncommitted. If you uncommit any inventory, you must run the Refresh Working File utility [IN5C] before proceeding.

---