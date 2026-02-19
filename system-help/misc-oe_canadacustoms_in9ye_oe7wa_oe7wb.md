---
title: "Oe Canadacustoms In9Ye Oe7Wa Oe7Wb"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Oe Canadacustoms In9Ye Oe7Wa Oe7Wb - 4GL Help Documentation"
long_description: "This topic provides detailed information about Oe Canadacustoms In9Ye Oe7Wa Oe7Wb in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Managing Canada Customs Paperwork
=================================

Canada Customs requires specific paperwork to accompany shipments from the United States to Canada.  allows you to record the information required to be able to generate this paperwork.

Setup
-----

The two related forms (USMCA Certificate of Origin and the Canada Customs form) can be found in the Warehouse Controls > Forms. Adjust the form print options as required.

In addition, each product that you will be shipping to Canada must have an HTSUS (Harmonized Tariff Schedule of the United States) Code. This can be assigned at the product line or product level.

The HTSUS code on the product line is used as a fallback when the code is blank on the product code, so it is not necessary to mass populate the HTSUS code on products that would have the same code as the product line.

**To record the HTSUS Code for a single product line:**

1. Go to the Product Line Maintenance (IN16) and select the product line.
2. Press F9 to display the additional fields.
3. F4 into Options and enter the HTSUS Code for that product line.

To mass update the HTSUS Code for multiple product lines or enter HTSUS Codes at the product level:

1. Choose Inventory Control » Inventory Utilities » Export/Import Product HTSUS Codes [IN9YE].
2. Export the product line data:
   1. Select Export.
   2. Select the product line or enter “ALL”.
   3. Click Save.  will generate an Excel spreadsheet containing all the products from the selected product line(s) and any HTSUS codes previously entered.
3. Open the spreadsheet and enter or modify the HTSUS codes as necessary.
4. Import the data:
   1. Go to IN9YE again.
   2. Select Import.

Generating the Paperwork
------------------------

You can generate the Canada Customs paperwork after you have invoiced the order.

* To print the USMCA Certificate of Origin, choose Sales Order Entry » Order Entry Reprints » US-Mexico-Canada COO Reprint [OE7WA].  
  If you select one invoice, you can click Print.   
  If you select “ALL” documents, you must first select the Customer, Ship-To, and Invoice Date, then click Print; the form will contain lines items for all invoices of the selected customer for the selected Invoice Date.

  The HTSUS code that prints is the product HTSUS code. If the HTSUS code is blank for the product, then it will print the HTSUS code for the product line instead.

* To print the Canada Customs form, choose Sales Order Entry » Order Entry Reprints » Canada Customs Paperwork Reprint [OE7WB].   
  If you select one invoice, you can click Print.   
  If you select “ALL” documents, you must first select the Customer, Ship-To, and Invoice Date, then click Print; the form will contain lines items for all invoices of the selected customer for the selected Invoice Date.

---
