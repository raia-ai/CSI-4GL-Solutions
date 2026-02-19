---
title: "Madcap_-_SM3_Help-Content-ExternalFiles-SM3_eCommerce_Portal_User_Guide"
source: "Madcap_-_SM3_Help-Content-ExternalFiles-SM3_eCommerce_Portal_User_Guide.pdf"
tags: ["4GL", "eCommerce", "User Guide", "Steel Manager", "4GL Solutions", "Quote", "Order", "Portal", "Metal Industry"]
version: 1.0
last_updated: 2025-12-04
short_description: "A user guide for the 4GL eCommerce Portal, providing instructions for creating quotes, managing orders, viewing invoices, and accessing mill certificates. This guide is intended for customers of 4GL Solutions using the Steel Manager III platform."
long_description: "This document is the comprehensive 4GL eCommerce Portal User Guide, created by 4GL Solutions for users of their Steel Manager III (SM3) software. It details the step-by-step processes for interacting with the eCommerce portal, designed specifically for the metal industry. The guide covers essential functions such as creating a new quote by selecting products, filtering inventory, and specifying quantities. It also explains how to view, edit, copy, and convert existing quotes into sales orders. The document further provides instructions on monitoring sales orders, viewing proofs of delivery, accessing invoices, and retrieving mill certificates. Illustrated with screenshots and clear instructions, this guide serves as a primary reference for customers to efficiently manage their procurement and documentation needs through the 4GL online platform."
---
# 4GL eCommerce Portal User Guide
**4GL STEEL MANAGER III | 4GL Solutions TECHNOLOGY FOR THE METAL INDUSTRY**
> THOUGHTFULLY, PURPOSELY, DESIGNED FOR STEEL.
---
## About this Guide
This document contains instructions for using the 4GL eCommerce Portal.
A PDF of each module's instructions is embedded in the portal and is available for distribution to our customers.
---
## Contents
*   [Creating a Quote](#creating-a-quote)........................................................................ 1
*   [Viewing or Editing Quotes / Converting a Quote to an Order](#viewing-or-editing-quotes--converting-a-quote-to-an-order)............ 4
*   [Viewing Sales Orders](#viewing-sales-orders)................................................................... 7
*   [Viewing Proof of Deliveries](#viewing-proof-of-deliveries)......................................................... 8
*   [Viewing Invoices](#viewing-invoices).......................................................................... 9
*   [Viewing Mill Certificates](#viewing-mill-certificates).......................................................... 10
---
## Creating a Quote
This section describes how to create a new quote using the portal. The main navigation includes tabs for **Create Quote**, **Quotes**, **Orders**, **Proof of Delivery**, **Invoices**, and **Mill Certs**.
### 1. Display the product list
*   Scroll the Product line list, or type a few letters to see lines that match your entry.
*Image of Step 1: Location and Product Line selection. Shows a dropdown for location (Acme Newmarket Industries) and a search box for product line (roul), with results like "ARB - ALUMINUM ROUND BAR" and "SRB - STAINLESS ROUND BAR".*
*   Click the heart icon (♡) to view your list of favorites.
### 2. Filter the product list
*   Optionally, enter any item specifications and click **Apply Filters** to reduce the size of the list. Click **Clear Filters** to restore the full list for the selected product line.
*Image of Step 2: Item Specifications filter. Shows fields for Spec Types (6061-T6) and Dimensions (7" B221).*
*   To view the inventory info for a product, click the inventory icon. This displays all logs/bundles. If a log has an accompanying mill cert, the MTR icon will be blue; click it to view the PDF.
*Image of inventory details for "ARB 7" x 15' B221 6061-T6". The table shows columns for Warehouse, LOG #, Est. Arrival, Length, Est. Pieces, Quantity (LB), Heat #, Mill, Origin, and MTR. The MTR column has a blue document icon, indicating an available mill certificate.*
### 3. Select the products you want"
*   Enter either the number of **Lengths/Pieces** or the **Quantity** required. Depending on the product: *   You may be prompted to change your entry if the selected product is available in fixed lengths only.
*   If processing is available for the product, you will see a **Process** column and will be able to select the type of processing you require.
*   When you click in one of those fields, the Mill Info window may open for you to select specific logs instead of entering pieces or quantity.
*   To override the product behavior (i.e. entering Pieces, Quantity, or logs), click the **Custom Cut** icon to create a custom cut. You are prompted to enter a description. Any logs that were preselected will be cleared. No price will be issued for this product.
*   Select the **Buying Unit** of measure. The Quantity field will convert to the Buying Unit when the quote is saved. If you selected logs, the Buying Unit is disabled and returns to the default UOM.
*   Select the **Pricing Unit** that you want to be quoted.
> If this is a product you frequently order, click the heart icon (♡) to add it to your list of favorites.
*Image of the product selection table for Aluminum Round Bar. It includes columns for Product, Theo Wgt, Inventory, Custom Cut, Lengths/Pieces, Quantity, Buying Unit, Pricing Unit, Add to cart, and Favourite.*
*   Click the shopping cart icon to add it to the shopping cart.
*   Repeat to add other products.
### 4. Review your shopping cart and finalize the quote
*   The **Cart** icon reflects the number of products added.
*Image of a cart icon with a badge showing "(1)".*
*   Hover over the icon to view the items added.
*Image of a cart summary pop-up showing a list of products with Description, Pcs, Qty, and UOM.*
*   Click **Cart** to change any items or add or remove items.
*Image of the Shopping Cart page. It displays a detailed table of items with options to modify Lengths/Pieces, Quantity, Buying Unit, and Pricing Unit, or delete items. Buttons for "+ Add Item", "Delete All", and "Submit" are visible.*
*   When you are finished, click **Submit**.
*   A summary is shown with the quote number. The stock level and estimated arrival of additional stock is also shown. If there is not enough in stock quantity (as ordered, including estimated arrival), the line(s) will be highlighted and you will see a message alerting you that the sales team will review the order. In this case, the price may be changed to zero pending review, and/or the requested quantity will be changed to reflect the available stock.
*   A PDF of the quote is emailed to you and the appropriate staff are notified.
---
## Viewing or Editing Quotes / Converting a Quote to an Order
The **Quotes** page shows all open quotes that have not been converted to orders.
Optionally, filter the list by **Date**, **Warehouse**, **Quote ID**, and/or **Contact** and click **Apply Filters** to help look for a specific quote. Click **Clear Filters** to restore the full list.
*Image of the Quotes page with filters and a list of quotes. The list has columns for Quote ID, Date, Expiry Date, Warehouse, Contacts, etc. Callouts explain the icons: *
- **Contacts Column: ** Click the name to send an email to the salesperson.
- **Mail Icon: ** Email the document to yourself.
- **View Icon (Magnifying Glass): ** View a PDF of the document.
- **Details Icon (List): ** View the status of an order (any lines waiting to be priced by the salesperson, the estimated arrival date of incoming material).
---
## Viewing Proof of Deliveries
The **Proof of Delivery** page shows all invoices, with links to associated proof of delivery documents if they exist.
Optionally, filter the list by **Date**, **Warehouse**, **Invoice ID**, **Order #**, **PO #**, and/or **Status** and click **Apply Filters** to help look for a specific invoice. Click **Clear Filters** to restore the full list.
The **Mail** and **View** icons are only enabled if there is a proof of delivery document associated with the invoice.
- **Modify Icon (Pencil): ** Add/change/remove items.
- **Order Icon (Arrow): ** Convert to an order.
### Copying a Quote
To copy an existing quote, click the **Copy** icon. If the original quote is not expired, all the lines will be copied and repriced (freeze lines will not be repriced). If the original quote is expired, any freeze lines will be unfrozen and repriced.
### Modifying a quote
To change or remove items or add new items, click the **Modify** icon. You cannot modify a quote that has expired.
Make any changes, additions, or deletions. You can delete but not modify a line that has been frozen by the salesperson (indicated by "greyed out" values).
To view the inventory info for a product, click the inventory icon. If this icon is green, one or more logs have been selected for the product; in this case, if you click in the **Lengths/Pieces** or **Quantity** field, you will be prompted to select from the available logs.
Click **Save Modifications**. An updated quote is emailed to you and the appropriate staff are notified. Click **Return** to return to the Quotes list.
*Image of the "Modify Quote ID: Q004554" page. It shows a table of products similar to the shopping cart, allowing for edits. The "Save Modifications" and "Return" buttons are at the top.*
### Converting a quote to an order
Click the **Convert to Order** icon. You cannot convert a quote that has expired.
In the header area, enter the **Request Date** and **Customer PO** number, and change any of the shipping details and instructions if necessary. The **Ship Address** field allows you to select from any of your predefined shipping addresses, or the warehouse address for pickup, or select “Manual Address" and enter a new address. The **Ship Via** may change according to the selected shipping address, but can be overridden.
*Image of the "Convert Quote: Q003886 To Order" page. It shows fields for Request Date, Customer PO, Ship Via, Ship Term, Ship Address, and Special/Shipping Instructions.*
Note that the pricing reflects prices in effect at today's date; any changes from prices on the original quote are indicated as either higher or lower than the quoted price. Prices may not be shown if there is insufficient inventory. The table also shows the stock level and estimated arrival of additional stock. If there is not enough in stock quantity (as ordered, including estimated arrival), or if any line has no price, the line(s) will be highlighted and you will see a message alerting you that the sales team will review the order. In this case, the price may be changed to zero pending review, and/or the requested quantity will be changed to reflect the available stock.
*Image of a quote conversion details pop-up (Q003593). It shows ordered quantity, in-stock quantity, and estimated arrival dates for back-ordered items. A message at the bottom reads: One or more lines exceed available inventory. Your order will be submitted to the sales team for review."*
To change the quantity ordered, click **Modify Quote**. Make your changes, click **Save Modifications** and then click **Return** to return to the order.
When you are ready to submit the order, click **Create Order**. A PDF of the order is emailed to you and the appropriate staff are notified. The quote is removed from the Quotes page and the new order is included on the Orders page. Click the order number to open the order PDF in a separate tab or click **Quotes** to return to the Quotes page.
> Order W006848 has been created and a confirmation email has been sent.
> Click here to return to Quotes
---
## Viewing Sales Orders
The **Orders** page allows you to monitor the status of all your orders.
Optionally, filter the list by **Date**, **Warehouse**, **Order #**, **PO #**, **Contact**, and/or **Status** and click **Apply Filters** to help look for a specific order. Click **Clear Filters** to restore the full list.
*Image of the Sales Orders page with filters and a list of orders. Callouts explain the icons: *
*Image of the Proof of Delivery page with filters and a list of invoices. Callouts explain the icons: *
- **Email Sales Column: ** Click the name to send an email to the salesperson.
*Image of the Invoices page with filters and a list of invoices. Callouts explain the icons: *
*Image of the Mill Certs page with filters and a list of invoices. Callouts explain the icons: *
> You can also view the mill info for a product on the **Create Quotes** page: click the inventory icon beside a product to see all logs; if a log has an accompanying mill cert, the MTR icon will be blue; click it to view the PDF.
>
> *Image of the inventory details screen, highlighting the blue MTR (mill certificate) icon in the table.*
---

# Madcap_-_SM3_Help-Content-ExternalFiles-SM3_eCommerce_Portal_User_Guide
