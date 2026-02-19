---
title: "Initialize Product Master Sync [KA33]"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Initialize Product Master Sync [KA33]"
long_description: "This topic provides detailed information about Initialize Product Master Sync [KA33] in the 4GL system."
---


Initialize Product Master Sync [KA33]
=====================================

This function will inquire into a Kasto Master data item.

It will set up a HLSA – Master Data Inquiry Telegram in KAR\_RCV to be processed by the Communication Engine.

It also allows an option to synchronize if the 03 (Range of items) is selected.

If this is selected the function will create a KAM\_MST Masterfile ‘sync’ file for all  items in that range and then match them to those selected from Kasto.

This file can be used to analyse the state of the data in KA67 – Analyse Product Master Sync.

After running KA33, you should run Analyse Product Master Sync [KA67].

---
