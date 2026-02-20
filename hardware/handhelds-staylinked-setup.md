---
title: Handhelds-StayLinked_Setup
source: handhelds-staylinked-setup.md
tags:
  - 4GL
version: '1.0'
last_updated: '2026-02-19'
short_description: Handhelds-StayLinked_Setup
long_description: Documentation for Handhelds-StayLinked_Setup in the 4GL system.
---

# Handhelds StayLinked Setup

**StayLinked Setup** **Download**\*\* Link\*\*\*\*:\*\*

* Selectthe download link forSmartTE Administrator and Server Software
* Login andensure to click "Administrator Downloads" on the left pane and download theFull Windows version **Application Link:** Overview This documentation covers the process of adding handheld profiles to a client's StayLinked server using StayLinked Administrator.It also briefly covers theunderlying technical relationship between StayLinked, the SM3 server and the physical handheld devices. Finally, common troubleshooting scenarios are discussed. Adding and Connecting to a Server
* To add aserver to StayLinked Administrator, simply right click on the "Server List" and then click "Add". You can also click "Servers" on the top right-hand side of the screen and select "Add"
* A window will pop-up to allow you toadd the server information. The**Server Name**should the3-character customer. The**Server IP**would be the associated IP address for that customer.Refer totheSpreadsheet for the required information&#x20;
* To connect to a server, double click on it from the list on the left pane of the screen.The credentials are:
  * User ID: administrator
  * Password:esp&#x20;
* Once connected, the following menu options will be available for that server. In the screenshot below, we are connected to the SSL\_IEP server&#x20;
* **Connections > All Connections**: list all the handhelds that are connected to the server. For troubleshooting purposes, you are presented with information such as the MAC and IP addresses. Adding Profiles
* Clicking on**Client Configuration > Scan2Command Profiles**presents you with the screen necessary to create handheld users in StayLinked&#x20;
* In the**Scan2Command Profiles**window, right click a blank area of theright pane and click "Add" to add a new profile.Enter a**Profile Name** thenright click on the blank space underneath the "Mnemonic" heading and click on "Add new" to add a**Command** and**C\*\*\*\*aption**&#x20;
* Here is a breakdown of theabove screenshot.
  * The**Mnemonic** isthe command that the handheld sends to the server once the barcode is scanned. For example,da1\[enter] would essentially be the handheld typing"da1" and hitting the enter key to send the "Username/Password" information to the server.Rather the entire process is completed by the handheld user scanning the appropriate barcode.
* After creating all the commands, be sure to print out thebarcode sheet that would be given to the handheld users.To do this, click on "File" and "Print Preview". Select the print button and choose the "Microsoft Print to PDF" option. Save the document.   Finalize Handheld User Creation
* Aftercreating the users in StayLinked, you would need to ensure that the users are also createdon the company server. To accomplish this, log into the company's server via Putty; for this example, I will log into the SSL/IEP server.
* Run the following commands for each user that was added in StayLinked
  * useradd -g pro4 _user_
  * Passwd _user_
    * Enter the password for the user. Usually, the3-character code for the username is the same password&#x20;
* In the above example, da1 already exists on the server but you should typically not receive that error for new users.
* Now the da1 user has been successfully added in StayLinked and the SM3 server. Additionally, the login script has been saved and the users can simply scan the barcodes andthe handheld will translate the barcodeto the appropriate commands. Troubleshooting
