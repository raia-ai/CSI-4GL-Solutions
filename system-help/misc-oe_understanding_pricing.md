---
title: "Oe Understanding Pricing"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Oe Understanding Pricing - 4GL Help Documentation"
long_description: "This topic provides detailed information about Oe Understanding Pricing in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Understanding Sales Pricing
===========================

An order can include two different prices: pricing associated with the product, and pricing associated with the machine/process used.

Product Pricing
---------------

There are five options for product pricing. You can:

1. Set up default product pricing for individual products.
2. Set up default product pricing for individual products by customer.
3. Set up tiered default product pricing - products and customers are assigned to a tier.
4. Set up a price book of more complex default product pricing for specific grades/specifications of a product line that takes into account various factors that will be applied against a base price.
5. Have no pricing suggested for a product (price will default to zero and must be entered manually by the salesperson in the quote/sales order).

Each warehouse will be set up to use one of options 2-5:   
 > Default Sales Price in Order Entry = **C**ustomer Pricing (2), **P**redefined (3), Price **B**ook (4), or **Z**ero (5)

### Option 1 – Individual Product Pricing

Individual product pricing assigns a specific price to individual products, that applies to all customers. The price is entered using the costing unit of measure assigned to the product line, but will convert into the quote or sales order pricing unit of measure. No quantity breaks are defined.

Setting Up Individual Product Pricing

### Option 2 - Customer Pricing by Product

Products are priced individually by customer, with an effective date range for each price.

When you add a line to a quote/order, you can press F4 in the Price field to view the pricing details for the line. The stock price will reflect the customer pricing for this product if both PUMs are the same. If the PUMs are different between the inventory line and the customer pricing, the price shown will be the converted price based on the inventory line PUM. For example, if the customer price is $12 per foot and the PUM on the line is inches, then the resulting price will be $1 per inch.

If a product in an order does not have a current price for the customer, the price will be zero, allowing the salesperson to enter the price.

Setting Up Customer Pricing by Product

### Option 3 – Tier Pricing

Tier pricing is a system-wide pricing option in which pricing categories are created that include up to nine tiers of pricing. Each tier applies a factor (adder, divider, multiplier) to the base cost of the material. No quantity breaks are defined.

Products are then assigned to a pricing category; individual products can have a supplementary adder which will be calculated against the category base price and then the factors will be applied. While the categories are system-wide, the assignments are managed at the warehouse level. Any products not assigned to a category will be priced with a default tier factor.

All customers must be assigned to a specific tier. The tier a customer is assigned to is the same for every product (that has been assigned a category) in every product line.

In a quote/order, if the customer is assigned to a tier and the ordered product is assigned to a category, the appropriate tier price for that category will default in the quote/sales order (but can be overriden by the salesperson). The nine pricing levels will display in the pricing window with the applicable level in red text. A switch (Use Stock Cost Only For Pricing) controls if the full cost price (including machine) is used, or only the stock cost price is used.

Setting Up Tier Pricing

### Option 4 – Price Book

Price Book is ’s most comprehensive pricing option.

To establish a base price, a range of products can be captured using specifications and dimensions by product line. These specs and dimensions are entered into a table and base prices are entered against each range. If all customers are using the same factors, a multiplier, divider or adder can be entered against quantity limits to establish the default price against an item in quote or sales order entry.

Products can be grouped within or among product lines to establish pricing based on combined quantities. These can also be segregated by specifications.

Customers can be assigned to pricing ranks, and each rank can have different pricing by product line and by quantity break. The rank is a one-character alphanumeric code, so up to 35 ranks can be defined (A-Z, 1-9).

Customer pricing may be set up for a particular product and customer that will override the price book pricing.

Setting Up Price Book Pricing

Machine Pricing
---------------

In addition to the product sales price, you can charge based on the machine process used to create the product, for example you can set up pricing either based on product length and/or thickness, or based on the machine time required.

Maintaining a List of Machines

Example: Viewing the Pricing on a Sales Order
---------------------------------------------

In the following example, the Waterjet machine is defined in the Machine Master. For SPL products up to 999 inches long and 4 inches thick, the pricing includes an entry of $0.63 per piece for 2-4 pieces: [add background text related to product pricing for this example]

![](../Resources/Images/machine_price_ex1.png)

In the sales order, we’ve added a product from the SPL product line to an order line and chosen the Waterjet as the Primary Process. The size of the product is within the parameters above:

![](../Resources/Images/machine_price_ex2.png)

Click … in the Sales Price field to see the price calculations. The machine cost is shown in an “M” line. Because the quantity ordered was 2, it used the second price point set in the machine pricing, $0.63 per piece.

![](../Resources/Images/machine_price_ex3.png)

Press F9 to display the calculations:

![](../Resources/Images/machine_price_ex4.png)

---
