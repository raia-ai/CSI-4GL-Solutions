---
title: "Sales-Costing_Average_vs_Actual_method_based_on_Product_Line_and_Individual_Product_Level"
source: "Sales-Costing_Average_vs_Actual_method_based_on_Product_Line_and_Individual_Product_Level.pdf"
tags: ["Costing Method", "Average Costing", "Actual Costing", "Inventory", "Product Line", "Product Level", "IN16", "IN1ZC", "IN92", "4GL"]
version: 1.0
last_updated: 2025-12-03
short_description: "A technical guide explaining the difference between Actual and Average costing methods in the 4GL Solutions system. It details how to set and manage costing defaults at the Product Line level (IN16) and how to configure specific costing methods for individual products (IN1ZC), including the process for recalculating average costs (IN92)."
long_description: "This document provides a comprehensive walkthrough of configuring and managing inventory costing methods within the 4GL Solutions software, specifically focusing on the distinction between 'Actual Costing' and 'Average Costing'. It is structured in two main parts. The first part covers the 'Product Line Level,' explaining how to use the IN16 program to check and set the default costing method for an entire product line (e.g., ASH). This default determines the costing method applied to new products created under that line. The second part details the 'Product Level,' which is the ultimate control point for an item's costing method. It provides step-by-step instructions on using the IN1ZC program to view or change the costing method for a specific product from Average ('V') to Actual ('A') or vice-versa. The document includes important operational notes, such as the financial implications of switching from Average to Actual and the requirement to rebalance the General Ledger. It concludes with instructions on running the IN92 utility to recalculate average costs after making changes, emphasizing that this should be done when no other users are in the system to avoid data locks. Screenshots of the IN16, IN1ZC, and IN92 screens are included for clarity."
---

## Costing Method Based on Product Line and Individual Product Level"
**Description: ** Actual vs Average Costing setup for products and product lines.
Let me break this down in two parts to help clarify how costing methods are handled in the system: ## 1. Product Line Level
You can check the default costing method set for a product line by following these steps: -   Navigate to **IN16**
-   Select the product line (e.g., **ASH**)
-   Click on **More Options** to open the *Product Line Options* window
-   Under **Costing Method**, you'll see whether the default is set to **Average** or **Actual**
This default setting determines how costing is applied when new products are created under that product line. However, please note that the actual costing method used is controlled at the **product level**.
For the ASH product line, the default is set to **Average Costing**.
### Screenshot: IN16 Product Line Options
The screenshot below shows the `Product Line Options` window in the `4GL Product Line` screen (`IN16`), where the **Costing Method** is set to `Average` for the `ASH` product line.
---

## Sales-Costing_Average_vs_Actual_method_based_on_Product_Line_and_Individual_Product_Level