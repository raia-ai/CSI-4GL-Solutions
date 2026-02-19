---
title: "Update SigmaNEST IP"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Update SigmaNEST IP"
long_description: "Help documentation for Update SigmaNEST IP in the 4GL system."
---


Update SigmaNEST IP
===================

This function is used to confirm and update the IP and the SigmaNEST job. It is used after the Conf Production & SigmaNEST Program function is used to pick and validate the log used for the production job. You will be alerted if the process cannot continue due to a material origin mismatch in the finished goods.

You may be prompted to enter the elapsed time taken for the job; see Time Tracking.

Configuration


IN19 > Label Options > Function Label Usages - Set up a label usage for a shipping label (SL types) and select the “O” column to set a shipping label to print for finished goods reserved against an order. When the IP is confirmed, if there are finished good logs allocated to the order the user will be asked if they want to print shipping labels.  
Optionally set up label usages for Parent logs and Drop logs; if these are not set, no label will print for them.

---
