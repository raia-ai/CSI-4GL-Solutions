---
title: "Accounting-AP_-_Accounts_Payable-Accounting_Module_Bullet_Points_-_Rev_Dec_2020"
source: "Accounting-AP_-_Accounts_Payable-Accounting_Module_Bullet_Points_-_Rev_Dec_2020.pdf"
tags: ["4GL Solutions", "Steel Manager III", "Accounting", "Accounts Receivable", "Accounts Payable", "General Ledger", "ERP", "Metal Industry", "Financial Reporting"]
version: 1.0
last_updated: 2025-12-04
short_description: "This document outlines the features and functionalities of the accounting modules within the 4GL Solutions' Steel Manager III software, specifically focusing on Accounts Receivable, Accounts Payable, and the General Ledger. It details processes for managing customer credit, payments, invoicing, and financial reporting tailored for the metal industry."
long_description: "This is a detailed guide to the accounting capabilities of the Steel Manager III (SM3) ERP system, developed by 4GL Solutions for the metal industry. The document is divided into key accounting areas: Accounts Receivable (AR), Accounts Payable (AP), General Ledger (GL), and Management Analysis Reporting. For Accounts Receivable, it describes tools for credit control, customer history inquiries, automated invoicing, and collections management to minimize bad debt. The Accounts Payable section covers vendor invoice tracking, accrual accounting for received goods, payment processing (including checks and EFT), and variance analysis. The General Ledger section explains its role as the central repository for all financial transactions, detailing file maintenance (Chart of Accounts), transaction processing (including recurring journals), an integrated cash book for bank reconciliation, and powerful inquiry and reporting tools. The final section highlights the system's extensive reporting capabilities, including standard reports, a custom report writer, and management dashboards, all designed to provide comprehensive financial insight. The document includes screenshots and process diagrams to illustrate key functions."
---

