---
title: "Wh Conf Prod Sigmanest Wf1L"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Wh Conf Prod Sigmanest Wf1L - 4GL Help Documentation"
long_description: "This topic provides detailed information about Wh Conf Prod Sigmanest Wf1L in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
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
