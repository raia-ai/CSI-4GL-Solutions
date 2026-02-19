---
title: "Accounting-AR_-_Accounts_Receivable-Procedure_credit_for_tax"
source: "Accounting-AR_-_Accounts_Receivable-Procedure_credit_for_tax.docx"
tags: ["accounting", "accounts receivable", "credit note", "debit memo", "sales tax", "procedure", "ERP", "GL entries", "tax credit", "AR"]
version: "1.0"
last_updated: "2025-12-03"
short_description: "This procedure outlines how Accounts Receivable processes a credit for sales tax by using a Credit Memo (CM) and a Debit Memo (DM). It covers required setup in the ERP, including creation of a taxable and non‑taxable sales cost code and a debit/credit reason code, and details the steps for entering the CM and DM so that only the tax portion is credited while maintaining accurate general ledger and sales tax reporting."
long_description: "This document provides a concise, step‑by‑step procedure for issuing a credit related to sales tax within Accounts Receivable. The process relies on two transactions—Credit Memo (CM) and Debit Memo (DM)—to correctly reverse or reclassify the tax component without disturbing the underlying revenue lines. It begins with minimal setup in the ERP: creating the appropriate sales cost codes to distinguish taxable and non‑taxable entries and establishing a Debit/Credit reason code for traceability and reporting.

The procedure then walks through entering the Credit Note. The credit is referenced to the original invoice, but no line details are copied over. Instead, a cost line is added using a miscellaneous sales taxable code and a designated tax reason code, with the amount equal to the invoice subtotal excluding tax. This isolates the taxable base for the credit. A preview confirms the impact prior to posting.

Next, a Debit Memo is entered. If the CM has already been updated, it can be referenced; otherwise, a placeholder reference is used. The DM includes a cost line using a miscellaneous sales non‑taxable code with the same tax reason code, and the amount again equals the subtotal excluding tax. This creates the offsetting entry needed to ensure that only the tax element is ultimately credited while preserving revenue recognition on the original invoice. A preview again validates the expected outcome.

The document also highlights the expected general ledger impact once both documents are updated, providing assurance that the postings align with accounting intent. Finally, it notes how the sales tax report (OE7XI) will reflect the transactions, supporting downstream reconciliation and compliance. Together, these instructions ensure that tax credits are processed consistently, transparently, and in a way that maintains accurate AR subledger, GL balances, and tax reporting."
---
## Credit for Tax Procedure

## Setup Required
- Create a new sales cost code TAX & mark as non-taxable  OE16
- Create a new Debit/Credit reason code OE19

## Procedure Using option 2 – CM & DM

### Enter Credit Note
- Reference invoice#, do not copy over any lines
- Add Cost Line:
  - Use Sales Cost: MSC for misc sales taxable & reason code TAX
  - Invoice value is the subtotal excluding tax
  - This will preview as follows:

### Enter Debit Memo
- If CM is updated can reference it otherwise put ** in reference
- Enter Cost line as follows:
  - Use Sales Cost : TAX for misc sales non-taxable
  - Reason code TAX
  - Invoice amount is subtotal Excluding tax
  - This will preview as follows:

## General Ledger Impact
- This is what the GL entries will look like when these are updated:
> Note: I also had the original invoice here to see full picture

## Reporting
- Here is what the sales tax report OE7XI will look like:
