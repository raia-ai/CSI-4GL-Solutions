---
title: "Ap Accrual Accounting About"
source: "madcap.md"
tags: ["4GL", "AP", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Ap Accrual Accounting About - 4GL Help Documentation"
long_description: "This topic provides detailed information about Ap Accrual Accounting About in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the AP module."
---
About Accrual Accounting
========================

Accrual accounting is an accounting method that measures the performance and position of a company by recognizing economic events regardless of when cash transactions occur. The general idea is that economic events are recognized by matching revenues to expenses (the matching principle) at the time in which the transaction occurs rather than when payment is made (or received). This method allows the current cash inflows/outflows to be combined with future expected cash inflows/outflows to give a more accurate picture of a company's current financial condition.

Accrual accounting is considered to be the standard accounting practice for most companies, with the exception of very small operations. Accrual accounting provides a more accurate picture of the company's current condition – it is the opposite of cash accounting, which recognizes transactions only when there is an exchange of cash.

provides an option to automatically accrue all inventory items, received at time of receipt (when processed), where a vendor invoice has not been processed and monies paid to the vendor. Accruals are based on estimated costs from the purchase order for all costs included in the purchase shipping term for the vendor.

At time of processing (entering) vendor invoices, actual costs from the invoice can be compared with estimated costs from the purchase order. An acceptable variance % (positive or negative) can be entered as a system parameter, which will hold invoices with variances that fall outside of the acceptable range which can be reviewed by a manager before processing the invoice for payment.

Variance reports can be produced by buyer code for a specified period, accrual aging and write-off of accrual variances.

When all vouchers have been received for a transaction, the variance for each receipt must equal zero, otherwise you must write-off variance ($ are in accrual account) to a GL account.

Automatic Distribution of Variances
-----------------------------------

When entering an A/P voucher for accruals (inventory items), you can have  automatically1 post the variance back to Inventory (if the logs are still in stock) or Cost of Sales (if the logs are sold). It does this by creating and posting an inventory adjustment. Margins on your invoices will reflect the actual cost of sales.

Example:

* We received 1900 feet at a price of 2.9875 (2.39 USD).
* 1,000 feet has been sold.
* Let's assume we have an invoice for $2.50/ft - when we pay the invoice, we enter the actual price on the invoice.  calculates a variance of $209.00 US.
* The AP voucher must be in balance, so we need to charge the variance account.
* When the AP voucher is posted,  will create a price adjustment for the stock remaining in inventory.
* If we look at the invoice, the costs have changed –  will post the price increase to cost of sales and will describe the increase of cost as a “Sales Adjustment”.

Configuration


1  > Cater for Partial Accruals and Purchase Variance

How SM3 Handles Accruals in the General Ledger
----------------------------------------------

1. At time of purchase order / outside processing posting of receipts  
   (assume a receipt landed cost of $1000)

![](../Resources/Images/AP_Accruals1.png)

2. At time of entering/posting AP Voucher [AP21B]  
   (assume vendor invoice is $10 higher than PO price - total invoice amount $1,010.00)

![](../Resources/Images/AP_Accruals2.png)

3. Payment of invoice

![](../Resources/Images/AP_Accruals3.png)

Option

2b. If  is set to automatically distribute variances to inventory or cost of goods sold

![](../Resources/Images/AP_Accruals4.png)

\*(partial if stock not 100% sold)

\*\*No taxes are taken into consideration with above examples

---
