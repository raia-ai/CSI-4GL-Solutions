---
title: "Accounts Receivable"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Accounts Receivable"
long_description: "Help documentation for Accounts Receivable in the 4GL system."
---


Accounts Receivable
===================

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 32615 | New function to send statements to customer contacts | A new report function sends statements to contacts at one or all customers. The statement contains the same details as AR7E (assuming default selections). To facilitate this, the Document Delivery form in Customer Maintenance now includes statement options for each contact. | AR17, AR7V |  |
| 38364 | Additional fields added to AR7R Excel output | Additional columns (business number, start date, last sale date) have been added to the Detailed AR Aging report Excel output, and the Country column has been removed. | AR7R |  |
| 38894 | Define valid values for customer UDF fields | The User Defined Fields Maintenance now allows for specific values to be assigned to a UDF. If populated, then in AR17>UDFs you will only be able to select from those valid values. | AR1N |  |
| 39020 | Edit PO number in AR33 | In the Document Application form, you can now press F9 to display and change the PO number on the Customer Statement. | AR33 |  |
| 39144 | Statement fields added to AR7J | The new statement fields added in AR17>Document Delivery (see 32615 above) have been added to the Customer Doc Delivery (Excel) report. | AR7J |  |
| 39577 | Customer remark functionality differs depending if operator has remarks categories defined in MS32 | **If the user has Remarks Categories defined** for their operator, they can: - view remarks that have a customer type category or have a blank category - add remarks with a customer type category that is in their MS32 list (cannot leave blank) **If the user does not have Remarks Categories defined** for their operator, they can: - view all remarks for a customer - add remarks with a customer type category or leave category blank | MS32 Customer>Remarks (View) Customer>Remarks(Input) |  |

---
