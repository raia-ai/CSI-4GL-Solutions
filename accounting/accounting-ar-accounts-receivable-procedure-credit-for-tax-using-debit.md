---
title: "Accounting-AR_-_Accounts_Receivable-Procedure_credit_for_tax_using_debit"
source: "Accounting-AR_-_Accounts_Receivable-Procedure_credit_for_tax_using_debit.docx"
tags: ["accounting", "accounts-receivable", "AR", "tax-credit", "debit-note", "finance-operations", "procedures", "invoice-processing", "ERP"]
version: "1.0"
last_updated: "2025-12-04"
short_description: "This document outlines the Accounts Receivable procedure for issuing a debit in order to record or claim credit for tax. It provides step-by-step guidance, data requirements, and control points for processing in AR, ensuring compliance, auditability, and accurate ledger impact."
long_description: "This procedure document describes, in detail, how Accounts Receivable personnel should process a credit for tax using a debit within the AR subledger. The guidance is intended for finance operations, shared service centers, and accounting teams responsible for customer billing and statutory tax handling. It explains the end-to-end workflow beginning with identifying the tax credit scenario, validating source documents, and preparing the required entries. The document delineates the roles and responsibilities, pre-requisites, and master data dependencies, followed by clear, actionable steps for entering a debit transaction that yields a tax credit effect. Where applicable, it points out mandatory fields, document numbering conventions, and references to customer accounts, tax codes, and periods. In addition to the procedural steps, the document includes expected accounting entries, examples, and control checks that ensure compliance with internal policies and external tax regulations. It highlights common pitfalls—such as using an incorrect tax code or period—and provides tips for reconciliation and reporting. The procedure emphasizes segregation of duties, approval routing, and the supporting evidence required for audit trails. If the process is supported by an ERP system, the document provides screen-level guidance, indicating navigation paths, form fields, and validations to confirm that the debit transaction is configured to produce the appropriate tax credit. Any variations by jurisdiction are noted, along with references to related SOPs such as credit/debit memo handling, tax configuration, and AR close activities. Finally, the document outlines post-transaction review steps, including extracting reports, reconciling to the general ledger, and maintaining documentation retention in accordance with company policy. Appendices may include sample forms, templates, or tables summarizing field definitions and accounting impacts to assist users during execution."
---

Credit for tax procedure

- Setup required:
- Create a new sales cost code TAX & mark as non-taxable OE16

- Create a new Debit/Credit reason code OE19

- Procedure Using option 2 - CM & DM:

- Enter Credit Note
- Reference invoice#, do not copy over any lines
- Add Cost Line:

- Use Sales Cost: MSC for misc sales taxable & reason code TAX
- Invoice value is the subtotal excluding tax
- This will preview as follows:

- Enter Debit Memo
- If CM is updated can reference it otherwise put ** in reference
- Enter Cost line as follows:

- Use Sales Cost : TAX for misc sales non-taxable
- Reason code TAX
- Invoice amount is subtotal Excluding tax
- This will preview as follows:

- This is what the GL entries will look like when these are updated:

- ** note I also had the original invoice here to see full picture

- Here is what the sales tax report OE7XI will look like:
