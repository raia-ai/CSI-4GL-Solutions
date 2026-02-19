---
title: "Rn 3.19 Sec"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rn 3.19 Sec - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rn 3.19 Sec in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Security
========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 38517 | System timeouts | logs out after a defined period of inactivity. This period is set both at the operator level as well as a global timeout. Operators are set up with a default timeout of 60 minutes, and global timeout is set to 5 minutes. If the operator is changed to a timeout value of zero, the global timeout will be used instead. The global timeout is set in MS33 > System Timeout. Operator timeouts are set in MS32 > Security > Timeout; a new screen (MS9E) allows you to change the value for multiple users at the same time.  A new inquiry screen, MS61, allows you to view any operators who had their session time out, along with which function/screen they were in at the time and what the timeout value (i.e. 60 minutes) was. | MS33, MS32, MS9E, MS61 |  |

---
