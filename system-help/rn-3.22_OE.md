---
title: "Order Entry"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Order Entry"
long_description: "Help documentation for Order Entry in the 4GL system."
---

Order Entry
===========

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 39653 | Use order writer as sender when emailing delivery note/packing list | New switch controls who a packing list email is sent from: if the switch is enabled, the email is sent from the order writer. If not enabled, the email is sent from the salesperson. | > Email Packing Lists With Writer As Sender |  |
| 39660 | Summary version of MN71 | Two new checkboxes (Summary and Freight) have been added to the Manifest Loading Summary to create summary output that prints one row for each document as well as the freight cost of the selected cost code and the margin and margin% of the invoice. | MN71 |  |
| 39676 | Inquiry button added to manifest Assign tab | A magnifying glass icon at the bottom left of the Unassigned and assigned Run Items sections on the Assign tab allows you to open the inquiry window for the selected item (there is no inquiry for miscellaneous documents). | MN31 |  |
| 39681 | Territory added to OE74 and OE7YL Excel output | A Territory column has been added at the end of the Excel output for the Invoice Summary by Document and Sales by Salesperson by Customer reports. | OE74, OE7YL |  |
| 39706 | Include MTRs option added to OE7B | The Sales Order reprint now includes an option to Include MTRs. | OE7B |  |
| 39770 | Name change on underlying table | If you write your own custom reports, you should know that column OECST\_RAW\_IUM\_UNT\_QTY on table OEC\_CST was renamed to OECST\_UNT\_QTY\_USE |  |  |
| 39766 | OE62 POD button checks both stock and sales warehouses | When searching for an Invoice POD (via the POD button on the Billing/Shipping tab of the Stock Inquiry by Warehouse),  first searches the stock warehouse, then the sales warehouse. | IN62 |  |
| 39785 | Automatic surcharge calculations | The cost line definitions in the Warehouse Order Defaults now allow for a C line to be defined with a percentage of the total order up to a maximum value, instead of defining a specific value, to be applied to all orders. | IN19 > Order Defaults > Maintain Cost Lines |  |
| 39806 | Changes to Customs paperwork | The USMCA Certificate of Origin and the Canada Customs forms can now consolidate multiple invoices for the same customer shipping to the same address. | OE7WA, OE7WB |  |
| 39868 | OE7XH can now be output to Excel | The Quote Summary by Salesperson can now be output to an Excel spreadsheet. | OE7XH |  |
| 39881 39882 | Print Euro or Sterling symbol on invoice | A Symbol column has been added to the Currency Rates table to specify the symbol to be used on invoices: GBP, EUR, or blank (which will use $). This requires that the Invoice form option is set to Display Dollar Sign. | MS34 IN19 > Forms > Invoice > form options |  |
| 39897 | Price per weight added to OE61 | The Details and Summary tabs on the Sales Order Inquiry now show the price per weight (per LB) for each line. This is the sales value divided by the weight, irrespective of the PUM of the order line. | OE61 |  |
| 39988 | Change required date on OE72C | The Blanket Order Pick Slip Release displays the Required Date from the order header as well as each order line. You can change the date for order lines individually, or change the header date (and optionally apply the new date to all order lines). | OE72C |  |
| 40029 | Barcode added to MTRs | System and Overlayed MTRs now include a barcode at the top for the warehouse code, document number, and document index. |  | MTR Delivery Options |
| 40061 | Changes to OE7YK | The Customers With No Sales report now allows sales orders to be included in the report, and can be output to Excel. | OE7YK |  |
| 40264 | Add Govt Approved form options | A new form option has been added to the pick slip, quote, and sales order to define “Gov Approved Only Text”, to print when the material origin on the quote/order is set to “G”. | IN19 > Forms > 05, 07, 08 |  |
| 40271 | Stocking warehouse added to OE42 | The Shipping Confirmation page now includes a “Stk” column that displays the stocking warehouse for the invoice/sales order. | OE42 |  |

---