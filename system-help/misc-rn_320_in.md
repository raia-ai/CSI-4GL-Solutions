---
title: "Rn 3.20 In"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rn 3.20 In - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rn 3.20 In in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Inventory
=========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 39001 | Archive folder for MTRs | New switches (“MTR Archive Folder (Mounted)” and “MTR Archive Folder (Windows)”) allow you to set up an archive folder so that you can move older MTRs out of the main MTR folder to keep the main folder at a manageable size. When retrieving an MTR,  will look first in the main folder, then in the archive folder if the file is not found in the main folder. | SWTMNT (see MTR Storage Location(s)) |  |
| 39026 | CUM added to replacement cost export | The Replacement Costs export now includes a Cost UOM column. | IN9ZQ |  |
| 39115 | Correction to icons for receipt logs in IN62 | If a log is both quarantine/program and compatible, it will be shown with the “compatible” icon. If a log is both quarantine/program and pre-receipt, it will be shown with the “pre-receipt” icon. | IN62 |  |
| 39313 | Label printing for branch transfers | Branch transfer shipping labels will print the info of the sales order that the BT is allocated to if a new warehouse option (“Print Order Label for Allocated Transfer Logs”) is enabled and the log is reserved on a sales order in the receiving warehouse. Log numbers must remain the same between sending and receiving warehouses for BT. | SWTMNT |  |
| 39414 | IN71 by Log shows leg dimensions | Logs that have legs will have the leg size description(s) listed in a separate row below them in the "Size" column D. | IN71 |  |
| 39435 | IN7ZQ can include not shipped transfers | An option to include not shipped transfers has been added to the Open Branch Transfers Report. If this option is not set, the report only includes transfers that have been shipped but not yet received (i.e. BT is confirmed but not received).  If the option is set, the report also includes transfers that have not been confirmed yet. | IN7ZQ |  |
| 39607 | New Log Tracking Report | A new Excel report returns log movements for all logs that fit the selected criteria. | IN7XA |  |
| 39635 | IN72 Excel output includes time and sequence | The Excel output of the Movements By Product or Log report now includes columns for the movement entry Time, and the Sequence: the sequence is by warehouse, date, and product. If one product has multiple movements in a single day, the sequence will start from 1 and increase for each movement ordered by time. | IN72 |  |
| 39704 | IN7ZG includes logs committed on IP, linear nesting and inventory adjustment documents. | The Log Reservation Report now prints the IP document number, nesting document number, or the adjustment document number under the work order column if the log is reserved against any of those documents.  For IP documents, it will print the warehouse name for customer/vendor.  For nesting documents, it will print the customer on the sales quote/order for the customer/vendor.  For adjustments, it will print blank for the customer/vendor. | IN7ZG |  |

---
