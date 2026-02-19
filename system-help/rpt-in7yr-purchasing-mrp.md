---
title: "IN7YR - Purchasing MRP"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "IN7YR - Purchasing MRP"
long_description: "Help documentation for IN7YR - Purchasing MRP in the 4GL system."
---

IN7YR - Purchasing MRP
======================

The Purchasing MRP (Material Requirements Planning) report identifies inventory on hand and what materials are needed for orders in the pipeline.

You can enter order quantities and prices into the resulting spreadsheet, then run PO3E to convert it into another Excel file formatted for import into a purchase order.

1. Choose Purchasing » PO Reports » Purchasing Custom Reports » Purchasing MRP [IN7YR].
3. Enter or select a Product Line.   
   If you leave it as “All”, enter a Keyword to filter on the product description.   
   If you select a specific product line, you can further filter on individual specs (e.g. Grade, STD, Gauge, Length/Width, etc.)

Complete any of the remaining fields to get the type of information you require:

1. Indicate if you want to only show products with On Order quantity.
2. Select a Supplier to show commit in quantity from PO or production orders for the selected vendor.
3. Select a Customer to show on hand quantity from logs that are assigned to the customer; the average sold quantity from sales for the customer, and the commit in quantity reserved on sales orders for the customer.
4. Enter the minimum and/or maximum months on hand (MOH) or months in pipeline (MIP):  
   MOH = On Hand Quantity / Average Usage over the period specified in the second month usage field.  
   MIP = (Available Quantity + Transfer Quantity) / Average Usage over the period specified in the second month usage field.
5. Select the Branches (additional warehouses) to be included. The report will display the on hand quantity, the available quantity, and the commit in quantity of all the selected warehouses.
6. The Stock/Nonstock field looks at the Buyouts only flag on a product (IN18>Warehouse): **S**tock=no B flag, **N**onstock=B flag. Select **B**oth if you don't want to filter on this flag.
7. In the No Sale Since field, enter the date to only see products where the last sale was prior to this date.
8. Enter the minimum and/or maximum Age.
9. Enter three numbers to determine Month Usage buckets (e.g. 3, 6, 12). The report will display the average sold quantity based on the selected number of months.
10. Enter the Minimum Length or Minimum Area. These apply to on hand inventory.

The resulting spreadsheet includes the following columns:

| Column | Description |
| --- | --- |
| Warehouse | Warehouse |
| Product Code | Product code |
| Item No | Product line and pseudo code |
| Description | Product description |
| Unit | IUM |
| Pc Wt | Theoretical weight |
| OH Inv | On hand quantity for selected warehouse |
| OH ATP | Available quantity for selected warehouse |
| Age | Weighted age of all logs in the warehouse L = Log weight  H = That items total weight in inventory  D = How many days old that log is (today's date - log received date)  A = weighted age of that lot of steel  The formula for each individual lot of steel would be (L / H) \* D = A  Then you take the “A” of all the lots of material and add them together.  A1 + A2 + A3 +A4… = Weighted average age |
| 3M Avg | 3 month average usage for selected warehouse IV/CM/DM quantities in 3 month period divided by 3 |
| 6M Avg | Same as above but for 6 months |
| 12M Avg | Same as above but for 12 months |
| On Order | Committed in quantity for the selected warehouse |
| Next Qty | Quantity on the earliest incoming PO line |
| Next Due | Delivery date on the earliest incoming PO line |
| Transfer | BT transfer in quantity - BT transfer out quantity |
| MOH | OH Inv / 6M Avg |
| MIP | (OH ATP + Transfer) / 6M Avg |
| Branch Inv | On hand quantity for all warehouses except for the selected warehouse |
| Branch ATP | Available quantity for all warehouses except for the selected warehouse |
| Branch OO | Committed in quantity for all warehouses except for the selected warehouse |
| Br Cust | Number of customers from sales in 6 month period for the selected warehouse |
| Top % Br | Percentage of sales for top customer in 6 month period for the selected warehouse |
| Br Top Cust | Top customer name in 6 month period for the selected warehouse |
| All Cust | Number of customers from sales in 6 month period for all warehouses |
| Top % All | Percentage of sales for top customer in 6 month period for all warehouses |
| All Top Cust | Top customer name in 6 month period for all warehouses |
| Branch SLs | Number of order lines invoiced in 6 month period for selected warehouse |
| Br Avg Sell Qty | Average selling quantity on order lines invoiced in 6 month period for selected warehouse |
| Avg Cost Br | Average cost for selected warehouse |
| Avg SP Br | Sum of sales value / sum of sold quantity for order lines invoiced in 6 month period for selected warehouse |
| All SLs | Number of order lines invoiced in 6 month period for all warehouses |
| All Avg Sell Qty | Average selling quantity on order lines invoiced in 6 month period for all warehouses |
| Avg Cost All | Average of Average cost in all warehouses |
| Avg SP All | Sum of sales value / sum of sold quantity for order lines invoiced in 6 month period for all warehouses |

---