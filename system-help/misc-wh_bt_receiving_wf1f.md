---
title: "Wh Bt Receiving Wf1F"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Wh Bt Receiving Wf1F - 4GL Help Documentation"
long_description: "This topic provides detailed information about Wh Bt Receiving Wf1F in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Branch Transfer Receiving
=========================

If the barcode scanned is associated with a warehouse different from the operator's warehouse, they may be1 warned or prevented from proceeding.

If the product line's warehouse options' Receipt Allocation Method is set to “N”, when you receive the branch transfer you will be asked if you want to allocate the logs and print shipping labels for the logs reserved against the order.

If the order is in PBP status, when you choose to allocate and print labels, the order is changed to PCK status.

Configuration


1  > Validate Warehouse in Branch Transfer Hand Held Receiving; if set to **H**ard Warning, they are given an explanation and cannot proceed; if set to **S**oft Warning, they are given a warning but have the option to proceed; if set to **N**o Warning, they are not given a warning and can proceed.

---
