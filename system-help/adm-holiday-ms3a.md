---
title: "Recording Holidays"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Recording Holidays"
long_description: "Help documentation for Recording Holidays in the 4GL system."
---


Recording Holidays
==================

Define the holidays observed in each warehouse. This schedule is used to skip over holidays in addition to weekends when calculating shipping days, requested date, etc.

Holidays may or may not be the same as observed by the public: you may have company-specific shut-down days, or your warehouses may observe holidays on different days (e.g. one warehouse may observe a particular holiday on a Friday and another warehouse may observe it on a Monday).

1. Choose Administration » Administration » Holiday Maintenance [MS3A].
2. Select the Warehouse that the schedule applies to.
3. Enter the Date of the holiday, and a Description.

When calculating shipping days and requested days,  looks at this schedule as well as the “Order Shipping Date Lead Time in Days” switch (MS33>System) to ensure that the Requested Date on an order is skipping over weekend and holidays.

For example:

* order is entered on Wed Oct 4
* lead time switch is set to 3
* Mon Oct 9 is defined in MS3A as a holiday
* the requested date on the order will default to Oct 10 (skipping Sat, Sun and Mon).

---
