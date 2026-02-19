---
title: "Printers Adding A Printer To Cups"
source: "Printers-Adding_a_printer_to_CUPS.md"
tags: ["4GL", "Hardware and Devices"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Printers Adding A Printer To Cups"
long_description: "This document provides detailed information about printers adding a printer to cups in the 4GL system."
---

title: "Printers-Adding a printer to CUPS"
source: "Printers-Adding_a_printer_to_CUPS.pdf"
tags: ["CUPS", "Printer", "Network Printing", "Linux", "System Administration", "SM3", "Raw Queue", "PPD", "JetDirect"]
version: "1.0"
last_updated: "2025-12-03"
short_description: "A concise guide detailing the step-by-step process for adding a network printer to the Common Unix Printing System (CUPS). It covers accessing the CUPS web interface, configuring the connection via AppSocket/HP JetDirect, and setting up the printer as a raw queue, which is a necessary step for integration with SM3 network printing."
long_description: "This document provides a detailed, illustrated tutorial for system administrators on how to add and configure a network printer using the CUPS web interface. The guide begins with instructions on accessing the CUPS administration page via a web browser on a Linux system. It then walks the user through the 'Add Printer' wizard, specifying the use of the `AppSocket/HP JetDirect` protocol and providing an example connection string (`socket://192.168.2.69:9100`). The tutorial emphasizes a specific configuration required for compatibility with SM3: setting up the primary printer entry with a 'Raw' make and 'Raw Queue (en)' model. This initial setup creates the base printer. Subsequently, the guide explains how to create separate printer entries for each physical tray by referencing the tray number (e.g., `4GL1`, `4GL2`). It also covers alternative methods for driver installation, such as providing a PPD file manually or using a generic PostScript driver if a specific one is unavailable. Finally, it shows how to set default options like media source for each tray-specific printer to ensure jobs are routed correctly."
---

# Adding a printer to CUPS

This guide outlines the process for adding a network printer using the CUPS (Common Unix Printing System) web interface.

## Accessing the CUPS Interface

1.  Please go into the NX client for your server's I.P. address.
2.  Once you reach the home screen, please select the **Firefox web browser logo**.

    