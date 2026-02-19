---
title: "Adm Client Install"
source: "madcap.md"
tags: ["4GL", "ADMIN", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Adm Client Install - 4GL Help Documentation"
long_description: "This topic provides detailed information about Adm Client Install in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the ADMIN module."
---


Installing the PROIV Client
===========================

There are two versions of PROIV available:

* PROIV v8.3.22.23 (required for  3.13 and prior)
* PROIV v9.901.4 (required for  3.14 and higher)

Installing the Client
---------------------

Refer to Client and Server Requirements for supported operating systems. You must have Windows Administrator access to install on new PCs.

If you are upgrading from a prior version of the PROIV client:

| Upgrading from | Upgrading to | Then |
| --- | --- | --- |
| v7 | v8 or v9 | Remove the older PROIV client prior to installing the current version (Windows > Control Panel> Programs and Features > Remove Programs). |
| v8 | v9 |
| v8 (older) | v8 (current) | You do not need to remove the older version. |
| v9 (older) | v9 (current) |
| In all cases, DO NOT remove the .piv files installed on your desktop. | | |

1. Go to https://4glsol.com/secure-downloads/ and enter SM3 as the password to continue.
2. Select the appropriate version of PROIV according to the version of  you will be using:

   ![](../../Resources/Images/ADM_client_download.png)
3. Save the file to your PC (or network, if you will be installing on multiple computers).
4. Once the download has finished, the setup wizard will open. Click Next through the wizard screens to accept the license agreement and to use the default directories and files, then click Install.
5. The installation/upgrade will take approximately 3 minutes, depending on your PC. When it is done, click Finish.
6. There is a batch job at the end of this install – accept the License and click Next.
7. Click Finish for all files to be extracted. If you are updating a previous v8 (or v9), select YES to update existing PROIV clients (your .piv files).

**IT staff**: The install will create the folder “NorthgateArinso”, install the .piv file on the desktop, and install the appropriate graphics files. See Appendix for the actual batch job steps.

Setting Up the Client (for new PROIV installations)
---------------------------------------------------

Next you need to populate the 4GL.piv file installed on your desktop with the necessary configuration information for your  account.

1. Click the 4GL.piv file on your desktop. The following screen opens:

   ![](../../Resources/Images/ADM_client_ProIV_menu.png)
2. Choose Edit » Session Properties and then click Connection.

   ![](../../Resources/Images/ADM_client_ProIV_connection.png)
3. Complete the following fields:
   * PROIV Hostname or IP Address – in xxx.xxx.xxx.xxx format
   * Command to run PROIV Virtual Machine – each customer has their own unique command; use lowercase only (ends with “run”)
   * UNIX User name \* – 3 digit  login, lowercase only
   * UNIX Password\* – password assigned to user, lowercase
   * Use Binary Telnet must NOT be selected

   \* Use the login information of the user who will be using this PC; login information is assigned in MS32.

   Open this screen on a computer that already has a connection to and copy the IP address and Command.
4. Leave all other settings as default, then click OK.
5. Click the save button ![](../../Resources/Images/ADM_client_i_save.png) in the menu bar, or choose Session » Save.
6. **\*\* Before logging in, complete the Windows Security Setup below.**
7. Click the yellow lightning bolt ![](../../Resources/Images/ADM_client_i_connect.png) to start a session to ensure connection to the  server.

Windows Security Setup
----------------------

Users require FULL control on the NorthgateArinso > PROIV Version 8 (9) > Client Folder installed on the client PC.

To change Windows security on the client:

1. Click the Windows Start button and enter File Explorer.
2. Select your C: drive, then navigate to Program Files (x86) > NorthgateArinso > PROIV Version 8(9)   
   (some PC configurations may be “Program Files” instead of “Program Files (x86)”).

   ![](../../Resources/Images/ADM_client_win_sec.png)
3. Right-click on the Client folder, and choose Properties.
4. On the Security tab, click Edit. In the *Group or User names* section click “Users”, then select “Allow” beside “Full control”. All of the Allow check boxes will be selected. Click Apply.

   ![](../../Resources/Images/ADM_client_win_sec2.png)

If you are unable to perform any of the above steps your IT group vendor may have to perform due to lack of Windows administration rights.

There are a number of Windows folders on the network that  may use:

* MTRs (Material Test Reports)
* Proof of Delivery (POD)
* Product Image
* Product Shape
* General Document Path

All  users require READ access to the above folders. Users who may be administering the documents will require READ/WRITE access. For customers who have multiple locations, there may be multiple folders for each location.

If you are not sure of the Windows path for the above folders, .

IT Administrators
-----------------

### Batch Job Steps During Install

1. Go to Control Panel > Programs > Turn Windows features on or off.
2. Select Telnet Client and click OK.

   ![](../../Resources/Images/ADM_client_admin1.png)

### Default Directory for PROIV

When installing the PROIV client, programs will be installed in Program Files (x86) – will create NorthgateArinso folder. You must change to this directory in the PROIV Application settings:

1. Click the 4GL.piv file on your desktop to open PROIV.
2. Choose Edit » Session Properties and then click Appearance.
3. Change the path in the following fields:
   * Directory containing Images
   * Alternate Image Search Directory Paths
   * Application Definitions File Location

   ![](../../Resources/Images/ADM_client_admin2.png)

### Windows 7/8 Errors

* **Unable to start windows Telnet**
    
  You likely have not entered the correct Unix login code and/or password (all in lower case only).
* **Windows errors (there will be multiple) when downloading graphics files to PC**
    
  See “Windows Security Setup” above to change security settings on your PC.

### Excel Date Formats

See Fixing the Date Format in Excel Reports.

---
