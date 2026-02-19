---
title: "Rn 3.20 Oe"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rn 3.20 Oe - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rn 3.20 Oe in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Order Entry
===========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 39004 | Print tolerances on packing list | The form options for the packing list now include an option to include [T]OL for tolerances. | IN19>Forms>03>Form Options>Additional Details Print Order |  |
| 39043 | Convert S lines to C lines in OE45 | When you enter a credit note against an order and select Generate Lines, any S lines are converted to C lines on the credit note. | OE45 |  |
| 39093 | Deselect all labels | When printing shipping labels, the window to change quantities for each log now includes a Clear button to deselect all quantities. | OE7YA |  |
| 39166 | Repricing can be based on pricing qty or reserved qty | A new flag has been added next to the price field at the top of the Reprice window. When this flag is set the price is calculated using the reserved quantity instead of the pricing quantity. | OE31 |  |
| 39282 | Show Doc Status in OE31 PO Allocation tab | A new column has been added to the PO Allocation tab of a line item to display the document status. | OE31 |  |
| 39342 | OE31 Contacts allow all fax/email options | When accessing the customer contacts from the Contacts tab of a sales order, the fax and email check boxes have been changed to text fields that allow more options for indicating if quotes and sales orders should be sent by fax and/or email. For each field, enter **Y**es, **D**efault behavior (at time of quote/order entry, contacts to receive a fax/email can be confirmed and/or modified), **A**ctive (this contact will always receive the document via fax/email) or blank (the contact will not receive the quote electronically). | OE31 |  |
| 39521 | Reassign document lines to current manifest | A Scan field has been added to the Assign tab of the manifest. After selecting a Run ID, you can scan a document and it will be assigned to that run, even if it has no logs picked or was previously assigned to another run (unless it has been loaded, is closed, or belongs to a different warehouse). | MN31 |  |
| 39698 | Run OE91 by product line or product code | The Refresh Commit Out Quantities utility can now be run for a specific product code or product line, or “ALL”. | OE91 |  |

---
