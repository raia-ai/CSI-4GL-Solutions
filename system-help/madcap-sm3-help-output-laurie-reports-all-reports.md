---
title: "Madcap_-_SM3_Help-Output-Laurie-Reports-All_Reports"
source: "Madcap_-_SM3_Help-Output-Laurie-Reports-All_Reports.docx"
tags: ['madcap', '4GL', 'help', 'reports', 'user-guide', 'documentation', 'procedures', 'reference', 'reporting']
version: "1.0"
last_updated: "2025-12-04"
short_description: "Compiled help documentation for 4GL 'Laurie' Reports covering all available reports, their purpose, parameters, filters, and usage notes. Structured for quick reference."
long_description: "This document is a consolidated help output for 4GL 'Laurie' Reports, intended to provide users with comprehensive information about all reports available in the system. It outlines the intent and usage of each report, including key fields, filters, groupings, and parameters. Where applicable, it includes procedural steps, definitions, caveats, and examples to ensure accurate execution and interpretation of results. The content is organized into clear sections and subsections so that readers can navigate by report category, locate specific report names, and understand input requirements and expected outputs. Tables and lists have been converted into Markdown for consistency and readability in a knowledge base and vector store context."
---

Table of Contents













































































































































































































































AP13 - Vendor Analysis
This report lists vendor payment information.
- Choose Account Payable » AP Reports » Vendor Analysis [AP13].
- Enter or select Warehouse code (defaults to all warehouses).
- Select whether to filter by a All Vendors or enter "R" for one (by default, all vendors are selected).
- Enter the Starting Vendor and Ending Vendor to be included in the report.
- Enter or select the Effective Date.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AP74 - Vendor Remarks Listing
This report lists vendor remarks.
- Choose Accounts Payable » AP Reports » Vendor Remarks Listing [AP74].
- Enter or select Warehouse code (defaults to all warehouses).
- Select a Vendor.
- Select a date range to list remarks for (by default, Date From is 01/01/00 and Date To is today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AP75 - Vendor Invoice Listing
This function produces a Vendor Invoice report.
- Choose Accounts Payable » AP Reports » Vendor Invoice Listing [AP75].
- Enter or select Warehouse code (defaults to all warehouses).
- Select a Vendor.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Filter to create Summary or Detailed report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AP76 - Accrual Analysis Report
This accrual report displays actual (from invoice) costs, estimated (from purchase order) and variance between the two costs, for each cost type, within a date range, for a selected or all buyers. This will also link return receipts with PO accruals.
- Choose Accounts Payable » AP Reports » Accrual Analysis Report [AP76].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter or select Buyer code (by default, report is generated for all buyers).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Filter by Currency (by default, report is sorted by Vendor)
- Enter "Y" to indicate whether to show only accruals that have zero actual value or leave default to show all.
- Enter "Y" to indicate whether to show only accruals that have variance or leave default to show all.
- Filter to create Summary or Detailed report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AP77 - AP Aging Report
This report displays money owed to vendor. It can be run for a single vendor or ALL, currency type, invoice date or effective date.
- Choose Accounts Payable » AP Reports » AP Aging Report  [AP77].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter or select a Vendor (by default, all are selected).
- Select whether to produce a Detailed or Summary report.
- Select the Aging Date to include, in MM/DD/YY format (by default, today's date is used).
- Enter or select Vendor currency (by default, all currency is selected).
- Enter or select Vendor category (by default, all are selected).
- Enter Date Used: Effective date or Invoice date.
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
AP7B - Check Listing
This function produces a list of checks issued within a date range.
- Choose Accounts Payable » AP Reports » Check Listing [AP7B].
- Enter or select Warehouse code (defaults to all warehouses).
- Select a Vendor.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select whether to sort by Vendor or leave blank to sort by check number (defaults to sort by vendor).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AP7C - Void Check Listing
This function produces a list of void checks by vendor within a date range.
- Choose Accounts Payable » AP Reports » Void Check Listing [AP7C].
- Enter or select Vendor code (by default, report is generated for all vendors)
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AP7D - Check Listing (Keyed on Voucher)
This function produces a list of checks issued to vendors within a date range.
- Choose Accounts Payable » AP Reports » Check Listing (Keyed on Voucher) [AP7D].
- Select a Vendor.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select whether to sort by Vendor or leave blank to sort by check number (defaults to sort by vendor).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AP7E - Debit Accruals Report
This function produces a report of variance write-offs (favorable or unfavorable) filtered by a date range for a selected warehouse.
- Choose Accounts Payable » AP Reports » Debit Accruals Report [AP7E].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AP7F - Accruals Aging Report
This function produces an accruals aging report used to report accrual status as at certain date and to balance accrual sub-ledger to General Ledger.
- Choose Accounts Payable » AP Reports » Accruals Aging Report [AP7F].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter or select Buyer code (by default, all is selected).
- Select the Aging Date to include, in MM/DD/YY format (by default, today's date is used).
- Select whether to sort by Currency code (by default, it is sorted by Vendor).
- Enter "Y" to filter by accruals that have zero actual value (by default, all accruals are shown).
- Enter blank to filter out accruals that are not equal to zero (by default, accruals with a variance are shown).
- Select whether to produce a Detailed or Summary report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AP7G - Payment Confirmation
This function produces a list of paid checks, sorted by vendor, within a date range.
- Choose Accounts Payable » AP Reports » Payment Confirmation [AP7G].
- Select a Vendor.
- Enter number of the Check to confirm (by default, a range of checks within dates will be reported).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AP7J - Paid Vouchers Report
This report is available as an Excel download only.
- Choose Accounts Payable » AP Reports » Paid Vouchers Report [AP7J].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Vendor code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
AP7K - Vouchers With No Attachments
- Choose Accounts Payable » AP Reports » Vouchers With No Attachments [AP7K].
- Enter or select Vendor code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AP7L - Purchase Variance Report
This function is available as an Excel download only.
- Choose Accounts Payable » AP Reports » Purchase Variance Report [AP7L].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Vendor code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Enter or select Min Var. .
- Press Enter to process the report.
AP7M - Cash Requirements Forecast
This function produces a cash requirements forecast and aging report, within a 90 day date range.
- Choose Accounts Payable » AP Reports » Cash Requirements Forecast  [AP7M].
- Select a Vendor.
- Enter or select the starting date Date 1 and ending date Date 2 for the report (defaults to today's date for Date 1, 30 days from today for Date 2 and 30 days from Date 2 for Date 3.
- Enter "Y" to show the aging in the functional currency (default is blank = no).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AR71 - Printing Cash Receipt
This function prints posted or unposted cash receipts for a specified period.
- Choose Accounts Receivable » AR Reports » Cash Receipt Register  [AR71].
- Enter or select Warehouse code (defaults to all warehouses).
- Select the Bank Code.
- Enter or select Deposit Number (defaults to all).
- Enter or select Fiscal Period (defaults to all).
- Enter the Start Date and Ending Date for the deposit transactions to be included in the report.
- Select the Payment Type (defaults to all types).
- Indicate if you want to include Only Posted receipts or leave blank to exclude them.
- Select whether to produce a Detailed or Summary report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.

AR72 - Projected/Potential Annual Sales
This report prints the projected potential annual sales by salesperson.
- Choose Accounts Receivable » Reports » Projected/Potential Annual Sales [AR72].
- Select the Salesperson code to be used for the report (by default, report includes all salespeople).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
Sales Next Year Projected value is maintained in .
AR75 - Listing Customers
This function is used to print report displaying customer accounts.
- Choose Accounts Receivable » AR Reports » Customer Listing [AR75].
- Enter or select the Customer code (defaults to all).
- Select Multi Territories.
- Select the Inside Salesperson whose customers are to be included on the report (defaults to all).
- Select the Outside Salesperson whose customers are to be included on the report (defaults to all).
- Select how to sort the list: by customer Name or Postal/zip code (default).
- Enter "Y" to Show Inactive only, leave blank to exclude them.
- Specify whether to Show Details on the report: no (blank, default) or Yes.
- Show whether to show the customer's Ship To address(es): no (blank, default) or Yes.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AR7A - Displaying Remarks Assigned to Customers
This report displays the remarks assigned to customers (Customer remarks are maintained in the Remarks (Input) function.)
- Choose Accounts Receivable » AR Reports » Customer Remarks [AR7A].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Customer code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AR7B - Listing Customers w/Multi Ship Locations
This report displays a list of customers who have multiple ship-to addresses. Locations are maintained in the  file.
- Choose Accounts Receivable » AR Reports » Customers w/Multi Ship Locations [AR7B].
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AR7C - Y-T-D vs Potential Sales Comparison
This report contains year-to-date sales, last year sales, and potential sales for all customers, and a percent difference between the two.
- Choose Accounts Receivable » Reports » Y-T-D vs. Potential Sales Comparison [AR7C].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Salesperson code.
- Enter the starting Date for transactions to include in the report (by default, today's date is used).
- Indicate if you want to sort order by Customer name, Target Percent Difference or Actual Sales.
- Select whether to produce a Detailed or Summary report.
- Indicate if you want to show Target  percent values only.
- Indicate if you want to Include Inactive customers.
- Indicate if you want the province summary to be based on the Ship To or the Bill To address.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AR7D - Detailed AR Aging Report
This function produces a detailed Accounts Receivable Aging report, including customer and transaction remarks.
Amounts due beyond the Aging date print in the “Unrealized AR” column of the report.
Customer General Remarks print for all remarks entered assigned with Category AR and Print remarks is set to Y(Yes) in Contact Type Maintenance – MS3P.
**A subset of this report is available for export to a bank in XLS format**: Accounts Receivable Aging Export [AR7U].
- Choose Accounts Receivable » AR Reports » Detailed AR Aging Report  [AR7D]
- Enter or select Warehouse code (defaults to all warehouses).
- Enter or select the Territory code (defaults to all).
- Enter or select the Customer code (defaults to all).
- Select whether to produce a Detailed or Summary report.
- Select whether to display only those documents in the Customer AR Credit file that have a status of Open, that is, do not have monies applied against them (by default, ALL documents are shown).
- Select the Aging Date to include, in MM/DD/YY format (by default, today's date is used). 
Amounts due beyond the Aging date are shown in the “Unrealized AR” column.
- Enter the number of Aging Days 1, that is, days the customer payment is overdue) (by default, 30 days).
- Enter the number of Aging Days 2 (by default, 60 days).
- Enter the number of Aging Days 3 (by default, 90 days).
- Enter the number of Aging Days 4 (by default, 120 days).
- Enter the number of Past Due Days a document must be in order to be included in the report (by default, all documents are included).
- Indicate the currency type: Functional (currency assigned to warehouse) or Source (customer’s currency).
- Select whether to age data by Invoice date (default) or Due date.
- Select how to sort customers: by Currency, Salesperson, or Territory (default).
- Select whether to include Inside Salesperson (default) or Outside Salesperson.
- Select whether to include Customer Details and  Remarks.
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
AR7E - Sending Customer Statements by Fax/Email
This function produces electronic customer statement for multiple customers at the same time. For each customer, you define if the statement will be sent by fax, email, both, or print a hard copy.
- Choose Accounts Receivable » AR Reports » Customer Statements Fax/Email [AR7E].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Customer category (defaults to all).
- Enter or select the Territory code (defaults to all).
- To restrict the report to a single salesperson, select a Salesperson code (by default, the report includes data related to all sales people).
- To ensure that a statement is printed for any customers who are not set up for fax or email, select the Default Print check box.
- To only produce statements for customers who have requested them (as stored in the customer file)1, set Request Only? to “Y”. By default, a statement is produced for all customers.
- By default, only Open documents (that is, do not have monies applied against them) are included. To include all documents, select ALL; you can then enter a from date to see all transactions on or after that date.
- Select the Aging Date to include, in MM/DD/YY format (by default, today's date is used).
- Enter or select Fiscal Period.
- Indicate the currency type: Functional (currency assigned to warehouse) or Source (customer’s currency).
- In the Invoice or Due Date field, specify whether to age data by Invoice date or Due date.
- Indicate if you want to  Show Avg Days to Pay for the customer.
- Indicate if you want to Show the AR Contacts.
- Enter the number of Past Due Days a document must be in order to be included in the report (by default, all documents are included).
Customers will be included in the report even if they have no documents past due in the specified amount of days. However, such customers will not receive a statement by email or fax.
Do not enter anything in the Reset field without the guidance of 4GL Support - if you enter D or N, any values previously changed in the table (Type, fax number, email address, Print flag) are wiped out (or restored to the values in the customer file) and you would have to set up your desired statement values again for all customers. The Reset field is used the first time the AR7E is run to pull the default information from the customer files, but subsequently you should only modify the customized statement settings in the AR7E table as described below. For these reasons, access to this function should be restricted.
Once you have cycled through all the input fields, the table shows matching customers.
- The Grand Total is the dollar value of a customer’s outstanding receivables. Press F4 to open the customer AR Inquiry screen to view further details.
- Change the delivery method for a customer if required:
  - On initial setup, the Type flag is set depending if there is an email address and/or fax number in the customer file (Email, Fax or Both). Change this field as required, e.g. to change a B to an E.
  - If Type = B or F, confirm that the Fax Number is correct.
  - If Type = B or E, press F9 to confirm that the Email Address is correct.
  - If a customer prefers a hardcopy instead of an electronic statement, delete what is in the Type field (to set it to None), press F9 and enter “Y” in the Print field .
- Press F3 to process and generate the statements.
  - If you made any changes in the table, enter “H” to save the changes, then press F3 again to reopen the Process Options screen.
  - When you are ready to generate the statements, enter “P” to process them. A statement is sent (or printed) according to the settings in the table. Note that the electronic delivery will always use the fax number/email address set in this table, regardless of what is set in the customer file.
Configuration
1 [AR17] > Statement = “Y”; for first time setup, enter the email address for statements in the Web/Email field
AR7F - Printing Customer Statements
This function allows you to print all customer statements, or send a statements electronically to one customer at a time. If you want to electronically send customer statements to a group of (or ALL) customers, use .
Customer statements will always print portrait/condensed, regardless of the print window settings. Different versions of customer statements are available.1
- Choose Accounts Receivable » AR Reports » Customer Statement  [AR7F].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Territory code (defaults to all).
- Choose to Sort by Territory: Yes or No (blank).
- Enter or select the Customer code (defaults to all).
- To only print statements for customers who have requested them (as stored in the customer file)2, set Request Only? to “Y”. By default, a statement is printed for all customers.
- By default, only Open documents (that is, do not have monies applied against them) are included. To include all documents, select ALL; you can then enter a from date to see all transactions on or after that date.
- Select the Aging Date to include, in MM/DD/YY format (by default, today's date is used).
- Enter the number of Past Due Days a document must be in order to be included in the report (by default, all documents are included).
- Indicate the currency type: Functional (currency assigned to warehouse) or Source (customer’s currency).
- Select whether to include only customer accounts with a balance over the credit limit : Yes or No (default).
- Specify whether to age data by Invoice date (the default) or Due date.
- By default, the report shows the Average Days to Pay for the customer (Yes): to change this, select No.
- By default, the report shows the AR contact (Yes): to exclude this information, select No.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
Configuration
1  [MS33] > AR Options
2 [AR17] > Statement = “Y”
AR7G - Listing Blanket Tax Exemption Customers
This report displays customers with tax exemptions or all customers.
- Choose Accounts Receivable » AR Reports » Blanket Tax Exemptions [AR7G].
- Enter "Y" to display all customers regardless of tax status (by default, only tax-exempt customers are shown).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AR7H - Summary AR Aging Report
This function produces a detailed Accounts Receivable Aging report, sorted by Currency Code.
- Choose Accounts Receivable » AR Reports » Summary AR Aging Report  [AR7H].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter or select the Territory code (defaults to all). .
- Enter or select the Customer code (defaults to all).
- Select whether to produce a Detailed or Summary report.
- Select the Aging Date to include, in MM/DD/YY format (by default, today's date is used).
- Enter the number of Past Due Days a document must be in order to be included in the report (by default, all documents are included).
- Indicate the currency type: Functional (currency assigned to warehouse) or Source (customer’s currency).
- Specify whether to age date by Invoice date (default) or Due date.
- Specify whether to sort by Territory: Yes (default) or No.
- Specify whether to include only customers with an AR balance: Yes or No (default).
- Enter "Y" to have the report double spaced or leave blank for single spaced.
- Enter "Y" to include customers who are over their credit limit, leave blank to exclude them.
- If set to Yes, enter the Minimum Credit Limit to be used.
- Enter "Y" to include Customer details or leave blank to exclude them.
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
AR7I - Printing Document Applications
This function prints all Accounts Receivable documents, sorted by customer.
- Choose Accounts Receivable » AR Reports » Document Applications [AR7I].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter or select the Customer code (defaults to all).
- Enter or select Type of Entry code.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Enter "Y" to include Plus Balance or leave blank to exclude.
- Enter "Y" to include Minus Balance or leave blank to exclude.
- Enter "Y" to include Zero Balance amounts or leave blank to exclude.
- Enter "Y" to show Applied Only (defaults to all).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AR7K - Generating a Financial Impact Report (Excel)
This report lists the financial impact ($ and description) entered in the Quick Credit Note Entry ().
This report is only available as an Excel download.
- Choose Accounts Receivable » AR Reports » Financial Impact (Excel) [AR7K]
or Sales Order Entry » Order Entry Reports » Miscellaneous & Custom Reports » Miscellaneous Reports » Credit Note Financial Impact [AR7K].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
AR7L - Sales By Customer By Product Line Budget
This function prints the Sales Budget by customer, as defined in the customer file.
- Choose Sales Order Entry » Order Entry Reports » Salespsn By Cust By Pline Budget [AR7L].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter or select Salesperson code as well as Inside or Outside designation.
- Select the Date for the report (by default, report includes data to the current date).
- Choose to sort by Customer name, Target Percent Variance or actual Sales.
- Indicate if you want to show  Target Only.
- Specify if you want the Province Summary to be by Bill-to or Ship-to address.
- Specify if you want the salesperson Budget to be by Weight, sales Value or Margin value.
- Select whether to produce a Detailed or Summary report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AR7M - Analyzing Customer Credit
This function is used to export credit limit analysis.
This report is only available as an Excel download.
- Choose Accounts Receivable » AR Reports » Customer Credit Analysis [AR7M].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Press Enter to process the report.
AR7N - Salesperson Call Report
- Choose Sales Order Entry » Order Entry Reports » Salesperson Call Report [AR7N].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Salesperson code along with Inside our Outside denotation.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Enter or select Category code: AR = accounts receivable, IS = inside sales, OS = outside sales.
- Enter Priority: High, Medium, Low, or ALL.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AR7O - Receipt Voucher Reprint
- Choose Accounts Receivable » AR Reports » Receipt Voucher Reprint [AR7O].
- Select the Bank Code.
- Enter or select the Deposit Number you want to reprint.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AR7P - AR Aging Report - Custom
- Choose Accounts Receivable » AR Reports » AR Aging Report [AR7P].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter or select the Territory code (defaults to all).
- Enter or select the Customer code (defaults to all).
- In the Open/All Documents field, indicate if you want to include All documents or only documents in the Customer AR Credit file that have a status of Open (do not have monies applied against them).
- Select the Aging Date to include, in MM/DD/YY format (by default, today's date is used).
- If necessary, change the number of Aging Days for each period.
- If you only want to include documents a certain number of days past due, enter the number of Past Due Days .
- Indicate if you want aging calculated by Invoice or Due date.
- Select whether to Sort By Currency, Salesperson or Territory. 
If you entered “S”, select the Salesperson Type to include (Inside or Outside).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AR7Q - AR Follow Up Report
- Choose Accounts Receivable » AR Reports » AR Follow Up Report [AR7Q].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter or select the Customer code (defaults to all).
- Enter or select Operator code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AR7R - Detailed AR Aging Report
This function generates a detailed report based on money owed by customers and aged according to the document date entered. A list of open documents for each customer will also be provided.
- Choose Accounts Receivable » AR Reports » AR Aging Report [AR7R].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter or select the Territory code (defaults to all).
- Enter or select the Customer code (defaults to all).
- Select whether to produce a Detailed or Summary report.
- In the Open/All Documents field, indicate if you want to include All documents or only documents in the Customer AR Credit file that have a status of Open (do not have monies applied against them).
- Select the Aging Date to include, in MM/DD/YY format (by default, today's date is used).
- If necessary, change the number of Aging Days for each period.
- If you only want to include documents a certain number of days past due, enter the number of Past Due Days .
- Indicate the currency type: Functional (currency assigned to warehouse) or Source (customer’s currency).
- Indicate if you want aging calculated by Invoice or Due date.
- Select whether to Sort By Currency, Salesperson or Territory. 
If you entered “S”, select the Salesperson Type to include (Inside or Outside).
- Indicate if you want to show Customer Details and Remarks.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
AR7T - Sales by State/Province
This report summarizes all invoices, credits and debits for the previous fiscal year and current fiscal year by customer bill-to address or the document ship-to address. It filters by salesperson if one is entered.
This report is only available as an Excel download.
- Choose Accounts Receivable » AR Reports » Sales By State/Province Report [AR7T].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select one or more Salesperson and enter the salesperson type (Inside or Outside).
- If necessary, change the As At Date. The YTD Actual Sales in the report will include sales for the current fiscal year up to this date.
- In the Province Summary field, indicate if you want to summarize the report by customer Bill-to or document Ship-to address.
- Press Enter to generate the report.
ARC - Printing Customer Labels - 1.33x4
This function is used to print labels based on sales activity selections.
- Choose Accounts Receivable » AR Reports » Customer Labels - 1.33 X 4  [ARC].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter the number of Activity Days a customer must have to have labels printed for them (by default, labels are printed regardless of activity days  ).
- Enter or select Sales Days.
- Enter the minimum Sales Amount (in dollars) that must have accumulated in the Activity Days a customer must have to have labels printed for them.
- Leave default to Sort Alphabetically, or enter blank to not.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
GL73 - Trial Balance
This function prints a trial balance.
- Choose General Ledger » GL Reports » Trial Balance [GL73].
- Enter or select the Fiscal period code.
- Enter the End Date for the fiscal period in (MM/DD/YY) format.
- Enter "Y" to select this fiscal period (by default, the report is balanced to date).
- Enter or select General Ledger Account From code (by default, all accounts are selected).
- Enter or select General Ledger Account To code (if all is selected in Account from field, this field is skipped).
- Enter "Y" to display General Ledger accounts with balance zero (by default, these accounts are not shown).
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
GL75 - Detailed GL Activity
This function is used to print a Detailed General Ledger Activity for a specified date range (range can include multiple fiscal years).
- Choose General Ledger » Financial Report Writer » Detailed GL Activity [GL75].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Type "A" to sort dates in ascending order (by default, the dates are sorted in descending order).
- Enter or select General Ledger Source code (by default, all are selected).
- Enter or select the General Ledger Account code From (by default, all are selected).
- Enter or select the General Ledger Account code To (if "ALL" is entered in Account From this field is skipped).
- Enter "U" to display Unposted transactions (by default, Posted are displayed)
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
GL76 - Summary GL Activity
This function is used to print a Summary General Ledger Activity report.
- Choose General Ledger » GL Reports » Summary GL Activity [GL76].
- Enter Warehouse number (by default, your assigned warehouse is selected).
- Enter General Ledger Account code (by default, all are selected).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Enter or select Source code (by default, all are selected).
- Enter "U" to display Unposted transactions (by default, Posted are displayed)
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
GL78 - Journal Entry Report
This function is used to print journal entry details for a selected fiscal period.
- Choose General Ledger » GL Reports » Journal Entry Report [GL78].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter Document number, max seven alphanumeric characters.
- Enter or select Accounting Period code (by default, all are selected).
- Enter or select Start and End dates (by default, ending date is today's date).
- Select Sub Account journal entries: Accounts Receivable, Accounts Payable, Accruals, Inventory, Other Sub Accounts = "Y" (by default, all are selected).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
GL7A - Rolling Trial Balance - Excel
This function generates rolling trial balance report with output to Excel.
This function is only available as an excel download.
- Choose General Ledger » GL Reports » Rolling Trial Balance - Excel [GL7A].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Fiscal Period Start and End.
- Enter or select General Ledger Account From code (by default, all accounts are selected).
- Enter or select General Ledger Account To code (if all is selected in Account from field, this field is skipped).
- Enter "Y" to display General Ledger accounts with balance zero (by default, these accounts are not shown).
- Enter “Y” to display General Ledger accounts budget amounts (by default, these accounts are not shown).
- Report can only be downloaded to Excel using XLS printer code.
IN71 - Stock List By Logs/Product/Grade
This function is used to create Inventory Stock list - Logs by product displaying inventory logs on-hand.
To display available quantity, use the IN7YG - Product Availability report [IN7YG].
- Choose Inventory Control » Inventory Reports » Stock List by Log/Product/Grade [IN71].
- Produce report at the Product level (default), Log level, or Grade level.
- Enter or select the Product code (by default all products are selected).
- Indicate if you want to show products with inventory On Hand .
- Indicate if you want to Show Program (defaults to Y).
- Indicate if you want to show inventory in Quarantine.
- Indicate if you want to Show Zero logs (logs/products with zero quantity); by default, they are not shown.
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Product Line code (by default, all are selected).
- Enter or select the Spec Type code (by default, all are selected).
- Enter or select Specification code (field defaults to ALL if Spec Type is ALL).
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
The Excel output includes columns for each possible spec.
IN72 - Movements by Product or Log
This function is used to produce a Movements By Product or Log report for a specified type of entry and date range.
- Choose Inventory Control » Inventory Reports » Movements by Product or Log [IN72].
- Select whether to display Log or Product details.
- Enter or select the Product code (by default, all are selected).
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Type of Entry (by default, ALL are selected).
- Enter the From Date and To Date (To Date defaults to today's date).
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
IN73 - Adjustment Authorization
This function reprints the Adjustment Authorization report.
- Choose Inventory Control » Inventory Reprints » Adjustment Authorization [IN73].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Type of Entry code (by default, Adjustment "AJ" is selected).
- Enter or select Adjustment Document number .
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN74 - Transactions In A Date Range
This function reports on inventory transactions within a date range for a specified type of entry.
- Choose Inventory Control » Inventory Reports » Transactions In a Date Range [IN74].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Product Line (by default, all are selected).
- Enter or select the Type of Entry (by default, all are selected).
- Indicate if the Run Type should extract data from the Beginning date or the End date.
- Enter the Date From  and Date To  (To Date defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN75X - Stock List At A Certain Date
- Choose Inventory Control » Inventory Reports » Stock List At A Certain Date [IN75X].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Product Lines you want to report on.
- Enter or select the Date on which you want to check the stock levels.
- Select whether to produce a Detailed or Summary report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN75 - Stock List As At A Certain Date
This function produces an Inventory Stock list snapshot, at a specified date.
- Choose Inventory Control » Inventory Reports » Stock List At a Certain Date [IN75].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Select one or more Product Lines.
- Enter or select the Fiscal Period to report on.
- Choose between a Summary or Detail report.
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
IN76 - Detailed Adjustments By Date
This function is used to produce Detailed Adjustment Report by Date range, totaled by adjustment.
- Choose Inventory Control » Inventory Reports » Detailed Adjustments by Date [IN76].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter the Start and End  dates that goods were received (both default to today's date).
- Indicate if you want to Include Average Cost Adjustments: enter Yes, Only average cost adjustments, or leave blank for no.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN79 - Product Aging
This function is used to create Inventory Stock list by Age Date (date product was received) of product, with subtotals by product line.
- Choose Inventory Control » Inventory Reports » Product Aging [IN79].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- If necessary, change the number of days for the First, Second, Third, and Fourth aging periods (these default to 30/60/90/120 respectively).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7CA - Reprint Log and Location Label
- Choose Inventory Control » Inventory Reprints » Reprint Log & Location Label [IN7CA].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Log Number.
- Press Enter to process the report.
IN7C - Inventory Label by Log Number
This function reprints log labels. It requires a  installed on your network or attached to your computer.
- Choose Inventory Control » Inventory Reprints » Inventory Label by Log Number [IN7C].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Log Number(do not need to precede with "L" or leading zeros). The log must have an MTR file assigned.
- Press Enter to process the report.
IN7D - Inventory Totals By Product Line Group
- Choose Inventory Control » Inventory Reports » Custom Reports » Inv Totals By Product Line Group [IN7D].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Pline group.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7E - Bin Location Label
This function reprints log labels for all products within a selected bin location. The default printer must be defined in MS3F.
- Choose Inventory Control » Inventory Reprints » Bin Location Label [IN7E].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select Location Type: Kasto, Floor Stock (default), Quarantine Stock, Program stock, or Other.
- Enter or select the Bin Location.
- Press Enter to process the report.
IN7F - Active Logs With Original Receipt
This function produces Active (on-hand quantity > 0) with original receipts, adjustments and all other documents which can add inventory, sorted by log number.
- Choose Inventory Control » Inventory Reports » Custom Reports » Active Logs With Original Receipts.  [IN7F].
- Enter or select Warehouse code (defaults to all warehouses).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7G - Logs With No MTR Attached
This function produces logs with no MTR files attached (in log details). Should be run periodically by your quality control department or just prior to a physical inventory count.
- Choose Inventory Control » Inventory Reports » Custom Reports » Logs With No MTR Attached [IN7G].
- Enter or select Warehouse code (defaults to all warehouses).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7H - Mill Tests
This function produces mill test reports. Each MTR image and list logs associated with that MTR are printed as separate reports.
- Choose Inventory Control » Inventory Reports » Custom Reports » Mill Tests [IN7H].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select From Log and To Log numbers (by default, From Log = all logs and To Log = last log number assigned, unless From Log = "ALL" in which case To Log is skipped).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7I - MTR By Log Number
This function prints mill test reports assigned to a specific log.
- Choose Inventory Control » Inventory Reprints » MTR By Log Number [IN7I].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter Log Number; the log number must have an MTR file assigned (do not need to precede with "L" or leading zeros).
- Enter a file name for the MTR Image.
- Enter or select the MTR Type.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7K - Stock List By Finish/Mill
This function produces an Inventory stock list by finish, mill price.
- Choose Inventory » Inventory Reports » Stock List By Finish/Mill [IN7K].
- The report will be produced at the Product level; enter "L" to filter by Log level instead.
- Indicate if you want to show products with inventory On Hand .
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Line code (by default, all are selected).
- Enter or select the Grade (defaults to all).
- Enter or select Finish (defaults to all).
- Mill code (defaults to all).
- Indicate if you want to Show Price/Value on report (by default, this is not selected).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7L - Stock List by Bin Locations
This function produces an Inventory Stock List by Bin Location.
- Choose Inventory » Inventory Reports » Stock List by Bin Locations [IN7L].
- Enter or select Product code (defaults to all).
- Indicate if you want to show products with inventory On Hand . Enter "Y" for yes or blank for no.
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Line (defaults to all).
- Enter or select Spec Type (defaults to all).
- Enter or select Specification code (defaults to all).
- Select Bin From and To location; Kasto, Floor Stock (default), Quarantine Stock, Program Stock, Other, and enter or select From/To Warehouse Bin location (by default, all bin locations are selected).
- Indicate if you want to Show Zero logs (logs/products with zero quantity); by default, they are not shown.
- Indicate if you want to Show Value.
- Indicate if you want to sort by Product or by Bin location).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7M - Inventory Valuation
This function produces an Inventory Valuation report.
- Choose Inventory Control » Inventory Reports » Custom Reports » Inventory Valuation [IN7M].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Line (by default, all product lines are selected).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7N - Products with Negative Theoretical Weight
This function produces a report of selected products with Negative Theoretical Weight.
Products displayed on this report require immediate attention.
- Choose Inventory Control » Inventory Reports » Custom Reports » Products with Negative Theo Weight [IN7N].
- Enter or select Product Line code (by default, all are selected).
- Indicate if you want to include products that have been Deactivated.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7P - Products With Adders
This function produces a report of selected products with adders assigned.
- Choose Inventory Control » Inventory Reports » Custom Reports » Products With Adders [IN7P].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select a Product Line and Inventory Category (by default, all are selected).
- Indicate if you want to show products with inventory On Hand .
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
IN7Q - Zero Cost Logs
This function is used to create Zero Cost Logs report.
- Choose Inventory Control » Inventory Reports » Custom Reports » Zero Cost Logs [IN7Q].
- Indicate if you want to produce the report at the Log or Grade level.
- Enter or select Product code (by default, all are selected).
- Indicate if you want to show products with inventory On Hand .Leave default to show products, enter blank to hide them.
- Indicate if you want to Show Program (defaults to Y).
- Indicate if you want to show inventory in Quarantine.
- Indicate if you want to Show Zero logs (logs/products with zero quantity); by default, they are not shown.
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Line code (by default, all are selected).
- Enter or select Specification Type code (by default, all are selected).
- Enter or select Specification  code (by default, all are selected; if Specification Type = "ALL" this field is skipped).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7R - Inventory Log By Origin Type
This function produces a Inventory Log by origin type report.
- Choose Inventory Control » Inventory Reports » Custom Reports » Inventory Log By Origin Type [IN7R].
- Enter or select Type of Entry code.
- Enter or select Product code (defaults to all).
- Indicate if you want to show products with inventory On Hand .
- Indicate if you want to Show Program (defaults to Y).
- Indicate if you want to show inventory in Quarantine.
- Indicate if you want to Show Zero logs (logs/products with zero quantity); by default, they are not shown.
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Line code.
- Enter or select Specification Type code (defaults to all).
- Enter or select Specification  code (by default, all are selected; if Specification Type = "ALL" this field is skipped).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7S - Log Aging
This function produces a report to perform a price adjustment on product line(s).
This report is only available as an Excel download.
- Choose Inventory Control » Inventory Reports » Log Aging [IN7S].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select at least one Product Line.
- Press Enter to process the report.
IN7T - Inventory by Log Price
This function produces a report of selected products by log price range. Log price does not print on report.
- Choose Inventory Control » Inventory Reports » Custom Reports » Inventory by Log Price [IN7T].
- Enter or select Product code (by default, all are selected).
- Indicate if you want to show products with inventory On Hand .
- Indicate if you want to Show Program (defaults to Y).
- Indicate if you want to show inventory in Quarantine.
- Indicate if you want to Show Zero logs (logs/products with zero quantity); by default, they are not shown.
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Line code (by default, all are selected).
- Enter or select Specification Type code (by default, all are selected).
- Enter or select Specification code (by default, all are selected. If "ALL" is selected for Specification Type, then this field is skipped).
- Enter the starting Cost Price range (by default, zero cost is selected).
- Select whether to produce a Detailed or Summary report.
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
IN7U - Inventory Label By Bin Location
This function reprints log labels for all products within selected bin location(s), selected log number range. It requires a  installed on your network or attached to your computer.
- Choose Inventory Control » Inventory Reprints » Inventory Label By Bin Location [IN7U].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select Location Type: Kasto, Floor Stock (default), Quarantine Stock or Other.
- Enter or select the Bin Location (by default, all bin locations are selected).
- Enter the Minimum and Maximum  log numbers (by default, all numbers are selected).
- Indicate if you want to print logs with Available quantity only.
- Press Enter to process the report.
IN7V - Product Category Analysis
This function produces an Inventory report summarized by product category.
- Choose Inventory Control » Inventory Reports » Custom Reports » Product Category Analysis [IN7V].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Indicate if you want to include Alloy Surcharge in base price.
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
IN7W - Products By Category
This function produces a Products by Product Category report, sorted by product line.
- Choose Inventory Control » Inventory Reports » Custom Reports » Products By Category [IN7W].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Line code (defaults to all).
- Enter or select the Inventory Category (defaults to all).
- Indicate if you want to show products with inventory On Hand .
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.

IN7X - Excess and Overage
This function produces a product excess and overage report.
This report is only available as an Excel download.
- Choose Inventory Control » Inventory Reports » Excess and Overage [IN7X].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Select at least one Product Line.
- Enter or select End Day of Month date (this defaults to the last day of current month).
- Indicate if you want to Include Summary.
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
IN7YA - Chemical Properties by Heat
This function is used to display chemical properties by heat number.
This report is only available as an Excel download.
- Choose Inventory Control » Inventory Reports » Chemical Properties by Heat  [IN7YA].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Product code.
- Enter or select the Product Line code.
- Press Enter to process the report.
IN7YB - Stock List By Customer
This function creates a report to display log numbers assigned to customers. The Excel output includes log remarks.
- Choose Inventory Control » Inventory Reports » Stock List By Customer [IN7YB].
- Enter or select the Product code (by default, all are selected).
- Indicate if you want to show products with inventory On Hand .
- Indicate if you want to Show Program (defaults to Y).
- Indicate if you want to show inventory in Quarantine.
- Indicate if you want to Show Zero logs (logs/products with zero quantity); by default, they are not shown.
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Customer code (defaults to all).
- If the customer has multiple Ship To locations, select the one you want to report on.
- Enter or select Product Line and Spec Type (by default, all are selected).
- Enter or select Specification code; this defaults to "ALL" if the Spec Type = "ALL".
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
IN7YE - Log Split Report
This function is used to display log splits for a specified time period.
- Choose Inventory Control » Inventory Reports » Log Split Report [IN7YE].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the log split Document number(s) (by default, all are selected).
- If you did not select a specific Document number(s), enter the Date From and Date To(both default to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7YF - Inventory Classification Report #1
- Choose Inventory Control » Inventory Reports » Inventory Classification Report #1
or Purchasing » PO Reports » Inventory Classification Report [IN7YF].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7YG - Product Availability
This function is used to create an Inventory Stock list, showing available quantities.
- Choose Inventory Control » Inventory Reports » Product Availability [IN7YG].
- Leave default to report at Product level or select Log level or Grade level.
- Enter or select Product Code (by default, all products are selected). .
- Indicate if you want to show products with inventory On Hand .
- Indicate if you want to Show Program (defaults to Y).
- Indicate if you want to show inventory in Quarantine.
- Indicate if you want to Show Zero logs (logs/products with zero quantity); by default, they are not shown.
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Product Line.
- Enter or select Spec Type (defaults to all).
- Enter or select Specification code (defaults to all).
- Indicate if you want to Sort by Length (sort logs by their size description).
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
IN7YI - Customer Part Sales
- Choose Sales Order Entry » Order Entry Reports » Customer Part Sales [IN7YI].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Customer code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7YJ - Inventory Turns Report
- Choose Inventory Control » Inventory Reports » Inventory Turns Report [IN7YJ].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select at least one Product Line.
- Enter or select the Spec Type.
- Enter the number of Months Back to use in calculating report values.
- Indicate if you want to Show Inactivate accounts; leave blank to hide them.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7YK - ICC Report
This report is only available as an Excel download.
- Choose Purchasing » PO Reports » ICC Report [IN7YK].
- Enter or select Warehouse code (defaults to all warehouses).
- Press Enter to process the report.
IN7YL - Inventory Turns
This report is only available as an Excel download.
- Choose Inventory Control » Inventory Reports » Custom Reports » Inventory Turns Report [IN7YL].
- Enter or select at least one Warehouse.
- Enter or select the aging Date - this must be the last day of the month.
- Enter the number of Months Back to include in the Target % calculation.
- Enter or select Drop-In PO's.
- Press Enter to process the report.
IN7YM - Customer Material Adjustment
- Choose Inventory Control » Inventory Reprints » Customer Material Adjustment [IN7YM].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Type of Entry.
- Enter or select the Document No.
- Enter or select the Customer.
- Indicate if you want to Print Labels.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7YO - Actual and Replacement Cost Analysis
- Choose Inventory Control » Inventory Reports » Custom Reports » Actual & Replacement Cost Analysis [IN7YO].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Line code (defaults to all).
- Indicate if you want to Show Details.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7ZC - Product Usage And Incoming
This function displays product usages for last 12 months, 6 months and current available inventory as well as inbound details for product code.
- Choose Purchasing » PO Reports » Product Usage And Incoming  [IN7ZC].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product code (by default, all are selected).
- Enter or select Product Line code (by default, all are selected).
- In the Months USG 1 and Months USG 2 fields, enter the number of months back to get the first and second sets of monthly usage numbers.
- Enter or select Date To (by default, today's date is selected).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7ZG - Log Reservation Report
This function is to display log reservations by product or product line(s).
- Choose Inventory Control » Inventory Reports » Log Reservation Report [IN7ZG].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product code (by default, all are selected).
- Select the Log Types to display: Reserved logs, logs Not reserved, or  All.
- Enter or select the Product Line (by default, all are selected).
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
IN7ZH - Scrap Analysis by Date
This function is used to create an Inventory Scrap Report for a specified date range.
- Choose Inventory Control » Inventory Reports Inventory » Scrap Analysis by Date [IN7ZH].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select a Product Line (by default, all are selected).
- Enter the Scrap Type to filter report by; Order, Zero, Track, Revalue, Undefined, All (default).
- Indicate if you want to show products in the Scrap Bin only.
- Enter or select the Date From and Date To (both default to today's date).
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
IN7ZI - Inventory Sales Usage Report
This report shows inventory stock usage (including open sales orders), by product code, displaying last 12 months of sales history.
- Choose Purchasing » PO Reports » Inventory Sales Usage Report [IN7ZI].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Product Line.
- Optionally, further refine the report by entering the Grade, STD or Finish (or select "ALL"), or the Diameter or Length.
- Enter the Date the report should include data up to; it will include open work orders and invoices 12 months prior to this date.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
IN7ZW - Weighted Average Receipts
This function produces a Weighted Average Receipt report.
- Choose Inventory Control » Inventory Reports » Custom Reports » Weighted Average Receipts [IN7ZW].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select a Product Line (by default, no product line is selected).
- Enter or select Date From and Date To (by default, Date From is 01/01/01 and Date To is today's date).
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
IN7ZY - Inventory Restocking By Piece
This function is used to create an inventory restocking report displaying on-hand piece inventory. Summarizes product totals regardless of specification.
- Choose Inventory Control » Inventory Reports » Custom Reports » Inventory Restocking By Piece [IN7ZY].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Line code (defaults to all).
- Indicate if you want to include Insufficient Only.
- Indicate if you want to include  Bundles.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE71 - Sales Quotation
This function reprints/fax/emails a sales quotation. MTRs may be included with an emailed quote1.
- Choose Sales Order Entry » Order Entry Reprints » Sales Quotation [OE71].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Document number for the quote you want to reprint (quote document numbers always begin with a "Q").
- Indicate if you want to Include Pricing Factors.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
Configuration
1 SWTMNT > Email MTRs with Quote
OE72A - Picklist Reprint by Manifest Run
This function reprints pick slips for a manifest run by sales order and bin location.
- Choose Sales Order Entry » Order Entry Reprints » Picklist Reprint by Manifest Run [OE72A].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select the Manifest and Run ID.
- If you want to print by machine, select the check box and select a machine or leave "ALL" machines.
- If you want to print by bin location, select the check box and select a bin or leave "ALL" bins.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE72B - Master Picklist Reprint
This function reprints pick slips for all open sales order lines in PCK or PBP status that have the selected delivery date. Pick slips will print by sales order number.
- Choose Sales Order Entry » Order Entry Reprints » Master Picklist Reprint [OE72B].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Document Number you want to reprint the pick lists for, or enter "ALL".
- Enter or select the Delivery Date for which you want to reprint pick lists.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE72 - Picklist
This function reprints/fax/emails a picklist for a branch transfer. “**REPRINT** will print below the document number. You will not be able to reprint a picklist from a document that has a status of Closed. You can reprint a picklist for orders with a status of PCB, but only lines with a status of PCK will print.
Operator security controls access to this function; contact  for assistance.
- Choose Sales Order Entry » Order Entry Reprints » Picklist [OE72].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Type of Entry: branch transfer (BT), processing purchase order (PP), production order (PR), or sales order (SO).
- Enter or select the Document Number you want to reprint the picklist for.
- If you do not want to include all line items, press F4 on Filter Lines to indicate the lines you want to Select or Deselect.
- If a machine was specified for each line in the order, you can choose to Print by Machine and select the Machine(s) to print.
- If logs were selected for line items in the order and the logs were assigned to a bin location, you can choose to Print by Bin Loc and select the Bin Location(s) to print.
- Indicate if you want to Print Product Images for any products that have an image attached to the product code.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
If circulating the reprint, be sure to destroy previously-printed documents for same document number.
OE73 - Delivery Note
This function reprints/faxes/emails a delivery note. “**REPRINT** will print below the document number. You will not be able to reprint delivery notes with a status of Closed.
- Choose Sales Order Entry » Order Entry Reprints » Delivery Note [OE73].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select the Type Of Entryand enter or select the Document number you want to reprint.
- Indicate if a mill report (material test report/MTR) is required: Yes (include the original MTR), Overlayed (include the original with company header overlaid), Sys (system-generated MTR from company, not mill), Both (original and system-generated), or blank for no. See also MTR Delivery Options.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE74 - Invoice Summary By Document
This function produces a report containing sales value, inventory quantity and gross margin percentage for each product line by customer within a given date range.
For a detailed breakdown by tax code see the OE7XI - Invoice/Credit Summary (Tax Breakdown) report.
- Choose Sales Order Entry » Order Entry Reports » Invoice Summary By Document [OE74].
- Enter or select Warehouse code (defaults to the warehouse assigned to you), including type (Inventory or Sales warehouse, and enter "C" if you want to include child warehouses.
- Enter or select the Territory code (defaults to all).
- Enter or select the Type of Entry to report on: CM = credit memo, DM = debit memo, IV = invoice, defaults to all.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if you want to sort documents by Salesperson or Order Writer.
- Indicate if you want to sort the report by: Document Number, Date, Operator, or View detail Lines.
- Enter "Y" if you want credit and debit notes to reference the corresponding invoice date, otherwise enter "N".
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE75 - Invoice/Credit or Debit Note
This function is used to reprint/fax/email a credit or debit memo.
- Choose Sales Order Entry » Order Entry Reprints » Invoice/Credit or Debit Note [OE75].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select the Type of Entry, then enter or select a Single Document number or use the Multiple Document field to select more than one document.
- Indicate if you want to Include POD (proof of delivery1) in a separate PDF from the invoice.
- Indicate if you want to include a "Reprint" watermark on the reprint.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
Configuration
1 PODs must be scanned and stored in a network folder, similar to MTRs; the POD folder address is defined in IN19.
OE76 - Credit/Debit Memo Authorization
This function is used to reprint a credit or debit memo authorization, and is valid only if Credit/Debit memo authorization is required.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Misc Reports » Credit/Debit Memo Authorization [OE76].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select the Type of Entry, then enter or select the Document number.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE77 - Sales Order/Quote Report
This report lists sales orders and/or quotes.
- Choose Sales Order Entry » Order Entry Reports » Sales Order/Quote Report [OE77].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Select the Order Types to include on the report:  Sales orders (default), Quotes, or All.
- Select which order statuses to include:  Open, Released, Shipped, or All orders.
- Specify how to group data: by order Writer, Salesperson, or Invoice number.
- Indicate if you want to Group by Currency on the orders.
- In the Operator field, select a salesperson to report on, or leave "ALL". If you did not select "ALL" you can select Additional Operators.
- Indicate whether you want to view data for the Customer Salesperson (on the customer file); or leave blank to reference the salesperson on the invoice.
- Indicate if the report should use the Order date or the Expected Ship date.
- Enter or select a Customer (by default, all are selected).
- Indicate if credit and debit notes should reference their corresponding invoice date, and if invoices should reference the sales order date.
- Indicate if invoices should reference the sales order date (i.e. only show orders generated in the specified date range).
- Indicate if you want to only include sales adjustments in extras for margin calculation.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if you want to only generate a Summary report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE79 - Sales by Customer by Month
This function generates a report containing monthly invoiced sales and gross margin percent by customer, reporting on a rolling 12-month period.
- Choose Sales Order Entry » Order Entry Reports » Sales by Customer by Month [OE79].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select End Date Of Month (by default, last day of current month is selected).
- Enter or select Customer Start Date (customers with a start date after this date will be included).
- Select whether to produce a Detailed or Summary report.
- Enter or select the Territory code (defaults to all).
- Enter or select a State/Province code (by default, all are selected).
- Indicate how you want to create the report by: Salesperson, Outside salesperson, or Order Writer.
- Enter or select an Operator code (by default, all are selected).
- Indicate if you want to use the Customer Salesperson or leave blank to use the salesperson on the invoices.
- Indicate if you want the report to be Group by Operator.
- Indicate how you want to Sort the data: by Customer name, Descending Sales, or Postal/zip code.
- Indicate if you want to include customers with Zero Sales in the past year.
- Indicate if you want to Show Details of the customers (postal code, phone #, contact, etc.).
- Indicate if you want to Include Inactive customers.
- Indicate if you want to include orders based on Avg Cost, or leave blank to include profit orders based on actual cost.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7AA - Sales & Profits By Salesperson Summary
This function produces a report showing sales and profits by salespeople, for customers. It will also print sales to customers with no Inside/Outside salesperson assigned.
If you want to run a report with a From/To date range, use .
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Misc Reports » Sales & Profits By Salesprsn Summary [OE7AA].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Indicate whether to group report by Inside salesperson, Outside salesperson or order Writer.
- Enter or select a Salesperson code (defaults to all).
- Enter or select the Date to which information will be included in the report (defaults to today’s date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7AB - Sales and Profits By Salesperson Summary
This report shows sales and profits by salespeople, allowing for input of From/To Date range for customers.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Sales and Profits By Slsprsn Summ [OE7AB].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Indicate whether to group the report by Inside or Outside salesperson.
- In the Customer Salesperson field, enter "Y" to use the salesperson on the customer file, or leave blank to use the salesperson on the invoices.
- Enter or select a Salesperson or "ALL".
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7AC - By Product Within Dimension Range
- Choose Sales Order Entry » Order Entry Reports » By Product Within Dimension Range [OE7AC].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Line code.
- Enter or select the specifications and dimensions to limit the report to; these vary depending on the product line selected.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if you want a Detailed report or leave blank for a summary.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7AE - Return Slip
- Choose Sales Order Entry » Order Entry Reprints » Return Slip [OE7AE].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select the Type of Entry ("CM" or "DM").
- Enter or select the Document you want to print a return slip for.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7A - Sales By Salesperson By Customer By Product Line
This report includes the invoiced sales value, weight quantity and gross margin percentage for each product line by customer, within a given date range.
- Choose Sales Order Entry » Order Entry Reports » Sales By Salespsn By Cust By Pline [OE7A].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Indicate if you want to sort data by Operator (default) or Territory.
- If Sort Order="O", select if the report should then be grouped by Salesperson or Order Writer. 
If Sort Order="T", select the Territories to be included (in the window, indicate if you are Selecting or Deselecting territories.
- Specify to create the report by Salesperson or Order Writer.
- Enter or select Operator code (defaults to all).
- Enter or select Customer number (defaults to all).
- Enter or select Product Line code (defaults to all).
- Enter the Dimension you want to report on.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if credit and debit memos should be referenced using the corresponding invoice date instead of credit/debit memo date.
- Specify whether to create a Summary or Detailed (default) report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7BA - Proforma Invoice
This invoice may be printed automatically if a pre-invoice is required in the customer file, or if credit terms require it for COD orders.
- Choose Sales Order Entry » Order Entry Reprints » Proforma Invoice [OE7BA].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Document you want to reprint.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7B - Sales Order
This function reprints/fax/emails a branch transfer (BT), processing purchase order (PP), production order (PR), or sales order (SO).
If you have alternate headings , use OE7BB instead to reprint the sales order; OE7BB is the same as OE7B but includes an additional field to select the alternate heading to use.
- Choose Sales Order Entry » Order Entry Reprints » Sales Order [OE7B].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- The Entry Type defaults to SO, but you can change this if required to branch transfer (BT), processing purchase order (PP), or production order (PR.
- Enter or select the Document you want to reprint (the list is filtered according to the Entry Type selected).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7C - Sales Journal Reprint
This function is used to reprint a part of the sales journal.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Misc Reports » Sales Journal Reprint [OE7C].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7DA - By Product Within Date Range
This function produces a report which displays the total weight, inventory, quantity, pieces, cost value, sales value, margin and gross margin percentage for all sales within a specified date range, broken down by product. This report totals product line, warehouse and provides grand totals for all numerical columns.
- Choose Sales Order Entry » Order Entry Reports » By Product Within Date Range [OE7DA].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Product Line.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate how you want to Sort the data: by product Description or Quantity sold.
- Indicate if you want to Group the data by product line.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7D - By Product Line By Grade By Salesperson
This report displays the total inventory quantity, weight , sales value and gross margin percentage for all sales of products with a given specification type and specification, within a specified date range. Report totals by salesperson, specification, product line, warehouse and grand totals.
- Choose Sales Order Entry » Order Entry Reports » By Pline By Grade By Salesperson [OE7D].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Product Line.
- Enter or select the Salesperson (defaults to all).
- Enter or select the Specification Type (defaults to GRD = Grade).
- Enter or select a Specification code (defaults to "ALL").
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if credit and debit memos should be referenced using the corresponding invoice date instead of credit/debit memo date.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7F - Invoice - No Warehouse Input
This function reprints/faxes/emails a range of invoices.
- Choose Sales Order Entry » Order Entry Reprints » Invoice - No Warehouse Input [OE7F].
- Select the Type of Entry: BI=branch invoice, BT=branch transfer, CM=credit memo, DM=debit memo, IV=sales invoice, TO=inventory transfer out.
- Select the range of Document numbers to print.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7G - Open Order Report
This function produces a report listing all open Work Orders and remaining quantities to be shipped.
- Choose Sales Order Entry » Order Entry Reports » Open Order Report [OE7G].
- Enter or select the Warehouse code and the warehouse type (Inventory or Sales).
- Enter or select the Territory code (defaults to all).
- Enter or select the Customer code (defaults to all).
- Enter the Document Status to include (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if the date range should be based on the Order date or the Requested date.
- Indicate if the report should be Sorted by Product, Work Order by Salesperson, Request Date, or Customer.
- Select one or more Salesperson and enter the salesperson type (Inside or Outside).
- Enter or select a Product Line (by default, all are selected).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.

OE7H - Daily Booking Summary Report
- Choose Sales Order Entry » Order Entry Reports » Daily Booking Summary [OE7HA].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7I - Invoice Summary By Day
This report generates a daily summary of all work orders which have been shipping confirmed within a given date range.
- Choose Sales Order Entry » Order Entry Reports » Invoice Summary By Day [OE7I].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Product Line Group (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7K - Daily Sales Report
This function generates and emails a daily sales report.
- Choose Sales Order Entry » Order Entry Reports » Daily Sales Report [OE7K].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select Date.
- Specify the invoice types to run report for: SHP = all shipped but not invoiced, UPD = Invoiced sales by not yet paid, or ALL. 
When you press Enter the report will be generated and emailed.
OE7R - Commission Report #1
This function is used to print an Inside Salesperson commission report. It will only list invoices paid within a date range, and reflects the Commission Rate assigned to the Inside Salesperson in screen OE13 .
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Misc Reports » Commission Report #1 [OE7R].
- Enter or select a Salesperson code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7S - Sales Journal GL Summary Reprint
This function is used to reprint a part of the General Ledger Sales Journal Summary.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Misc Reports » Sales Journal GL Summary Reprint [OE7S].
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7U - Gross Profit Report
This function produces a gross profit report based on warehouse and salesperson for a given time frame. The report displays processing cots, unit costs, extended costs, freight costs, unit sales values, extended sales values, margin and margin percentage on a document-to-document basis, and includes totals by salesperson, warehouse and grand total.
- Choose Sales Order Entry » Order Entry Reports » Gross Profit Report [OE7U].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select Salesperson code(defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7V - Commission Report #2
This function prints an Inside salesperson commission report for invoices paid within a date range for those invoices processed on screen OE4D .
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Misc Reports » Commission Report #2 [OE7V].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter or select a Salesperson code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7W - Late Sales Order Report
This function generates a report listing all late (requested date to ship is prior to today's date) sales orders by customers.
- Choose Sales Order Entry » Order Entry Reports » Late Sales Order Report [OE7W].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select a Customer code (by default, all are selected).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Type the minimum number of Days Late an order must be to be included.
- Indicate if you want the report to be Sorted by Customer.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7XB - Outside Salesperson Commission
This function is used to print an outside salesperson commission report for invoices paid within a date range for those invoices processed on screen OE4J.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Misc Reports » Outside Salesperson Commission [OE7XB].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter or select Salesperson code (defaults to all).
- Indicate if you want to use the salesperson on the customer file; leave blank to use the salesperson on the invoices.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7XC - Machine Profitability Report v1
- Choose In-House Production » In-House Production Reports » Machine Profitability Report v1 [OE7XC].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select a Machine code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7XD - Log Reservations By Work Order
This function generates a report listing open sales orders including product codes (displaying log detail), sorted by customer.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Log Reservations By Workorder [OE7XD].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Product code and Product Line code (default to all).
- Enter or select Customer number (defaults to all).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7XF - Creating a Sales Tax Report
This function produces a report of taxable and non-taxable invoices, sorted by Tax code, within a date range.
- Choose Accounts Receivable » AR Report » Sales Tax Report [OE7XF].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select Tax code (defaults to all).
- Select whether to filter by T = taxable, E = tax exempt, B = both.
- Enter or select Type of Entry code.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select whether to produce a Detailed or Summary report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7XG - Additional Revenue Analysis Report
This function produces a report of taxable and non-taxable invoices, sorted by tax code, within a date range.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Additional Revenue Analysis Report [OE7XG].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select a Sales Cost code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7XH - Quote Summary By Salesperson
This function prints a summary report listing quotes by Inside/Outside Salesperson code.
- Choose Sales Order Entry » Order Entry Reports » Quote Summary Report By Salesperson [OE7XH].
- Enter or select the Warehouse code and the warehouse type (Inventory or Sales).
- Enter or select the Customer code (defaults to all).
- Select one or more Salesperson and enter the salesperson type (Inside or Outside).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7XI - Invoice/Credit Summary (Tax Breakdown)
This function prints a summary report of taxable and non-taxable invoices, listing tax codes, within a date range.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Invoice/Credit Summary (Tax Brk) [OE7XI].
- Enter or select Warehouse code (defaults to the warehouse assigned to you), including type (Inventory or Sales warehouse, and enter "C" if you want to include child warehouses.
- Enter or select the Territory code (defaults to all).
- Enter or select the Type of Entry to report on: CM = credit memo, DM = debit memo, IV = invoice, defaults to all.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate the Invoice Types you want to run the report for: SHP = all shipped but not invoiced, UPD = invoiced sales but not yet paid (default), ALL = all invoices.
- Indicate if you want to sort documents by Salesperson or Order Writer.
- Enter "Y" if you want credit and debit notes to reference the corresponding invoice date, otherwise enter "N".
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7XJ - Inventory Classification Report #2
- Choose Sales Order Entry » Order Entry Reports » Inventory Classification Report #2 [OE7XJ].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Select at least one Product Line.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how you want the report to Sort By: ICC, Product, Weight, Value, Margin, GM%, Onhand, Group 1-2-3, or Total number of transaction.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7XL - Monthly By Day Invoicing Summary
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Misc Reports » Monthly By Day Invoicing Summary [OE7XL].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- In the Sales Adj field, if you want to only include sales adjustments in extras for margin calculation, enter "Y"; otherwise leave blank.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7XM - Machine Profitability Report v2
- Choose In-House Production » In-House Production Reports » Machine Profitability Report v2 [OE7XM].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select a Machine code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select whether to produce a Detailed or Summary report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7XN - Monthly Sales By Product Summary
- Choose Sales Order Entry » Order Entry Reports » Monthly Sales By Product Summary [OE7XN].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Product code you want to report on.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7XP - Output Delivery Note Logs To Excel
- Choose Sales Order Entry » Order Entry Reprints » Output Delivery Note Logs To Excel [OE7XP].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Type of Entry to include.
- Enter or select the Document number.
- Enter "Y" in OK to generate; the report opens in Excel.
OE7XQ - Pre-Invoice Report
- Choose Sales Order Entry » Order Entry Reports » Pre-Invoice Report [OE7XQ].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Salesperson code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Enter the document Status to include: PRT, INV, END or ALL.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7XR - Invoices With No POD Attachment
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Misc Reports » Invoices With No POD Attachment [OE7XR].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Customer code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7XS - Sales By Territory
This report is only available as an Excel download.
- Choose Sales Order Entry » Order Entry Reports » Sales By Territory [OE7XS].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter Date To (defaults to today's date). When you press Enter, the report is generated and opens in Excel.
OE7XT - Customer Part Shipping Label
This function is used with custom-generated shipping labels. If you plan to use this function, please contact  to discuss your custom label requirements.
- Choose Sales Order Entry » Order Entry Reprints » Customer Part Shipping Label [OE7XT].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Type of Entry, Document and  Line.
- If the label settings1 for this label is greater than 1, enter the Quantity to print.
- Enter the number of Labels to reprint.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
Configuration
[IN19] > Label Options > Label Printer Defaults > SL04 > Num
OE7X - Sales By Customer By Product Line
This function produces a report containing sales value, weight quantity and gross margin percentage for each product line by customer within a given date range.
- Choose Sales Order Entry » Order Entry Reports » Sales By Customer By Product Line [OE7X].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select a Customer code (by default, all are selected).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if you want to include Customer Groups, Product Line Details and Surcharges.
- Indicate how the data should be Sorted: Alphabetically, lowest to highest sales Value, lowest to highest Weight, or lowest to highest Gross margin.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YA - Shipping Label
This function is used to reprint shipping labels for invoices, branch transfers or outside processing orders.
- Choose Sales Order Entry » Order Entry Reprints » Shipping Label [OE7YA].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Type of Entry, then the Document number.
- Enter "Y" in OK to print the label.
OE7YB - Salesperson Productivity Report
- Choose Sales Order Entry » Order Entry Reports » Salesperson Productivity Report [OE7YB].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select one or more Salesperson and enter the salesperson type (Inside or Outside).
- Enter or select the Territory code (defaults to all).
- Enter or select the Date.
- Indicate if you want to Show salespeople with zero sales/quotes.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YC - Credit / Debit Note Reason
This report displays credit/debit notes sorted by the reasons they were generated.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Misc Reports » Credit/Debit Note Reason [OE7YC].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter the Type of Entry: CM = credit notes only, DM = debit notes only, or ALL.
- Enter or select the Reason code (defaults to all).
- Enter or select the Customer (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Enter or select the Document Status: SHP = shipped, not yet invoiced, UPD = invoiced (default) or ALL.
- Enter or select the Operator (defaults to all).
- Indicate if you want to sort the report by Salesperson or order Writer.
- Indicate if you want to Use Avg Cost; leave blank to use actual cost.
- Indicate if you want to only print a Summary version of the report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YD - Customer Backorder
This report shows backorders by customer.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Misc Reports » Customer Backorder [OE7YD].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Customer code (defaults to all).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YE - Sales By Customer By Product
This function produces a report which displays sales grouped by customer and product year-to-date for current fiscal year.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Misc Reports » Sales By Customer By Product [OE7YE].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Customer code (defaults to all).
- Enter or select the Product Line.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YF - Open Order Credit Caution
This function produces a credit caution report for open orders.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Open Order Credit Caution [OE7YF].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Indicate how many Aging Days must be outstanding for invoices to be included (must be greater than zero).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YG - Sales By Cust By Product Line Two Year Usage
This function generates a report which displays sales grouped by customer and product line for two years.
- Choose Sales Order Entry » Order Entry Reports » Sales By Cust By Pline Two Year Usage [OE7YG].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select End Day of Month (defaults to last day of current month).
- Enter or select a Customer (defaults to all).
- Select one or more Salesperson and enter the salesperson type (Inside or Outside).
- Select one or more Product Line.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YH - Sales By Salesperson By Customer
This report shows sales by customer or by salesperson.
- Choose Sales Order Entry » Order Entry Reports » Sales By Salesperson By Customer [OE7YH].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Customer code (defaults to all).
- Enter or select the Territory code (defaults to all).
- Indicate if you want to only show customers with activity in the specified date range.
- Enter or select Salesperson and filter by salesperson type: Inside, Outside, Order Writer. Indicate if the salesperson source is Customer or Order.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select if you want the report to Sort By sales Value or gross Margin.
- If you selected "ALL" in the Salesperson field, indicate if the report should Group All Salespeople. If selected, all data will be consolidated under one salesperson heading.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YJ - Sales By Customer By Product
This function produces a report which displays sales grouped by customer and product.
- Choose Sales Order Entry » Order Entry Reports » Sales By Customer By Product [OE7YJ].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Customer code (defaults to all).
- Enter or select Product Code (by default, all products are selected).
- Enter or select the Product Line.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YK - Customers With No Sales - 3 & 6 Month
This function produces a report which displays customers with no (zero) sales for a given period, grouped by salesperson.
- Choose Sales Order Entry » Order Entry Reports » Customers With No Sales - 3 & 6 Mt [OE7YK].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter or select Salesperson code (defaults to all).
- Enter or select Start Date and End Date (defaults to today's date).
- Indicate if you want to Show Inactive customers.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YL - Sales By Salesperson By Customer 2
This report shows a two-year comparison of sales by customer by salesperson.
- Choose Sales Order Entry » Order Entry Reports » Sales By Salesperson By Customer 2 [OE7YL].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Customer code (defaults to all).
- Indicate if you only want to show customers with activity in the specified date range.
- Select one or more Salesperson and enter the salesperson type (Inside or Outside).
- Enter the Date To (defaults to today's date).
- Select if you want the report to Sort By sales Value or gross Margin, and indicate if it should also Sort By Salesperson.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YM - Order Extras Summary
This report lists all order extras. The report displays month-to-date and year-to-date sales for each cost code as well as the general ledger account associated with cost code.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Order Extras Summary [OE7YM].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Extras Code you want to report on (defaults to all).
- Enter or select the End Date for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YN - Customer Classification By Sale
This report lists all open sales orders and the remaining quantities to be shipped, by order writer.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Customer Classification By Sales [OE7YN].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Select the Salesperson Type (Inside, Outside, or order Writer), then enter or select the Salesperson (defaults to all).
- Enter or select a customer Classification (defaults to all).
- Enter the To Date (defaults to today’s date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YO - Sales Analysis by Product Line Group
This report lists Year Sales analysis by product line groups. Data will only include "I" lines on invoice details.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Sales Analysis by Prod Line Group [OE7YO].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select Product Line (defaults to all).
- Enter the Year you want to report on.
- Select whether to produce a Detailed or Summary report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
Configuration
Product line groups are maintained in IN1Q and assigned to a product line in .
OE7YP - Pre-Invoice
- Choose Sales Order Entry » Order Entry Reprints » Pre-Invoice [OE7YP].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Document you want to reprint.
- Optionally select an Alternate Heading.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YQ - Sales By Product Line By Vendor
This report lists sales by product line by vendor.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Sales By Product Line By Vendor [OE7YQ].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Vendor code.
- Enter or select Product Line (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YR - MTR by Customer PO/SO/Invoice
This function is used to reprint/fax/email the MTRs for a given customer purchase order.
- Choose Sales Order Entry » Order Entry Reprints » MTR by Cust PO/SO/Invoice [OE7YR].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Customer code (defaults to all).
- If you selected a Customer:
  - Enter the PO Number.
  - Select the Sales Order number associated with the PO.
  - Select the Invoice Number associated with the selected Sales Order.
If you did not select a Customer, you must manually enter a Sales Order number and an Invoice Number.
You do not have to enter preceding alpha or leading zeros for the Sales Order or Invoice Number fields.
- Indicate the MTR Type required: Yes (include the original MTR), Overlayed (include the original with company header overlaid), Sys (system-generated MTR from company, not mill), or Both (original and system-generated).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YT - Lost Quote Reason Report
This function prints a report listing quotes by Lost Quote Reason code.
- Choose Sales Order Entry » Order Entry Reports » Lost Quote Reason Report [OE7YT].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Customer code (defaults to all).
- Enter or select Salesperson code (defaults to all).
- Indicate if you want to Group by Operator code. If you leave this blank, the report will be sorted by quote reason.
- Indicate if you want to Show Remarks.
- Enter or select the Reason Code to report on (by default, all are selected).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YU - Sales By Customer By Order Writer Year Comparison
This report lists sales by customer by order writer, comparing total sales for the entire previous fiscal year against total sales of the date range entered.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Sales By Cust By Ord Wrt Year Comp [OE7YU].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Customer code (defaults to all).
- Enter or select the Order Writer (defaults to all).
- Enter or select the Territory code (defaults to all).
- Enter or select a Date From and Date To (defaults to first day of current fiscal year).
- Indicate if you want to Include Inactive customers (only enabled if "ALL" customers and "ALL" Order Writers are selected.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YX - Summary Open Order Report
This function generates a report listing open sales orders, and inventory lines on the sales orders.
- Choose Sales Order Entry » Order Entry Reports » Summary Open Order Report [OE7YX].
- Enter or select Warehouse code (defaults to all warehouses).
- Enter or select a product line group Pln Group (defaults to all).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YY - MTR By Delivery Note
- Choose Sales Order Entry » Order Entry Reprints » MTR By Delivery Note [OE7YY].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select theType of Entry, then enter or select the Document.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7YZ - Detailed Open Order By Customer
This function generates a report listing open orders sorted by customer.
- Choose Sales Order Entry » Order Entry Reports » Detailed Open Order By Customer  [OE7YZ].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Territory code (defaults to all).
- Enter or select the Customer code (defaults to all).
- Select the Order status to view: ASG (not processed), PCK (picking confirmation), CRD (work order on credit hold) or All.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if Date Range should be based on the Ordered date or the Requested date.
- Enter or select a Product Line (defaults to all).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7Y - By Territory By Product Line
This function produces a sales report based on warehouse, territory, and product line for a given time frame. The report displays total weight, cost value, sales value, extras, total value and margin % for each product line broken down by territory, including credit/debit notes, and is totalled by territory and warehouse.
- Choose Sales Order Entry » Order Entry Reports » By Territory By Product Line [OE7Y].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Territory code (defaults to all).
- Enter or select the Product Line.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select whether to produce a Detailed or Summary report or Both.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZA - By Product Line By Grade
This report displays the total inventory quantity, weight, cost value, sales value, margin and gross margin percentage for all sales within a specified date range, broken down by grade and totaled by product line, warehouse and grand total.
- Choose Sales Order Entry » Order Entry Reports » By Product Line By Grade [OE7ZA].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Product Line.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if credit and debit memos should be referenced using the corresponding invoice date instead of credit/debit memo date.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZB - Sales Tax
**This function generates two reports**: one displays sales tax liabilities, the second displays tax adjustments.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Sales Tax  [OE7ZB].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Salesperson code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZC - Customer Salesman Analysis
This report displays customer sales by salesperson within a date range.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Misc Reports » Customer Salesman Analysis [OE7ZC].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Customer code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if you want to generate a Detailed report (leave blank for a summary).
- Indicate if you want to Include Credits/Debits notes in the report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZD - Used vs Picked Quantity
This report compares used and picked quantities.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Misc Reports » Used vs Picked Quantity  [OE7ZD].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Enter the acceptable Variance as a percentage (can include up to two decimal places; e.g. 10.25% would be entered as 10.25).
- Enter the Document Status to report on: PRT = packing slip created, INV = invoiced, END = invoice posted, SHP = order shipped, POS = POS order, or ALL.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZE - By Product Line By Month
This report displays the monthly sales by product line.
- Choose Sales Order Entry » Order Entry Reports » By Product Line By Month [OE7ZE].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the End Day of Month (defaults to last day of current month) - the report will display invoiced sales information for the 12 months ending with this date.
- Enter or select the Territory code (defaults to all).
- Enter or select Product Lines (defaults to all).
- Indicate whether to Group by Operator according to the selected Operator Type (Salesperson, Outside salesperson, or order Writer).
- Indicate whether to use the Customer Salesperson, or leave blank to use the salesperson on the invoices.
- Specify to Sort data by Product line or Ascending sales.
- Indicate whether to include product lines with Zero Sales.
- Select whether to produce a Detailed or Summary report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZF - Inventory Classification Report
This report displays the monthly sales by product line.
Due to the size of the report, the Inventory Classification Code is only displayed in Excel output, regardless of the sort option selected.
- Choose Sales Order Entry » Order Entry Reports » Inventory Classification Report [OE7ZF].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select Product Line.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Specify how to sort the data: Product, Inventory classification code, Weight, Value, Margin, GM%, On Hand Quantity, 1 = number if 1 - 999 lb transactions, 2 = 1000 - 2500 lb transactions, 3= 2501+ lb transactions, or total number of Transactions.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZG - Order Entry Forms
This function is used to reprint/fax/email an order entry form. The number of copies/printer/tray are the same as when processing an original sales order.
- Choose Sales Order Entry » Order Entry Reprints » Order Entry Forms  [OE7ZG].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select a Document number to reprint.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZH - Sales Order Report By Date
The function produces a report listing all sales orders.
- Choose Sales Order Entry » Order Entry Reports » Sales Order Report By Date [OE7ZH].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select Salesperson code (by default, all are selected).
- Specify how to Sort the data: Customer, Document Date, Order Date, or Required date (default).
- Indicate if you want to Group By Operator, or leave blank to group by salesperson.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZJ - Shipped Orders Not Yet Invoiced
This function produces a report listing all sales orders which have been shipped (scanned) but not yet invoiced (used with barcode scanning).
- Choose Sales Order Entry » Order Entry Reports » Shipped Orders Not Yet Invoiced [OE7ZJ].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select Salesperson (by default, all salespeople are chosen).
- Indicate if the report should Sort By  Shipped Date or Order Date.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZK - Monthly Sales By Customer By Postal
This report displays monthly sales and gross margin percentage by customer.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Monthly Sales By Customer By Postal [OE7ZK].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the End Day of Month (defaults to last day of current month) - the report will display invoiced sales information for the 12 months ending with this date.
- Enter or select a Customer Start Date (customers with a start date after this date will be included) or leave blank to include all customers.
- Select whether to produce a Detailed or Summary report.
- Enter or select the Territory code (defaults to all). If a territory is selected, Province and Operator fields will default to ALL.
- Enter or select a State/Province (defaults to all). If a province/state is selected, Territory and Operator fields will default to ALL.
- Indicate whether to create report by Salesperson, Outside salesperson, or order Writer.
- Enter or select an Operator (defaults to all).
- Indicate whether you want to view data for the Customer Salesperson (on the customer file); or leave blank to reference the salesperson on the invoice.
- Indicate if you want to Group by Operator.
- Specify whether to sort the data by Customer name, descending Sales, or Postal/zip code.
- Specify whether to show the Bill to or Ship to address.
- Indicate if you want to include customers with Zero Sales in the specified time period.
- Indicate if you want to Show Details for each customer (contact, phone #, postal code, etc.).
- Indicate if you want to Include Inactive customers (zero sales transactions in the past year).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZL - Invoice Cost Analysis
This function generates an Excel file that provides invoice costs for a date range.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Invoice Cost Analysis [OE7ZL].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Type of Entry: CM = credit memo, DM = debit memo, IV = invoice, or ALL.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
When you press Enter, the report is generated and opens in Excel.
OE7ZM - Yearly Sales By Customer
This report generates a report containing yearly sales and gross margin percent by customer on a rolling 12-year period.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Years Sales By Customer [OE7ZM].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select Customer Start Date (customers with a start date after this date will be included).
- Select whether to produce a Detailed or Summary report.
- Enter or select a Territory code (by default, if "ALL" is selected the Province/State and Operator fields will default to "ALL").
- Enter or select a Province/State (by default, all are selected).
- Indicate how you want to create the report by: Salesperson, Outside salesperson, or Order Writer.
- Enter or select an Operator code (by default, all are selected).
- Indicate if you want to use the Customer Salesperson or leave blank to use the salesperson on the invoices.
- Indicate if you want the report to be Group by Operator.
- Indicate how you want to Sort the data: by Customer name, Descending Sales, or Postal/zip code.
- Indicate if you want to include customers with Zero Sales in the past year.
- Indicate if you want to Show Details of the customers (postal code, phone #, contact, etc.).
- Indicate if you want to Include Inactive customers.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZN - Invoice Costs
This report displays invoice costs for a date range.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Invoice Costs [OE7ZN].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select a Salesperson (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZO - Product Line Sales/Receiving
This report displays product line sales and receipts for a date range.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Product Line Sales/Receiving [OE7ZO].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select whether to produce a Detailed or Summary report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZP - Invoice Header Costs
This report displays invoice and debit/credit memo header costs for a date range.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Invoice Header Costs [OE7ZP].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Type of Entry(CM = credit memo, DM = debit memo, IV = sales invoice, or ALL), then enter or select the Document Number. If Type of Entry ="ALL", then Document Number defaults to ALL).
- Enter or select a Salesperson (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if you want to Display Logs.
- Indicate which costing method to use for report: System, AVerage, or Actual method.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZQ - Quote to Order Ratio
This function prints a report comparing quoted quantities and ordered quantities.
- Choose Sales Order Entry » Order Entry Reports » Quote to Order Ratio [OE7ZQ].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Customer code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZR - Bill of Lading
This function is used to reprint/fax/email a Bill of Lading.
- Choose Sales Order Entry » Order Entry Reprints » Bill of Lading [OE7ZR].
- Select the Type of Entry (IV = Sales Invoice (display only), BI = Branch Invoice, or CI = Consignment Invoice), then enter or select the Document number.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZS - Monthly Sales By Customer Summary
This function produces a report containing monthly weight, sales, margin and gross margin percent by customer for the past two years (current and previous calendar year).
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Monthly Sales By Customer Summary [OE7ZS].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Customer code.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZU - Product Line Summary
This report summarizes the available product lines.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Product Line Summary [OE7ZU].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select one or more Product Lines.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if you want to Group by Alloy type.
- Specify how to Sort the data: by sales Value, Margin, or Gross margin percentage.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZV - POS Sales
This function generates a Point of Sales sales report.
- Choose Sales Order Report » Order Entry Reports » Misc & Custom Reports » Custom Reports » POS Sales [OE7ZV].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Territory code (defaults to all).
- Enter or select the Type of Entry: CM = credit memo, DM = debit memo, IV = sales invoice, or ALL.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Specify whether to run the report by Salesperson or order Writer.
- Specify whether to sort the report by document Number, Operator, Date, or view detail Lines.
"L" will display detail lines of the invoice and sort the report alphabetically by product name, not by customer.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZW - Detailed Sales Order/Quote
This report compares quoted quantities and ordered quantities, including salesperson data.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Misc Reports » Detailed Sales Order/Quote [OE7ZW].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Type of Entry: SO = sales order, SQ = sales quotation, or ALL (default).
- Enter or select a Salesperson (defaults to all).
- Indicate if you want to Group by Salesperson.
- Specify how to sort the data: Customer, Date, sales Value of the document, or Product code.
- Indicate if you want to Include Details (document line item details).
- Indicate if you want to only include lines where there was Insufficient Stock at time of document entry, or leave blank to display all lines.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZX - Gross Profit Report By Extras Code
This function generates a Gross Profit By Extras Code report.
- Choose Sales Order Entry » Order Entry Reports » Misc & Custom Reports » Custom Reports » Gross Profit Report By Extras Code [OE7ZX].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select a Customer (defaults to all).
- Enter or select a Salesperson (defaults to all).
- Enter or select an Extras Code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7ZZ - Sales By Cust By Prod Line By Grade
- Choose Sales Order Entry » Order Entry Reports » Sales By Cust By Prod Line By Grade [OE7ZZ].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Customer code (defaults to all).
- Enter or select one or more Product Line code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if credit/debit memos should reference the invoice date.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
OE7Z - Sales Order Report
This function generates a report listing all sales orders sorted by salesperson.
- Choose Sales Order Entry » Order Entry Reports » Sales Order Report [OE7Z].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Select one or more Salesperson and enter the salesperson type (Inside or Outside).
- Enter or select the Document Status to include (by default, all are selected).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if you want to display sales Values in the report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO53P - Inventory Re-Order Report
- Choose Purchasing » PO Reports » Purchasing Custom Reports » Inventory Re-Order Report [PO53P].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Lines and Grade.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Enter the number of Months Back to use in calculating report values.
- Enter the Sort Parameter: Product, Turns, Quantity, M = OnHand or ICC.
- Indicate if you want to Show Inactive products (those with no activity in the specified date range).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO53 - Re-Order Report
- Choose Purchasing » PO Reports » Re-Order Report [PO53].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Lines.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Enter Number of Months back to include on the report (defaults to 12).
- Enter or select Sort Parameter: Product, Turn, Quantity, M = Onhand or ICC.
- Indicate if you want to Show Inactive (products with no activity in the specified date range).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO71 - Purchase Order Reprint
This function is used to reprint a purchase order.
- Choose Purchasing » PO Reprints » Purchase Order [PO71].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select the Type of Entry (defaults to PO).
- Enter or select Document number.
- Indicate if you want to include Open lines only or leave blank for ordered quantities.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO72 - Open PO By Product
This function displays open purchase orders by delivery date for selected (or all) warehouses/vendors for a specified delivery date time period.
- Choose Purchasing » PO Reports » Open PO By Product [PO72].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select a Vendor.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if you want to show the customer name on report. If "Y" is selected, sort/currency type/hide value fields are set at default and cannot be changed.
- Select how you want to Sort the report: by Product code or by purchase order Number.
- Indicate the currency type: Functional (currency assigned to warehouse) or Source (customer’s currency).
- Indicate if you want to Hide $ Values on the report.
- Indicate if you want to Include Receipts that are on hold.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO73 - Open PO By Product Line By Month
This function is used to display outstanding purchase orders which have not been completely received, for selected warehouse and selected (or all) product lines.
- Choose Purchasing » PO Reports » Open PO By Product Line By Month [PO73].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select one or more Product Lines.
- Indicate if you want to Breakdown report data by grade. If you leave blank or enter "N", the report will be summarized by product line.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO74 - Direct Receipt/Receipt Return
This function is used to reprint direct receipt or receipt returns.
- Choose Purchasing » PO Reprints » Direct Receipt/Receipt Return [PO74].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select the Type of Entry code (defaults to RC-receipt).
- Select the range of Document numbers to include.
- Enter or select Vendor (defaults to all).
- Indicate if you want to Print Labels.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO75 - Receipts By Currency By Date
This function is used to display detailed receiving reports by selected date range, by vendor.
- Choose Purchasing » PO Reports » Receipts By Currency By Date [PO75].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Type of Entry (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Enter or select Vendor code (defaults to all).
- Select the Status (defaults to all).
- Select whether to produce a Detailed or Summary report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO77 - Stock Usage and Re-Order
- Choose Purchasing » PO Reports » Stock Usage and Re-Order [PO77].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Line (defaults to all).
- In the Back Weeks field, enter the number of weeks to go back to start accumulating usage figures.
- In the Back Months field, enter the number of months back to use to calculate the average monthly usage.
- Enter the Display Type : products with Suggested quantity, Release quantity, Both, Either or All.
- Indicate if you want to Sort By Available quantity.
- If you entered “All” in the Warehouse field, indicate if you want to Group by Whse.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO79 - Receipts By Vendor By Document
This function is used to display receipts by vendor, by product lines for a selected time perioe. You have the option to filter by grade/dimension.
- Choose Purchase Order » PO Reports » Receipts By Vendor By Document [PO79].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select Product Line code (defaults to all).
- Enter the Grade and Finish (defaults to all).
- Enter the Dimension From and Dimension To.
- Select a Vendor.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select whether to produce a Detailed or Summary report.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO7A - Purchase Order Pick Up Reprint
This function is used to re-print purchase order pick up, purchase order pick up documents can automatically print when PO is processed.
- Choose Purchasing » PO Reprints » Purchase Order Pick Up [PO7A].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select the Type of Entry (defaults to PO).
- Enter or select Document number to reprint.
- Optionally Filter Lines to include or exclude.
- Indicate if you want to include Open lines only or leave blank for ordered quantities.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO7B - Late Purchase Orders
This function is used to display late (by specified days late) purchase orders, by delivery date for selected warehouse, selected (or ALL) vendors for a specified delivery date time period and/or # of days late in ascending purchase order number.
- Choose Purchasing » PO Reports » Late Purchase Orders [PO7B].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select a Vendor Code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Indicate if you want to Show Ontime receipts.
- Indicate if you want to Show Early receipts. If you enter “Y”, enter the Min and Max Early Days.
- Indicate if you want to Show Late receipts. If you enter “Y”, enter the Min and Max Late Days.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO7C - Detailed Re-Order Report
- Choose Purchasing » PO Reports » Detailed Re-Order Report [PO7C].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Lines.
- Enter the number of Weeks Back 1 and Weeks Back 2 to calculate the first and second sets of sales quantity.
- Indicate which Open Orders to display: PO, SO, Both or None.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO7D - Direct Receipts By Shipment Number
This function is used to display Shipment Receipts.
- Choose Purchasing » PO Reprints » Direct Receipts By Shipment Number [PO7D].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Document number.
- Indicate if you want to Print Labels.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO7E - Open PO By Vendor By PO Number
This function is used to display open purchase orders by selected (or all) vendors for a warehouse.
- Choose Purchasing » PO Reports » Open PO By Vendor By PO Number [PO7E].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select a Vendor.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO7F - PO By Vendor By Month (Wgt)
This function produces a report that displays open purchase orders by selected (or all) vendor type for a warehouse, aging $ values by expected delivery dates.
- Choose Purchasing » PO Reports » PO By Vendor By Month (Wgt) [PO7F].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Aging Date (defaults to last day of last month).
- Enter or select the Vendor Type (defaults to all).
- Enter or select one or more Product Line.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO7G - Open PO By Vendor By Month (Wgt/Val)
This function is used to display Open Purchase Orders by selected (or all) Vendor Types for a Warehouse, aging $ values by expected delivery dates.
- Choose Purchasing » PO Reports » Open PO By Vendor By Month (Wgt/Val)[PO7G].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Aging Date (defaults to last day of current fiscal period).
- Enter the Report Type: Product line or Vendor. If "V" is selected, Prod Line/By Grade fields are not available. If "P" is selected, the Vendor Type field is not available.
- Enter or select the Vendor Type (defaults to all).
- Enter or select Currency code (defaults to all). If you select a currency code, enter the currency type: Functional (currency assigned to warehouse) or Source (customer’s currency).
- Press F4 to select Product Lines, or leave blank to default to all.
- Indicate if you want to sort/subtotal product lines By Grade.
- Indicate if you want to show Details of purchase orders and pre-receipts .
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO7H - Receipts By Vendor By Product
This function is used to display receipts by vendor, by product for a selected time period/product line for a selected warehouse or all warehouses.
- Choose Purchasing » PO Reports » Receipts By Vendor By Product [PO7H].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select a Vendor.
- Enter or select Product Line (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO7J - Ordered/Received By Document
This function is used to display a summary of open purchase orders and received purchase orders for a warehouse.
- Choose Purchasing » PO Reports » Ordered/Received By Document [PO7J].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Vendor code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Enter or select the Currency  (defaults to all). If you select a currency code, enterthe currency type: Functional (currency assigned to warehouse) or Source (customer’s currency).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO7K - Open PO By Product - Excel
This function is used to display open purchase orders and download to Excel.
This report is available as an Excel download only.
- Choose Purchasing » PO Reports » Open PO By Product - Excel [PO7K].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select a Vendor.
- Enter or select the Buyer (defaults to the buyer assigned to the selected vendor).
- Press Enter to process the report.
PO7L - Purchasing By Product Incoming By Month
This function displays purchases by product line, by future months (5).
- Choose Purchasing » PO Reports » Purchasing By Product Incoming By Month [PO7L].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Line (defaults to all).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO7M - Corporate Re-Order Report
This function is used to display purchases by product displaying previous/current month and 12 future months.
This report is only available as an Excel download.
- Choose Purchasing » PO Orders » Corporate Re-Order Report [PO7M].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Line code (defaults to all).
- Press Enter to process the report.
PO7N - Receipts/Sales By Log By Vendor
This function is used to display all log receipts by warehouse, by vendor, by log and provide selling information if the log has been sold.
- Choose Purchasing » PO Reports » Receipts/Sales By Log By Vendor [PO7N].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Select a Vendor.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO7O - Open Pre-Receipt Logs Report
- Choose Purchasing » PO Reports » Open Pre-Receipt Logs Report [PO7O].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select Product code (defaults to all).
- Enter or select Product Line (defaults to all).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO7P - Pre-Received Logs
This report is only available as an Excel download.
- Choose Purchasing » PO Reports » Pre-Recevied Logs [PO7P].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select Vendor code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select the Log Status to include: Received, Pre-received, or Both.
- Indicate if you want to Show log Value .
- Press Enter to process the report.
PO7R - Incoming Shipment Checklist
- Choose Purchasing » PO Reprints » Incoming Shipment Checklist [PO7R].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Document number.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.

PO7S - Receipt Return Proforma Invoice
- Choose Purchasing » PO Reprints » Receipt Return Proforma Invoice [PO7S].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Document number.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PO7U - Purchasing Report
This report is only available as an Excel download.
- Choose Purchasing » PO Reports » Purchasing Custom Reports » Purchasing Report [PO7U].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Product Lines.
- Enter or select Spec Type (defaults to all).
- Enter or select the end Date.
- Press Enter to process the report.
PO7W - Rebate Analysis Report
This report is only available as an Excel download.
- Choose Purchasing » PO Reports » Rebate Analysis Report [PO7W].
- Enter or select the Warehouse code plus Child Warehouse indicator (defaults to warehouse assigned to operator).
- Enter or select the Vendor.
- Enter or select the Rebate Type (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select which Rebates to show.
- Press Enter to process the report.
PP72 - OP Packing Slip
- Choose Outside Processing » OP Reprints » OP Packing Slip[PP72].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Document Number.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PP73 - Process Analysis by Vendor
This function produces a report that displays all outside processing orders for a specified vendor, cost code and/or date range.
- Choose Outside Processing » OP Reports » Process Analysis by Vendor [PP73].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select a Vendor.
- Enter or select Cost Code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PP74 - Open OP Orders By Vendor
This report displays all open Outside Processing and Inside Processing orders for a specified vendor or type of entry.
- Choose Outside Processing » OP Reports » Open OP Orders By Vendor [PP74].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Type of Entry (defaults to all).
- Enter or select Vendor code (defaults to all).
- Select to Sort By document Number or due Date.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PP75 - Yield Analysis
This report shows the yield amounts for outside processing orders.
- Choose Outside Processing » OP Reports » Yield Analysis [PP75].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Type of Entry code (defaults to all).
- Type Under Yield % up to 2 decimal places.
- Type Over Yield % up to 2 decimal places.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PP76 - Sub-Contract
Enter the original production order number.
- Choose Outside Processing » OP Reprints » Sub-Contract [PP76].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Type Of Entry.
- Enter or select the Document number.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PP77 - OP Receiving
- Choose Outside Processing » OP Reprints » OP Receiving [PP77].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Type of Entry : TF = Inventory Transfer, TU = Transfer Undo.
- Enter or select the Document Number.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PP78 - OP Bill of Lading
This function is used to reprint a bill of lading.
- Choose Outside Processing » OP Reprints » OP Bill of Lading [PP78].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Document code.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PP79 - OP Picking Slip
This function is used to reprint a picklist.
- Choose Outside Processing » OP Reprints » OP Picking Slip [PP79].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Type Of Entry (defaults to processing purchase order, PP).
- Enter or select Document Number.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PP7A - OP Pick-Up
- Choose Outside Processing » OP Reprints » OP Pick-Up [PP7A].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Type of Entry.
- Enter or select the Document Number.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PR73 - Production Analysis Report
This function prints a report on machine production performance, sorted by machine code.
- Choose In-House Production » In-House Production Reports » Production Analysis Report [PR73].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Machine Code (by default, all are selected).
- Enter or select Date From and Date To (by default, both are today's date).
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
PR74 - Raw Material Requirements
**This function prints two reports**: one showing the raw material requirements, and one showing the finished goods requirements.
- Choose In-House Production » In-House Production Reports » Raw Material Requirements [PR74].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Press F4 to select the Finished Goods (products that have recipes defined in PR14).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PR75E - Production Traveler
- Choose In-House Production » In-House Production Reprints » Production Traveler [PR75E].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Type of Entry code.
- Enter the original Document Number.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PR75 - Production Order
This function reprints a production order.
- Choose In-House Production » In-House Production Reprints » Production Order [PR75].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Type of Entry (by default, Production Order is selected "PR").
- Enter the original Document Number.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PR76 - Traveler Work Order
- Choose In-House Production » In-House Production Reprints » Traveler Work Order [PR76].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Document Number.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PR77 - Production Confirmation
This function reprints a production order confirmation.
- Choose In-House Production » In-House Production Reprints » Production Confirmation [PR77].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Type of Entry.
- Enter or select the Document Number.
- Indicate if you want to Print Labels.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PR7C - Production Estimated Vs Actual Time - Machine Costs
Report displaying usage values by machine.
This report displays machine costs; for machine revenue, use .
- Choose In-House Production » In-House Production Reports » Production Estimated Vs Actual Time [PR7C].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Customer code (defaults to all).
- Enter or select Machine code (by default, all are selected).
- Enter or select Date From and Date To (by default, today's date is selected for both).
- Leave default to filter report by all jobs or type "Y" to filter by complete jobs.
- Select how/where the report should be output (click … to choose from a list). When you press Enter the report will generate.
PR7D - Production Cost By Work Order
- Choose In-House Production » In-House Production Reports » Production Cost By Work Order [PR7D].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Type of Entry code.
- Enter or select the Customer code (defaults to all).
- Enter or select the Document Number (defaults to all).
- Enter Cost Factor ($/min) -
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Enter INV Status (defaults to all).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PR7E - Linear Nesting Project Reprint
- Choose In-House Production » In-House Production Reprints » Linear Nesting Project Reprint
or Inventory Control » Inventory Reprints » Linear Nesting Project Reprint [PR7E].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Project Number.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PR7F - Sales of Processed Material
- Choose In-House Production » In-House Production Reports » Sales of Processed Material [PR7F].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Customer code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PR7G - Production Estimated Vs Actual Time - Machine Revenue
Report displaying usage values by machine.
This report displays machine revenue; for machine costs, use .
- Choose In-House Production » In-House Production Reports » Production Estimated Vs Actual Time [PR7G].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Customer code (defaults to all).
- Enter or select the Machine code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Enter Estimated Time code: Cost or Revenue.
- Enter "Y" to sort by Complete only or leave blank to not.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PR7H - Yield Gain/Loss Analysis Report
This function is only available as an Excel download.
- Choose In-House Production » In-House Production Reports » Yield Gain/Loss Analysis Report [PR7H].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select a Type code.
- Enter or select a Vendor code.
- Enter or select a Mill code.
- Enter or select a Product Line code.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Press Enter to process the report.
PR7J - Profitability Report
- Choose In-House Production » In-House Production Reports » Profitability Report [PR7J].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select Type of Entry code: BT = branch transfer, CC = customer consignment, IV = sales invoice,  SO = sales order.
- Enter or select the Document number.
- Enter or select the Customer number.
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PR7M - Open IP/OP Report
This report is available as an Excel download only.
- Choose In-House Production » In-House Production Reports » Open IP/OP Report [PR7M].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Type of Entry code (defaults to all).
- Enter or select the Process code (defaults to all).
- Enter or select the Machine code (defaults to all).
- Enter or select the starting date Date From and ending date Date To for the report (defaults to today's date).
- Press Enter to process the report.
PR7O - Linear Nest Prod Order Reprint
Reprint screen for the linear nesting document; the data matches the production document (IN3F) including the barcode.
- Choose In-House Production » In-House Production Reprints » Linear Nesting Prod Order Reprint [PR7O].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Enter or select the Project Number.
- Select how/where the report should be output (press F4 to choose from a list). When you press Enter the report will generate.
PR7P - Export Production Schedule to Excel
This report exports lines from the Production Schedule to Excel.
- Choose In-House Production » Sales Order Controlled » Export Schedule to Excel [PR7P].
- Enter or select the Warehouse code (defaults to the warehouse assigned to you).
- Select the Process to export, or choose "ALL".
- Optionally select one or more Product Line to be included or excluded.
- Select the Document type and number, or choose "ALL".
- Optionally select a finished good Project.
- Select the Machine to export, or choose "ALL".
- Optionally enter a date range to filter on, or leave blank for all dates. These dates default to the Requested date, but you can change it to reference the Estimated or Actual schedule date.
- If you want to filter on a document status, select the Status check box and select the status.
- Click Export.