---
title: "Sales Price Book Notes Rb"
source: "Sales-price-book-notes-RB.md"
tags: ["4GL", "Sales and Order Entry"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Sales Price Book Notes Rb"
long_description: "This document provides detailed information about sales price book notes rb in the 4GL system."
---

title: "Sales Price Book Notes"
source: "Sales-price-book-notes-RB.pdf"
tags: ["sales pricing", "price book", "tier pricing", "customer pricing", "markup", "costing method", "system configuration", "IN19", "IN15", "OE"]
version: "1.0"
last_updated: "2025-12-03"
short_description: "Handwritten notes detailing the configuration and logic of a sales pricing system, covering price books, costing methods, markups, customer-specific pricing, and tiered pricing structures."
long_description: "A comprehensive transcription and structuring of handwritten notes concerning a complex sales pricing system. The document outlines various pricing methods, including the primary 'Price Book' (IN15), customer-specific pricing (OE4M), and system-wide 'Tier Pricing'. It details how the system determines a sales price, starting with the default setting in IN19 (OE) and flowing through a hierarchy of overrides. Key concepts covered include different costing methods (Average vs. Replacement), master markup maintenance (IN1W), markup by customer ranking (IN1V), and pricing categories (IN1G). The notes also describe system utilities for importing/exporting data (e.g., OE1J, OE1I) and recalculating prices (IN1J). This document serves as a technical guide for understanding and configuring the various modules and flags that control product pricing within the sales order process."
---

## Price Book and General Pricing Logic

This section provides help in understanding the Sales Pricing and SO (Sales Order) - Prod Pricing Menu.

### IN19 (OE) - Default Sales Price in OE
- **'B'**: Second Tier Price Book, Cost Source 'O'.
- **If Blank**: Looks at `IN15` - Price Book.

### Price Book (IN15)
- Defines base prices.
- Prices are entered for each product line, including quantity breaks.
- This pricing method looks at reserved weight.
- **Usage Condition**: This is ONLY USED IF the `IN19 (OE)` "Second Tier Price Book Cost Source" flag is blank.
- **Product Grouping**: Can group products for quantity break pricing.
    - `DISABLE Grouping` switch is available.

#### Price Book Example & Calculation
- **Base Price**: Can be either manually typed in, the replacement cost, or sourced from `IN15`.
- **Price/lb Calculation Formula**:
    1.  `(Price Book #) * (Theoretical Weight LB (to 4 decimal places)) = $`
    2.  `$ / (Reserved Weight (rounded, zero decimal)) = $$ / lb`
- **Example Calculation for Price Book 3.76**:
    - **1 pc**: `3.76 * (7.872 * 1)` divided by reserved weight = `3.70`
    - **5 pc**: `3.76 * (7.872 * 5)` divided by reserved weight = `3.79`

### IN19: Costing Method for Orders
- **A - Average**: Average of all logs. Includes received inventory. Does not reflect pre-receipts.
- **R - Replacement**: All product lines or nothing. If no replacement costs, the system defaults to 'A' (Average).
- **Setup**: Import/export is set up manually.
    - `IN9P`: Replace one by one.
    - `IN9Z`: Apply 'A' to all.
    - `IN9ZQ`: Import/Export utility.

### M333 (OE) - Costing Method Switch
- Can also switch the costing method between AVG and Replacement.

---

## Markup Pricing

### Master Markup Maintenance (IN1W)
- **Setup**: Set up once.
- **Example**:
    - `cat = 10`
    - `descrip = 10`
    - `type = M`
    - `factor = 1.10`
- **Result**: This configuration applies a 10% markup, calculated as `1.10 * cost = price`.

### Markup By Customer Ranking (IN1V)
- Can be configured with or without grade, with grade specs.
- Follows a hierarchy.
- Allows setting quantity breaks and a Master Markup code.

### Combined Pricing Definition (IN1U)
- **'P' column**: 'Y' if grouping is applied only for a stated product line.
- **'blank'**: Grouping applies to all product lines.
- **F9**: Accesses the second base price.

---

## Customer Pricing

### Customer Pricing: By Product
- This method will **override** the price book.
- Set `IN19 (OE) "Default Sales Price in OE"` = 'Customer'.

#### OE4M -> Customer Pricing
- Manages a list of products for a specific customer.
- Sets a specific price for a defined date range.
- Allows price updates by a new price or by a percentage of the old price.

#### OE9YF - Delete Utility
- Deletes records from `OE4M`.

#### Customer Pricing Import (OE9XA)
- Use `TEMPLATE` or `FILE` to import customer pricing data.

### Customer Master (ARIF) - "Pre Option"
- Set rank by product line.
- This checks against `IN1V` (Markup by Customer Ranking).

### OE - Price in Order
- `COST` = Replacement Cost.
- The Sales Order Booking Report will show replacement costs.

---

## Tier Pricing

*Appears in "Sales Pricing" on Sales Order entry.*

### IN19 (OE) - Default Sales Price in OE
- **'P'**: Predefined.
- If a customer is assigned a tier level, it is highlighted.

### System-Wide Tier Configuration
- 9 tiers available.
- No quantity breaks.
- **Logic**: `cost val`, `% tier val`, `sales val`. Margin = margin % of sales value.
- **MS37 - Default Tier Factor**:
    - Each tier has a factor: `Adder`, `Multiplier`, or `Divider`.
    - These factors are applied to the base cost.
    - *Note: "Letters on M337 Mean Nothing".*

### Pricing Categories (IN1G)
- Set up all categories.
- Each category has a base price and 9 tier factors.
- `Divider`: e.g., 1.9 = 10% Margin.
- `Replacement Cost`: Can be distributed to all products.
- `Price Tolerance`: Used for price approvals.
    - `MS32 - OE/option`: Price Approval Discount Limit %.
- Categories are then assigned to products.

### Set Categories to Products (IN1H)
- Can add an 'adder' (e.g., $1.00).
- The adder amount (e.g., $1.00) will be added to the base price, and then the tier factor is applied.

### Default Tier Factor (MS37)
- Applies if no product category (`IN1H`) is assigned.
- *Note: "Letters mean nothing".*

### Customer Tier Assignment (AR17)
- Assign each customer to a specific tier.

### IN19 (OE) - Force Tier Price Check
- **N - No**: No check.
- **Y - Yes (Any Pricing Method)**: If a salesperson overrides the defaulted sales price.
- **M - Modified (Any Pricing Method)**: If a salesperson overrides the defaulted sales price to something lower.
- **T - Tier Pricing**: If a salesperson overrides the sales price to something lower than Tier 1.
    - *This check is only for products with an assigned pricing category.*

---

## Individual Product Pricing

### Individual Product Pricing (IN10K)
- No quantity breaks.
- Set up Sales Price for a specific Part Number (P/N) and Customer (Cust).
- `F9`: Can see inventory.
- `Column 'C'`: See change history.
- **Usage**: Used in conjunction with:
    1.  Default product pricing for individual products by customer.
    2.  Tiered default product pricing (if tier price is not found).
    3.  Price book.
- **Hierarchy**: The individual price will **supersede** other pricing methods.
- **Import/Export**: `IN9YC`.

---

## System Utilities & Data Management

### Exports / Imports
- **Price Book**:
    - `exp OE1J`
    - `imp OE1I`
- **Markup by Customer Ranking**:
    - `exp OE1L`
    - `imp OE1K`
- **Customer Ranking**:
    - `exp OE1N`
    - `imp OE1M`

### Predefined - Tier Pricing (IN1X)
- Distributes Category Factory Distribution factors to all categories.
- Can change values (e.g., for Divider).
- **Important**: If you use this, you must **RUN `IN1J`** to recalculate sales prices immediately after.

### Category Price Recalculation (IN1J)
- Run this if you need to update/recalculate sales pricing on `IN1H`.

### Copy Category Price (IN1K)
- Copies category price assignments on `IN1H` from one warehouse (WH) to another.

### Adjust Category Adders (IN9Z1)
- Pick a category and adjust/modify the 'adders' defined in `IN1H`.
