---
title: "Wh Inv Inquiry Wf1B"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Wh Inv Inquiry Wf1B - 4GL Help Documentation"
long_description: "This topic provides detailed information about Wh Inv Inquiry Wf1B in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Inventory Inquiry
=================

Count physical inventory.

![](../Resources/Images/WH_inv_count.png)

[update with content from / add related topic to Inventory Count Data Entry IN5E]

following is added per BG 39192 :

If you search by Log, you can search by case or log number, and it will return a product code for valid inventory or pre-received logs (including production FG logs).

If you search by Order:

* Added per BG 392321: If you include a warehouse prefix, the system filters logs from that stocking warehouse. If you do not enter a warehouse prefix, the system searches for the order in your operator’s warehouse.
* If you search by order number alone, the search window appears and works the same way as if you were to use INQUIRY in HH Picking Confirmation (WF11). You can choose your search type, and an index or log number.
* If you search by order number suffixed with a line index, the search window appears with the search type and index already populated.
* If you search by order number but omit a document index, you will be prompted to enter the index.

---
