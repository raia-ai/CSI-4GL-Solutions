---
title: "Configuring the Customer Portal"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Configuring the Customer Portal"
long_description: "This topic provides detailed information about Configuring the Customer Portal in the 4GL system."
---


Configuring the Customer Portal
===============================

The Customer Portal is supported on Chrome, Edge, and Firefox.

Click here to view the documentation for using the portal to see the customer point of view.

Customer Setup


Set up the customer’s eCommerce options:

1. In the customer file [AR17], press F4 in the eCommercefield.
2. Indicate if you want to hide any of the following on quote confirmations and quote-to-sales order conversions:

* Hide Logs? (this hides the Inventory column entirely on the Create Quotes page of the portal)
* Hide Instock Quantity?
* Hide Incoming Quantity?
* Incoming Logs For In-Stock Calculation on quotes (Include, Exclude, or use Warehouse switch settings).

3. Select the Pricing Method for Non Stock Quantity. During create/modify/convert to order, if the available\* quantity is less than the requested quantity, if you have selected:
   * Zero Price: the price will be changed to zero (and the salesperson will be notified) but the requested quantity will not be changed
   * Adjust Quantity: the requested quantity will be changed to the available quantity and price will be issued.

   This switch setting applies to all products for all contacts for this customer. If a user has access to specific product lines only (via Contacts > Product Lines as described below), you can overwrite these default settings for that user.  
   \* Incoming quantity may be considered as available quantity for inventory calculations depending on the Incoming Logs For In-Stock Calculation switch.

Set up web logins for each customer user who requires access to the portal:

1. In the customer file, press F4 in the Contacts field.
2. Add the user as a contact if they are not already listed.
3. For each contact who should have access to the portal, complete the following:

* Language, if the contact uses a language different from the default customer language.
* Web Login user name and Web Password (the Web Login name must be unique across all customers).
* The warehouses they can access (Whse List) separated by commas (leave blank for all), and the default Whse when the user creates quotes in the portal.
* Which Web Modules they can see.
* Optionally, open the Product Lines window to identify specific product lines visible to this user in the portal; if no product line is selected, then all will be visible to the user. Here you can also overwrite the default Non-Stock Pricing Method (see #3 above) for each product line accessible to the user.

Open ECOM01 (eCommerce User Access Log – Audit) to see the login/logout history of each portal user as well as their IP address.



System Setup


Configuration is required in the following forms:

### TK12 (Class/Task Type Maintenance)

Make sure following four records are defined for eCommerce:

![](../../Resources/Images/ADMIN_portal_config_TK12.png)

### IN16 (Product Line) > [select product line] > F9

#### > Warehouse > eCommerce

* eCommerce Enabled? - If this check box is selected, the product line will be visible on the portal.
* eCommerce IUM Max Qty Allowed - Enter the maximum quantity that portal users can enter for products in this product line. If this field is left blank, users can enter any quantity in the portal.
* Open the Product Manager window to select the operator who is the product manager for this product line; this user will be notified when inventory for this product line is running low on the portal.
* Standard Packaging? - If this check box is selected, the standard packaging description (the first comments field in IN18) will be shown in the Quantity column on the Create Quote page.
* eCommerce SUM, eCommerce PUM - Optionally, disable individual SUM or PUM values so they are not visible in the portal.
* Processing Options - Optionally, define a primary and one or more secondary processes for different ranges of quantities and the product line’s first dimension. The secondary process field can include multiple processes, comma-separated. The customer will select the process when creating a quote in the portal.

#### 

* Default Blank Quote Pricing Unit, Default Blank Quote Selling Unit - If enabled, the default Pricing Unit/Selling Unit on a quote is blank and portal user must select the UOM when adding a product to the quote. (Regardless of this switch setting, user must always select the Buying Unit.)
* Do Not Include Incomings To In-Stock Calculation - If enabled, incoming logs are not included as in-stock quantity for ecommerce quote/orders. Customer maintenance setting supercedes the warehouse setting.
* Fixed Length Product Line - If the product line can only be ordered in specific fixed lengths, enter the length in inches. A portal order must adhere to multiples of this length.
* No Cut Product Line  - Enable this switch if the product line is non-cuttable. If the switch = “No” (the product line is cuttable), when a portal user selects the product line when creating/modifying a quote, they will see a message “Cut lengths not available online. Please contact your sales representative directly.” If the switch = “Yes” (the product line is non-cuttable), no message appears.
* Packaging Required Product Line - Enable this switch if packaging is required for this product line. If the switch = “Yes”, portal users will see a message when selecting the product line when creating/modifying a quote, and also in the shopping cart, reminding them to also select the packing material.

### IN1ZB (Warehouse/Product E-Comm Setup)

Use this form to maintain the Behavior and Cut Values for all products in a product line in a specific warehouse house or ALL warehouses at once.

* Select the Behavior for each product, or click Behavior to set the values for all displayed products at once:
  + **L**ogs - portal user will select inventory at the log level instead of entering values in the Pieces and Quantity fields.
  + **Q**uantity - portal user can only enter Pieces/Quantity
  + **H**ybrid - portal user can either select logs or enter Pieces/Quantity (but not both).
* If custom cuts are allowed for the product, select the Cut check box, or click Cut Product to define the setting for all displayed products at once.   
  If Cut Product is set for a product, the user must enter the Cut Product Description when creating a quote on the portal and no price will be issued for that product.

### MS39 (Document Status Maintenance)

Add the following “WEB” status to be displayed when a quote is converted to an order on the portal:

![](../../Resources/Images/ADM_portal_config_MS39.png)

Optionally, enter a specific eCom Desc for any of the other system status codes that will be customer-facing.

### OE13 (Salesperson)

For each salesperson or outside salesperson, indicate if they will receive the PDF (via email or fax) of a quote or order created from the portal; and also who is their Manager.

### OE15 (Sales Shipping Terms)

For any shipping term that should not be available when converting a quote to an order, select the D check box.

If a shipping term should be limited to certain warehouse(s) (for the portal only), press F9 to display the Whse List and enter the warehouse codes separated by commas. If this field is left blank, the shipping term will be visible on the portal for all warehouse codes. If a quote on the portal has a shipping term that isn't valid for the specified warehouse, it will be blank and the user must select a valid shipping term.

A Freight message may be shown on the Convert Quote to Order page based on the Ship Via and Shipping Term selected.



Taking the Portal Offline for Maintenance


There may be occasions when the portal must be taken offline to perform system maintenance. This will normally be done by 4GL. If you find the need to do this yourself,  for assistance with scripts that will:

* put the site into maintenance mode (on or off)
* clear all existing sessions (when turned off)
* clear all existing physical old quotes and orders (when turned off)

---
