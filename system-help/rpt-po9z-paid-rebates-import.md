---
title: PO9Z - Paid Rebates Import
source: madcap.md
version: '1.0'
last_updated: '2026-02-19'
short_description: PO9Z - Paid Rebates Import
long_description: Help documentation for PO9Z - Paid Rebates Import in the 4GL system.
---

# PO9Z - Paid Rebates Import

Use this function to import the Rebate Analysis Report ([PO7W](https://4glsol.com/sm3-helpdocs/Content/Reports/rpt_PO7W_Rebate_Analysis_Report.htm)) and apply the rebates.

1. Open report PO7W and enter “Y” in the Apply Rebates column for each rebate you want to apply.
2. Save the document as a tab-delimited text file.
3. Open PO9Z.
4. Click the File icon to retrieve the file. To check for errors, select the Validate Only check box and then click Save. This will create a file outlining the errors but will not import the file.\
   or\
   If you are ready to import the file, click Save.
5. After importing, open the PO7W report again. You will see an “A” beside each log that you entered “Y” for in step 1 if you selected show applied or both.

**NOTE:** To unapply a rebate, open PO7W and enter “U” in the Apply Rebates column and repeat steps 2 and 3.

***
