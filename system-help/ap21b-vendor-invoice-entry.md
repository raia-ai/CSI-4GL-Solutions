---
title: "Entering a Vendor Invoice"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Entering a Vendor Invoice"
long_description: "Help documentation for Entering a Vendor Invoice in the 4GL system."
---


Entering a Vendor Invoice
=========================

This function is used to enter and/or update vendor invoices for accounts payable tracking.

[tip re scanning vendor invoices to be added as an attachment]

Inventory Items follow the same process as Non-Inventory vouchers with the exception that MS33 is utilized to automatically distribute payments. The system will take your purchase variance and automatically make adjustments. The steps are outlined below:

1. Enter MS33 in search function
2. Navigate to AP Options under Accounting header and press F4.
3. Select Cater For Partial Accruals And Purchase Variance and set the value to “Y”

Non-Inventory Vouchers follow the process outlined below:

1. Choose Accounts Payable » Vendor Invoice Processing » Voucher Entry Maintenance [AP21B].

   The search function allows you to filter the results to the right:

2. Enter or select Type of Entry code: DC = direct check, DD = direct disbursement,  VC = AP voucher.
3. Enter Document number.

If you press new you will be taken to the Header tab:

3. Enter a Remit To address, this is populated from your vendor file. You can have multiple addresses for a single vendor.
4. Enter a Description to explain what the voucher is for.
5. Select Invoice Type, this field is assigned from vendor profile. .
6. Skipped in video Select Payment Code.
7. Enter Invoice Number. The number has to be unique.
8. Enter or select Invoice Date. This field defaults to today however, if your period is open you may back date.
9. Enter or select Due Date.
10. Enter the date to be recorded in your GL. Effective Date defaults to your invoice date
12. Enter Exchange Rate. I think this field may be prefilled from a cashbook?? This is where John's video stops.

    Next, you will then be taken to the Details tab. The system will look at your Invoice Type and require a balance. You will not be allowed to process if the invoice is not balanced.  will auto balance by adding an extra line item.

Double click on an account, if you double click on accruals the first step will be required:

1. Vendor may not be the vendor where the accrual was made. In this case you would need to change to original PO vendor here.   
   Press Receipt Details to make adjustments to the receipt.

1. Enter Foreign Value.
2. Enter Description: This extra description is used to distinguish between multiple similar items in the invoice.

If the receipt has a variance click Distribute to balance against Purchase Discounts account.

Applying a Variance Invoice to a Closed AP Line
-----------------------------------------------

When applying an additional invoice to a closed purchase order line:

1. Select the Zero Variance check box, as the invoice has been fully paid.
2. In the Receipt Details window, click Sel Paid and enter the amount being invoiced; this will create a variance.
3. Click Distribute to balance the voucher. You can ignore the variance warnings.
4. Perform the Proof Listing and update the voucher. An inventory adjustment will be generated for the variance amount.

---
