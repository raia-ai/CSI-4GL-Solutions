---
title: "PO9Z - Paid Rebates Import"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "PO9Z - Paid Rebates Import"
long_description: "Help documentation for PO9Z - Paid Rebates Import in the 4GL system."
---

PO9Z - Paid Rebates Import
==========================

Use this function to import the Rebate Analysis Report (PO7W) and apply the rebates.

1. Open report PO7W and enter “Y” in the
   Apply Rebates column for each rebate you want to apply.
2. Save the document as a tab-delimited text file.
3. Open PO9Z.
5. After importing,
   open the PO7W report again. You will see an “A” beside each log that you entered “Y” for in step 1 if you selected show applied or both.

To unapply a rebate, open PO7W and enter “U” in the Apply Rebates column and repeat steps 2 and 3.

---