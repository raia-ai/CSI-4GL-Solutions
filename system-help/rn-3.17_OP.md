---
title: "Outside Processing"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Outside Processing"
long_description: "This topic provides detailed information about Outside Processing in the 4GL system."
---


Outside Processing
==================

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 38106 | OP forms now look at IN19 to decide remarks to print | The Finished Goods remarks that print on sub-contract, production order form, production order work order, and job traveller forms are now controlled by IN19 Form Options. | IN19 > Form Options |  |
| 38154 | Allow users to re-open closed FG lines | The Close FG button has been changed to a toggle, so that if you select an FG line that has been closed, the button becomes Open FG. | PP36 |  |
| 38155 | Allow entry of zero quantities in OP Receiving | In the Receiving window, the Current Units reflects the received amount on the lift record, and can only be changed or set to zero in the lift record. If the lift is deleted, then the figures can be adjusted on the main screen. | PP36 |  |
| 38370 | Linking of OP/IP documents when created from an SO | When there is one or more machine lines on a sales order defined as an Outside process as well as machines lines defined as Inside process, the resulting OP and IP documents are linked: - The Commitments tab for the FG in the OP shows that it has been allocated to the new IP - The Committed In tab for the RM in the IP shows that it is linked to the new OP.  Once both are processed, the sales order will print. | PR41B |  |

---
