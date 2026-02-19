---
title: "IN7XA - Log Tracking Report"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "IN7XA - Log Tracking Report"
long_description: "Help documentation for IN7XA - Log Tracking Report in the 4GL system."
---


IN7XA - Log Tracking Report
===========================

This Excel report returns log movements for all logs that fit the selected criteria:

* all or a selected Warehouse
* all or selected Product and Product Lines
* invoice date range
* If the Sales Only check box is selected, the report only returns log movements of type IV, CM, or DM.

The report displays the following columns:

* Warehouse
* Vendor (if the origin log came from a receipt)
* Origin log: the original log that this log came from
* Parent log
* PO Number (if the origin log came from a receipt)
* TOE (type of entry of the log movement)
* Document (of the log movement)
* Document date (of the log movement)
* Product Description
* Case number (of the log)
* Date Received (on the log)
* IUM quantity (of the log movement)
* IUM (inventory unit of measure)
* Cost price (of the log movement)
* CUM (costing unit of measure)
* Cost value (of the log movement)

The report will also print values for the following columns if the log movement is of type IV, CM, or DM:

* Sales warehouse
* Document line
* material weight (weight of the stock line)
* weight UOM
* cost value of the stock line
* sales value of the stock line
* margin
* margin %

---
