---
title: "Package Maintenance"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Package Maintenance"
long_description: "Help documentation for Package Maintenance in the 4GL system."
---


Package Maintenance
===================

This screen is used when you are strapping or bundling logs together to create a “package” out of multiple logs. Packages can be created after logs have been picked/assigned to a document.

Creating or Modifying a Package
-------------------------------

1. To create a new package, scan STRTPKG.   
   To modify a package that has already been assigned to a selected run, enter the Pkg ID.

   To generate a package for each sales order reserved against an IP or nesting project, scan CRTPKG and then scan the IP number (or nesting project number).
2. If necessary, and if allowed for your operator ID1, change the Whs.
3. For a package that has not been loaded, enter the number of labels required in the Tot field. For multi-part packages (e.g. 1 of 3, 2 of 3, 3 of 3) you would enter the number of parts to the package in the Tot field. Note: Inventory will only be assigned to the package itself, not to the package part, so you will not have traceability as to what inventory went into package part 2 for example.
4. Optionally enter or select a package Type (e.g. bundle, skid, pallet).
5. Assign a Bin location to the package (you may be prevented from entering a non-existent bin location, or you may only be warned)2. The bin location may require a location type prefix3; if an invalid prefix is entered, a prompt will appear showing valid options.
6. To load logs to the package:
   * Scan an IP number (unless multiple sales orders with different ship-to's were reserved against the IP) or barcode4 that shows the IP number, set and finished good index, to add the finished goods logs to the package.
   * Scan a sales order number to add all logs from the document assigned to the specified run to the active package.
   * Scan a concatenation of a sales order number and index number to add all logs from the document line assigned to the specified run to the active package.\*
   * Scan a concatenation of a sales order number and log number to add the log, if assigned to the specified run, to the active package.\*
   * Scan a production number to add all logs allocated to sales orders assigned to the specified run to the active package.\*
   * Scan a linear nesting project number to add all logs allocated to sales orders assigned to the specified run to the active package.\*

\* If no logs are added after scanning these, it means there are no outstanding unpackaged logs that are assigned to the specified run, or no run if no run specified.

Like picking confirmation, any logs scanned must be on the same manifest and run as the active package. If the active package does not belong to a manifest or run, only logs that do not belong to a manifest or run can be added to the package.

When adding logs to a package you will be warned if the log is already in another package, if the log is assigned to a different run than the current package, or if the log is assigned to a different manifest than the current package. If a log has already been loaded on a run, it will be unloaded when added to a package.

All logs scanned must have the same ship-to destination on the order.

7. To view the logs, scan INQUIRE; press F9 to view the description for each log.
8. To remove one or more logs from the active package, scan DELETE. Alternatively, scan ABORT to abort the entire package and remove all logs added. Removed logs are then available to be added to a new package.

   If you deleted logs from a package and then create a new package and scan the same production order, or if you scan other sales orders and/or nesting documents that belong to the same customer, a window will display all the logs in the document that are already in the other package and adds the remaining logs that were not already in the other package.
9. To stop modifying the active package, scan EXIT.
10. When you are finished with the package, scan ENDPKG to print a label for the active package. If you entered a number >1 in the Tot field, that many labels will print: each will show “1 of [total]” and the barcode will have a sequence appended to the package ID.

If you need to reprint the package label(s) at a later date, after the package has been loaded, use the Package Label Reprint [WFP4] function.

### Merging Packages

You can merge packages that have the same ship-to information. You cannot merge a package that:

* contains a log that has been loaded on a manifest run
* contains a log that has already been delivered
* contains no logs

To merge the contents of another package into one you are currently maintaining, enter the package ID of the package you wish to merge in the Act field. All logs and counts from the merged package are added to the active package being maintained, and the merged package will be closed. Repeat as needed to merge additional packages into the active one.

Configuration


1 MS32 > Change Transactional Whse

2 SWTMNT > Hard Warning on Bin Location Check?

3 SWTMNT > Only Floor Bin Location Types are Utilized? = N

4 IN19 > Forms > PDS30POR > Form Options > Barcode Finished Goods

---
