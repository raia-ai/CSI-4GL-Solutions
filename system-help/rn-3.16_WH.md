---
title: "Wireless Handheld"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Wireless Handheld"
long_description: "Help documentation for Wireless Handheld in the 4GL system."
---

Wireless Handheld
=================

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 37898 | Changes to FINAL function in HH Picking Confirmation | The following changes have been made to the FINAL function in the HH Picking Confirmation screen: • it cannot be used when no lines are picked • it will close only partially picked lines when option 2 is selected • completion code messages have been clarified | WF11 |  |
| 38219 | WF11 Allow Substitution changes | A new setting has been added to the operator-level flag for log substitution during picking. This setting (**S**ales) controls log substitution based on if the salesperson allocated logs for an order line: - if no logs were allocated by the salesperson, the HH user can transfer any log (assuming compatible with order line product, foreign/domestic, etc.) - if logs were allocated by the salesperson, the HH user can only transfer the allocated log; they cannot clear the log nor add/transfer other logs. | WF11, MS32>Options>Order Entry>Allow HH Substitution=“S” |  |
| 38225 | WF19 Set Scheduled Date to Start Date if “Start” scan | In the Time Tracking function, you can bypass the Schedule action; if you choose 2 (Start), the Schedule date and time will be set to the Start date and time. | WF19 |  |

---