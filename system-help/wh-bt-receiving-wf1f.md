---
title: "Branch Transfer Receiving"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Branch Transfer Receiving"
long_description: "Help documentation for Branch Transfer Receiving in the 4GL system."
---


Branch Transfer Receiving
=========================

If the barcode scanned is associated with a warehouse different from the operator's warehouse, they may be1 warned or prevented from proceeding.

If the product line's warehouse options' Receipt Allocation Method is set to “N”, when you receive the branch transfer you will be asked if you want to allocate the logs and print shipping labels for the logs reserved against the order.

If the order is in PBP status, when you choose to allocate and print labels, the order is changed to PCK status.

Configuration


1  > Validate Warehouse in Branch Transfer Hand Held Receiving; if set to **H**ard Warning, they are given an explanation and cannot proceed; if set to **S**oft Warning, they are given a warning but have the option to proceed; if set to **N**o Warning, they are not given a warning and can proceed.

---
