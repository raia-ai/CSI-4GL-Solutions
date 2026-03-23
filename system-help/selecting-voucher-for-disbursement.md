---
title: Selecting Vouchers For Disbursements
source: madcap.md
version: '1.0'
last_updated: '2026-02-19'
short_description: Selecting Vouchers For Disbursements
long_description: Help documentation for Selecting Vouchers For Disbursements in the 4GL system.
---

# Selecting Vouchers For Disbursements

## Manually Selecting Disbursements to be Paid

This function is used to select disbursements to be paid. After you process the selection, vouchers are removed after the checks are processed.

1. Choose Accounts Payable » Disbursements Processing » Multiple Disbursements \[AP33A].
2. Use the fields at the top to filter the vouchers.
3. Select a voucher. You are prompted to enter the voucher amount to be applied and any discount. Repeat for additional vouchers that you want to pay.
4. When you are finished, press F3 and process the disbursements.

## Selecting Disbursements Based on Criteria

This function is used to select all disbursements to be paid that match defined criteria.

1. Choose Accounts Payable » Disbursements Processing » Automatic Disbursements \[AP3K].
2. Enter or select Due Date.
3. Enter or select Account Type.
4. Enter or select Vendor Category.
5. Enter or select Payment Term.
6. Leave “Y” to show Negative Inventory or enter blank to hide negative inventory.
7. Enter “Y” to print Journal or leave blank to not print journal.

## Listing Vouchers Selected for Disbursement

This function is used to generate a report listing for all vouchers which have been selected for payment. From here you can delete vouchers or clear disbursement file.

1. Choose Accounts Payable » Disbursements Processing » Cash Disbursements Journal \[AP34].
2. Enter “Y” to sort by Vendor or leave blank to not sort by vendor.
3. Select Payment Method: Check, EFT, Wire or All.

## Deleting Vouchers From Disbursements

This function is used to delete individual vouchers from the disbursements file.

1. Choose Accounts Payable » Disbursements Processing » Delete Vouchers From Disbursements \[AP3F].
2. Enter Voucher number, partials allowed.
3. Select row and press Delete button in menu along bottom of screen.

## Deleting a Voucher

To delete voucher from the ready to pay status:

1. Press F6 on Voucher.
2. Press F7 to select it for deletion.
3. Select yes to carry out the deletion.

Deleted voucher will still be viewable from multiple disbursements window but will have its status set to blank.

## Clearing the Disbursement File

This function is used to delete all entries in the disbursements file.

This function will clear the disbursements selected.

1. Choose Accounts Payable » Disbursements Processing » Clear Disbursement File \[AP35].
2. Enter “Y” to process Clear Disbursements.

***
