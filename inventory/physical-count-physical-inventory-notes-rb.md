---
title: "Inventory-Physical_Count-physical-inventory-notes-RB"
source: "Inventory-Physical_Count-physical-inventory-notes-RB.pdf"
tags: ["Physical Inventory", "Inventory Count", "IN5B", "IN71", "INSE", "IN56", "IN51", "Warehouse Management", "ERP", "SOP"]
version: 1.0
last_updated: 2025-12-03
short_description: "A set of handwritten notes detailing the procedural steps for conducting a physical inventory count. The guide covers pre-count preparations, inventory initialization, data entry, variance reporting, and final inventory updates using specific system transaction codes."
long_description: "This document contains detailed, handwritten standard operating procedures (SOPs) for performing a physical inventory count within an ERP system. The process is broken down into sequential steps, each associated with specific transaction codes (e.g., IN71, IN5B, INSE, IN56, IN51). The notes begin with pre-count preparations, including running a stock list report (IN71) and reviewing pre-count checklists. The core of the process involves initializing the inventory count (IN5B), which freezes the inventory snapshot and sets all tags to zero. The notes emphasize the importance of restricting system access during this phase. Subsequent steps cover data entry (INSE), either manually or via handheld devices (HH), and detail what transactions can and cannot be performed during the count. The guide also covers generating and reviewing variance reports (IN56, IN5K) to identify discrepancies before finalizing the count. The final step involves updating the inventory subledger (IN51), which posts adjustments and completes the process. The document includes important warnings, tips, and configuration details, such as password requirements and system switch settings."
---

## Physical Inventory Process
### Pre-Count Review"
- **0641**: NO PICKED weight
- **0642**: All invoiced
- **Review PROCOUNT online CHECKLIST** - Document
---
### Step 1: Pre-Count Reports and Preparation
**Run IN71 report first.**
> **SAVE**: PRE INVENTORY COUNT INVENTORY
> Run **IN71** (Stock list by log) -> Export to Excel.
1.  **Check for Activity: **
-   **(1A) 0641 - No picked wt:** Check Active logs in **IN69**.
-   **(1B) 0642 - Nothing to invoice:** Check Inquiry.
2.  **LIMIT ACCESS TO IN5B.**
---
### Step 2: Inventory Count Initialization (IN5B)
**This creates a snapshot of the inventory before the count.**
> **WARNING: Restrict Access**
> If you redo the initialization after counting has started, **all you have counted will be lost**. All is reinitialized. This can be done by PROD.line if necessary.
-   **IN5B**: All inventory tags are set to zero.
-   This process is led by the Warehouse.
-   This prints 2 reports: 1.  **Invent Count**
2.  **Prestock**
-   **Note:** If uncommitted with `IN5C` (worksheet IP), then run `IN5C` again to refresh for SO.
#### IN5B Parameters
-   **Document date: ** The date you are updating G/L (generally the last day of the month).
-   **DESCRIPTION: ** Make it good (e.g., date - WH - all products).
-   **Tag Range: **
-   Run **IN69** to see the number of ACTIVE TAGS.
-   Start Tag #: 1
-   End Tag #: 1,000,000
-   Used for people who precount.
-   **IN55**: If you don't put enough tags, you have to expand tag allocation.
This process gives a Document # ("N#").
---
### Step 3: Inventory Count Data Entry (INSE)
> **MS32 MANAGER Security** is required to enter the new Log "N" on INSE.
-   **Manual Entry** (if not using Handheld): -   New Log "N" in the log field.
-   Fields: chg, length, locat., weight, PC.
-   **Handheld (HH) Entry**: `WF15`
> **Note: Adding Tags Post-Initialization**
> If you find something, you can add a tag to the inventory **BEFORE** final posting using **INSD**.
---
## Rules and Guidelines During Count
### System Restrictions
-   No receiving.
-   No location changes (`chg`).
-   No invoicing.
### Personnel
> -   **BUT: Cannot POST a PO or IP receipt.**
> -   **Cannot confirm or create packing slips.**
-   **Add/Update Log to Count (INSD)**
-   If a log exists, zero the quantity and then go into **INSE** to count.
-   `WF1Y`
---
### Step 4: Review Variance Reports
> **Review before final update.**
#### Inventory Count Variance Report (IN56)
-   Lists all tags with a variance (`%`, `Qty`, and `Value`) greater than the acceptable variance.
-   Can be run multiple times.
-   **Once the count is posted, you cannot run it again.**
-   If using Avg Costing, you can't run it again.
> **SAVE a final copy!** (paper, excel) before posting.
#### Tag Report (IN5K)
-   Shows what was counted. Review before final update.
-   Can list missing/not counted tags.
-   Can be run as often as you want.
---
### Step 5: Update Inventory (IN51)
> **PASSWORD: ICHGLS" (POST)**
-   This is run when the count is done.
-   Updates the Inventory subledger.
-   Creates Adjustments for posting variance (`IN16`) to the **INV VARI ACCOUNT**.
#### Working Papers
-   ONE LOG PER PAGE
#### Final Update? (Y/N)
-   **Y (Yes): ** Logs that haven't been counted will be adjusted to zero Qty.
-   **N (No): ** More updates will be done. Only logs that were counted will be updated.
---
## Post-Count Procedures
### Run Post-Count Report
-   After posting the Inventory Count (IN51), **run IN71 immediately** and keep the report.
-   **184GLSOL**: Pay 1 HR to have 1 HGL Person ON CALL.
### System Switches
-   **SWITCH: ** Auto bill string: counted or empty.
---

## Inventory-Physical_Count-physical-inventory-notes-RB