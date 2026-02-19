---
title: "Adm Timeouts"
source: "madcap.md"
tags: ["4GL", "ADMIN", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Adm Timeouts - 4GL Help Documentation"
long_description: "This topic provides detailed information about Adm Timeouts in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the ADMIN module."
---
Setting System Timeouts
=======================

logs out after a defined period of inactivity. This period is set both at the operator level as well as a global timeout. Operators are set up with a default timeout of 30 minutes, and global timeout is set to 5 minutes. If the operator has a timeout value of zero, the global timeout will be used instead.

The global timeout is set in MS33 > System Timeout.

The operator timeout is set in MS32 > Security > Timeout; you can change the value for multiple users at the same time in MS9E.

You can use MS61 to view any operators who had their session time out, along with which function/screen they were in at the time and what the timeout value (i.e. 30 minutes) was.

---
