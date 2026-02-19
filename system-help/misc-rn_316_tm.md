---
title: "Rn 3.16 Tm"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rn 3.16 Tm - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rn 3.16 Tm in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Task Manager
============

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 37889 | Releasing orders from Task Manager with Required Date in past | New switch controls what happens if a user releases a sales order from the Task Manager and there is at least one order line with the Required Date in the past: If set to “N” (no check) - the order is released as normal. If set to “S” (soft warning) - a message will alert the user but the order will be released. If set to “H” (hard warning) - a message will appear and the order will not be released. The salesperson will have to withdraw the order and make the appropriate changes before it can be released. | > Check If Requested Date On Order Line Is Before Today  TK1 |  |

---
