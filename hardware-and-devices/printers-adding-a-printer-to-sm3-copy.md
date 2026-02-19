---
title: "Printers-Adding_a_printer_to_SM3_-_Copy"
source: "Printers-Adding_a_printer_to_SM3_-_Copy.docx"
tags: ["4GL", "Steel Manager 3", "printers", "CUPS", "how-to", "configuration", "setup", "IT operations", "standard defaults"]
version: "1.0"
last_updated: "2025-12-03"
short_description: "This concise procedure explains how to register a printer in Steel Manager 3 (SM3) once the device has already been created in CUPS. It outlines where to start in 4GL (MS35), the essential printer details to enter, and the default settings that should be applied for consistency across environments. The guide concludes with the save action so that the printer becomes available for use within 4GL. It is intended for operators or support staff who maintain 4GL printer records and need a quick, repeatable checklist that aligns with standard defaults and naming conventions."
long_description: "This document provides a focused, step-by-step guide for adding a printer to Steel Manager 3 (SM3) after the device has already been configured in CUPS. In many environments, the print subsystem is managed centrally via CUPS, while SM3 requires a corresponding internal registration so that the application can reference the correct device code, display name, and default behaviors. The steps below ensure that the 4GL configuration mirrors the working CUPS setup and that operational defaults — such as DV column values, labeling and collation settings, number of copies, and tray selection — are consistently applied.

Use this guide when a printer is confirmed to be reachable and operational in CUPS but does not yet appear in 4GL selection lists or workflows. The process begins in 4GL at the MS35 menu option, where new printers are registered. From there, you will start the add process and enter two essential identifiers: a unique Printer Code and a clear, user-facing Name. Choose a code that conforms to your organization’s naming conventions and a name that will be instantly recognizable to end users. Maintaining alignment between the CUPS configuration and these SM3 identifiers reduces ambiguity and helps with support, reporting, and day-to-day operations.

Once the identifiers are set, apply the required defaults to establish predictable behavior across all newly added devices. Set the DV column to 3. Keep the L&C column ticked (enabled) unless the customer specifically advises otherwise. Set the Number of Copies to 1 to avoid unintended multi-copy output, and leave Trays at 1 unless there is a documented, approved variance for that printer. These defaults serve as a baseline that minimizes surprises for users and makes troubleshooting more straightforward, because everyone starts from the same known configuration.

After entering details and defaults, save the record (F3) so the device becomes available to SM3. At this point, the printer should be selectable where applicable within 4GL processes. If any behaviors do not match expectations, validate that the CUPS queue name and device configuration are correct, and confirm that the 4GL Printer Code and Name match your standards. Deviations in naming or defaults are a common source of confusion and can be corrected by editing the 4GL record.

This procedure is intended for operators, administrators, or support staff responsible for 4GL printer maintenance. It assumes the printer has already been added and tested in CUPS and that network access, permissions, and drivers have been addressed upstream. By following the steps below, you establish a reliable, repeatable method for registering printers in 4GL that promotes consistency, reduces rework, and supports efficient, predictable printing across the environment."
---

## Overview

This guide explains how to register a printer in Steel Manager 3 (SM3) after it has already been added in CUPS.

## Steps to Add the Printer in 4GL

1. From the 4GL main menu, go to MS35.
2. Start the Add process and enter printer details:
   - Printer Code: Enter the unique code for the printer.
   - Name: Enter the printer’s name exactly as it should appear.
3. Set required defaults:
   - DV Column: Always set to 3.
   - L&C Column: Keep ticked (enabled) unless the customer specifically advises otherwise.
   - Number of Copies: Always set to 1.
   - Trays: Leave as 1.
4. Hit F3 to save.