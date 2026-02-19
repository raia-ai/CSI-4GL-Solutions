---
title: "Inventory Scrap Policy Notes Rb"
source: "Inventory-scrap-policy-notes-RB.md"
tags: ["4GL", "Inventory Management"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Inventory Scrap Policy Notes Rb"
long_description: "This document provides detailed information about inventory scrap policy notes rb in the 4GL system."
---

title: "Inventory Scrap Policy Notes"
source: "Inventory-scrap-policy-notes-RB.pdf"
tags: ["inventory management", "scrap policy", "costing methods", "ERP systems", "log split", "IN16", "IN1T", "INIZC", "product costing"]
version: "1.0"
last_updated: "2025-12-04"
short_description: "Handwritten notes detailing the setup, maintenance, and processes for an inventory scrap policy within an ERP system. Covers costing methods, system codes (IN16, IN1T, INIZC), scrap types, and log splitting procedures."
long_description: "This document contains a transcription and structuring of handwritten notes concerning the implementation and management of a scrap policy for inventory, likely within a specific ERP system. It outlines the initial setup, including the choice between actual and average costing methods and the configuration of product lines and scrap codes. The notes detail a 'Scrap Maintenance Policy' governed by system code IN1T, which defines various scrap types (R, O, Z, T) and their financial implications on orders and inventory value. The document also explains the process of log splitting, how scrap is handled during this process, and the functionality of related inquiry screens like IN6C. Key system codes such as IN16 (Product Line Scrap Field), INIZC (Product Costing), and IN10Z0 (Scrap Log Cleanup) are explained. The notes provide a comprehensive overview of how scrap is created, valued, tracked, and removed from inventory."
---

## Setting Up Scrap Policy

> **Reference:** SEE PENN STAINLESS SCRAP POLICY

### Costing Method: Actual vs. Average
- **INIZC:** System code for Product Costing and Method Maintenance.
- **A:** Actual Cost
- **V:** Average Cost
- If using average costing and the scrap factor was not 100%, all existing inventory logs would be revalued by the cost difference.
> **Note:** Cannot devalue stock if the IN16 option states average costing.

### Inventory and Product Line Configuration

- **IN71 - Stock List by Log:**
    - Shows 'G' logs.
    - Displays weight but no piece count.
- **IN16 - Product Line Scrap Field:**
    - Defines the scrap `percent`.
    - Defines the `cost` (old way: unit cost - lbs).

### Homogenous Logs
- Allows for a 1"G" scrap log per product line.
- Requires the IUM (Inventory Unit of Measure) and CUM (Costing Unit of Measure) to correspond and be the same.
- A single scrap log can be used for multiple product lines.

### Setting Up a Single Scrap Log for Multiple Product Lines
1.  **Set up IN16** to point to the same Scrap Product Code.
2.  **Requirement:** All product lines must have the same CUM (Costing Unit of Measure).
3.  The Scrap Product Code is located in the `'+' - scrap field - IN16`.
4.  Reference DRP product line - Peerless as an example.

### Costing at the Product Level
- You can set Average Costing on a standard length and Actual Costing on cut codes.
- **IN1ZC (Product Costing):** Used for method maintenance. This is where you can revalue ("R" or "Y").

---

## Scrap Maintenance Policy (IN1T)

This policy is used in log splits, IPA, and OPA.
- **IN1T:** Defines scrap policy rules. (Documented via email to Joe).
    - Only affects cost on an order, not revenue.
    - Can be defined by **Product Line**.
    - Can be defined by **dimensions**.
    - All clauses must be TRUE for the policy to apply.

### Scrap Types

**R - Drop/New**
- A new scrap log is created at a revalued cost.
- The value difference is added to the order.
- This creates an incentive for companies to sell offcuts at a higher margin.
- **Log Split Action:** Creates another log and revalues.
- **Example:**
    - Return to log on order: extra 5% value.
    - Return drop to inventory: at 95% value.
    - Configuration: Type = `R`, % = `95%`.

**O - No Scrap Record Created**
- A scrap log is **not** created in inventory.
- The full scrap quantity and value are added to the sales order.
- **Log Split Action:** No log is created. The weight of the drop goes to the sales order line, and the customer is charged for the entire original piece.

**Z - Zero Value Scrap Record**
- A scrap record (log) is created with quantity (LBS) but zero value and no piece count.
- The scrap quantity/value is added to the order.
- The cost of the scrap is zero.
- **Log Split Action:** Creates a scrap log with quantity, but it is not revalued (cost is zero). The value of the scrap is added to the order.

**T - Revalued Scrap Record**
- A scrap record (log) is created.
- Both the original log and the new scrap log are revalued.
- **Log Split Action:** Creates a scrap log and revalues.
- **Example:**
    - `T` with revalue % = `98%`.
    - The log on the order would be charged 2% of the value.
    - The new scrap log (`G`) would be valued at 98%.

---

## Log Splitting and Scrap Management

### Split Log Inquiry Screen (IN6C)
- Will show revalued percentages (`%`'s) in the "Rvl" (Revalue) column.
- The **Scrap type and %** can be overwritten at the time of the log split.
- The rules in **IN1T** are more specific to product + specs and will supersede the general settings in **IN16** (which apply to all product lines based on % or cost).

### Log Split Process
- A log split cannot change the value of the original inventory piece.
- **ALLOC button:** Used for "true scrap".
- **PROD LINE IN16 Log Split option:**
    - Scrap allocation to the order.
    - Scrap allocation to the original log.

### Cleaning Up Scrap Logs
- **IN10Z0:**
    - Still requires processing an adjustment through IN31 and authorizing it in IN32.
    - Used to perform a monthly adjustment to remove scrap from inventory.
    - Creates an adjustment for all 'G' logs with on-hand quantity and/or on-hand pieces.

### Handheld Device Behavior
- Handhelds will display a "Y" in the column for "Scrap$" if a scrap policy has been applied.
- The scrap policy **cannot** be overridden on the handheld device.
