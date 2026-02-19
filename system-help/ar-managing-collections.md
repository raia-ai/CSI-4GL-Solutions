---
title: "Managing Collections"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Managing Collections"
long_description: "Help documentation for Managing Collections in the 4GL system."
---


Managing Collections
====================

There are many different ways Credit/Collection staff can contact delinquent or past due accounts. Likely the most popular is to print an Aging Analysis, call those customers who have past due invoices, and write notes on the report for follow-up. This method has it downsides:

* a printed report displays “static data” – a data snapshot at the time the report is printed, and the report is out of date the next business day
* notes written on a report belong to the individual who has the report on their desk, so it is difficult for Credit Managers to be aware of notes for a particular account or an invoice that a customer has a concern with, especially if the Credit Manager is in a different physical location
* if there is a large volume of calls to be made, sometimes accounts can be missed as another report is printed for the Collections department to use.

provides a paperless method, providing up-to-date data to the Collections department and the ability to record notes on the transaction level:

1. List all customers with transactions past due xxx days.

Using the Customer AR Inquiry [AR61], select all customers who have transactions past due xxx days. For example, Credit Hold=**P**ast due, and Past Due=“50” (i.e. at least one transaction has monies owing for more than 50 days).

![](../Resources/Images/AR61_past_due.png)

2. Review transactions.
   1. To view all open (partial or full) documents on a customer’s account, press F4 on the Grand Total field for that customer.
   2. In the Customer Open A/R screen, enter Selection=**A**ll documents, and TOE=“ALL” (all types of entry).
   3. Before contacting the customer, review any previous notes (“+” sign is displayed in R column) entered for a transaction.
3. Contact the customer.
   1. The customer contact phone number and contact name are displayed at the top.
   2. To enter notes as a result of communication with customer, press F4 in the R field for an individual transaction. After exiting the Customer Document Remarks screen, a “+” displays in the R column.

   Optionally, include a follow-up date for the remark added; these can be reported in the AR Follow Up Report.

All individuals with access to credit information (Credit Managers/Controllers) will be able to view notes.

---
