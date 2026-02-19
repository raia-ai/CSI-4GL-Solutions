---
title: "Excluding Sales From Usage"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Excluding Sales From Usage"
long_description: "This topic provides detailed information about Excluding Sales From Usage in the 4GL system."
---


Excluding Sales From Usage
==========================

The Usage Table Maintenance function is used to maintain the usage information, for a warehouse for individual products. Usage information defaults to sales and all transfer out data. Use this screen to remove abnormalities in usage history; for example, you may want to exclude one-off large sales from your usage tables so that your inventory re-order reports are not skewed by these anomalies.

A salesperson can quickly mark a line item in an order to be excluded from usage: when adding a line item, select the Ex Usg checkbox. This sets the flag against the invoice and excludes the order from the usage table.

1. Choose Purchasing » Inventory Re-Order » Usage Table Maintenance [PO52].
2. Select a Product Line to populate the table.
3. In the row for the appropriate product, double-click in the M or W cell to open the Usage Maintenance for that product.

![](../Resources/Images/Diversified FG/PO_usage_table_exclude_sales1.png)

4. The usage will be shown as Sales (from invoices to the customer) or Production. Double-click in the appropriate field to view the usage details.

![](../Resources/Images/Diversified FG/PO_usage_table_exclude_sales2.png)

5. In the Usage Details, enter “Y” in the Excl Usage field.

![](../Resources/Images/Diversified%20FG/PO_usage_table_exclude_sales3.png)

The total usage for that period is reduced by the amount on that particular document.

---
