---
title: Creating and Printing Handheld Login Sheets
source: madcap.md
version: '1.0'
last_updated: '2026-02-19'
short_description: Creating and Printing Handheld Login Sheets
long_description: >-
  Help documentation for Creating and Printing Handheld Login Sheets in the 4GL
  system.
---

# Creating and Printing Handheld Login Sheets

## Creating Handheld Login Sheets

1. In the StayLinked Administrator window, expand your server name to display the Scan2Command Profiles, then right-click in the right window pane and choose Add.
2. The Add Scan2Command Profile window will open. Enter a Profile Name (this will print at the top of the Barcode login sheet). Choose “Code 128” in the Symbology field.\
   To add the handheld barcodes, right-click in the window and choose Add New.
3. You will need to add a command for the username, password, login script and Exit. The caption is what will be displayed under the barcode and the command is what will be barcoded.
   * User:
   * Password:
   * Login Script (your login script will be your 3-digit company code + wifrun):
   * Exit:
4. Choose File » Save Changes.

## Printing a User-Specific Handheld Login Sheet

1.  In the StayLinked Administrator window, expand your server name to display the Scan2Command Profiles:

    You will see a list of all handheld users on the right side.
2. Double-click on the user (or right-click and choose Edit) for whom you want to print a login sheet.
3. Choose File » Print. The login sheet will print to your default Windows printer.

## Sample Printed Login Sheet

***
