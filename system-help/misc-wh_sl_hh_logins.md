---
title: "Wh Sl Hh Logins"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Wh Sl Hh Logins - 4GL Help Documentation"
long_description: "This topic provides detailed information about Wh Sl Hh Logins in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Creating and Printing Handheld Login Sheets
===========================================

Creating Handheld Login Sheets
------------------------------

1. In the StayLinked Administrator window, expand your server name to display the Scan2Command Profiles, then right-click in the right window pane and choose Add.

   ![](../Resources/Images/WH_SL_Scan2_add.png)
2. The Add Scan2Command Profile window will open. Enter a Profile Name (this will print at the top of the Barcode login sheet). Choose “Code 128” in the Symbology field.  
   To add the handheld barcodes, right-click in the window and choose Add New.

   ![](../Resources/Images/WH_SL_Scan2_add2.png)
3. You will need to add a command for the username, password, login script and Exit. The caption is what will be displayed under the barcode and the command is what will be barcoded.
   * User:

     ![](../Resources/Images/WH_SL_Scan2_add_user.png)
   * Password:

     ![](../Resources/Images/WH_SL_Scan2_add_pwd.png)
   * Login Script (your login script will be your 3-digit  company code + wifrun):

     ![](../Resources/Images/WH_SL_Scan2_add_login.png)
   * Exit:

     ![](../Resources/Images/WH_SL_Scan2_add_exit.png)
4. Choose File » Save Changes.

   ![](../Resources/Images/WH_SL_Scan2_add_save.png)

Printing a User-Specific Handheld Login Sheet
---------------------------------------------

1. In the StayLinked Administrator window, expand your server name to display the Scan2Command Profiles:

   ![](../Resources/Images/WH_SL_Scan2_profiles1.png)

   You will see a list of all handheld users on the right side.
2. Double-click on the user (or right-click and choose Edit) for whom you want to print a login sheet.
3. Choose File » Print. The login sheet will print to your default Windows printer.

   ![](../Resources/Images/WH_SL_Scan2_profiles2.png)

Sample Printed Login Sheet
--------------------------

![](../Resources/Images/WH_SL_Scan2_sample.png)

---
