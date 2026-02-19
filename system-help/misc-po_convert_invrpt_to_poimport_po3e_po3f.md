---
title: "Po Convert Invrpt To Poimport Po3E Po3F"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Po Convert Invrpt To Poimport Po3E Po3F - 4GL Help Documentation"
long_description: "This topic provides detailed information about Po Convert Invrpt To Poimport Po3E Po3F in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Convert Inventory Report to PO Import Template
==============================================

If you are using the Material Requirements Planning report (IN7YR) or the Inventory Sales Usage Report (IN7ZI), you can enter order quantities and prices into the resulting spreadsheet, then run a utility to convert it into another Excel file formatted for import into a purchase order.

1. Generate the report (IN7YR or IN7ZI).
2. Open the Excel spreadsheet and populate the additional columns as required (width, length, BUM, BUM quantity, PUM, PUM quantity, price, delivery date, remark type, remark desc).
3. For IN7YR: choose Purchasing » PO Entry/Maintenance » Convert MRP Rpt To Imp Temp [PO3F].  
   For IN7ZI: choose Purchasing » PO Utilities » Convert Inv Usg Rpt To PO Imp Template [PO3F].
4. Retrieve the Excel spreadsheet that you edited, then click Save.

   Another Excel spreadsheet is created to match the PO import template format, with the data you entered in the first spreadsheet. The product code corresponds to the products from the first spreadsheet.

   Any rows that did not have a value in the BUM Quantity column are excluded.
5. The new spreadsheet can now be imported into a purchase order.

---
