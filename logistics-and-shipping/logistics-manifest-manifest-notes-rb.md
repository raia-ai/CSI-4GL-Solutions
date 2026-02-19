---
title: "Logistics Manifest Manifest Notes Rb"
source: "logistics-manifest-manifest-notes-rb.md"
tags: ['SM3', 'Logistics And Shipping']
version: "1.0"
last_updated: "2026-02-19"
short_description: "Logistics Manifest Manifest Notes Rb"
long_description: "This document provides detailed information about logistics manifest manifest notes rb in the 4GL system. It includes procedures, reference information, and best practices for users and administrators."
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
