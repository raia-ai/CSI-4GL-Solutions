---
title: "Rn 3.24 Ip"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rn 3.24 Ip - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rn 3.24 Ip in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
In-House Production
===================

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 40053 | IP from PR41B allows multiple raw materials | When creating an IP from the Production Schedule, you can now select multiple raw material lines and create many-to-many or many-to-one sets. | PR41B |  |
| 40454 | View and Mod options in IN3F | The Linear Nesting Project Maintenance page includes two new columns: - Press F4 on the View field to open the inquiry window for the nesting document. - Press F4 on the Mod field to open the nesting window in edit mode. | IN3F |  |
| 40575 | New spec compatibility table for plate nest integration | The specification codes for a product line now include a new column, “P”. This table allows you to enable one-way compatibility for two specs. For example, if you selected the P column for grade 304 and added 316, you are allowing users to select a 316 grade log when the original spec required was 304. However, this does not allow a 304 grade log to be used when a 316 grade was required. | IN16>Spc>Cde; PR51 |  |
| 40595 | Display special instruction in IP selection | When selecting an IP, you will now see an Instr column containing the first special instruction from the production order. | PR34, PR36 |  |

---
