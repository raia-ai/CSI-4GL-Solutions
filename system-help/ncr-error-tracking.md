---
title: "Non-Conformance Reporting and Error Tracking"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Non-Conformance Reporting and Error Tracking"
long_description: "This topic provides detailed information about Non-Conformance Reporting and Error Tracking in the 4GL system."
---


Non-Conformance Reporting and Error Tracking
============================================

If NCRs are mandatory for the warehouse1, the following fields on the Header tab of a credit memo are mandatory: Error Track ID, Operator, Department, Error, and Description. You can either enter a new ID and related fields, or select an existing Error Track ID from the same warehouse (the related fields will be populated with the fields associated with that ID).

The Error ID will be associated with the credit note, and will print on the Credit Note Financial Impact report [AR7K] and the Error Tracking Report [MS72]. The values on AR7K, MS72, and OE62 all match.

There may be times when you want to capture an NCR without a credit note to track an internal “mistake” that doesn’t involve a customer, such as a machine operator making a mistake while cutting some stock. For these NCRs, use the Error Tracking module in the Admin menu to track and report on errors by operator code, by department:

* MS11 - create departments
* MS31 - manage the types of entries
* MS32 - assign default departments to operators
* MS3J - record the department errors:
  + Operator field is the operator who made the error
  + Department is the department where the error was made
  + Error field only shows error codes assigned to the selected department (in MS11)
* MS3Y - add and change entries, view/edit all entries for a particular day
* MS72 - Error Tracking report

Configuration


1 > Mandatory Non-Conformance Reporting

---
