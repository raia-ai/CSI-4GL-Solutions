---
title: "Wh Ship Label Wf22"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Wh Ship Label Wf22 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Wh Ship Label Wf22 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Create Shipping Labels
======================

[explain difference between this (prints SL03 in IN19 Label Options > Label Printer Defaults) and Print Shipping Labels WF17 (prints SL02)]

[this is from the old help, but it doesn’t match the SHPLBL function described at the bottom of Pick Orders/Transfers which includes a field to select the label type (heat/pkg/generic) - is that difference correct, or should this function (and screenshot) be updated to include that field?]

Print shipping label(s) for individual sales orders (document number prefixed with “I”), branch transfers (document number prefixed with “T”) or Outside Processing orders (document number prefixed with “C”).

![](../Resources/Images/WH_ship_labels.png)

1. Scan or enter (or press F4 to select) the order/branch transfer Doc number (if entering manually, you can omit the letter or leading zeroes).
2. Type the number of each bundle type1 (this determines how many shipping tags will print).
3. Type “1” to print the tags or “0” to save for later.

Sample


![](../Resources/Images/WH_ship_labels_sample.png)

[confirm config path; old help said System Maintenance>OE Options but I think the below is correct]

Configuration


1 OE Options > Packaging Types

---
