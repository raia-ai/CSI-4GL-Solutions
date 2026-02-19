---
title: "Cb Post Cash Book To Gl Cb41"
source: "madcap.md"
tags: ["4GL", "GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Cb Post Cash Book To Gl Cb41 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Cb Post Cash Book To Gl Cb41 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the GL module."
---


Post Cash Book to GL
====================

This function will update the GL with any entries from CB31 that have not been posted. It is required to close off at month-end. It can also be used to close the bank to prevent further activity.

This function is not necessary if the “Auto Transfer Bank Detail to Recon File” switch () is enabled to automatically post entries from CB31.

1. Choose General Ledger » Cash Book/Bank Rec » Post Cash Book to GL [CB41].


5. Enter or select the Posting Date.
6. Select the checkbox to Close Bank or leave blank to leave it open.

---
