---
title: "Using the Customer Portal"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Using the Customer Portal"
long_description: "Help documentation for Using the Customer Portal in the 4GL system."
---

Using the Customer Portal
=========================

This topic illustrates the experience of your customers using the Customer Portal. When they first log in, they will see the Welcome screen. The links at the top represent the modules; you control which modules a user is granted access to.

![](../../Resources/Images/Portal_UG_welcome.png)

Creating a Quote


1. Display the product list:
   * Scroll the Product line list, or type a few letters to see lines that match your entry:

   Click ![](../../Resources/Images/i_portal_heart_red.png) to view your list of favorites.
2. Filter the product list:
   * Optionally, enter any item specifications and click Apply Filters to reduce the size of the list.
   * Click Clear Filters to restore the full list for the selected product line.
   * To view the inventory info for a product, click ![](../../Resources/Images/i_portal_ellipsis.png). This displays all logs/bundles; if a log has an accompanying mill cert, the icon will be blue; click it to view the PDF.
3. Select the products you want:
   * Enter either the number of Lengths/Pieces or the Quantity required. Depending on the product:
     + You may be prompted to change your entry if the selected product is available in fixed lengths only.
     + If processing is available for the product, you will see a Process column and will be able to select the type of processing you require.
     + When you click in one of those fields, the Mill Info window may open for you to select specific logs instead of entering pieces or quantity.
     + To override the product behavior (i.e. entering Pieces, Quantity, or logs), click ![](../../Resources/Images/i_portal_edit.png) to create a Custom Cut. You are prompted to enter a description. Any logs that were preselected will be cleared. No price will be issued for this product.
   * Select the Buying Unit of measure. The Quantity field will convert to the Buying Unit when the quote is saved.   
     If you selected logs, the Buying Unit is disabled and returns to the default UOM.
   * Select the Pricing Unit that you want to be quoted.

   If this is a product you frequently order, click ![](../../Resources/Images/i_portal_heart_grey.png) to add it to your list of favorites.

   ![](../../Resources/Images/ADM_portal_using_quote.png)

   * Click ![](../../Resources/Images/i_portal_add.png) to add it to the shopping cart.
   * Repeat to add other products.
4. Review your shopping cart and finalize the quote:
   * The Cart icon reflects the number of products added; hover over the icon to view the items added. ![](../../Resources/Images/i_portal_cart.png)
   * Click Cart to change any items or add or remove items.

   ![](../../Resources/Images/ADM_portal_using_cart.png)

   * When you are finished, click Submit.
     + A summary is shown with the quote number. The stock level and estimated arrival of additional stock is also shown. If there is not enough in stock quantity (as ordered, including estimated arrival), the line(s) will be highlighted and you will see a message alerting you that the sales team will review the order. In this case, the price may be changed to zero pending review, and/or the requested quantity will be changed to reflect the available stock.
     + A PDF of the quote is emailed to you and the appropriate staff are notified.


Viewing or Editing Quotes / Converting a Quote to an Order


The Quotes page shows all open quotes that have not been converted to orders. Optionally, filter the list by Date, Warehouse, Quote ID, and/or Contact and click Apply Filters to help look for a specific quote. Click Clear Filter to restore the full list.

Click the name under Email Sales to send an email to the salesperson. Click the prompt under Mail to email the quote to yourself. Click the prompt under View to view a PDF of the quote.

![](../../Resources/Images/ADM_portal_using_view_quotes.png)

### Copying a Quote

To copy an existing quote, click ![](../../Resources/Images/i_portal_details.png). If the original quote is not expired all the lines will be copied and repriced (freeze lines will not be repriced). If the original quote is expired any freeze lines will be unfrozen and repriced.

### Modifying a Quote

To change or remove items or add new items, click ![](../../Resources/Images/i_portal_edit.png).

You cannot modify a quote that has expired.

![](../../Resources/Images/ADM_portal_using_mod_quote.png)

Make any changes, additions or deletions. You can delete but not modify a line that has been frozen by the salesperson (indicated by “greyed out” values).

To view the inventory info for a product, click ![](../../Resources/Images/i_portal_ellipsis.png). If this icon is green, one or more logs have been selected for the product; in this case if you click in the Lengths/Pieces or Quantity field, you will be prompted to select from the available logs.

Click Save Modifications. An updated quote is emailed to you and the appropriate staff are notified. Click Return to return to the quotes list.

### Converting a Quote to an Order

Click ![](../../Resources/Images/i_portal_convert.png).

You cannot convert a quote that has expired.

In the header area, enter the Request Date and Customer PO number, and change any of the shipping details and instructions if necessary. The Ship Address field allows you to select from any of your predefined shipping addresses, or the warehouse address for pickup, or select “Manual Address” and enter a new address. The Ship Via may change according to the selected shipping address, but can be overridden.

![](../../Resources/Images/ADM_portal_using_convert1.png)

Note that the pricing reflects prices in effect at today’s date; any changes from prices on the original quote are indicated as either higher or lower than the quoted price. Prices may not be shown if there is insufficient inventory. The table also shows the stock level and estimated arrival of additional stock. If there is not enough in stock quantity (as ordered, including estimated arrival), the line(s) will be highlighted and you will see a message alerting you that the sales team will review the order. In this case, the price may be changed to zero pending review, and/or the requested quantity will be changed to reflect the available stock.

![](../../Resources/Images/ADM_portal_using_convert2.png)

To change the quantity ordered, click Modify Quote. Make your changes, click Save Modifications and then click Return to return to the order.

When you are ready to submit the order, click Create Order. A PDF of the order is emailed to you and the appropriate staff are notified. The quote is removed from the Quotes page and the new order is included on the Orders page. Click the order number to open the order PDF in a separate tab or click Quotes to return to the Quotes page.



Viewing Sales Orders


The Orders page allows you to monitor the status of all your orders.

Optionally, filter the list by Date, Warehouse, Order #, PO #, and/or Status and click Apply Filters to help look for a specific order. Click Clear Filters to restore the full list.

![](../../Resources/Images/ADM_portal_using_view_orders.png)



Viewing Proof of Deliveries


The Proof of Delivery page shows all invoices, with links to associated proof of delivery documents if they exist.

Optionally, filter the list by Date, Warehouse, Order #, PO #, Contact, and/or Status and click Apply Filters to help look for a specific invoice. Click Clear Filters to restore the full list.

The Mail and View icons are only enabled if there is a proof of delivery document associated with the invoice.

![](../../Resources/Images/ADM_portal_using_view_PoD.png)



Viewing Invoices


The Invoices page shows all invoices issued against your sales orders.

Optionally, filter the list by Date, Warehouse, Invoice ID, Order #, PO #, and/or Status and click Apply Filters to help look for a specific invoice. Click Clear Filters to restore the full list.

![](../../Resources/Images/ADM_portal_using_view_invoices.png)



Viewing Mill Certificates


The Mill Certs page shows all invoices, with links to associated packing slip and mill certificate documents, if they exist.

Optionally, filter the list by Date, Warehouse, Invoice ID, Order #, PO #, and/or Status and click Apply Filters to help look for a specific invoice. Click Clear Filters to restore the full list.

The Mail and View icons are only enabled if there is a packing slip and/or mill certificate document associated with the invoice.

![](../../Resources/Images/ADM_portal_using_view_mill_certs.png)

You can also view the mill info for a product on the Create Quotes page: click ![](../../Resources/Images/i_portal_ellipsis.png) beside a product to see all logs; if a log has an accompanying mill cert, the icon will be blue; click it to view the PDF.

---