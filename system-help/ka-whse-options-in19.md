---
title: "Setting Up Kasto Warehouse Options"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Setting Up Kasto Warehouse Options"
long_description: "Help documentation for Setting Up Kasto Warehouse Options in the 4GL system."
---


Setting Up Kasto Warehouse Options
==================================

Kasto Options are accessed in the Warehouse Options [IN19].

| Option | Description |
| --- | --- |
| Kasto Unload Station | 02 (determined by Kasto) |
| Kasto Cutting Station | 01 (determined by Kasto) |
| Load Start Date | 01/01/20 (starting point for searches) |
| Unload Start Date | 01/01/20 (starting point for searches) |
| Auto Generate Adjustments | blank |
| Label Print Matrix | to be determined IN19 |
| Sync Start Date & Time | blank (used in Sync Analysis) |
| Sync End Date & Time | blank (used in Sync Analysis) |
| Allow Modification of Kasto Logs | Y |
| Debug the KASSND File | blank (for debugging purposes only) |
| Default Compartment Type | 05 |
| Is Kasto Enabled for This Warehouse? | Y |
| Kasto Debug Flag? |  |
| Location to Create Telegrams | /home/4gl/kasto (temporary Directory) |
| Log Zero Lengths For All Picking Documents | blank |
| Network Location to Receive Telegrams | /mnt/kasto/tcpsnd (Kasto Send Directory) |
| Network Location to Send Telegrams | /mnt/ksto/tcprcv (Kasto Receive Directory |
| Populate Heat Numbers on Picking Documents | Y (log the Heat Number on the output transaction) |
| Station Where Inventory is Loaded | 03 (determined by Kasto) |
| Use Kasto Piece Count? | Y=uses the Piece Count logged by KASTO; blank=the Piece Count will be calculated as it is currently, but can be overridden |

---
