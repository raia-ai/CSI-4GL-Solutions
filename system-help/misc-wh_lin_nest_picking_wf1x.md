---
title: "Wh Lin Nest Picking Wf1X"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Wh Lin Nest Picking Wf1X - 4GL Help Documentation"
long_description: "This topic provides detailed information about Wh Lin Nest Picking Wf1X in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Linear Nesting Picking
======================

To pick material for a linear nesting production document, use the Linear Nesting Picking handheld function.

Scan the production document and then the log/feed you are picking.

You may be asked if you want to print one label per piece/log1, otherwise one label will print for the document.

If a log is not valid, or the product/size is not on the project, or there is not enough left for that product/size, an error message will display. Otherwise the log transfer window will open and you can enter the number of pieces you are picking.

You are not picking against a specific feed on the production document, but rather the production document as a whole.

Available options:

* VIEW – view a list of required feeds and picked feeds so you can see what’s left to pick
* TFRREV – reverse the log transfer

Upon exit a message will alert you if the full order has not been picked.

A log transfer will be processed and the resulting baby log will be picked/stored against the production document.

A Logs button in the project maintenance (IN3F) and project inquiry through order inquiry displays all the logs picked on the project. Furthermore through IN3F you can delete logs from the project as well as exclude a nest pattern from commit-out.   
If the “Check For Picked Logs In Linear Nesting Log Split” switch is enabled, when you use the Linear Nesting Log Split you will be warned if you select a log that was not picked.

Configuration


1  > Allow Multiple Labels in Linear Nest Picking

---
