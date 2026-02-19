---
title: "In-House Production"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "In-House Production"
long_description: "Help documentation for In-House Production in the 4GL system."
---


In-House Production
===================

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 38386 | Save changed filters or reset to default on PR41B | When you change the default values at the top of the Machine Production Schedule, your values are retained the next time you open the form. A new Reset button allows you to return the values to the defaults. | PR41B |  |
| 38587 | Allow Allocate in log split if negative scrap is allowed | If the Material Allocation Method (Allow Negative Scrap) switch is enabled, when processing a log split in the Production Confirmation you can now click Allocate to allocate the negative scrap proportionately over all of the lines until it is reduced to zero. | PR42B |  |
| 38661 | Partial/complete flag set to “C” when picked log allocated to “Both” | When picking a log in the Production Schedule, if you allocate it to “Both” (picked and used), the partial/complete flag in the Production Confirmation will be set to “C”. | PR41B, PR42B |  |
| 38683 | MUN theoretical weights | When a miscellaneous item is used as a finished good, the IUM/WGT window opens to establish a theoretical weight. | PR34 |  |
| 38867 | Document Index added to PR42B | An Index field has been added to the Production Confirmation | PR42B |  |
| 38990 | Can now enter finished sizes against finished goods | When entering tolerances against finished goods, users can now add finished size against the dimensions as well. When creating an IP from a sales order, the finished sizes are copied from the sales order line to the finished good line of the IP document. | PR34 |  |
| 38991 | Print finished size, sales order number, line number, and UDF on the production order form | A new form option enables the sales order number, line index, and UDF to be printed for production order forms (form 30).  If tolerances were defined for a finished good, they will also be printed on the production order. | IN19>Forms>Display Sales Order Alloc and UDF |  |
| 39031 | View Header/Lot Costs on IP Inquiry | A new button on the Sets tab of the IP Inquiry allows you to view the Header/Lot Costs. | PR64, PR65 |  |
| 39119 | Linear nesting parity | Linear nesting from PR41B has been brought inline with nesting from order entry, e.g. the ability to input RTS in the Linear Nesting Cutting Schedule window. | PR41B |  |
| 39181 | Print linear nest production orders when processing sales order | When a sales order is processed in OE31, or released in OE3L if batch printing is turned on, or approved from credit approval in the Task Manager, the linear nest production order for each nesting document that belongs to the sales order will print with the picking slips, based on the form printer options in IN19 for form 57. | OE31, OE3L, TK1 |  |
| 39488 | Lift output flag added to PR18 to allow it to be disabled | A Lift column has been added to the Process form. This does not need to be enabled as the default behavior is to create lifts for finished goods in the IP documents.  If you do not want to create a lift, then you should set the flag to “N”. | PR18 |  |
| 39589 | Customer parts exported to SigmaNEST from credit memo or PR57 | When a credit memo for a SigmaNEST IP containing a customer part log is processed, the customer part log is automatically exported to SigmaNEST.  A “Show Parts” filter check box, and Prt column, have been added to Plate Nest Integration-Inventory (PR57); you can select part logs and export them to SigmaNEST. | PR57 |  |

---
