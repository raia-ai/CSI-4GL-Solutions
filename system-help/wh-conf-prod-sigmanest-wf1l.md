---
title: "Conf Production & SigmaNEST Program"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Conf Production & SigmaNEST Program"
long_description: "Help documentation for Conf Production & SigmaNEST Program in the 4GL system."
---

Conf Production & SigmaNEST Program
===================================

This function is used to pick and validate the log used for the production job.

Scan the document, which brings up the plate assigned to the job. If the operator used a different plate, scan the different log (must be same material and dimensions and material origin). If they chose a different size plate, the remnant will be different and the job must go back to the CAD department to be renested on the new plate.

After this is completed, use Update SigmaNEST IP to confirm and update the IP and the SigmaNEST job.

When performing a log swap,  will attempt to submit the transaction to SimTrans every five seconds; if the maximum defined attempts1 is reached, you will be prompted to resubmit or cancel the swap.

Configuration


1  > SimTrans Transaction Check Max Attempts

---