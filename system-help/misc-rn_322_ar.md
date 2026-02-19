---
title: "Rn 3.22 Ar"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Rn 3.22 Ar - 4GL Help Documentation"
long_description: "This topic provides detailed information about Rn 3.22 Ar in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Accounts Receivable
===================

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 39329 | Option to print delivery note added to AR17 | The Document Delivery options in the Customer Maintenance file now include an option to print the delivery note.  The packing list/delivery note will print when the Customer Copy (“C”) checkbox is not selected in the IN19 print options; if the Customer Copy checkbox is selected in the IN19 print options, then the delivery note will only print if the checkbox in AR17 is also selected. | AR17, IN19>Forms>Packing List print options |  |
| 39605 | Email subject and body added to AR7V | Email fields (Subject and Message) have been added to the Fax/Email Statement to Contacts function. These default from MS33 the first time the function is run but then use the last value for each subsequent run. | AR7V |  |
| 39624 | Document delivery options for pre-invoice added to AR17 | New Document Delivery > Delivery Note options in the Customer Maintenance file allow you to set up fax and/or email for pre-invoices for a customer ship-to. | AR17 |  |
| 39834 | Customer UDF fields increased to 100 | The User Defined Fields Maintenance now allows up to 100 characters for UDF values. | AR1N |  |
| 39944 | Group added to AR9LA | A Group column has been added to the “Export Customer Contacts To Excel” output. | AR9LA |  |
| 40067 | AR7D fixes made for consistency | Customer Details are excluded from Excel output whether the checkbox is selected or not; for PDF output, the customer details are printed below each customer. | AR7D |  |
| 40312 | Switch to disallow customer maintenance without invoice option | A new switch, “Allow No Invoice Print/Email Option on Customer”, if not enabled, forces a user to set the invoice checkbox on the Document Delivery window, either at the top or for any of the contacts. | MS33 > Accounts Receivable > Additional Options  AR17, AR1I, AR1J |  |
| 40478 | AR7D allows for summary of Customer Details | The Customer Details field on the Detailed AR Aging Report is now a dropdown that allows: - “S” - summary - only prints YTD Sales, Last Payment, and Last Payment Amount below each customer line. - “D” - prints all customer details  - blank - does not print any customer details | AR7D |  |

---