## 4GL Solutions: TECHNOLOGY FOR THE METAL INDUSTRY
## ACCOUNTS RECEIVABLE
### Introduction
The accounts receivable module in STEEL MANAGER III gives the user the ability to offer their customers credit facilities, and at the same time place a tight control on delinquent accounts. It also highlights all outstanding documents and ensures a timely collection of these, and at the same time, minimizes the exposure to bad debts. The accounts receivable module in STEEL MANAGER III will bring your average days to pay down to an acceptable level. With the help of built in credit checks, your bad debt exposure will be minimized.
### Highlights
Your collections process will be made easier with the help of our comprehensive document application and tools, such as: - **System Credit controls on new orders.** If an order fails credit, the Credit Manager will automatically receive a Task advising them of the order on Credit Hold. All the credit information will be instantly viewable by the Credit Manager. Once the manager has made a decision to either approve or disapprove the order, the sales person will automatically receive a Task advising them.
- **Inquiries into a customer's credit history,** the status of any open orders, invoices and receipts. Immediate on-line viewing of ageing buckets.
- **Delivery of Invoices and Statements via Email/Fax** (at time of shipment) is available directly from STEEL MANAGER III.
- **AR inquiry by aging** allowing the credit department to concentrate on problem accounts.
- **Ability to enter notes** on Transactions and/or Customer during Collection process.
- **Interest charged** on Past due accounts.
- **Ability to drill down to source document level**.
- **Full integration with other modules** improving the accuracy and timing of information.
### New Accounts
New accounts will be faxed or emailed a credit application form and “new customer package" straight from SM3. Once completed and returned, these documents can be electronically attached to the customer profile for safe storage and easy retrieval.
**Figure 10.1: Customer File Maintenance**
[Image: A sample Excel spreadsheet showing a rolling trial balance with GL account descriptions and monthly financial data.]
For auditing and balancing purposes, **Steel Manager III** comes with a standard detailed GL report. This report can be filtered by date, source of transaction, account, account range, and posted/non-posted entries. The user will find this an invaluable tool when checking and balancing account details.
Another very useful report built into the software is the cash forecasting report. This report will allow the operator to forecast cash flow based on historical financial information. For example, the receivables are analyzed on the average days to pay of a particular customer and the payables are analyzed based on the average time it takes to pay a vendor. Fixed expenses that do not go through the receivables or payables can be entered into the system so that they are also considered in the forecast report.
### Period Ends
Steel Manager III will allow the user to close periods to prevent unwanted transactions from hitting the GL. Please note that once a period has been closed, customers will still be able to affect the period through one or more GL journal entries. Generally, this feature would be used by controllers to post closing entries. It also includes a year-end function that will generate a year-end report, clear out all of the P&L accounts and post the difference to retained earnings. Furthermore, it will cycle your dates file so that you have a new-year open for transactions.
### Report Writer
Over and above the standard reports, **Steel Manager III** is equipped with a parameter driven report writer which will allow customers to customize their financial statements (balance sheet and income statement). The module will allow grouping of accounts, creation of headings, sub-totals, totals, and implementation of other useful features.
## MANAGEMENT ANALYSIS - REPORTS
There is a wealth of information available to management to monitor the health of your business.
- **Comprehensive Reports** give insight into many aspects of your business such as sales, margin, margin percent, profitability, sales by salesperson, top selling material, best-selling grades, and more. There are approximately 300 standard reports to choose from, many of which can be exported to Excel.
- Our integrated **Financial Report Writer** will allow you to create your own custom reports, extracting data from any GL Code, and designing the report the way you want to.
- **Remote Reporting** is a useful tool that allows managers to remain current by automatically emailing the latest sales numbers to their PC, Blackberry, or cell phone.
- **Management Dashboard** is a great tool for metal center managers that will save time by giving you a complete overview of your entire company with just one glance.
- **Corporate Inquiries** give multi-warehouse companies the flexibility to see all their available material, sales, orders pending, and incoming material in a single window.
- **Cash Forecasting** allows you to see your cash availability for any selected future date. This information is based on payables, cash book, and receivable history.
- **Paperless Reporting** is the new age of management systems and company analysis. Steel Manager III has numerous detailed inquiries and built in reporting screens that allow you to manipulate data on the fly, giving you new totals and on demand functionality.
- **ODBC Connectivity** gives you complete access to your database. This will allow you to use Crystal Reports and to export to Excel spreadsheets.
## ACCOUNTING MODULE STANDARD REPORTS
| Category | Report Name | Code |
Once a sales order is created it is then passed through a credit check. 4GL Credit Checks include: - Is the Customer over the Credit Limit?
- Are there any past Due Transactions over XX days?
- Has there been no activity for XX days?
- or whether the customer has been placed on manual Credit Hold?
If any one of the checks fails, Sales Order will be “held” and will be transferred to the credit department via Task Manager.
The credit department can then do an inquiry into the customer's credit. This is a very informative screen, and will give the user plenty of information with which to contact the customer and negotiate the release of the current and any future orders. Information that is available for the user is as follows: start date, credit line, last sale date and amount, average days to pay, highest credit date and amount, last payment date and amount, sales history, open AR and orders.
**Figure 10.3: Cash Receipt Entry**
- **Accrual accounting: ** Receipts are accrued at the time of receipt to assist in matching expenses with revenues in the same accounting period
- **Option to distribute variances from material and outside processing invoices.** 4GL will automatically create a cost adjustment for in stock material or if sold will adjust the cost of sales on the invoice
- **Reports and inquiries** keep track of payments due, vendor analysis, and cash requirements and aging
- **EFT/ACH Payments**
- **Automatically create “Positive Pay”** file to send to bank
### Accruals
When inventory is received, the system will automatically create an accrual entry. The inventory account will be debited and accrual account credited. Each cost component of the landed cost will be accrued separately so they can be referenced individually from the vendor invoicing function.
The following schematic communicates how Steel Manager III handles accruals. Your accountant can close Month-Ends without having to wait for Invoices from the supplier (including Freight/Brokerage, etc.)
### How 4GL handles Accruals in General Ledger
**1. At time of Purchase Order / Outside Processing Posting of Receipts**
(Assume a Receipt Landed cost of $1000)
| Inventory | Accruals |
|: --- | :--- | :--- |
| **General Ledger** | | |
| File Listings | Chart of Accounts Description | GL21 |
| | Chart of Accounts Open Balance | GL22 |
| | Current Budget Listing | GL23 |
| | Projected Budget Listing | GL24 |
| | GL Budget Comparison Listing | GLX25 |
| | Non-Utilized GL Accounts Report | GLX26 |
| Cash Book Report Menu | Print Cash Book Detail | CB71 |
| | Bank Reconciliation Report | CB72 |
| | Cash Forecast Report | CB73 |
| GL Reports | | |
| Trial Balance | Trial Balance Report | GL73 |
| | Rolling Trial Balance – Xls Output | GL7A |
| Activity Reports | Detailed General Ledger Activity | GL75 |
| | Summary General Ledger Activity Report | GL76 |
| Journal Entries | Journal Entry Report | GL78 |
| Financial Report Generator | have ability to design their own Financial Reports | |
| | Financial Report File Maintenance | RG1 |
| | Financial Report Parameter Listings | RG2 |
| | Financial Report Title Listings | RG3 |
| | Create Duplicate Financial Report | RG4 |
| | Financial Report Print - Whole Dollars | RG6 |
| **Accounts Receivable** | | |
| File Listings | Potential Customer | AR21 |
| | Banks Master File | AR22 |
| | Customer Credit Group | AR24 |
| | Customer Bill-To/Ship-To | OE24 |
| | Debit/Credit Reason Codes | OE29 |
| Listings | Customer – 12 Month Budget | AR76 |
| Aging Reports | Detailed Aging Report | AR7D |
| | Customer Statements Fax/Email | ARZE |
| | Customer Statement | AR7F |
| | Summary Aging Report - One Page | AR7H |
| | Detailed AR Aging Report | AR7R |
| Cash Receipts | Cash Receipt Register | AR7I |
| | AR Document Application Report | AR7I |
| | Receipt Voucher Reprint | AR7O |
| Listings / Labels | Customer | AR75 |
| | Create Customer Labels – 1.33x4 | ARC |
| | Create Customer Labels – 1.33x4 | ARD |
| Other | Projected/Potential Annual Sales | AR72 |
| | Customer Remarks | AR7A |
| | Customers W/Multi Ship Location | AR7B |
| | Y-T-D Vs. Potential Sales Comparison | AR7C |
| | Blanket Tax Exemption Report | AR7G |
| | Export Customer Document Delivery to Excel | AR7J |
| | Credit Note Financial Impact Report | AR7K |
| | Salesperson Budget by Customer | AR7L |
| | Export Credit Limit Analysis Report to Excel | AR7M |
| | Outside Salesperson Call Report | AR7N |
| | Accounts Receivable Aging Report | AR7P |
| | Accounts Receivable Follow-up Report | AR7Q |
| | Sales Tax Report | OE7XF |
| **Accounts Payable** | | |
| File Listing | Vendor Mailing Labels | AP15 |
| | Payee Masterfile Listing | AP17 |
| | Vendor Mailing Labels (4X1-1/3) | AP18 |
| | Vendor Filing Labels (4X1-1/3) | AP2B |
| | Vendor Masterfile Listing | PO21 |
| Disbursements Processing | Check Writing | AP363 |
| Check Reconciliation Menu| Returned Check Proof Listing | AP62 |
| | Returned Check Entry | AP61 |
| | Outstanding Check Listing | AP63S |
| | Void Check Listing | AP64 |
| AP Reports Checks | Check Listing | AP7B |
| | Check Listing (Keyed on Voucher) | AP7D |
| | Void Check Listing | AP7C |
| | Payment Confirmation | AP7G |
| | Paid Vouchers Report | AP7J |
| Other | Vendor Analysis | AP13 |
| | Cash Requirements Forecast & Aging | AP5 |
| | Vendor Remarks Listing | AP74 |
| | Vendor Invoice Listing | AP75 |
| | Accrual Analysis Report | AP76 |
| | AP Aging Report | AP77 |
| | Debit Accruals Report | AP7E |
| | Accrual Aging Report | AP7F |
| | Vendor Invoice Listing By Account Type | AP7H |
| | Vouchers with No Attachments | AP7K |
| | Purchase Variance Report | AP7L |
| | Cash Requirements Forecast | AP7M |
| | Rebate Analysis Report | PO7W |
| | Paid Rebates Import | PO7Z |
**Figure 11.1: Vendor Invoice Ref. To Receipt Details**
3. Check batch processing. This can be achieved by entering select parameters into a screen. If the parameters are met, the invoice will be selected for payment. Some of the select parameters are: vendor type and payment terms.
4. **Steel Manager III** also provides the ability to create payments to be processed by EFT (electronic funds transfer) or ACH payments. EFT batches can be created in the same manner as check batches which are outlined in the previous points.
Checks may easily be voided by selecting the original check number. By voiding a check, the entries generated from the original check will be reversed with a separate entry.
Payments and void checks will create an entry into the integrated cash book (Bank Reconciliation). Please see the General Ledger documentation for a more detailed discussion of the cash book functionality.
A separate function can be used to track which checks have been mailed.
### Reports and Inquiries
There are a number of different inquiry screens available to the user. The vendor payables inquiry allows users to see the current accounts payable status of a particular vendor on the screen. This screen will show outstanding invoices as well as invoices that have already been paid. In the case of previously paid invoices, the system displays the check number with which the selected invoice(s) were paid.
The accrual inquiry screen displays receipts that have not had a vendor invoice associated with them, as well as receipts that have already been linked to an invoice. The system provides the ability to drill down into the estimated field in order to show the breakdown of the accrual (base price, freight, insurance, etc.). By drilling down on the actual column the operator has the ability to view the details of the vendor invoices. Finally, the write off field displays General Ledger journal entries that have affected the selected accrual record (figure 11.2).
**Figure 11.2: Purchase Variance Inquiry**
**Features include: **
- Integrated cash book (Bank Reconciliation)
- Report writer
- Ability to drill down to the document level
- Financial Report Generator allows the creation of custom financial reports
- Sales and Cost of Sales can be reported by product line
- Multi-currency capability
- Option to save non-financial data within a GL account, i.e. headcount against salary GL account, pounds sold against sales account
### File Maintenance
The Chart of Accounts can be imported into Steel Manager III via Excel spreadsheets. Steel Manager III can handle a variety of formats for its account codes, but the recommended format would be xxxx-yy where xxxx represents the account code and yy would represent a warehouse code (if there were multiple warehouses). By having the last two characters as the warehouse code, it is possible to track financial transactions by warehouse. On each account, the operator can indicate whether the account should be consolidated (warehouse code to be 00) or not consolidated, in which case the warehouse ID will represent the last two characters of the GL code).
Steel Manager III allows input of budget numbers into the GL. These numbers will be entered against the chart of accounts and will later be used by the financial report generator to conduct budget vs. actual comparisons.
### Transaction Processing
Standard Journal Entries can be entered into the system. Through the journal entry screen entries are allowed into accounts such as Accounts Receivable, Accounts Payable, and Accruals. When accounts such as these are used, there is an option to affect the sub-ledgers directly. For example, if Accounts Receivable is affected, the journal can be applied to a customer invoice.
Recurring journals can also be entered. In this case, a frequency and occurrence can be entered. The frequency will define whether the journal will be every month, two months, etc. The occurrence will define how many journal entries will actually be created. For example, if a recurring journal with a frequency of 2 and an occurrence of 3 is entered, the system will create 3 journal entries – one every 2 months. This is useful for fixed expenses where the value of the journal does not fluctuate.
### Cash Book
Steel Manager III has an integrated Cash Book and bank reconciliation. Every time the bank(s) are affected in the system, an entry will be created in the cash book. This will occur when writing a check, voiding a check, receiving cash, reversing a cash receipt, or if a journal entry affects the bank. Although these entries are automatic, the operator may optionally make entries directly into the cash book. This direct entry is often used for bank charges and other entries of this nature.
The bank reconciliation will allow comparison and reconciliation of the bank statement with the entries in the cash book by checking off entries. At the end of the process, the closing balance on the bank statement should match the balance in the cash book. The reconciliation will show checks that have not yet cleared the bank as well as other entries that have not yet affected the bank account.
### Inquiries
The General Ledger detailed inquiry screen will allow the operator to view the activity of any specified account. This inquiry screen will allow for to drill down to a summary level (daily entry), a detailed level (document level), and will actually allow drill down into the document itself. For example, an operator could drill down into the inventory account and see that there was a credit of $15,000 for a particular date. If he/she drills down further, the invoices that make up the $15,000 can be seen. The operator could then drill down into the invoice to see the line items that are on the invoice.
### Standard Reports
STEEL MANAGER III comes equipped with a number of standard reports.
The trial balance report will allow the operator to specify which fiscal period the report is for. It will also give an option to specify this period only. Furthermore, there is an option of specifying a range of accounts (to filter the report as desired).
A rolling TB can be extracted directly into Excel. This is an extremely powerful, time saving feature that will allow easy analysis of quarterly, bi-annual, and annual numbers (figure 12.1).
**Figure 12.1: Sample Excel Spreadsheet**
---

## Accounting-AP_-_Accounts_Payable-Accounting_Module_Bullet_Points_-_Rev_Dec_2020