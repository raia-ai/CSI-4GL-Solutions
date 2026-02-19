---
title: "Purchasing"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Purchasing"
long_description: "This topic provides detailed information about Purchasing in the 4GL system."
---


Purchasing
==========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 37996 | Excel PO Import cater for random lengths | If the product line allows random dimensions, you can enter a random length/width, in the form of min-max (e.g. 10-20) in the Excel import file. | PO3D |  |
| 38048 | Select All button added to PO45 | The MTR Indexing By Receipt / Heat # form now allows you to Select All (or Deselect All). | PO45 |  |
| 38058 | Receipt Confirmation task created from PO41 | If a sales order has the same product reserved as the received product on the PO, a Receipt Confirmation task is sent to the salesperson. | PO41, TK1 |  |
| 38409 | Changes to manifest when lines added to a PO | If you add lines to a PO that has already been processed, or update the pickup date, the changes will not be reflected in the manifest until you reprocess the PO (if MS32>PO Re-Approval is required).  If PO Re-Approval is not required, the changes will be reflected in the manifest when you exit the PO. | MN31, PO31,  MS32>Options>Purchase Order>Additional Options>PO Re-Approval |  |
| 38416 | New switch for receipt confirmation task | A new switch (“Create Receipt Confirmation Task”) controls if and when a receipt confirmation task is created: - If the switch is set to blank, then no new receipt confirmation tasks will be created.  - If the switch is set to "H" (hard allocation only), then new receipt confirmation tasks will be create for sales orders that are allocated to the received PO line. - If the switch is set to "S" (soft allocation only), then new receipt confirmation tasks will be created for sales orders that have committed out for the same product. If an open receipt confirmation task already exists for a sales order, it won't create a new task no matter what the switch is set to. | , PO41, WF23 |  |

---
