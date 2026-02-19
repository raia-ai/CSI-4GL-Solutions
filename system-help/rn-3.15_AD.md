---
title: "Administration"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Administration"
long_description: "Help documentation for Administration in the 4GL system."
---

Administration
==============

| Ticket | Title | Description | Function |
| --- | --- | --- | --- |
| 33779 | Make route table warehouse dependent | Routes can now be assigned to a warehouse in route maintenance. If the warehouse code is left blank the route will be accessible from any warehouse (i.e. ALL warehouses). | MS3S |
| 36946 | Add ability to kill session from the Record Lock screen | If your operator is configured as a Super User (in MS32), you can now kill another user session directly from the Record Lock screen. | RECLOCKS  [this BG was hidden when Super User field was removed in 3.22] |
| 37514 | Add Prov/State filter to City Master file listing | The City Master file listing can now be filtered by a province or state, or left as ALL. | MS5F |
| 37515 | Create County Listing report | New County Master file listing of entries in MS46; excludes the description of the tax code and the tax rate. | MS5H |
| 37938 | Don't allow all numeric operator codes | operator codes can no longer be created with only numbers. | MS32 |
| 38123 | Deprecate MS95 | The Restart License Server function has been deprecated. Please contact 4GL if you have any license issues. | MS95 |

---