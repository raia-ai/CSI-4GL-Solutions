---
title: "In-House Production"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "In-House Production"
long_description: "This topic provides detailed information about In-House Production in the 4GL system."
---


In-House Production
===================

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 38369 | Option to exclude nest pattern from commit-out | A new column “E” has been added to the Linear Nesting Cutting Schedule to allow you to exclude a nest pattern from commit-out. | IN3F |  |
| 38443 | IP confirmation to allow selection of smaller compatible log | New switch (“Allow Sel of Lower Size Comp Dim Logs in Prod Conf”) allows you to confirm a smaller log in IP confirmation. | PR36 |  |
| 38353 38434 | The Raw Material Log tab in IP Entry and IP Receiving now allow Swap and Split | The Logs tab now includes buttons to Swap or Split a log. | PR34, PR36 |  |
| 38667 | Allow non-compatible logs to be entered in IP Receiving | A new switch (“Allow Logs for all Products to be Picked”) allows you to enter a log from a different product line if it has the same IUM and CUM. This also requires the operator OE switch “Disallow All Prod” to be turned off. | PR36, MS32 |  |
| 38851 | Linear nest production order includes barcode | If the project description on the form begins with a document number, there will be a barcode above it that contains the warehouse code and the document number from the project description. |  |  |
| 38861 | Switch to delay processing a posted SigmaNEST program | A new warehouse switch (“SigmaNEST Post Buffer Period”) allows you to set a buffer (in seconds) before a posted SigmaNEST program is processed. This prevents  from processing a program while SigmaNEST is still processing it, causing parts to be missing from the generated IP. |  |  |
| 38868 | Linear nesting production order now includes the order writer | A new "Doc Writer" heading is displayed on the right side of the page. If the project description starts with a work order number, the "Doc Writer" displays the order writer for that work order. |  |  |
| 38870 | Order writer added to PR7P | A new “Writer” column has been added to the Production Schedule Excel export that displays the order writer from the sales order. | PR7P |  |
| 38874 | Create an IP document from a sales order | When a line in a sales order references a machine code that is defined (in PR11) as an Inside process, when the SO is processed an FG will be created and the set allocation screen presented before the IP document is created. | PR36 |  |

---
