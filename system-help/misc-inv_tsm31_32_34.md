---
title: "Inv Tsm31 32 34"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Inv Tsm31 32 34 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Inv Tsm31 32 34 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Storing and Retrieving Inventory
================================

Storage Order Upload
--------------------

This handheld function is used to load inventory into the Toyota system.

1. Choose Toyota ASRS System » Storage Order Upload (F01) [TSM31].
2. Establish a few floor logs that you want to store (Location code “F”).
3. Enter or scan the logs one at a time.
4. After all logs have been entered, enter “FINAL”.

The selection of logs will be processed and an Item Count will be displayed.

Retrieval Order Upload
----------------------

This handheld function is used to retrieve inventory from the Toyota system. This can be done either by document or by log number.

### Retrieving By Document

1. Choose Toyota ASRS System » Retrieval Order Upload by Doc (F02) [TSM32].
2. Establish sales orders in picking confirmation, ensuring that each line is barcoded.
3. Enter or scan the sales order number, then scan the lines one at a time.
4. After all lines have been scanned, enter “FINAL”.

The selection of logs will be processed and an Item Count will be displayed.

### Retrieving by Log Number

1. Choose Toyota ASRS System » Retrieval Order Upload by Log (F02) [TSM34].
2. Enter or scan the logs one at a time.
3. After all lines have been scanned, enter “FINAL”.

---
