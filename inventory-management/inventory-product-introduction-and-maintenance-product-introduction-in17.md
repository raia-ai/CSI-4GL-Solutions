---
title: "Inventory-Product_Introduction_and_Maintenance-Product_introduction_in17"
source: "Inventory-Product_Introduction_and_Maintenance-Product_introduction_in17.pdf"
tags: ["product introduction", "inventory management", "steel manager iii", "in17", "product master", "file maintenance", "warehouse management"]
version: 1.0
last_updated: 2025-12-03
short_description: "This document outlines the procedure for adding a new product to the warehouse using the IN17 (Product Introduction) function in Steel Manager III. It provides step-by-step instructions on accessing the screen and details the purpose and usage of each field in the Product Master Introduction form."
long_description: "A detailed guide on the IN17 (Product Introduction) process within the Steel Manager III system. This document serves as a reference for users responsible for inventory and product master data management. It explains two methods for accessing the 'Product Master Introduction' screen: through the main menu and via a direct command prompt. The core of the document is a comprehensive, multi-page table that describes each field on the introduction screen, from 'Product Code' and 'Product Line' to 'Warehouse' assignments and confirmation prompts. For each field, the guide specifies its description and provides clear instructions on its use, including keyboard shortcuts like <F4> to open selection windows. It covers essential product attributes such as specifications, dimensions, weights, units of measure (UOM), and optional data like product images and chemistry validation codes. The guide concludes with instructions on how to finalize the product creation process by assigning it to warehouses and confirming the transaction."
---
# Product Introduction - IN17
This guide explains how to add a new product to one or more warehouses in Steel Manager III using the IN17 function."
**Reports: **
- Product Master - IN2B
## Accessing Product Introduction (IN17)
You can access the Product Introduction screen in two ways: 
- **Via Menu: ** Click **Masterfile > File Maintenance Menu > Product Introduction** in the Inventory Control Main Menu.
**Or**
- **Via Command: ** Type `IN17` in the prompt and press `<Enter>`.
The **Product Master Introduction** screen will open.
## Product Master Introduction Fields
The following table describes the fields on the Product Master Introduction screen (WIPRDENT).
| Field | Description | Use |
|: --- | :--- | :--- |
| **Product Code** | System Product code and Pseudo Code. | - Display only - will be blank until Product has been entered. |
| **Product Line** | The Product Line the product code belongs to. | - Type Product Line Code or Press `<F4>` to open the **Select Product Line** window. |
| **Specification** | Product Specifications e.g. Grade, Finish. | - Press `<F4>` to open the **Specification Details** window. |
| **Size** | Specify Product Size. | - Press `<F4>` to open the **Product Dimensions** window. |
| **Description** | Product Description. **Note: ** If the Product Line Options setting is set to use Pseudo Code, custom descriptions will be overridden. | - Type Product Description. |
| **Length / Piece** | Length per piece (in Standard Length Units). Only displayed for products with a fixed length (F). | - Display only. |
| **Square / Piece** | Square per piece (in Standard Length Units squared). Only displayed for products with fixed dimensions (F). | - Display only. |
| **Volume / Piece** | Volume per piece (in cubic Standard Length Units). Only displayed for products with fixed dimensions (F). | - Display only. |
| **Weight: ** <br> Per inch <br> Per Foot <br> Per Square Foot | Weights entered if "Per Standard Length Theoretical Weight Calculation" option is set in the **Product Line Options**. Generally: <br> - Long Products - Weight per Foot <br> - Flat Products - Weight per Square Foot <br> - Piece Products - Weight per Piece | - Type weight in standard UOM's. Up to 4 decimal places. |
| **Inventory UOM** | Stocking UOM for Product Lines. | - Display only. <br> - Press `<F4>` to view the **Inventory UOM** window. |
| **Costing UoM** | Costing UOM for Product Line. | - Display only. <br> - Press `<F4>` to view the **Costing UOM** window. |
| **Buying UOM** | Buying UOM for Product Line. | - Display only. <br> - Press `<F4>` to view the **Buying UOM** window. |
| **Selling UOM** | Selling UOM for Product Line. | - Display only. <br> - Press `<F4>` to view the **Selling UOM** window. |
| **Pricing UOM** | Pricing UOM for Product Line. | - Display only. <br> - Press `<F4>` to view the **Pricing UOM** window. |
| **U.D.F.s** | User Defined Codes. | - Not used. |
| **Comments** | Additional comments for the Product code (3 lines, 30 characters each) e.g. "not suitable for water applications". Comments are visible in **Product Warehouse Details**. | - Type additional comments. |
| **Product Image** | Option to assign a Product Image file (picture). The file can be viewed on the Product Warehouse details window. The path to the Product Image file is assigned in **Warehouse Maintenance (IN19) – IN Options**. | - Type the Product Image file name (optional). |
| **Chem Val code** | If using "System Generated MTR's", this option assigns a Chemistry Validation code for the new Product code. Chemistry Validation codes are created in screen **IN14 > CVC**. | - Press `<F4>` to open the **Select Alloy Chemistry Validation Code** window or leave blank if not using "System Generated MTR's". |
| **Create?** | Create Product Code? <br> Y = Yes | - Type `Y` or `/` to exit (cancel) the transaction. |
| **Add Whse?** | Add Product Code to all Warehouses. <br> Default: Blank (No) | - Type `Y` (Yes) to add the Product Code to all Warehouses. <br> - Upon exiting the window (F3), the system will open the **Input Average Cost** window. |
| **Warehouse** | Assign the product to specific warehouses. | - Press `<F4>` to open the **Active Warehouse** window. |
| **Order Remarks** | Option to add Product Order Remarks. Remarks print on Customer Documents (as a second line). | - Press `<F4>` to open the **Input Product Order Remarks** window. |
| **Ok?** | Confirm input of Product Code Changes. | - Type `Y` (Yes) to proceed. |
---

# Inventory-Product_Introduction_and_Maintenance-Product_introduction_in17
