---
title: "IP-In-house_Production-PR41-Machine-Production-Schedule-fields"
source: "IP-In-house_Production-PR41-Machine-Production-Schedule-fields.docx"
tags: ["manufacturing", "in-house production", "PR41", "machine production schedule", "ERP", "process scheduling", "screen fields", "user guide", "operations"]
version: "1.0"
last_updated: "2025-12-03"
short_description: "This document details the Machine Production Schedule (PR41B) screen used in the In‑House Production module. It explains every search filter, the list view columns, and the available actions from the right‑hand toolbar and bottom action bar. The guide clarifies how to filter by warehouse, process, document, customer, project, machine, date range, and status; how totals are calculated; and how to interpret key column indicators. It also documents workflow buttons such as Release, Nesting, Create IP/OP, Allocate, Schedule, and Logs, enabling schedulers to release, plan, and execute work consistently."
long_description: "This reference describes the Machine Production Schedule (Form PR41B), a central workbench for production schedulers to review and action order line items that carry a Process code and are in Picked or Pre‑picked (PBP) status. The schedule aggregates eligible lines across orders and provides filtering, sorting, and bulk action capabilities, and it also feeds the Production Dashboard. By consolidating needed information and controls in one place, PR41B helps schedulers coordinate work, align material availability with capacity, and synchronize downstream documentation.

The Search Filters section explains how to constrain the worklist by Warehouse, Process, Document number/type, Customer, Project, Machine, date criteria (Estimated, Actual, or Requested), and picking Status. It also describes utility elements such as Total Time, Reset, and the clock icon that calculates Selected Time from estimated durations. Multi‑selection options on key filters (e.g., Warehouse and Process) allow targeted batching of like work. These filters ensure that users can focus on the most relevant set of lines for release, scheduling, or nesting.

A smart, sortable list presents the resulting line items and supports column re‑ordering and resizing. The document includes a complete dictionary of list columns, covering identifiers (warehouse, document, index, writer), scheduling fields (Estimated Schedule, Actual Schedule, Requested Date), customer and logistics attributes (customer name, ship via), material context (raw material, finished product, UOM, default bin), time estimates, and operational flags. Allocation codes (P, S, H, L, or C) clarify how a line was picked; completion (C) and origin (F/D) indicators, plus understock and incoming statuses, help users quickly assess readiness and constraints.

Action controls are grouped on the right and bottom. Right‑hand actions include Release (to move lines from PBP to PCK and print pick slips), legacy Process printing, Excel export, and nesting tools—linear and plate—to optimize material usage and reduce scrap. Create IP and Create OP generate internal or external processing documents using selected lines as raw material, streamlining the handoff from scheduling to execution. Bottom‑bar actions support detailed review, adding or deleting process codes on lines, picking, moving process codes, assigning replacement machines, editing Actual Schedule, toggling allocation indicators, mass‑setting Estimated Schedule from Requested Date, and viewing or editing allocated logs.

Use this guide as a field‑level and control‑level specification for PR41B behavior. It is intended for production schedulers, planners, and power users who operate the In‑House Production module, as well as for trainers and implementation teams who require authoritative documentation for configuration, testing, and standard operating procedures.

In addition to defining field meanings, the document captures behavioral nuances—such as how Estimated Schedule can be derived from Requested Date via the Est Sched function, or how allocation toggling interacts with downstream confirmations—so teams can predict outcomes of bulk actions. The structure and terminology align with the PR11 Machine Master, OE41 picking, and related nesting modules, providing consistent vocabulary across the production toolset."
---
## Overview

### Title
Machine Production Schedule - PR41B

### Description
All order line items are pulled to this screen if a ‘Process’ is assigned to a line item on an order, and the line item is in ‘Picked’ or ‘Pre-picked’ (PBP) status.  A production scheduler uses to view order lines to be fulfilled and can release/process like items together.  This screen also feeds the Production Dashboard.

## Search Filters

### Warehouse
Individual or ALL warehouse can be selected
- Even if ‘ALL’ is selected, in the ‘+’ field beside Warehouse field, multiple warehouses can be selected

### Process
Individual or ALL process codes can be selected, to match the Primary Process field on the Sales Order line item.
- Even if ‘ALL’ is selected, in the ‘+’ field beside Process field, multiple Processes can be selected

### Document No.
Type of document to select to show line-item detail for; options are BT (Branch Transfer), CC (Customer Consignment) and SO (Sales Order)
Field beside the document number type selection is to enter in a specific document number, or type ALL

### Customer
Can enter or search for a particular Customer Account number or ‘ALL’

### Project
To select a particular Nesting Project number, or leave blank for ALL

### Machine
Machine assigned to the order line item, or ‘ALL’, verified against PR11 Machine master table

### From Date
Can select ‘E’ (Estimated scheduled date), ‘A’ (Actual Schedule date) or ‘R’ (Requested Date), and then enter in a to / from date range, or leave the date range blank

### Status
A checkmark in the radio button will select all status (either PCK or PBP), or singular status can be selected of these two choices from drop down menu

