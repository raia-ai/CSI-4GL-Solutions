---
title: "Rn 3.18 Op"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rn 3.18 Op - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rn 3.18 Op in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Outside Processing
==================

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 38135 | Manifest tab added to OP inquiry | A Manifest tab has been added to the OP inquiry to view the manifest runs related to the order delivery. | PP64 |  |
| 38140 | OP lot header cost | Hdr/Lot Costs button allows you to enter a header or “M” line lot charge to be distributed proportionally by weight across all finished goods lines in a set. | PP34, PP35, PP36 |  |
| 38141 | Auto Receiving function for OP documents | New Auto Receive button has been added to the Sets tab of OP Receiving documents. Similarly a new wireless hand-held function has been created to perform this process.  In order to use this function, the OP document must include only one raw material, one raw material log, one or more FG items, each FG item should have attached lifts, and at least one FG should be committed to a sale. | PP36, WF1R |  |
| 38252 | Create an OP doc from a linear nest document | New Nest button on OP entry allows you to create an OP document by linking to a linear nest document. The system will create an OP document with one set per pattern; each set will have one raw material, one log and a number of finished goods. | PP34 |  |
| 38253 | Auto-Allocate sets window added to PR41B | When creating an OP from PR41B you are now prompted to select the vendor, then the set allocation window is shown to allow you to auto-allocate sets. | PR41B |  |
| 38290 | Date filters added to PP65 | The OP by Confirmation Number inquiry now includes fields to filter records by a date range. The default is the past 30 days. | PP65 |  |
| 38320 | Replacement cost column added to PP34, PP35, PP36, and PP64 | A “Rep Cost” column has been added in both the raw material and the finished goods sections in OP Entry, OP Confirmation, OP Receiving, and OP Order by #. | PP34, PP35, PP36, PP64 |  |
| 38353 38434 | The Raw Material Log tab in OP Entry and OP Receiving now allow Swap and Split | The Logs tab now includes buttons to Swap or Split a log. | PP34, PP35 |  |
| 38413 | FG remarks are now included in OP pick-up print | Finished good remarks now print below the finished good lines on the OP pick-up print. | IN19 > Forms > form 31 > Remark Line Types |  |
| 38459 | Separate width/length columns in log selection | When selecting a log, the width (if applicable) and length are displayed as follows: • If the product is a square product, you will see separate width and length columns.  • If the product is a long product you will only see the length column. • The dimensions will be displayed in the Search Unit defined in IN16>Options for the product; if not defined, it will use the unit set up in MS33>Length UOM. | PP34 |  |
| 38621 | Auto Receive creates lifts for finished goods | When a set has one RM, one RM log, and all finished goods have no lifts, the Auto Receive function will create a lift for each FG. | PP34 |  |

---
