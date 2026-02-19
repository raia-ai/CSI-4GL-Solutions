---
title: "Madcap_-_SM3_Help-Content-Admin-Requirements-Barcode_Scanner_Printer"
source: "Madcap_-_SM3_Help-Content-Admin-Requirements-Barcode_Scanner_Printer.txt"
tags: ["barcode", "scanner", "printer", "hardware-requirements", "inventory", "labeling", "4GL", "administration", "IT", "MTR-reports"]
version: "1.0"
last_updated: "2025-12-03"
short_description: "This document outlines the hardware requirements and recommendations for barcode scanners and label printers used with SM3 administrative workflows. It covers the primary handheld scanner for inventory operations, compatible label printer specifications, optional USB scanner settings for invoice confirmations, and requirements for heat scanning related to MTR reports, including PDF scanning and editing software options."
long_description: "This guide consolidates the essential hardware requirements for barcode scanning and label printing used in 4GL-supported administrative and warehouse workflows. It defines the intended uses of the handheld barcode scanner across common inventory functions—bin location changes, picking confirmations, physical inventory, and label management—and identifies a compatible model known to perform well in these scenarios. It also specifies the label printer model and network environment expectations so that IT teams can ensure dependable printing performance within a Windows-based infrastructure.

In addition to the primary hardware, this document describes an optional USB-connected scanner that supports Code 39 and 1D symbologies. For smooth data capture into host applications, the USB scanner must be programmable to send a line feed/carriage return after each scan and should be able to override Caps Lock. This configuration is particularly useful for invoice confirmation workflows, where quick and accurate data entry is a priority.

Finally, the document addresses heat scanning requirements for MTR (Material Test Report) processes. Any scanner capable of capturing images to PDF can be used, and for PDF editing and document management, the use of tools such as PaperPort or eCopy is recommended. Some organizations standardize on multifunction devices (for example, Canon Imagewriters) to combine copying, scanning, and printing needs, including a scan-to-PDF capability. Collectively, these guidelines help administrators and IT departments select, configure, and support the right mix of scanning and printing equipment to maintain efficient and reliable operations across inventory and documentation workflows."
---

## Barcode Scanner and Printer Requirements


## Bar Code Scanner
This device is used for scanning inventory items for:

- Bin location changes
- Picking confirmation
- Physical inventory
- Labels

Recommended model: Symbol MC3190-G, 38-key wireless handheld.

## Bar Code Printer
Recommended model: Printronix TT4M2 Label Printer, 8" OD.
Requires a network connection to the customer's network running Microsoft Windows XP or higher.

## USB Scanner
> [so these are the requirements for the scanner, but this kind of scanner is optional and needed only for invoice confirmation scanning?]

A USB scanner that scans Code 39 and has 1D scanning capabilities is supported. It must be configurable to:
- Send a line feed/carriage return after each scan
- Override Caps Lock

The USB scanner can be used for invoice confirmation (optional).

## Heat Scanner (MTR Reports)
Any scanner may be used as long as it can scan images to PDF.
To edit PDF images, it is recommended to use PaperPort or eCopy software.
Some clients use Canon Imagewriters to combine copying, scanning, and printing requirements (with an option to scan to PDF).
