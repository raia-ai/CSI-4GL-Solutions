---
title: "Purchasing-Non-Inventory-Purchases"
source: "Purchasing-Non-Inventory-Purchases.docx"
tags: ["purchasing", "non-inventory", "procurement", "accounts-payable", "purchase-orders", "general-ledger", "ERP", "procedures", "controls"]
version: "1.0"
last_updated: "2025-12-04"
short_description: "This document outlines the end-to-end procedure for creating and processing non-inventory purchases, including configuration of purchase cost codes, vendor account defaults, purchase order entry, receipts, and voucher or direct cheque processing. It highlights the use of specific menus (e.g., PO14, PO1B, AP21B-B), the required Line Type and Sales Cost code, and the GL impact of receipts for consumable items."
long_description: "This procedure document provides step-by-step guidance for handling non-inventory purchases—typically consumable items that are not tracked as stock. It begins with the configuration required to accurately capture costs and post to the correct General Ledger accounts. Users first create a dedicated purchase cost code for consumables (for example, CON) in the PO14 Purchase Costs menu, ensuring the appropriate requisition flags and unit of measure settings are applied. The document emphasizes that the GL accounts associated with this cost code drive the accounting entries produced later in the process.

Next, the Vendor Account Types are configured in the PO1B menu so that non-inventory vendors default to the correct credit account (e.g., 2490-00) during voucher entry. Depending on vendor payment terms and reporting requirements, organizations may choose to use a liability account with an accrual subledger to track amounts owed for consumables that have been received but not yet paid. This configuration enables better visibility and reconciliation of accrued liabilities for non-inventory purchases.

Operationally, the process continues with entering a purchase order for a non-inventory vendor. In the PO details, users add a cost line using the Add Cost function, select Line Type S (which allows entry of a quantity or pieces), and assign the newly created Sales Cost code (CON). Users then enter the quantity and cost and save the PO. The PO is processed and a receipt is entered against it. The resulting General Ledger Detail (GLD) should reflect postings to both accounts defined on the cost code, confirming that the configuration is working as intended.

Finally, the procedure concludes with the financial settlement step, where a vendor invoice is entered via Voucher Entry/Maintenance (AP21B-B) or, alternatively, a direct cheque is issued via AP Disbursements (AP21B_B) after selecting the bank. These steps ensure that non-inventory purchases flow from configuration to PO entry, receipt, and payment, with consistent GL postings that align to the organization’s accounting structure and reporting needs."
---

## Title
Non-Inventory Purchases

## Description
Create PO for Non-Inventory Items

## Steps
1. Create PO cost code for consumable items (CON) on PO14 Purchase Costs menu
   - Enter the Cost code with a checkmark in the ‘Req’ column field and ‘A’ for ALL in ‘1’ column and ‘PC’ in ‘PUM’ column
   - The GL codes entered against the cost code
2. In the Vendor Account Types PO1B menu, set the Non-Inventory Vendor Account type to have the default GL Account of 2490-00 come up for voucher entry (or whatever you call this credit account)
3. Note: This code could be a liability account with a subledger of accrual, so that you can see what is owing and not yet paid in consumables; it would depend on the vendor payment terms
4. Enter in a PO for non-inventory vendor
   - On Details tab, use the “Add Cost” button to add a cost line to the PO
   - The ‘Line Type’ should be “S”, so that you are able to enter in # of pieces
   - The ‘Sales Cost’ code should be your new cost code “CON”
   - Enter in the # of pieces (or select a different unit of measure) and the cost
   - Enter through or click on ‘Save’ button to save
5. Process PO
6. Enter in Receipt against PO
7. GLD shows that the receipt hit both accounts set up on cost code in the GL
8. Enter in a voucher/vendor invoice in Voucher Entry/Maintenance screen AP21B-B menu or Process a Direct Cheque in AP Disbursements menu -  AP21B_B (you need to select a bank)