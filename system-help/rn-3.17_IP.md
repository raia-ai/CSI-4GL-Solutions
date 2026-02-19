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
| 37716 | Sigma plate reservation | When you reserve a plate in SM3, it will now also reserve the plate in SigmaNEST. | OE31, OE41 | SD |
| 37965 | Change to WOData1 and WOData2 fields in SigmaNEST | When exporting a sales order to SigmaNEST, the WOData1 column in the SigmaNEST work order now shows a concatenation of the thickness and SigmaNEST material of the sales order line. The WOData2 column now shows the customer part number of the sales order line. | PR44B |  |
| 38052 | Add customer filter to PR41B/PR42B | A Customer field has been added to the Machine Production Schedule and Machine Production Confirmation to allow users to select a customer to filter the form data. The Export Production Schedule report will similarly filter the results by the selected customer. | PR41B, PR42B, PR7P |  |
| 38106 | IP forms now look at IN19 to decide remarks to print | The Finished Goods remarks that print on sub-contract, production order form, production order work order, and job traveller forms are now controlled by IN19 Form Options. | IN19 > Form Options |  |
| 38111 | Weight field added to FG Maintenance and Receiving screens | A display-only Weight field has been added to the FG entry and receiving screens next to the IUMs, allowing you to check the weight against the theoretical weight. | PR34 |  |
| 38154 | Allow users to re-open closed FG lines | The Close FG button has been changed to a toggle, so that if you select an FG line that has been closed, the button becomes Open FG. | PR36 |  |
| 38155 | Allow entry of zero quantities in IP Receiving | In the Receiving window, the Current Units reflects the received amount on the lift record, and can only be changed or set to zero in the lift record. If the lift is deleted, then the figures can be adjusted on the main screen. | PR36 |  |

---