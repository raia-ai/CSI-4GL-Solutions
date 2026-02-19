---
title: "Wh Phys Inv Wf15"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Wh Phys Inv Wf15 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Wh Phys Inv Wf15 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Physical Inventory
==================

Inventory counts are completed more efficiently if performed in teams of two: one person to count and the other to record (on paper or via handheld).

- A user must have appropriate access permission1 to create new logs when entering inventory count tickets.
- You may be prompted to enter the pieces before the quantity2, or you may only be able to enter only one of those fields3.

Configuration


1 MS32 > [operator] > Options > Manager (this permission is not used for any other purpose in )

2 IN16 > F9 > Warehouse > Inventory Count/Adj By Pieces = “Y”

3 IN16 > F9 > Warehouse > Additional Options > Input Only Quantity or Pieces During HH Count = “Y”

---
