---
title: "Time Tracking"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Time Tracking"
long_description: "Help documentation for Time Tracking in the 4GL system."
---

Time Tracking
=============

The Time Tracking [WF19] function can track time for a sales order or IP/nesting document. Document must be in PCK status.

1. Scan the document in one of the following formats:
   * warehouse code followed by the document number
   * warehouse code followed by the document number followed by a line index
   * document number
   * document number followed by a line index
   * sales order number, omitting the type of entry prefix (W)
2. Use the Act field to manage the accumulated job processing time:  
   1 – schedule the job|  
   2 – start the job  
   3 – pause  
   4 – unpause  
   5 – stop the job

You can bypass the Schedule action; if you choose 2 (Start), the Schedule date and time will be set to the Start date and time.

The total time is visible in the Sales Order Inquiry (OE61), on the Details>Scheduled tab. This would be populated for machines that have an end date and time, and is calculated as the difference in minutes between end and start minus any elapsed pause time.

Enforced Time Tracking
----------------------

If the “Production Time Tracking Mandatory on HH” switch is enabled:

* Plate nesting:
  + If time tracking was initiated in WF19, the timer will stop when the job is updated in Update SigmaNEST IP [WF1M].
  + If time tracking was not initiated in WF19, when the job is updated in WF1M the operator will be prompted to enter how long the job took.
* Linear nesting:
  + If time tracking was initiated in WF19, the timer will stop when the last section on the production order is split in WF1U.
  + If time tracking was not initiated in WF19, when the operator processes the first split they will be prompted to enter how long the job took. The elapsed time for the project is then calculated and proportioned based on the number of cuts.

---