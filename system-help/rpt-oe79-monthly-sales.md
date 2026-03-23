---
title: OE79 - Sales by Customer by Month
source: madcap.md
version: '1.0'
last_updated: '2026-02-19'
short_description: OE79 - Sales by Customer by Month
long_description: Help documentation for OE79 - Sales by Customer by Month in the 4GL system.
---

# OE79 - Sales by Customer by Month

This function generates a report containing monthly invoiced sales and gross margin percent by customer, reporting on a rolling 12-month period.

1. Choose Sales Order Entry » Order Entry Reports » Sales by Customer by Month \[OE79].
2. Enter or select End Date Of Month (by default, last day of current month is selected).
3. Enter or select Customer Start Date (customers with a start date after this date will be included).
4. Enter or select a State/Province code (by default, all are selected).
5. Indicate how you want to create the report by: Salesperson, Outside salesperson, or Order Writer.
6. Enter or select an Operator code (by default, all are selected).
7. Indicate if you want to use the Customer Salesperson or leave blank to use the salesperson on the invoices.
8. Indicate if you want the report to be Group by Operator.
9. Indicate how you want to Sort the data: by Customer name, Descending Sales, or Postal/zip code.
10. Indicate if you want to include customers with Zero Sales in the past year.
11. Indicate if you want to Show Details of the customers (postal code, phone #, contact, etc.).
12. Indicate if you want to Include Inactive customers.
13. Indicate if you want to include orders based on Avg Cost, or leave blank to include profit orders based on actual cost.

## Output

|                |                                                                        |                      |                             |
| -------------- | ---------------------------------------------------------------------- | -------------------- | --------------------------- |
| column heading | needs description? (if yes, populate one of the next two columns only) | glossary description | report-specific description |
| Customer       |                                                                        |                      |                             |
| Prev           |                                                                        |                      |                             |
| This           |                                                                        |                      |                             |
| Total          |                                                                        |                      |                             |

***
