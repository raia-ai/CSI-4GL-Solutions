---
title: "Wh Location Chg Wf13"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Wh Location Chg Wf13 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Wh Location Chg Wf13 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Bin Location Change
===================

Change a log’s warehouse bin location. You can retrieve a log with the log number or shipping label barcode. The package number will change the bin location for the actual package.

A user's ability to change warehouse depends on the Change Transactional Whse option in their Operator settings [MS32]; they may be allowed to change to any valid warehouse, to a specific list of warehouses only, or not at all.

To change the location for a single log:

1. Use WF13.
2. Scan or enter the Log number.
3. Scan or enter the New bin location code.

![](../Resources/Images/WH_loc_change.png)

To change the location for all (or multiple) logs in a bin:

1. Use WF13Q.
2. Enter the current bin #, scan the logs within, then select the new bin #.

[per testing notes; need clarification or ability to test; I checked IN1Y to get some bin #s but they were not accepted in WF13Q; asked GAW for clarification but he did not respond]  
- NOW ENTER/SCAN LOG NUMBER AFTER LOG NUMBER FOR ALL LOGS IN THAT BIN  
- TO SWITCH TO A NEW BIN, OPEN UP THE WINDOW AND SELECT 'NXTBIN'; THIS SHOULD POSITION YOU ON THE BIN LOCATION FIELD (NOTE: THS CAN ALSO BE ACHIEVED BY JUST HITTING ENTER)  
- TO IGNORE AN ENTERED LOG SELECT 'CANCEL' IN THE WINDOW'; AND TO TERMINATE SELECT 'EXIT'.

---
