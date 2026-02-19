---
title: "Global Utilities"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Global Utilities"
long_description: "Help documentation for Global Utilities in the 4GL system."
---

Global Utilities
================

|  |  |
| --- | --- |
| **LULITSPL** | Spawns a Child Log from the Parent Log equal to the Order quantity required. |
| **LULITDSC** | Disconnects any reserves by the Current Order to the Parent Log |
| **LULITTFR** | Checks if there are excess reserves on the Parent Log:   * If there are not, it will exit the function (we do not want to transfer Reserves from Parent to Child unnecessarily). * If there, are it will calculate the Excess Reserve. It will then process each reserve (OEL\_LOG) in turn:   + If the reserve is less than or equal to the Excess it will merely change the Log From Parent to Child.   + If it is not, it will spawn a Child Log with the minimum between the Reserve and the Excess.     The Reserve Transfer amount will then be down-dated on the Parent Log. |
| **LULITALL** | Reduces any Reserves on the Parent Log that are in excess of Available, and logs an Error record stating that the Reserve has been reduced by that amount. |

---