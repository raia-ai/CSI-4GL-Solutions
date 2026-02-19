---
title: "Manifest Load Confirmation"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Manifest Load Confirmation"
long_description: "This topic provides detailed information about Manifest Load Confirmation in the 4GL system."
---


Manifest Load Confirmation
==========================

This function is used to confirm loading of a truck. The load confirmation process is driven by the loading report generated from the manifest [MN31] and lists all of the logs/packages that need to be loaded onto the truck.

Any miscellaneous docs must be manually loaded on the manifest's Pick/Load tab.

1. Scan or enter the run ID barcode from the loading report.
2. Scan the material as it's loaded on the truck, either by scanning a shipping label or a package label (see below).
3. As needed, use any of the following action keywords:
   * VIEWMISS or VIEWERR - display logs that have not been loaded. Press F4 on the Err field to view the packages and logs picked for the work order that have not yet been loaded; for packages, you will see the count and the number of logs within it.
   * VIEWALL - display the total packages and non-packaged logs that have been loaded.
4. Once everything is loaded, the manifest may be finalized to generate the packing slip.

Loading a Log (Shipping Label)
------------------------------

A shipping label has a barcode that represents the document and log number. When the shipping label is scanned the log record on the document will be updated with the manifest document and run number. This process will update the Loaded field on the manifest.

User will be alerted if a log number is scanned which is not on this run, i.e. it has been assigned to a different run/date or it has not been assigned to a run at all. In either case the scan will not go through. User can view the logs that have not been loaded.

An error report will show if the expected (assigned) and actual (loaded) are different.

Loading a Package
-----------------

A user can load a package to a run in one of the following two ways:

* Scan a log belonging to a package to load all the logs in the package onto the run.
* Scan a package ID to load all the logs in the package onto the run.

For both cases, all logs belonging to the package must be assigned to the same manifest and run. The logs will not load until all the package counts have been entered.

When a package is scanned the loaded indicator will be set for all logs in that package.

If the package is a multi-part package (e.g. 1 of 3, 2 of 3, 3 of 3) multiple labels are generated for the package and it will not be considered loaded until all labels are scanned.

---
