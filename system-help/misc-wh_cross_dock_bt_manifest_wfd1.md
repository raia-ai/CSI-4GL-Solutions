---
title: "Wh Cross Dock Bt Manifest Wfd1"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Wh Cross Dock Bt Manifest Wfd1 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Wh Cross Dock Bt Manifest Wfd1 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Cross-Dock BT on Manifest
=========================

The Cross-Dock BT function [WFD1] allows users to scan a branch transfer delivery note to generate a miscellaneous document in a manifest document. This will be used when transfer material is “passing through” another warehouse and therefore still needs to be planned on a manifest run.

1. Enter the Whs and Date. If a manifest exists in the selected warehouse for the given date, the manifest number appears.
2. In the Doc field, scan the BT packing slip.
3. Enter 1 to process.

A miscellaneous document is created on the manifest for the warehouse and date specified in step 1. Document tracking records are added to all sales orders linked to the branch transfer, with the same status as the previous document tracking record but with a remark indicating the material has been cross docked at [xx] warehouse.

---
