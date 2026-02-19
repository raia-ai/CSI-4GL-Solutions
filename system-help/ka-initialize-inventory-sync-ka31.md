---
title: "Initialize Inventory Sync [KA31]"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Initialize Inventory Sync [KA31]"
long_description: "This topic provides detailed information about Initialize Inventory Sync [KA31] in the 4GL system."
---


Initialize Inventory Sync [KA31]
================================

This function will extract Inventory detail (On-Hand Balance, Heat Number, etc.) from Kasto. There are two processing modes: Non-Synchronized or Synchronized.

* Synchronized mode is determined from Selection parameter 06 All Articles (>0 by Charge)
* Non-Synchronized mode will return the selected information and output it to KAD\_DTL that can be viewed through KA63 – Kasto Unload Transaction Log

In both modes a single HLBM – Inventory Inquiry is created in KAR\_RCV for it to be processed by the Communication Engine.

Synchronized mode will first create a sync file KAS\_SNC from all  logs and then match these records to those extracted from Kasto. It will also set a variable on the WHS\_KA file to indicate that a sync is in progress.

This file can be used to analyse the state of the data in the following functions:

* KA68 – Heat/Length Analysis >0
* KA77 – Analyze Inventory Sync
* KA78 – Sync Analysis Report
* KA82 – Reset Sync Completion Code
* KA83 – Heat/Length Analysis >=0

After running KA31, you should run the following functions:

* Sync Analysis Report [KA78]
* Analyze Inventory Sync [KA77].
* Heat/Length Analysis >0 [KA68]
* Reset Sync Completion Code [KA82]
* Heat/Length Analysis>=0 [KA83]

---
