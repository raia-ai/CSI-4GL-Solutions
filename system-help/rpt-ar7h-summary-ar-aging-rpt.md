---
title: "AR7H - Summary AR Aging Report"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "AR7H - Summary AR Aging Report"
long_description: "Help documentation for AR7H - Summary AR Aging Report in the 4GL system."
---

AR7H - Summary AR Aging Report
==============================

This function produces a detailed Accounts Receivable Aging report, sorted by Currency code.

1. Choose Accounts Receivable » AR Reports » Summary AR Aging Report  [AR7H].
3. .



8. Indicate
9. Specify whether to age date by Invoice date (default) or Due date.
10. Specify whether to sort by Territory: Yes (default) or No.[in AR7D this field is described as being used to “filter” by territory. Presumably difference is intentional?]
11. Specify whether to include only customers with an AR balance: Yes or No (default).
12. Enter “Y” to have the report double spaced or leave blank for single spaced.
13. Enter “Y” to include customers who are over their credit limit, leave blank to exclude them.
14. If set to Yes, enter the Minimum Credit Limit to be used.
15. Enter “Y” to include Customer details or leave blank to exclude them.

Output
------

|  |  |  |  |
| --- | --- | --- | --- |
| column heading | needs description? (if yes, populate one of the next two columns only) | glossary description | report-specific description |
| Code |  |  |  |
| Customer Name |  |  |  |
| Credit Limit |  |  |  |
| Balance |  |  |  |
| September |  |  |  |
| August |  |  |  |
| July |  |  |  |
| Prior |  |  |  |
| CAD Customers |  |  |  |

---