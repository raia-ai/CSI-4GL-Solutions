---
title: "Logistics Manifest Manifest Notes Rb"
source: "logistics-manifest-manifest-notes-rb.md"
tags: ['SM3', 'Logistics And Shipping']
version: "1.0"
last_updated: "2026-02-19"
short_description: "Logistics Manifest Manifest Notes Rb"
long_description: "This document provides detailed information about logistics manifest manifest notes rb in the 4GL system. It includes procedures, reference information, and best practices for users and administrators."
---

title: "Logistics Manifest Notes RB"
source: "Logistics-Manifest-Manifest_notes-RB.pdf"
tags: ["logistics", "manifest", "load planning", "run template", "MN33", "MN31", "IN19", "WFL2", "inventory management", "order processing"]
version: "1.0"
last_updated: "2025-12-03"
short_description: "Handwritten notes detailing the process and configuration for manifest and load planning within a logistics or ERP system. Covers modules like MN33 (Run Template Maintenance), MN31 (Load Plan), and WFL2, along with related system options and procedures for assigning, picking, and loading orders."
long_description: "This document contains a series of handwritten notes outlining the workflow and setup for logistics operations, specifically focusing on Manifest and Load Planning. It details configurations within various system modules. Key areas covered include:
- **Manifest / Load Planning Setup**: The initial setup requires route codes to be defined on customer ship-to records.
- **MN33 (Manifest RUN Template Maintenance)**: This section describes how to set up run templates, link each run to a unique route for auto-assignment of orders, and an option to omit pick slips.
- **IN19 OE Options**: Mentions an option for 'Manifest Automatic Routing'.
- **MN31 (Manifest Load Plan)**: This is a core module with several tabs. The 'Run Tab' shows default runs and their status (Assigned, Picked, Loaded), and allows adding or modifying runs. The 'Documents Tab' lists all documents for a manifest. The 'Assign Tab' shows line items assigned to runs and allows for manual assignment. The 'Pick/Load Tab' details the process of picking and loading using handhelds (HH). The 'On Hold' tab lists orders on approval hold. The 'Runs Tab' describes processes for when a run is fully assigned.
- **Process Flows**: The notes describe practical workflows, such as using a USB scanner on the 'Assign Tab' to scan pick slips (W#) and index lines. It also details the process of using the Load Report with a handheld device (HH) in module WFL2 to scan manifests, logs, and packages before exiting. Finally, it outlines the shipping office's role in processing the run to generate pack slips."
---

## Manifest / Load Planning

-   Route code should be defined on Customer Ship-to records.

### Manifest RUN Template Maintenance (MN33)

-   Set up RUN templates.
    -   Each run should be linked to a ROUTE.
    -   Uniquely, if you want orders to auto-assign to a run.
-   `[ ] omit pick slips`
    > If "No Process/Machine" on a Wine item, can print picks by RUN ID.

### IN19 OE option - MANIFEST AUTOMATIC ROUTING

-   A switch allows for multiple manifests for the same day.

### MANIFEST LOAD PLAN (MN31)

*(pick req'd date or leave blank)*

> **Switch IN19 OE:** Warning if `LOAD REQ DATE` is from `PROCESS PCS`.

**Run Tab**

-   Shows default runs.
-   Shows status of run:
    -   ASSIGNED
    -   PICKED - by sales or HH
    -   LOADED
    -   STATUS
-   **Document BUTTON** -> generates document.
-   Can add another run or modify one on the list.
-   Does not update the MN33 table.

**Documents Tab**

-   Lists all documents assigned to this 'MANIFEST'.
    -   So all documents' required dates match the Manifest date.
-   Click on '...' Document ID, but you can pull in other documents from other dates.

**Misc. Doc**

-   Create any miscellaneous item to go on the truck.
    -   e.g., boxed gift, roll of tape, etc.

**Generate Misc. Doc**

-   Misc doc related to an existing document.
    -   e.g., something for an order from Customer Owned Warehouse.

**Assign Tab**

-   **By RUN ID**: Shows all line items assigned to a run.
    > *Must be per order, maybe.*
-   **Unassigned line items**: Also show and need to be manually assigned.
    -   e.g., IP, OP, SO without a rate or route is assigned to 2 runs.

*(Continued Below)*

**Pick/Load Tab**

-   When HH is picking logs (log.conf).
    -   **SWITCH IN19 OE**: "Only allow Log transfer in HH Picking confirmation".
        -   So that picked amount is confirmed on a child log so that it can be "LOCATED" to a bin location.
        -   OR - use PKG for everything.
-   Shows logs by run ID that have been loaded.

**On Hold Tab**

-   Orders on approval hold or PBP.

**Runs Tab**

-   When a Run is all assigned (but not loaded):
    -   Process -> run 'R' report.
    -   Create LOAD report.
    -   Give to operator.

### Using LOAD report & HH - WFL2

1.  Scan manifest #.
2.  Scan logs or packages.
    -   `VIEW ALL`
    -   `VIEW MISS`
    -   `VIEW ERR`
3.  When done, EXIT.
4.  Shipping office then Processes Run to get Pack Slips.

---

### Assign Tab (Continued)

-   Choose a run.
-   Put the cursor in the "Scan" field.
-   Use a USB Scanner to scan W#'s (pick slips) + index line.
    ```
    W#########
    SO#      index #
    ```

### IN19 FORMS OPTIONS (pick slip)

-   **BARCODE LINE NUMBERS** = `D` (document & line)
-   **DISPLAY LINE COUNTER** = `blank` (to display index #)