### Total Time
The accumulation of all ‘Es Tm’ column values for all line items in list

### Reset
Data on the screen will be refreshed

### Clock icon
For any highlighted line items, the total time will be calculated for those selected line items from the ‘Es Tm’ fields, and will display next to the ‘Selected Time’

## Screen List Columns

A list of all line items matching the search filter criteria will display on screen.  This is a smart screen, so columns can be sorted by clicking on column headers and column order can be rearranged, and column widths resized.

| Column | Description |
|---|---|
| Whs | Warehouse code associated with document line item |
| Document | Document number associated with line item |
| Pro | Primary Process entered on document line item |
| Mch | Replacement Machine if assigned to the line item |
| Est Sched | if the ‘Est Sched’ button is used at the bottom of the screen then the ‘Requested Date’ from the line item will populate this field |
| Act Sched | User can enter in an Actual Schedule date on a line item by using the ‘Schedule’ button at the bottom of the screen |
| Req Date | The ‘Requested Date’ on the document line item |
| Customer | The Customer Name attached to the document |
| Shp | The Ship Via code attached to the document |
| Raw Material | The product code selected on the document line |
| Finished Prd | The finished product with dimensions and specs on document line |
| Quantity | Quantity requested on document line |
| UOM | Unit of measure for the quantity requested on the document line |
| Es Tm | The estimated time to take to complete this process |
| A | Allocated By indication; This value can be ‘P’ indicting that it was picked through picking confirmation OE41, ‘S’ indicating that it was picked and sales order is still in ASG status, ‘H’ indicating picked by Hand Held device, ‘L’ indicating picked by Log Split or ‘C’ which is assigned if the ‘Allocate’ button is used at the bottom of the Machine Production Schedule menu |
| C | If the value is ‘Y’ then this line item is complete |
| O | The material origin requested on the document line item at time of entry.  The value ‘F’ indicates that Foreign material was requested, and the value of ‘D’ indicates that Domestic material was requested |
| Customer Part Number | If there is a Customer Part Number assigned to the document line item |
| Index | The Index number assigned to the line item on the document |
| Status | The picking status of the document, which can be ‘PCK’ for Picking status or ‘PBP’ for pre-picking status, and the document line requires releasing to change the status to ‘PCK’ so that it can be processed |
| Incoming | If the document line item is incoming on a PO or an OP, the value will be ‘Y’, if the line item was incoming on a PO or an OP, which is now received, the value will be ‘R’ |
| U | Understock indicator if the available inventory is not sufficient to fulfil this document line item |
| Writer | The operator ID that entered the document |
| Dflt Bin | The Default Bin value that is assigned to the product code on the line item, which is pulled from the IN18 Product Master file |

## Buttons on Right Hand Side of Menu

### Release
When one or many line items are selected, if their status is PBP, this button will change their status to PCK and print the picking slip documents for each of the line items selected.

### Process
This is rarely used, it is from old version, Form 16, where the job traveller document is printed for line items selected.

### Excel
Any line items selected are exported to an Excel spreadsheet.

### Lin Nest
Selected line items, whether for one customer or across customers are sent to the NEST module which looks at all available inventory which could be cut to meet the criteria/dimensions of the material on the line items selected.  This will create a Nesting document which will suggest which inventory to cut to increase yield and reduce scrap.

### Plt Nest
Selected line items, whether for one customer or across customers are sent to the Plate Nesting module which looks at all available inventory which could be cut to meet the criteria/dimensions of the material on the line items selected, best increasing yield and reducing scrap.

### Create IP
Any line items selected are used to create an IP (In House Processing) document and the selected line items are the Raw Material on the IP document.

### Create OP
Any line items selected are used to create an OP (Outside Processing) document and the selected line items are the Raw Material on the OP document.

## Buttons on Bottom of Menu

### Detail
The line item details of any lines highlighted can be viewed.

### Add
Add another Process Cost Code to a document line item that is in PBP or PCK status, which will then show on the Production Schedule menu.  This code is verified against the PR11 Machine Master table.

### Delete
Delete any selected line items from the Production Schedule menu, and the Process Cost Code will be deleted from document line item.

### Pick
Assign an inventory log to a selected line item.  If log is allocated to both picked and used, then the partial/complete flag in the Production Confirmation (PR42B) will be ‘C’, otherwise it will be ‘P’.

### Move
Change a Process Cost Code on the document line item’s costing.  The value in the ‘Process’ field will be changed for that line item.

### Assign
Assign a Replacement Machine code to the selected line item.  The value in the ‘Machine’ field will change.

### Schedule
Edit the ‘Act Sched’ information for the line item selected.

### Allocate
Toggle the value in the ‘A’ column between ‘C’, if it was not originally ‘C’, or back to its original value, which could be ‘P’, ‘S’, ‘H’ or ‘L’.

### Est Sched
The ‘Requested Date’ on the document line item is entered in the ‘Est Sched’ field for all line items.

### Logs
If any inventory log is allocated to the selected document line item, the inventory log information will display, and the user is able to edit the picked qty from the log.
