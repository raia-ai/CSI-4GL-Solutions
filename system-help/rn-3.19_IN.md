---
title: "Inventory"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Inventory"
long_description: "Help documentation for Inventory in the 4GL system."
---


Inventory
=========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 38420 | IN76 caters to “ALL” entities | When you run the Detailed Adjustment Report for “All” warehouses, the output depends on the setting of the “Change Report Warehouse” operator option: - If set to “A”, then the report will return results from all warehouses - If set to “Y”, then the report will return results from warehouses that share the same division as the operator’s warehouse. | IN76, MS32 |  |
| 38421 39341 | Reason code added to inventory adjustment | Both Inventory Adjustment by Product (IN31) and by Log (IN35) now allow users to capture a reason for the adjustment (reason codes are maintained in new table IN1ZD).  The reason is included in the Detailed Adjustments by Date report; this report also now includes a flag to exclude log transfers. | IN31, IN35, IN76 |  |
| 38717 | Inactive column added to IN2B Excel output | The Product Codes listing Excel output now includes an “Inactive” column that identifies any deactivated products. | IN2B |  |
| 39168 | Display kg equivalent on inventory label | If the IUM is other than kg, the inventory label (LRLBLLGB) prints both the IUM and the kg equivalent. |  |  |
| 39226 | Bin location search filter on IN7U | In the Inventory Label by Bin Location report, if you choose to select a location you can search from all locations or enter partial text to filter the locations to a subset. | IN7U |  |

---
