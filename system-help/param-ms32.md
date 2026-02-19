---
title: "Setting Up Automatic Reports for an Operator"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Setting Up Automatic Reports for an Operator"
long_description: "This topic provides detailed information about Setting Up Automatic Reports for an Operator in the 4GL system."
---


Setting Up Automatic Reports for an Operator
============================================

You can set up specific reports with individualized parameters to send to an operator during the nightly batch run.

1. Choose Security » Operators [MS32].
2. Select the operator and click Email Parameters.
3. Locate the report you want to set up. If the desired report is not listed, you can add it.
4. Select the R check box to indicate that the operator should receive it.

   If you set a batch report to be received for an operator but do not enter any alpha or numeric parameters, the Receive checkbox will be cleared.

   ![](../../Resources/Images/Diversified FG/SEC_op_email_receive1.png)
5. Press F4 beside the A check box to specify the alphanumeric parameters specific to the report, such as warehouse, customer, salesperson type, salesperson, etc. These options vary according by report.

   ![](../../Resources/Images/Diversified%20FG/SEC_op_email_receive2.png)
6. Press F4 beside the N check box to define the numerical parameters specific to the report, such as date range, i.e. how many days back for the start date and the end date. These are relative to when your report batch runs is processed: if it runs late in the day or evening, you should enter “0” in both fields so that it pulls records for the same date; if it runs early in the day (e.g. 1:00am), you would enter “1” in both fields to pull records from the previous date.

   ![](../../Resources/Images/Diversified%20FG/SEC_op_email_receive3.png)
7. Press F4 in the Bch field to select a specific batch run, or leave it blank for “ALL”.

---
