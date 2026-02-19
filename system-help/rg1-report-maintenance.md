---
title: "Creating a Custom Financial Report"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Creating a Custom Financial Report"
long_description: "Help documentation for Creating a Custom Financial Report in the 4GL system."
---


Creating a Custom Financial Report
==================================

The Financial Report Writer allows you to setup, maintain and print custom financial reports from balances in the GL accounts. All reports created in the Financial Report Writer can be exported to Excel (printer code XLS).

1. Choose General Ledger » GL Reports » Financial Report Writer » Report Maintenance [RG1].

   Step two is skipped when modifying an existing report.
2. Enter Report Number ID (up to two numeric digits).
3. Enter or select report Description. Description will print as a Report Header, identical to input, on reports.
4. In the Columns field, press F4 to define the columns for the report; in the Maintain Column Details screen:
   1. In the Field column, press F4 to select from the predefined library of fields.
   2. Enter column Headings, two lines will print as a column header identical to input on reports (uses spaces to center header).
5. In the Groups field, press F4 to define the rows for the report in the Group Maintenance screen; see below.
6. To add remarks or change the report to single spaced, press F9.

Adding Rows to the Report
-------------------------

To create rows in the report, you will add the general ledger accounts that pertain to the report. Each general ledger account you include is constructed into a group that may contain a header, line, and total; these are presented as the rows in the report.

In the Group Maintenance screen:

1. Enter a Group number (up to three numeric characters).  prints the lines in ascending Group number.

When creating lines leave gaps between the numbers to allow for new lines to be inserted in the future.

2. Enter a Heading; this is the text that will print as a Line description identical to input on reports.
3. Select the Group Type:

* Header – only displays the text entered in the Heading field; no GL accounts are attached to this Group Type
* Line – displays the text entered in the Heading field, and includes GL Accounts
* Total – displays the text entered in Heading field and the accumulated total of GL accounts (see If Group Type = “T” below).

4. To change sign, e.g. to show -123 as 123, select the check box in the +/- field.

**The rest of the procedure depends on the Group Type selected (L (Line)or T (Total):**

### If Group Type = “L” (Line)

1. To provide a title for the “Total” line for all the accounts, press F9 and enter a group number (up to three digits) in the Trailer field. [currently not working in Oracle, hide until fixed].
2. Press F4 in the Lines field to identify the lines in the report; in the Line Maintenance screen:
   1. Enter a Line number, up to three numeric characters.

   When creating lines leave gaps between the numbers to allow for new lines to be inserted in the future.

   2. Enter a Description.
   3. Press F4 to select the GL Accounts to be included for the line. In the Account Maintenance screen, select an account or press F9 to select a range of accounts. Enter sign of account: “+” = if totaling line account or “-” if not.
   4. In the Det Y/N field, select the check box if you want GL accounts to be displayed in report, or leave blank to hide them.
3. In the Percentage Calculation screen, press F4 in the Sub Total Group field to select a “Total” account.

Ensure a column is created to display percentage.

### If Group Type = “T” (Total)

The Total Details screen defines how subtotals and totals are calculated in the report.

It is based on populating four separate columns each time a value is added to report. A column can be totaled and printed, or it may be totaled, printed and then cleared (which will result in restarting the accumulation of values beginning from ‘0’ for the selected column and those before it). See the sample Income Statement below.

1. Select Sub Total Number: 1 = first, 2 = second, 3 = third, G = grand total.
2. To print the sub total on the report, select the Sub Total Print check box or leave blank to hide sub total.
3. To select the number of spaces to indent the total on the printed report, type column number of spaces in Column Number Indent field.
4. To clear accumulating sub total select the  Clear Sub Total check box, or leave blank to keep original sub total.
5. Press F4 in the Sub Total Group field to select a “Total” account.

Ensure a column is created to display percentage.

6. To switch sign select the Switch Sign check box or leave blank to keep original sign.

Sample Income Statement


This sample Income Statement illustrates how system accumulates totals, and is explained below the table.

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
|  | First Total | Second Total | Third Total | **Grand Total** |
| Sales | 100,000 | 100,000 | 100,000 | 100,000 |
| Cost of Goods Sold | -75,000 | -75,000 | -75,000 | -75,000 |
| Gross Profit ('Total 2' and clear) | 0 | 25,000 |  |  |
|  |  |  |  |  |
| Advertising Expense | -2,000 | -2,000 | -2,000 | -2,000 |
| Commissions Expense | -5,000 | -5,000 | -5,000 | -5,000 |
| Selling Expenses ('Total 1', clear an switch sign) | -7,000 |  |  |  |
| Office Supplies Expenses | -3,500 | -3,500 | -3,500 | -3,500 |
| Office Equipment Expenses | -2,500 | -2,500 | -2,500 | -2,500 |
| Administrative Expenses ('Total 1', clear and switch sign) | -6,000 |  |  |  |
| Total Operating Expenses ('Total 2", clear and switch sign) | 0 | -13,000 |  |  |
| Operating Income ('Total 3') |  |  | 12,000 |  |
|  |  |  |  |  |
| Interest Revenues | 5,000 | 5,000 | 5,000 | 5,000 |
| Gain on Sale of Investments | 3,000 | 3,000 | 3,000 | 3,000 |
| Interest Expense | -500 | -500 | -500 | -500 |
| Loss from Lawsuit | -1,500 | -1,500 | -1,500 | -1,500 |
| Total Non-Operating ('Total 2' and clear) | 0 | 6,000 |  |  |
| Net Income ('Total 3' and clear) |  |  | 18,000 |  |

Above table consists of five columns:

* First column displays the account, subtotal or total corresponding to the sample Income Statement
* Last four columns represent the four accumulating totals which the Report Writer uses to calculate all totals on the report.

Each time there is a value in the ‘Lines’ type of the Report Writer, it will be added to each ‘Total’ column, as illustrated above.

Each time a ‘Total’ type Line is created in the Report Writer, you have choice of which ‘Total’ column to display (1, 2 or 3), and if you require to clear total, in order to begin accumulating a new total in the same column.

In the example above, Gross Profit is the sum of ‘Sales’ and ‘Cost of Goods Sold’. We have selected to display the subtotal in Second Total and clear it (which will also clear all the totals to the left of itself, i.e. First Total).

Now the First and Second Total will begin the next calculation from ‘0’ but the Third and Grand Total will continue to add new values from where they left off, in this case ‘25000’.

So now when we take a look at the ‘Operating Income’ we can select to display the Third Total which will be the sum of all the values in the Third Total column at this point, ’12,000’. Do not need to clear this total, therefore, values below will not begin calculating from ‘0’ but rather continue from ’12,000’.

When you select to display the Third Total again it will be the accumulation of the ‘Net Income’, Third Total, and the values that follow, which will give us a total of ’18,000’. (You may choose to display the Grand Total, which will give you the same result, ’18,000’.)

---
