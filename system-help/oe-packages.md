---
title: "Creating and Loading Packages"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Creating and Loading Packages"
long_description: "Help documentation for Creating and Loading Packages in the 4GL system."
---


Creating and Loading Packages
=============================

A package is a group of logs picked for a sales order, outbound branch transfer or customer consignment. The package can contain logs picked for several of these documents, but the ship-to address for each document in the package must be the same, and each document must be on the same manifest and manifest run.

Contents of a package typically move together. For example:

* When you assign a package (or a log belonging to a package) to a run, or load a package/log, all logs in the package will be included.
* If logs for a line belong to a package, the logs will be automatically assigned or unassigned with the line.

Adding a Log to a Package
-------------------------

A log may be added to a package:

* at time of picking - a user can create a new package directly from the Handheld Picking Confirmation (WF11) and begin assigning logs to the new package as they pick them.
* after picking — a user can create a new package directly from Package Maintenance (WFP3) and modify the contents of existing packages.

WFP3 also allows a package to be created for each sales order reserved against an IP or nesting project.

A log picked for a single order line cannot be assigned to two different packages simultaneously.

Adding a Package to a Run
-------------------------

A package may be assigned to a run from the Manifest Load Confirmation (WFL2) or the Manifest Entry/Maintenance (MN31).

---
