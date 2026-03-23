---
title: Updating Pickup or Delivery Dates on POs
source: madcap.md
version: '1.0'
last_updated: '2026-02-19'
short_description: Updating Pickup or Delivery Dates on POs
long_description: >-
  Help documentation for Updating Pickup or Delivery Dates on POs in the 4GL
  system.
---

# Updating Pickup or Delivery Dates on POs

Use these functions to change the expected delivery or pickup date on one or more purchase order.

All open lines for a purchase order can be updated globally or each line can be updated individually.

## Change the Delivery Date

1. Choose Purchasing » Entry/Maintenance » Update Delivery Dates \[PO38].
2. Select purchase order Type of entry: BT = branch transfer, CC = customer consignment, CO = purchase order, PQ = PO Quotation.
3. Enter or select the Document Number or leave blank to select all open documents.
4. To change the delivery dates, select one or more lines and click Dlv Date.
5. To change the mill confirmation dates, select one or more lines and click Mill Conf.
6. To view or edit MOI details, select a line and click Edit MOI.
7. To add or replace MOI details for one or more lines, select the line(s) and click New MOI. Note that this will delete any existing MOI details on the selected lines, so you will be prompted to confirm your action.

## Change the Pickup Date

1. Choose Purchasing » Entry/Maintenance » Update Pick-up Dates \[PO3G].
2. Select purchase order Type of entry: BT = branch transfer, CC = customer consignment, CO = purchase order, PQ = PO Quotation.
3. To filter the list, optionally enter or select the Document Number and/or Vendor.
4. Select one or more lines and click Pick-up Date.
5. Enter a new date and click Save.
6. You are asked if you want to update the pickup dates on all lines in the selected documents.\
   If you click Yes, updates the pick-up date on the document header and all lines for each selected document.\
   If you click No, the pick-up date is updated on the document header only.

***
