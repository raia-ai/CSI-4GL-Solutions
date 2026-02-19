---
title: "SIMTRANS automation USER MANUAL"
source: "madcap-sm3-help-content-externalfiles-simtransmanual.md"
tags: ['SM3', 'System Help']
version: "1.0"
last_updated: "2026-02-19"
short_description: "SIMTRANS automation USER MANUAL"
long_description: "This document provides detailed information about simtrans automation user manual in the 4GL system. It includes procedures, reference information, and best practices for users and administrators."
---

title: "Madcap_-_SM3_Help-Content-ExternalFiles-SimTransManual"
source: "Madcap_-_SM3_Help-Content-ExternalFiles-SimTransManual.pdf"
tags: ["SimTrans", "SigmaNEST", "automation", "user manual", "transaction manager", "MRP", "ERP", "CAD/CAM", "SigmaTEK", "software"]
version: "1.0"
last_updated: "2025-12-03"
short_description: "A comprehensive user manual for SimTrans, a transaction manager by SigmaTEK designed to integrate SigmaNEST with other business systems like MRP and ERP. This guide covers installation, setup, system requirements, usage, and a detailed reference for all transaction types."
long_description: "The SimTrans User Manual is a comprehensive guide for the SimTrans online transaction manager, a software solution by SigmaTEK Systems, LLC. SimTrans is designed to bridge the gap between the SigmaNEST nesting software and other business systems, such as MRP and ERP. It automates the process of checking for and running new transactions. This manual covers all aspects of using SimTrans, starting with an introduction in Chapter 1 that details system requirements, a step-by-step installation guide, and initial setup procedures, including SigmaNEST configuration, user management, and global/district configurations. Chapter 2 explains the core functionality of SimTrans, detailing how transactions are created, processed, and how feedback is generated and returned to the business system. It provides a complete list of transaction variables. Chapter 3 serves as an extensive transaction reference, categorizing transactions for Material Management (SN6x), Programs and Work Orders (SN7x), Parts and Work Orders (SN8x), Stock Management (SN9x), Quote Management (QTx), and Cut-to-Length (CTLx). Each transaction is described with its purpose, required variables, and a sample SQL query. Chapter 4 provides additional resources, including FAQs, troubleshooting tips, and contact information for technical support. The manual is intended for users who need to integrate SigmaNEST with their business logistics and manufacturing processes."
---

# SIMTRANS automation USER MANUAL

## Copyright and Legal Information

Copyright © 2018 SigmaTEK Systems, LLC. All Rights Reserved.

Information in this document is subject to change without notice. The software described in this document is subject to a license agreement, which must be signed prior to use of the software. This manual may only be used in accordance with the terms of the license agreement. Copies or reproductions shall not be made except to the extent reasonably necessary, and all copies made are considered the property of SigmaTEK Systems, LLC. No part of this manual may be distributed or divulged to any third party without written permission from SigmaTEK Systems, LLC. The recipient shall maintain SigmaTEK Systems, LLC's proprietary information, as described in this manual, in confidence. Use of the software and/or this document constitutes acceptance of this agreement.

**SigmaTEK Systems, LLC**
1445 Kemper Meadow Drive
Cincinnati, OH 45240
513.674.0005

This manual may describe features that are not available in your version of SimTrans. To learn more about specific features or products, contact your SigmaNEST sales representative or visit www.sigmanest.com

## Chapter 1: Get Started

Thank you for choosing to invest in SigmaNEST, the world's leading nesting solution for all fabrication machines. The opportunity to serve you as our customer is an honor for our team. We look forward to working with you and helping you get the most from your complete SigmaNEST software solution.

SimTrans is an online transaction manager that bridges the gap between SigmaNEST and your other business systems. It typically runs in the background on a SigmaNEST workstation or on a centralized server. After setup, SimTrans automatically checks for and runs new transactions as they are created.

### System Requirements

This section outlines the system requirements for SimTrans and SigmaNEST. All specifications assume that SimTrans and SigmaNEST are the primary products used on the computer on which they are installed. If other demanding products are run on the same computer, the requirements should be adjusted accordingly.

A USB port or high-speed Internet connection is required to install the software. For licensing purposes, a USB port must also be available on each workstation (for a local license) or on a computer accessible through an internal network (for a network license). A Digi Anywhere USB device can be used for network USB access.

The SigmaNEST database requires Microsoft SQL Server 2014 (64-bit). You can install the SQL server during the SigmaNEST installation, or use an existing installation of this version or higher.

#### Single system/workstation minimum requirements

-   **Operating system:** 64-bit Windows 8.1 Pro
-   **Processor:** Intel/AMD dual-core
-   **Memory:** 4 GB
-   **Hard disk type:** 7200 RPM
-   **Hard disk capacity:** 120 GB
-   **Screen Resolution:** 1280x1024
-   **Video card:** Integrated chipset with Open GL version 4.0

#### Single system/workstation recommended requirements

-   **Operating system:** 64-bit Windows 10 Pro
-   **Processor:** Intel/AMD quad-core
-   **Memory:** 8 GB
-   **Hard disk type:** SSD
-   **Hard disk capacity:** 250 GB
-   **Video card:** Dedicated video card with Open GL version 4.0
-   **Network:** High-speed Internet connection

#### Server recommended requirements

> **Note:** The following requirements apply to both physical and virtual servers supporting up to 10 workstations. Requirements may be greater for servers supporting more than 10 workstations.

-   **Operating system:** 64-bit Windows Server 2012 R2
-   **CPU:** 1 or 2 Intel Xeon/AMD Opteron quad-core
-   **Memory:** 8 GB
-   **Hard disk type:** 3 or more drives configured as Raid 5, 7200 RPM
-   **Hard disk capacity:** 500 GB
-   **File system:** NTFS or ReFS
-   **Network:** High-speed Internet connection

### Installation

The SimTrans installation files are included with the SigmaNEST installation package. You can contact the Technical Support (page 223) team to request a USB flash drive with the installation files, or download the files directly from the SigmaTEK Connect site. Customers with a current maintenance subscription can download updates as they are released.

> **Warning:** During installation, you will be prompted to create or upgrade a database. **Do not upgrade your SigmaNEST database.** If you attempt to upgrade a SigmaNEST database, your data will be permanently lost. Create a new database instead.

#### Downloading the installation files

1.  In any web browser, visit connect.sigmanest.com.
2.  Click **Continue**, then enter your login information and click **Login**.
3.  In the **Support** section, click **Go**.
4.  In the **Product Downloads** section, click **Go**.
5.  A list of recent SigmaNEST releases is displayed. Find the most recent **Complete Image**, then click the **Download** button on the right.
    
    *   SigmaNEST Products
    *   SigmaNEST Release Notes (English) (pdf)
    *   SigmaNEST Complete Image (4.6 GB)
    *   SigmaNEST Product Only (647 MB)
    *   SigmaNEST Companion (513 MB)
    *   Color Offload (43 MB)
    *   Load Manager (36 MB)

6.  Save the .zip file to your computer, then right click it and select **Extract All** to extract the files.

#### Installing SimTrans

1.  Use Windows File Explorer to view the SigmaNEST USB drive, or the files you downloaded from the Connect site.
2.  Double-click **SNStartup.exe**.
3.  Hover your pointer over **Integration**, then select **SimTrans**.
    
    [Image: Screenshot of the SigmaNEST installer, highlighting the Integration menu with options for SimTrans, Load Manager, and Color Offload.]

4.  If prompted, click **Yes** to extract the Shop Floor (SimTrans) installer.
5.  Click **Install Shop Floor Products**.
6.  After the prerequisites have been installed, click **Next**.
7.  Select **SimTrans** and **SigmaNEST API** for installation.
8.  Choose whether to install SimTrans as a **32-bit** or **64-bit** program (we recommend 64-bit), then click **Next**.
9.  Click **Next** to begin the database installation.
10. Select an **SQL Server** to host the SimTrans database, then enter your login credentials.
11. If this is your first time installing SimTrans, enter a database name above the New Database button:
    -   Select **Load default data** if you want to add default values to the database.
    -   Select the database **Units** (imperial or metric).
    -   Click **New Database**. The database name is added to the **Databases** list.
12. If you are upgrading a previous installation of SimTrans, select the **Install** check box next to your existing database's **Name**.
    
    > **Warning:** Do not select your SigmaNEST database. If you attempt to upgrade a SigmaNEST database, your data will be permanently lost. Create a new database instead.

13. Click **Install/Update Database**. This step may take a few minutes.
14. When database setup is complete, click **Finish**.
15. In the **User name** box, enter the domain and user name that SimTrans will use when running as a background process. For example, if the domain name is SIGMATEK and the Windows user name is sigmanest.support, enter `SIGMATEK\sigmanest.support`.
16. Enter the **Password** associated with the Windows user name.
17. If you have other installed services that conflict with the SimTrans port numbers, you can modify the settings on the appropriate tab. Otherwise, click **Next**.
    
    > **Note:** Most users do not need to modify port numbers and can ignore these options. If you need to modify these settings, contact SigmaTEK Support or an IT professional for assistance.

18. Click **Next** to install SimTrans. This step may take a few minutes.
19. Enter your **Host** and **Port** in the Licensing Manager, then click **Refresh**.
20. Select your **Product** and **Add-ons**, then click **OK**.
21. Click the URL associated with SimTrans to open it in your default browser.

> **Note:** For additional assistance with installation, please contact the SigmaTEK Technical Support (page 223) team.

### SigmaNEST Setup

Before using SimTrans, you must enable the SimTrans-SigmaNEST connection in the SigmaNEST Configuration.

1.  In SigmaNEST, select the **Tools Help** tab and then click **Configuration**.
2.  Select the **System 2** tab, then select **Export Work Order information to SimTrans**.
    
    [Image: Screenshot of the SigmaNEST Configuration window on the System 2 tab, with the 'Export Work Order information to SimTrans' checkbox highlighted.]

3.  Click **OK** to save your changes.

### First-Time Setup

#### Log in

1.  Open any web browser and enter the SimTrans app URL.
    
    > **Tip:** By default, the URL is `http://{host PC name}:3000/`. If you changed the port number during installation, it is `http://{host PC name}:{port number}/`.

2.  Enter `admin` in the **Username** box and password in the **Password** box, then click **Log In**.
    
    [Image: Screenshot of the SimTrans login screen, showing fields for Username and Password.]

#### Change default Admin password

For security reasons, you should change the password associated with the default Admin account.

1.  On the toolbar, click **Users** (icon) > **Modify Users**.
    
    [Image: Screenshot of the SimTrans toolbar, showing the 'Users' menu with 'Modify Users' selected.]

2.  In the **Full Name** box, type `admin`.
3.  Enter a new **Password**, and then **Confirm Password**.
4.  (Optional) Link an **Email** address to the Admin account.
5.  Click **Modify User** to save your changes.

> **Tip:** See User Management (page 13) to learn more about adding and modifying users.

#### Verify application settings

1.  On the toolbar, click **Settings** (icon) > **Global Configuration**.
    
    [Image: Screenshot of the SimTrans toolbar, showing the 'Settings' menu with 'Global Configuration' selected.]

2.  In the **Transaction Filter** section, select **Process Transactions**.
    
    [Image: Screenshot of the Transaction Filter section in Global Configuration, with 'Process Transactions' and various sub-options checked.]

3.  Modify other settings as needed, then click **Save Changes**. To learn more about the Global Configuration settings, see Global Configuration (page 15).

#### Create a district

Districts are routing numbers used to connect SimTrans to specific SigmaNEST profiles. If you have multiple SigmaNEST installations, you can create unique district IDs and names for each connection.

[Image: Diagram showing SimTrans connecting to multiple SigmaNEST districts, each with a specific transaction type (e.g., SN70, SN88).]

> **Note:** SimTrans does not support the use of a Wide Area Network (WAN). If you need to manage remote sites, please contact SigmaTEK for more information on SimTrans Enterprise.

1.  On the toolbar, click **Settings** (icon) > **District Configuration**.
    
    [Image: Screenshot of the SimTrans toolbar, showing the 'Settings' menu with 'District Configuration' selected.]

2.  Enter a **District Name**, then click **Add New**.
    
    > **Tip:** You can name the district anything you want. Use something memorable that helps you associate the district with the linked SigmaNEST profile.

3.  Select the new district from the **Districts** list. The settings for the selected district will appear in the **District Details** section.
4.  Verify that the **SigmaNEST Path** is correct.
5.  Select a **SigmaNEST Profile** from the list to link the district to that profile.
    
    > **Tip:** The profile list is populated with previously created SigmaNEST profiles.

6.  Modify other settings as needed, then click **Save Changes**. Repeat the process as needed to add multiple districts. To learn more about the District Configuration settings, see District Configuration (page 18).

### User Interface

SimTrans has a minimalist design which displays transactions as they occur. After a specified number of transactions have run, the event log is cleared.

[Image: Screenshot of the SimTrans main user interface, showing the event log with a list of transactions, and controls to Start/Stop SimTrans.]

-   On the dashboard, click **Start** to begin transaction processing, or **Stop** to end it.
-   To view the transaction log, click **Dashboard** (icon).
-   To modify district settings, click **Settings** (icon) > **District Configuration**. See District Configuration (page 18) to learn more.
-   To modify program settings, click **Settings** (icon) > **Global Configuration**. See Global Configuration (page 15) to learn more.
-   To manage users, click **Users** (icon) > **Add User** or **Modify Users**. See User Management (page 13) to learn more.
-   To open the Help Center in a new tab, click **Help** (?).
-   To log out of SimTrans click **Log Out** (icon).

### User Management

You can use the User Management features to create accounts and set permissions for each SimTrans user.

> **Note:** Only admin users can add or modify user accounts.

#### Adding new users

1.  On the toolbar, click **Users** (icon) > **Add User**.
    
    [Image: Screenshot of the SimTrans toolbar, showing the 'Users' menu with 'Add User' selected.]

2.  Enter the user information. Select **Admin User** if you want the user to have administrative rights.

| Permissions | Admin User | Standard User |
| :--- | :---: | :---: |
| View dashboard | X | X |
| Start/stop SimTrans | X | X |
| Manage users | X | |
| Modify district settings | X | |
| Modify global settings | X | |

3.  Click **Add User** to create the account. Repeat the process as needed to add multiple users.

#### Modifying existing users

1.  On the toolbar, click **Users** (icon) > **Modify Users**.
    
    [Image: Screenshot of the SimTrans toolbar, showing the 'Users' menu with 'Modify Users' selected.]

2.  Modify the user's information as needed. Select **Admin User** if you want the user to have administrative rights.

| Permissions | Admin User | Standard User |
| :--- | :---: | :---: |
| View dashboard | X | X |
| Start/stop SimTrans | X | X |
| Manage users | X | |
| Modify district settings | X | |
| Modify global settings | X | |

3.  Click **Modify User** to save your changes.

### Global Configuration

You can use the Global Configuration settings to customize how your transactions are processed. To access these settings, click **Settings** (icon) > **Global Configuration** on the toolbar. After you have finished modifying the settings, click **Save Changes** to apply them.

[Image: Screenshot of the SimTrans toolbar, showing the 'Settings' menu with 'Global Configuration' selected.]

> **Note:** Only admin users can access the Global Configuration settings.

#### Language

-   If you want to change the **Language**, select a language from the list.

#### Transaction Processing

-   To automatically start processing when you sign in to Windows, select **Auto start**.
-   To change how often SimTrans checks for new transactions, enter the **Time interval** in seconds.
-   To limit the number of transactions recorded in the transaction log, select **Limit transaction log to**. Then enter the maximum number of **old records** to save.
-   To limit the number of events recorded in the event log, select **Limit event log to**. Then enter the maximum number of **old records** to save.
-   To set how many lines are displayed in the transaction and event logs, enter the maximum number of **log lines**.
-   To set the maximum allowed amount of time before each request times out, enter the **Max request time**.

#### Transaction Filter

Use the transaction filters to choose allowed transaction types. Any types that are not selected will not be processed. The table below lists sample transactions for each type.

| Transaction Type | Sample Transaction(s) |
| :--- | :--- |
| New orders | SN80, SN83, SN84, SN85 |
| Modify orders | SN81 |
| Cancel orders | SN82 |
| New stock | SN90, SN94 |
| Modify stock | SN91 |
| Remove stock | SN92 |
| Cut-to-Length | CTLx |

#### Part Transactions

-   To allow part files with invalid geometry, select **Handle invalid part geometry in SigmaNEST**. You can then use the repair functions in SigmaNEST to repair invalid parts.
-   To allow part files with missing geometry, select **Allow undefined part orders (SN84)**. You can then add the geometry in SigmaNEST to define it before nesting. See SN84 Add Existing Part to Order (page 120) for more information.
-   To allow CAD files with missing geometry, select **Allow undefined CAD orders (SN85)**. You can then add the geometry in SigmaNEST to define it before creating a part. See SN85 Add CAD Part to Order (page 126) for more information.
-   To enable subfolder searching in transaction SN84, select **Search part library for part files to load (SN84)**. See SN84 Add Existing Part to Order (page 120) for more information.
-   To enable subfolder searching in transaction SN79, select **Search part library for part files to delete (SN79)**. See SN79 Delete Part File (page 103) for more information.
-   To allow transactions that will result in a part quantity of 0, select **Process Qty = 0 for SN81B**.
    If this option is not selected, SimTrans blocks these transactions and logs them as errors. See SN81B Modify Work Order Parts (Balance Qty) (page 112) for more information.

#### Sheet Transactions

-   To allow transaction SN91A to create new sheets, select **Add sheets with SN91A if they don't exist yet**. See SN91A Modify Stock (Allow Qty = 0) (page 147) for more information.
-   To allow SN91A transactions that will result in a sheet quantity of 0, select **Delete sheets with 91A when Qty available = 0**.
    If this option is not selected, SimTrans blocks these transactions and logs them as errors. See SN91A Modify Stock (Allow Qty = 0) (page 147) for more information.

#### Contact Management

-   To allow transaction QT10 to edit customer information, select **Allow customer add transaction (QT10) to modify existing customers**.
    If this option is not selected, transaction QT10 adds another customer of the same name. See QT10 Add Customer (page 164) for more information.
-   To allow transaction QT20 to modify existing customer addresses, select **Allow address add transaction (QT20) to modify existing addresses**.
    If this option is not selected, transaction QT20 will add a new address. See QT20 Add Address (page 169) for more information.

#### Error Reporting

To report errors via email, select **Email errors to admin**.

-   In the **Reporting interval** box, enter how often the admin will be emailed (in minutes).
-   Enter the email information and login credentials to be used when reporting errors.

#### Failed Transactions

To remove failed transactions from the dashboard, select **Remove these transactions if they fail**. Then, select which transactions to remove.

If this option is not selected, failed transactions will be flagged with an error so that you can resolve the issue.

### District Configuration

Districts are routing numbers used to connect SimTrans to specific SigmaNEST profiles. You can configure each district individually using the District Configuration settings.

[Image: Diagram showing SimTrans connecting to multiple SigmaNEST districts, each with a specific transaction type (e.g., SN70, SN88).]

To access these settings, click **Settings** (icon) > **District Configuration** on the toolbar. Select a district from the list, then view and edit the settings on the right. After you have finished modifying the settings, click **Save Changes** to apply them.

> **Note:** This section describes how to customize an existing district. To learn how to set up a new district, see Create a district (page 10).
> 
> **Note:** Only admin users can access the District Configuration settings.

#### District Details

Select an existing district from the left list to view its details. You can modify the following fields as needed:

-   **District number:** The unique identifier associated with a district.
-   **District name:** A memorable name that helps you associate the district number with the linked SigmaNEST profile.
-   **SigmaNEST profile:** The exact name of the SigmaNEST profile that the district is linked to.
-   **SigmaNEST path:** The path to the SigmaNEST executable. (This field cannot be modified.)
-   To run a batch (.wol) file before or after processing transactions, enter the name or path in the **Execute before** or **Execute after** box.
-   If you entered the batch file's name, but not the path, enter the **Batch path**.

> **Note:** The **Batch path** is the default for all **Execute before** and **Execute after** commands, unless a different path is specified in those fields.

#### File Input

You can use the File Input settings to automatically import data files from other sources, such as an MRP or ERP system. See Importing External Data (page 26) for more information.

#### Geometry Conversion

You can use geometry conversion to automatically convert CAD drawings into SigmaNEST parts. See Geometry Conversion (page 29) for more information.

#### Program Feedback

The feedback from posted, updated, and deleted programs is written to the STxxARC tables in the SigmaNEST database. MRP and ERP systems can then read, modify, or delete the data. You can use the following options to customize the feedback settings.

-   To automatically archive completed work orders, select **Archive completed work orders**. If this option is not selected, the work orders must be manually archived.
-   If you have SimTrans Enterprise Client, select **Process SigmaNEST feedback** to enable communication between large, multi-district systems and SimTrans.
-   If you want to run a batch (.wol) file before or after processing feedback, enter the path or file name in the appropriate box. If the path is not specified, the **Batch path** set in the District Details (page 19) is used.

#### Work Order Export

If you want to export work orders and quotes to a specially formatted data file, see Exporting Work Order Data (page 30).

> **Note:** This option is typically used for MRP or ERP systems with specific formatting requirements.

#### Quote Feedback

To write quote feedback to the STxxARC tables in the SigmaNEST database, select **Process quote feedback**. This makes quote data available to your MRP or ERP system. Then, select the quote statuses that will be written to the tables.

-   **Active** refers to new quotes that are not yet submitted.
-   **Pending** refers to quotes that were submitted to the customer.
-   **Order received** refers to quotes which have been converted to work orders.
-   **Order lost** designates quotes which have been declined by the customer.

If you want to run a batch (.wol) file before or after processing quote feedback, enter the path or file name in the appropriate box. If the path is not specified, the **Batch path** set in the District Details (page 19) is used.

#### Part Load and Save Paths/CAD File Retrieval Path

The part load and save paths are used in transactions SN83 and SN84. These fields use a series of variables to designate where SimTrans should search for or save a part.

Similarly, the CAD file retrieval path is used in transaction SN85. It uses a specified path to designate where SimTrans searches for CAD files.

See Part and CAD Retrieval Paths (page 32) to learn how to construct paths for these fields.

#### Sheet Replace

You can use the sheet replace options to specify how sheet swapping and remnants are handled.

-   To allow sheet swapping between programs that are already in process, select **Swap when assigning with a sheet in process**.
-   To rename remnants based on the default sheet name, select **Rename remnant based on new sheet name**.
    For example, the remnant of Sheet1 is named Sheet1\_1 by default. Selecting this option renames the remnant Sheet2 instead.
-   To adjust the remnant suffix, modify the **Remnant name suffix**.
    For example, the default suffix is an underscore (\_), so the remnant of Sheet1 is named Sheet1\_1 by default. If you change the suffix to a hyphen (-), the remnant of Sheet1 will be named Sheet1-1 instead.
-   If you want to prevent specific database fields from being carried over from the sheet to the remnant, enter those fields in the **Fields excluded from transfer to remnant** box.

#### Event Types

The SimTrans event log is stored in the Event Log table of the TransAct database. The following table is a reference to all event types which may appear in the log.

| Event Type | Description |
| :--- | :--- |
| Program started | SigmaNEST profile not set |
| Program ended | Import data produced errors |
| Processing started | Import data nothing to do |
| Processing complete | Required field not supplied |
| Processing district | File processed |
| Import data started | WO export started |
| Import data complete | WO export completed |
| Batch file start | WO export no fields selected |
| Batch file complete | WO export folder does not exist |
| Archive WO start | WO export failed |
| Archive WO complete | Bin data not found |
| Archive WO error | Cannot unlock ZIP DLL |
| DB busy | Error unzipping file |
| No DB | Plugin warning |
| Newer SN version required | Plugin error |
| Trans disabled | Plugin message |
| Invalid trans type | Invalid shapes or parameters |
| SIM module required | Work order already exists |
| Trans converted to SN80 | No sheet name |
| Trans complete | Sheet already exists |
| Trans incomplete | Sheet in process |
| All trans started | Trying to remove more sheets than available |
| All trans complete | Sheet does not exist |
| Eng conv started | Sheet length or width zero |
| Eng conv complete | Part in process |
| Geometry conv | Sheet quantity cannot be zero |
| Geometry conv error | Could not load district |
| CTL processing disabled | No districts were processed |
| Exception | SigmaNEST error feedback |
| DB connection not set | Could not write sheet to DB |
| DB needs upgrade | Table missing |
| Feedback processing needs tables | Field missing |
| Feedback processing started | Cannot connect to SigmaNEST |
| Feedback processing complete | Trying to reconnect to SigmaNEST |
| Feedback processing failed | Connected to SigmaNEST |
| Feedback transferring | SP missing |
| Import data failed | Quote feedback needs tables |
| SIM not found | Quote feedback failed |
| Mat cost clearance density not set | Quote feedback started |
| File not found | Quote feedback complete |
| File deleted | SigmaNEST did not close properly |
| Directory not found | Program sheet replace no sheet found |
| SIM error | Program sheet replace multi sheet specify sheet |
| Config settings missing | Program sheet replace not enough available |
| Config file missing | Program sheet replace could not swap |
| SigmaNEST profile does not exist | Material cost update |

#### Importing External Data

You can set up SimTrans to automatically import data files from other sources, such as an MRP or ERP system. To do this, use the Import Spec Generator to determine how the data will be mapped. Then, select a folder to be monitored. Whenever SimTrans is running, it will monitor this folder for new data files, immediately processing the files as they are added to the folder.

**Enabling external data import**

1.  In the **District Configuration**, select a district and then scroll down to the **File Input** settings.
2.  Select **Input external data source**.
3.  In the **Input file extension** box, enter the extension of the file(s) to be imported (for example, .csv). The following file types are currently supported:

| Text | Lotus 1-2-3 | Paradox | ADO connection | HTML, XML |
| :--- | :--- | :--- | :--- | :--- |
| Word | Quattro Pro | Dbase | Advantage Table | |
| Excel | SPSS | MS Access | DBISAM Table | |

4.  In the **File import specification** box, enter the path to the .smi file. This file determines how the imported data is mapped. See Creating the mapping (.smi) file (page 26) for more information about .smi files.
5.  In the **Input file path** box, enter the path to the folder that will be monitored for new data files.
6.  In the **Processed file path** box, enter the path to the folder where the data files will be moved after they are processed.

**Creating the mapping (.smi) file**

1.  Open the Import Spec Generator (located in the SimTrans program folder).
2.  Click **Create**.
3.  Select a file type to import, then click **Next**.
    
    [Image: Screenshot of the SimTrans Import Spec Generator and the Import Wizard showing file format selection.]

4.  Click the ellipsis (...) next to the **Import from File** box. Then, browse to the location of the file to be imported and click **Open**.
5.  If the file originated in MS DOS, use the **File Origin** list to select **ANCII (MS\_DOS)**.
6.  Click **Next** to view the text settings.
7.  Choose the delimiter and record separator parameters that are appropriate to your file, then click **Next**.
8.  Enter the **First row** where the data starts (by default, this is 1). You can enter a **Last row**, or leave it blank.
9.  Modify the date, time, and number settings as needed to fit your data, then click **Next**.
10. A preview of the imported data is displayed. If you want to make changes to the import settings, click **Back** and modify the settings as needed.
11. If your data is displayed correctly, right click the column headings and select the appropriate fields to map the data to. When you have finished, click **Next**.
12. A list of database variables and their corresponding mapped fields are displayed. You can click the ellipsis (...) next to a source field to use the Expression Builder, if needed. After you have verified all the data, click **Next**.
13. A preview of your data is displayed. Click **Next** to confirm.
14. Select **Append: add records to the destination table**, then click **Execute** to begin the import. The TransAct table will be populated with the selected data.

#### Geometry Conversion

You can set up SimTrans to automatically convert CAD files to SigmaNEST part files. To do this, use the steps below to enable geometry conversion in the District Configuration (page 18), then select a folder to be monitored. Whenever SimTrans is running, it will monitor that folder for new CAD files, immediately processing the files as they are added to the folder.

> **Note:** SimTrans only processes CAD file types associated with purchased SigmaNEST modules. For example, if you place a SOLIDWORKS part in the folder, it will only be processed if you have purchased the SOLIDWORKS Import module.

1.  In the **District Configuration**, select a district and then scroll down to the **Geometry Conversion** settings.
2.  Select **Convert engineering drawings**.
3.  If you want to allow invalid geometry, select **Handle invalid part geometry in SigmaNEST**. You can then use the repair functions in SigmaNEST to repair the invalid geometry.
4.  In the **Engineering drawings source path** box, enter the path to the folder that will be monitored for new CAD files.
5.  In the **Engineering part target** box, enter the path to the folder where the CAD files will be moved after they are processed.
6.  If you want to run a batch (.wol) file before or after geometry conversion, enter the path or file name in the appropriate box. If the path is not specified, the **Batch path** set in the District Details (page 19) is used.
7.  Select the system that the CAD files were created in from the **CAD system associated with .PRT files list**.
8.  Click **Save Changes** (located below the district list).

#### Exporting Work Order Data

If your MRP or ERP system has specific formatting requirements, you can export work order and quote data to specially formatted data files. Use the following steps to set up the export options.

1.  In the **District Configuration**, select a district and then scroll down to the **Work Order Export** settings.
2.  Select **Work order and quote export**.
3.  Select a naming convention for exported quotes and work orders from the **File name / Order by** list.
4.  In the **Export folder** box, enter the path where the exported files will be located.
5.  Specify the file **Extension** for the exported files (for example, .csv).
6.  If you want, you can modify the **Column** and **Text delimiters** to change which characters are used to separate columns and text.
7.  Specify the **Date time format** to be used in the exported file. You can use any combination of separators and variables (displayed in the following table).
    For example, enter `m/d/yyyy` to format dates like this: 9/14/2018.
    Or, enter `dddd, mmmm d, yyyy` to format dates like this: Friday, September 14, 2018.

| Format Specifier | Variable | Example |
| :--- | :--- | :--- |
| Date (numerical) | `d` or `dd` | 1 or 01 |
| Day of the week (abbreviated) | `ddd` | Mon |
| Day of the week (full) | `dddd` | Monday |
| Month (numerical) | `m` or `mm` | 1 or 01 |
| Month (abbreviated name) | `mmm` | Jan |
| Month (full name) | `mmmm` | January |
| Year (numerical) | `yy` or `yyyy` | 18 or 2018 |

8.  Use the **Select From** list to choose the which database tables to export data from.
9.  If you selected a predefined set of tables (for example, `wo`, `Part`), use the **Export Fields** box to specify which data fields will be exported.
10. If you selected **Custom**, build a custom SQL query in the provided fields.
    
    > **Tip:** Need help? Contact your Services Representative or SigmaTEK's Technical Support (page 223) team for assistance with custom SQL queries.

11. Click **Save Changes** (located below the district list).

### Part and CAD Retrieval Paths

The part load and save paths use variables to determine where SimTrans searches for or saves a part. Similarly, the CAD file retrieval path determines where SimTrans searches for CAD files. You can set each of these paths in the District Configuration (page 18).

-   The **Part retrieval path** is used in transaction SN84 to designate where SimTrans looks for the specified part file.
-   The **Part creation path** is used in transaction SN83 to designate where SimTrans creates new parts.
-   The **CAD file retrieval path** is used in transaction SN85 to designate where SimTrans looks for the specified geometry file.

#### Constructing a path

You can use the variables in the table below to construct the path of your choice.

-   Each path variable is replaced with the data from the appropriate cell in the TransAct table when the transaction runs.
-   Variables can be used in combination with each other and/or with static text.
-   Each variable must be enclosed in angle brackets (<>), or it will be interpreted as static text.
-   Variables are not case-sensitive.

#### Path variables

| Variable | Definition |
| :--- | :--- |
| `<STPARTS>` | The SigmaNEST parts path (as defined in the SigmaNEST Configuration) |
| `<WO>` | The work order that contains the part |
| `<MATERIAL>` | The part's material |
| `<THICKNESS>` | The part's thickness, where decimal points are replaced by underscores (for example, 0.100 becomes 0\_100) |
| `<CUSTOMER>` | The customer who ordered the part |
| `<DWGNUMBER>` | The part's drawing number |
| `<REVNUMBER>` | The part's revision number |
| `<PROCESS>` | The machine process used to cut the part |
| `<PROGBY>` | The person who programmed or created the part |
| `<REMARK>` | Remarks associated with the part |
| `<ITEMDATA 1>` - `<ITEMDATA 18>` | Item data fields associated with the part |
| `<YEAR>` | The current year as a four-digit numerical value |
| `<MONTH>` | The current month as a numerical value between 1 and 12 |
| `<DAY>` | The current day of the month as a numerical value between 1 and 31 |

**Example**

If you want to save your parts to a customer subfolder inside the SigmaNEST parts folder, enter `<STPARTS>\<CUSTOMER>`.

If the parts path is `C:\SNDATA\Parts` and the customer is SigmaTEK, the parts will be saved to `C:\SNDATA\Parts\SigmaTEK`.

#### CAD file retrieval options

-   To enter a path using a combination of static text and variables (as in the examples above) select **Use this path**, then enter the path.
-   To use the CAD folder specified in SigmaNEST, select **Use SigmaNEST configured CAD folders**.
-   To use the part retrieval path specified in the **Part load and save paths** section, select **Use part retrieval path**.

### About Plugins

The SigmaTEK Services Group creates custom plugins for cases where you need specialized functionality. To learn more about custom plugins, contact your Services Representative, or SigmaTEK's Technical Support (page 223) team.

## Chapter 2: Using SimTrans

SimTrans operates by running transactions from your MRP or ERP system, then returning feedback. In this section, you will learn how transactions and feedback work.

### About Transactions

Transactions are units of work that are performed against a database. Changes made during a transaction are permanently committed if the transaction is successful. However, all changes are reverted to their original state if an error occurs during the transaction.

You can use transactions to add or modify stock and work orders, create SigmaNEST parts, and more. To view a complete reference to all transactions, see Transaction Reference (page 71).

#### How do transactions work?

Transactions are initiated by your MRP or ERP system and read by SimTrans. SimTrans then executes the transaction, passes any changed information to the SigmaNEST database, and updates the transaction log. If the transaction fails, no changes are made and SimTrans logs an error instead.

[Image: A diagram showing the flow of a transaction. 1) MRP/ERP system initiates the transaction. 2) SimTrans reads the transaction from the SimTrans Database. 3) SimTrans executes the transaction in SigmaNEST. 4) SigmaNEST updates its database (Work orders, Stock, Remnants, Parts). 5) SimTrans logs the transaction result.]

#### How are transactions created?

Transactions are loaded into the TransAct table in SimTrans. We recommend using one of the following methods to create transactions.

-   Directly edit the TransAct table using the SigmaNEST SQL Manager.
-   Enter the data through an SQL query.
    
    > **Note:** The SQL connection string is located in: `C:\inetpub\wwwroot\SimTransApi\Web.config > connectionStrings > SimTransContext`

-   Import a .csv file into the TransAct table.

#### When are transactions processed?

SimTrans checks for transactions based on your transaction processing settings. You can use the following steps to change how often SimTrans checks for new transactions.

1.  Click **Global Configuration**.
2.  In the **Transaction Processing** section, modify the **Time interval (seconds)**.
3.  Click **Save Changes**.

### Transaction Variables

The following table contains a complete list of all transaction variables, including data types and definitions.

| Variable | Type | Definition |
| :--- | :--- | :--- |
| **TransType** | varchar10 | Transaction number, for example SN60 or CTL22. |
| **District** | int | Unique database identifier. |
| **TransID** | varchar10 | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | Work order number. |
| **ItemName** | varchar50 or 100 | Part or stock name. Use varchar100 for part names. Use varchar50 for stock names. |
| **Qty** | int | Number of parts to order, sheets to add, etc. |
| **Material** | varchar50 | Material type (as defined in SigmaNEST). |
| **Thickness** | float | Material thickness. |
| **DueDate** | datetime | Work order due date. |
| **Customer** | varchar50 | Customer name. |
| **DwgNumber** | varchar50 | Drawing number associated with the part. |
| **Priority** | int | Part priority (as defined in SigmaNEST). |
| **ProgBy** | varchar50 | Name of programmer associated with the part. |
| **FileName** | varchar255 | Part or geometry file name. |
| **Length** | float | Sheet length or CTL part/stock length. |
| **Width** | float | Stock width. |
| **Remark** | varchar80 | Remark associated with the SigmaNEST part. |
| **RevNumber** | varchar50 | Revision associated with the SigmaNEST part. |
| **Cost** | float | Cost of the part or material. |
| **HeatNumber** | varchar50 | Heat number associated with the stock. |
| **ItemType** | int | For parts, 0 = standard part, 1= filler part. For stock, 0 = sheet, 1 = remnant, 2 = coil. |
| **OnHold** | bit (0,1) | 0 = not on hold, 1 = on hold (on hold means that the order is on hold and the part is not available for nesting). |
| **TypeDescr** | varchar50 | For SN85 transactions, the geometry file type (DXF, DWG, IGES, etc.). For CTL transactions, the part profile type. |
| **BinNumber** | varchar50 | Bin number associated with the stock. |
| **Location** | varchar50 | For stock transactions, the stock location. For quote transactions, the customer location. |
| **Mill** | varchar50 | Mill quality associated with the stock. |
| **PrimeCode** | varchar50 | Prime code associated with the stock. |
| **ItemData1-18** | varchar50 | Extra data fields associated with SigmaNEST parts. |
| **OrderShape** | varchar50 | Name of the SigmaNEST standard shape. |
| **ProgramName** | varchar50 | NC program name. |
| **ProgramRepeat**| int | value > 0 = specific repeat to update. 0 = update all repeats. |
| **BatchFile** | varchar255 | Batch file path to run before creating the part. |
| **Process** | varchar50 | The machine name/ID. |
| **StringData1-8** | varchar50 | Batch commands to run before creating the part, or other parameters as specified in the transaction. |
| **Param1-8** | float | Standard shape parameters, or other parameters as specified in the transaction. |
| **IDNegTol** | float | See Tolerance Values (page 44) for information about this variable. |
| **IDPosTol** | float | See Tolerance Values (page 44) for information about this variable. |
| **ODNegTol** | float | See Tolerance Values (page 44) for information about this variable. |
| **ODPosTol** | float | See Tolerance Values (page 44) for information about this variable. |
| **ErrorTag** | Boolean | true = transaction failed, false = transaction was successful. |
| **ItemID** | int | Unique customer or address ID used in QT transactions. |
| **PluginTag** | N/A | Reserved. |
| **SalesRep** | varchar50 | Sales representative ID. |
| **DueDateFormula**| varchar20 | Today ± offset. For example, Today+3 sets the due date to three days after the current day. |
| **TaxRate** | float | Tax rate as a percentage. |
| **StartDate** | datetime | Program start time. |
| **EndDate** | datetime | Program end time. |

### Tolerance Values

Tolerance values are only used for SN83 Add Standard Shape Part to Order (page 116) transactions, in cases where the standard shape (OrderShape data field) is RECT, DISK, GUSS, or RING. These values make allowances for machine error and/or manufacturing compensation, as requested by the customer.

For example, if you are manufacturing an assembly where a pipe fits through the diameter of a ring, it is better for the ring to be slightly larger rather than slightly smaller, because the pipe will not fit if the ring is too small. This is an example of positive tolerance on the diameter of the ring. You can also apply negative tolerances, depending on your assembly configuration.

#### Tolerance data fields

The following data fields are used to specify allowed tolerances in the TransAct database:

-   **ODPosTol** (outer diameter positive tolerance)
-   **ODNegTol** (outer diameter negative tolerance)
-   **IDPosTol** (inner diameter positive tolerance)
-   **IDNegTol** (inner diameter negative tolerance)

#### Example

For example, the part in the image below was created using an SN83 transaction with the following parameters: OrderShape = DISK, Param1 (diameter) = 10.00, ODPosTol = 0.040, and ODNegTol = 0.020.

[Image: A diagram of a 10" disk with a positive tolerance of .04 and a negative tolerance of .02.]

The outer diameter is then calculated to be the base value plus the average of the two tolerances, or `10.00 + {(0.040 - 0.020) / 2} = 10.010`.

### Transaction Chart

A complete transaction chart listing all transactions and their applicable variables is available online.

-   Spreadsheet: https://goo.gl/nmxuaf
-   PDF: https://goo.gl/h8W2pM

> **Tip:** See Transaction Reference (page 71) for a complete reference to all transactions, or Transaction Variables (page 38) for a description of each transaction variable.

### About Feedback

Feedback is an output of information that shows the result of a successful transaction. SigmaNEST writes feedback to the STxxARC tables in the SigmaNEST database when programs are posted, updated, or deleted.

[Image: A diagram illustrating the feedback flow from SimTrans/SigmaNEST to the STxxARC tables in the SigmaNEST Database, which can then be read by an MRP/ERP system.]

#### How does feedback work?

After SigmaNEST writes the feedback to the STxxARC tables, MRP and ERP systems can read, modify, or delete the data. Typically, you should set up your system to import data from the feedback tables and then delete the entries from the tables. This prevents data from being accidentally re-imported into your MRP or ERP system, which will result in unwanted duplicates.

> **Note:** Feedback tables are only intended to contain information temporarily. They do not act as a transaction archive.

#### Feedback types

There are six feedback processes that each write back to different tables in the SigmaNEST database. Each type of SimTrans transaction (sheet, remnant, work order, etc.) has a corresponding feedback type. For example, STWOARC feedback is for transactions that add, modify, or delete work orders. Select one of the following feedback types to learn more.

-   [Feedback: Parts in Process (page 48)](#feedback-parts-in-process)
-   [Feedback: Programs (page 52)](#feedback-programs)
-   [Feedback: Completed Parts (page 56)](#feedback-completed-parts)
-   [Feedback: Remnants (page 61)](#feedback-remnants)
-   [Feedback: Sheets (page 64)](#feedback-sheets)
-   [Feedback: Archived Work Orders (page 69)](#feedback-archived-work-orders)

#### Feedback: Parts in Process

The STPIPARC feedback table contains information about parts that are currently marked as "in process." SigmaNEST writes feedback to this table when work order parts are:

-   Posted
-   Updated
-   Deleted

The following list displays all variables in the STPIPARC table.

**STPIPARC Feedback Variables**

| Variable | Type | Definition |
| :--- | :--- | :--- |
| **ProgramName** | varchar50 | NC program name. |
| **RepeatID** | int | Repeat ID number of the program, if it was repeated multiple times. |
| **PartName** | varchar100 | Part name. |
| **SheetName** | varchar50 | Stock name. |
| **WONumber** | varchar50 | Work order number. |
| **QtyInProcess** | int | Number of parts being processed. |
| **PartLength** | float | Rectangular length of the part. |
| **PartWidth** | float | Rectangular width of the part. |
| **TrueArea** | float | True area of the part. |
| **RectArea** | float | Rectangular area of the part (smallest rectangle around the part). |
| **NestedArea** | float | Total area of nested parts and scrap. |
| **TrueWeight** | float | True weight of the finished part. |
| **RectWeight** | float | Rectangular weight of the finished part (smallest rectangle around the part). |
| **CuttingTime** | float | Estimated cutting time in seconds. |
| **CuttingLength**| float | Actual cutting length of the part. |
| **PierceQty** | int | Number of pierces in the part. |
| **TrueCost** | float | Cost of the true part shape using the average material cost. |
| **RectCost** | float | Cost of the rectangular part shape (smallest rectangle around the part). |
| **NestedCost** | float | Part cost, including scrap. |
| **MaterialCost** | float | Cost of the material used in the part. |
| **ProcessCost** | float | Cost of the process(es) used in the part. |
| **OutsourceCost**| float | Cost to outsource part. |
| **DrawingCost** | float | Cost of the part drawing. |
| **LineItemNumber**| N/A | Reserved. |
| **DueDate** | datetime | The part's due date (using the system's datetime format). |
| **TransType** | varchar50 | Text description of the transaction, for example, SN100 - posted, SN101 - deleted, or SN102 - updated. |
| **TotalCuttingTime**| float | Total time to cut all instances of the part (quantity x cutting time). |
| **MasterPartQty**| int | Initial part quantity, as specified during part creation. |
| **WOState** | int | 0 = unknown, 1 = complete (all parts included on one sheet), 2 = started (parts started across more than one sheet), 3 = continued (between started and finished), 4 = finished (parts finished across more than one sheet. |
| **RevisionNumber**| varchar50 | Revision associated with the SigmaNEST part. |
| **ArchivePacketID**| int | Field used by SigmaNEST for database tracking. |
| **ActualDuration**| float | Actual duration of the program. |

#### Feedback: Programs

The STPrgARC feedback table contains information about NC programs. SigmaNEST writes feedback to this table when an NC program is:

-   Posted
-   Deleted
-   Updated

The following list displays all variables in the STPrgARC table.

**STPrgARC Feedback Variables**

| Variable | Type | Definition |
| :--- | :--- | :--- |
| **ProgramName** | varchar50 | NC program name. |
| **RepeatID** | int | Repeat ID number of the program, if it was repeated multiple times. |
| **SheetName** | varchar50 | Stock name. |
| **Multisheet** | bit (0,1) | 0 = no multisheet nest, 1 = multisheet nest (sheets combined into a single layout). |
| **TaskName** | varchar50 | Task name. |
| **UsedArea** | float | Nested area of parts (used to determine yield). |
| **ScrapFraction** | float | Scrap area divided by area of sheet used (calculated by SigmaNEST). |
| **QtyInProcess** | int | Number of parts being processed. |
| **MachineName** | varchar50 | Name of machine. |
| **CuttingTime** | float | Estimated cutting time in seconds. |
| **PierceQty** | int | Number of pierces in the part. |
| **JobCost** | N/A | Reserved. |
| **PostDateTime** | datetime | Post date and time (using the system's datetime format). |
| **TransType** | varchar50 | Text description of the transaction, for example, SN100 - posted, SN101 - deleted, or SN102 - updated. |
| **CompDate** | N/A | Reserved. |
| **MachineID** | int | Machine name or ID (as defined in Load Manager). |
| **CutStartTime** | datetime | Program start time. |
| **CutEndTime** | datetime | Program end time. |
| **StaticCount** | N/A | Reserved. |
| **ArchivePacketID**| int | Field used by SigmaNEST for database tracking. |
| **ActualDuration**| float | Actual duration of the program. |
| **ActualStartTime**| float | Actual start time of the program. |
| **ActualEndTime** | float | Actual end time of the program. |
| **ActualState** | N/A | Reserved. |
| **CellName** | varchar50 | Machine cell name (as defined in Load Manager). |
| **LMMachineName**| varchar50 | Machine name or ID (as defined in Load Manager). |
| **UnloadLocation**| N/A | Reserved |
| **Tray** | N/A | Reserved |
| **StorageTime** | N/A | Reserved |
| **OperatorName**| varchar50 | Operator name (as defined in Color Offload). |
| **MinDueDate** | datetime | The earliest part due date in the program. |
| **StopReason** | varchar250 | Reason program was stopped. |
| **TimeLineID** | int | Field used by SigmaNEST for database tracking. |
| **Comment** | varchar255 | Comment added when posting the program from SigmaNEST. |
| **PostedByUserID**| int | SigmaNEST user ID. |

#### Feedback: Completed Parts

The STPrtARC feedback table contains information about parts that have been successfully cut. SigmaNEST writes feedback to this table when an NC program containing a completed part is updated.

**STPrtARC Feedback Variables**

| Variable | Type | Definition |
| :--- | :--- | :--- |
| **WoNumber** | varchar50 | Work order number. |
| **PartName** | varchar100 | Part name. |
| **ProgramName** | varchar50 | NC program name. |
| **RepeatID** | int | Repeat ID number of the program, if it was repeated multiple times. |
| **SheetName** | varchar50 | Stock name. |
| **PartFileName** | varchar255 | Full path and filename of the specified part. |
| **Material** | varchar50 | Material type (as defined in SigmaNEST). |
| **Thickness** | float | Material thickness. |
| **DrawingNumber** | varchar50 | Drawing number associated with the part. |
| **ProgrammedBy** | varchar50 | Name of programmer associated with the part. |
| **DueDate** | datetime | The part's due date (using the system's datetime format). |
| **Data1-18** | varchar250 | Extra data fields associated with SigmaNEST parts. |
| **QItemID** | varchar50 | Quote ID number. |
| **Description** | varchar50 | Description of the part. |
| **QtyOrdered** | int | Original part quantity ordered. |
| **QtyProgram** | int | Quantity of the part included in the specified program. |
| **SpecialProperties** | N/A | Reserved. |
| **SpecialProperties1-3**| N/A | Reserved. |
| **PartLength** | float | Rectangular length of the part. |
| **PartWidth** | float | Rectangular width of the part. |
| **TrueArea** | float | True area of the part. |
| **RectArea** | float | Rectangular area of the part (smallest rectangle around the part). |
| **NestedArea** | float | Total area of nested parts and scrap. |
| **TrueWeight** | float | True weight of the finished part. |
| **RectWeight** | float | Rectangular weight of the finished part (smallest rectangle around the part). |
| **CuttingTime** | float | Estimated cutting time in seconds. |
| **CuttingLength**| float | Actual cutting length of the part. |
| **PierceQty** | int | Number of pierces in the part. |
| **TrueCost** | float | Cost of the true part shape using the average material cost. |
| **RectCost** | float | Cost of the rectangular part shape (smallest rectangle around the part). |
| **NestedCost** | float | Part cost, including scrap. |
| **MaterialCost** | float | Cost of the material used in the part. |
| **ProcessCost** | float | Cost of the process(es) used in the part. |
| **OutsourceCost**| N/A | Reserved. |
| **DrawingCost** | N/A | Reserved. |
| **LineItemNumber**| N/A | Reserved. |
| **Remark** | varchar80 | Remark associated with the SigmaNEST part. |
| **TotalCuttingTime**| float | Total time to cut all instances of the part (quantity x cutting time). |
| **MasterPartQty**| int | Initial part quantity, as specified during part creation. |
| **ArcDateTime** | datetime | Date and time the part was archived (using the system's datetime format). |
| **ArchivePacketID**| int | Field used by SigmaNEST for database tracking. |
| **ActualWeight** | float | Actual weight as defined in SigmaNEST. |

#### Feedback: Remnants

The STRemARC feedback table contains information about remnants that were created during the cutting process. SigmaNEST writes feedback to this table when the remnant is checked back into inventory (during program update).

**STRemARC Feedback Variables**

| Variable | Type | Definition |
| :--- | :--- | :--- |
| **RemnantName** | varchar50 | Remnant name. |
| **ProgramName** | varchar50 | NC program name. |
| **RepeatID** | int | Repeat ID number of the program, if it was repeated multiple times. |
| **Material** | varchar50 | Material type (as defined in SigmaNEST). |
| **Thickness** | float | Material thickness. |
| **Length** | float | Rectangular length of the remnant. |
| **Width** | float | Rectangular width of the remnant. |
| **Area** | float | True area of the remnant. |
| **Qty** | int | Number of remnants. |
| **Cost** | float | Cost of the remnant. |
| **Location** | varchar50 | Sheet location. |
| **HeatNumber** | varchar50 | Heat number associated with the stock. |
| **BinNumber** | varchar50 | Bin number associated with the stock. |
| **Mill** | varchar50 | Mill quality associated with the stock. |
| **PrimeCode** | varchar50 | Prime code associated with the stock. |
| **SheetType** | int | 0 = remnant, 1 = stock, 2 = coil. |
| **SpecialProperties** | bit (0,1) | 0 = no special properties, 1 = has special property requirements, such as a certified material or special heat treatment. |
| **SpecialProperties1-3**| int | Specifies special property requirements, as assigned in the SigmaNEST Add/Edit Sheet dialog box. |
| **GeoID** | uniqueidentifier| Reference link to the Geo table where remnant geometry is stored. |
| **ArchivePacketID**| int | Field used by SigmaNEST for database tracking. |
| **SheetData1-4** | varchar250 | Sheet data from SigmaNEST. |

#### Feedback: Sheets

The STShtARC feedback table contains information about sheets that were used in a program. SigmaNEST writes feedback to this table when an NC program is updated.

**STShtARC Feedback Variables**

| Variable | Type | Definition |
| :--- | :--- | :--- |
| **ProgramName** | varchar50 | NC program name. |
| **RepeatID** | int | Repeat ID number of the program, if it was repeated multiple times. |
| **SheetName** | varchar50 | Stock name. |
| **TaskName** | varchar50 | Task name. |
| **UsedArea** | float | Nested area of parts (used to determine yield). |
| **ScrapFraction** | float | Scrap area divided by area of sheet used (calculated by SigmaNEST). |
| **QtyInProcess** | int | Number of parts being processed. |
| **MachineName** | varchar50 | Name of machine. |
| **CuttingTime** | float | Total estimated cutting time for the program. |
| **PierceQty** | int | Total number of pierces in the program. |
| **JobCost** | float | Cost of the nest. |
| **PostDateTime** | datetime | Post date and time (using the system's datetime format). |
| **Material** | varchar50 | Material type (as defined in SigmaNEST). |
| **Thickness** | float | Material thickness. |
| **Length** | float | Stock length. |
| **Width** | float | Stock width. |
| **Area** | float | Area of the sheet. |
| **Qty** | int | Number of sheets. |
| **Cost** | float | Cost of the sheet. |
| **Location** | varchar50 | Sheet location. |
| **HeatNumber** | varchar50 | Heat number associated with the stock. |
| **BinNumber** | varchar50 | Bin number associated with the stock. |
| **Mill** | varchar50 | Mill quality associated with the stock. |
| **PrimeCode** | varchar50 | Prime code associated with the stock. |
| **SheetType** | int | 0 = remnant, 1 = stock, 2 = coil. |
| **DateReceived** | datetime | Date and time the sheet was received (using the system's datetime format). |
| **DateCreated** | datetime | Date and time the sheet was created (using the system's datetime format). |
| **SpecialProperties** | bit (0,1) | 0 = no special properties, 1 = has special property requirements, such as a certified material or special heat treatment. |
| **SpecialProperties1-3**| int | Specifies special property requirements, as assigned in the SigmaNEST Add/Edit Sheet dialog box. |
| **SpecialInstruction** | varchar50 | Text field used for special instructions. |
| **CompDate** | N/A | Reserved. |
| **Single** | bit (0,1) | 0 = sheet was originally created with a quantity not equal to 1, 1 = sheet was originally created with a quantity of 1. |
| **OrigSheetName**| varchar50 | Original name of the sheet when it was added to the inventory. |
| **MachineID** | int | Machine name or ID (as defined in Load Manager). |
| **CutStartTime** | datetime | Program start time. |
| **CutEndTime** | datetime | Program end time. |
| **SheetData1-4** | varchar250 | Sheet data from SigmaNEST. |
| **Remark** | varchar300 | Remark associated with the sheet. |
| **GeoID** | int | Field used by SigmaNEST for database tracking. |
| **ArchivePacketID**| int | Field used by SigmaNEST for database tracking. |

#### Feedback: Archived Work Orders

The STWOARC feedback table contains information about archived work orders. SigmaNEST writes feedback to this table when a work order is archived.

**STWOARC Feedback Variables**

| Variable | Type | Definition |
| :--- | :--- | :--- |
| **WoNumber** | varchar50 | Work order number. |
| **ArcDateTime** | datetime | Date and time the work order was archived (using the system's datetime format). |
| **CustomerName** | varchar50 | Customer name. |
| **CustomerID** | int | Unique customer ID number. |
| **WODate** | datetime | Date and time the work order was created (using the system's datetime format). |
| **BillTo** | int | Billing address ID number. |
| **ShipTo** | int | Shipping address ID number. |
| **SpecialInstruction**| varchar50 | Text field used for special instructions. |
| **TotalSalesCost**| float | Amount quoted in SigmaNEST. |
| **TotalScrap** | N/A | Reserved. |
| **ContactName** | varchar50 | Contact name associated with the work order. |
| **TotalMaterialCost**| N/A | Reserved. |
| **TotalProcessCost**| NA | Reserved. |
| **TotalOutsourceCost**| N/A | Reserved. |
| **TotalGrossMargin**| N/A | Reserved. |
| **SalesRepID** | varchar50 | Sales representative ID. |

## Chapter 3: Transaction Reference

This chapter is a reference to all available transactions and their variables. Transactions are sorted by type and number. For example, SN7x transactions are related to programs and work orders, and listed in order from SN70 to SN78R. Select a transaction type to learn more.

-   [SN6x Transactions: Material Management](#sn6x-transactions-material-management)
-   [SN7x Transactions: Programs and Work Orders](#sn7x-transactions-programs-and-work-orders)
-   [SN8x Transactions: Parts and Work Orders](#sn8x-transactions-parts-and-work-orders)
-   [SN9x Transactions: Stock Management](#sn9x-transactions-stock-management)
-   [QTx Transactions: Quote Management](#qtx-transactions-quote-management)
-   [CTLx Transactions: Cut-to-Length](#ctlx-transactions-cut-to-length)

### SN6x Transactions: Material Management

SN6x transactions add, modify, and delete materials. Select a transaction from the following list to view the transaction description, variables, and a sample transaction.

-   SN60 Add/Modify Material (page 73)
-   SN62 Delete Material (page 75)
-   SN63 Add Material Cost (page 76)
-   SN64 Update Material Cost (page 78)
-   SN65 Remove Material Cost (page 80)

#### SN60 Add/Modify Material

SN60 adds new materials and updates existing materials.

**SN60 Variables**

| Variable | Type | Required | Definition/Description |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN60). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **Material** | varchar50 | yes | Material type (as defined in SigmaNEST). |
| **Thickness** | float | no | Material thickness. |
| **Cost** | float | no | The cost of the material. |
| **ItemData1** | varchar50 | no | The material group. |
| **ItemData2** | varchar50 | no | The material standard. |
| **ItemData3** | varchar50 | no | The machinability index of the material. |
| **ItemData4** | varchar50 | no | The IAC specification of the material. |
| **Param1** | float | no | The density of the material. |
| **Param2** | float | no | The shear strength of the material. |
| **Param3** | float | no | The die clearance of the material. |
| **Param4** | float | no | The K-Factor of the material. |
| **ItemData5** | varchar50 | no | 0 = the material cannot be used for Cut-to-Length parts, 1 = the material can be used for Cut-to-Length parts. |

**SN60 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, Material, Thickness)
VALUES ('SN60', 1, '1000', 'MS', 0.500)
```

#### SN62 Delete Material

SN62 deletes existing materials.

**SN62 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN62). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **Material** | varchar50 | yes | Material type (as defined in SigmaNEST). |

**SN62 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, Material)
VALUES ('SN62', 1, '1000', 'MS')
```

#### SN63 Add Material Cost

SN63 adds the cost of an existing material.

**SN63 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN63). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **Material** | varchar50 | yes | Material type (as defined in SigmaNEST). |
| **Thickness** | float | yes | Material thickness. |
| **Width** | float | no | Stock width. |
| **Cost** | float | yes | The cost of the material. |
| **ItemData1** | varchar50 | no | The cost type. Accepted values are "Raw," "Remnant," or "Scrap" (not case-sensitive). |

**SN63 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, Material, Thickness, Cost, ItemData1)
VALUES ('SN63', 1, '1000', 'MS', 0.500, 0.50, 'raw')
```

#### SN64 Update Material Cost

SN64 updates the cost of existing materials.

**SN64 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN64). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **Material** | varchar50 | yes | Material type (as defined in SigmaNEST). |
| **Thickness** | float | yes | Material thickness. |
| **Width** | float | no | Stock width. |
| **ItemData1** | varchar50 | no | The cost type. Accepted values are "Raw," "Remnant," or "Scrap" (not case-sensitive). |
| **ItemData2** | varchar50 | no | The column to update. Accepted values are "Cost," "Width," and "CostType" (not case-sensitive). |
| **ItemData3** | varchar50 | no | The new cost type parameter, if ItemData2 is "CostType." |
| **Param1** | float | no | The new cost or width value if ItemData2 is "Cost" or "Width." |

**SN64 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, Material, Thickness, ItemData2, Param1)
VALUES ('SN64', 1, '1000', 'MS', 0.500, 'cost', 0.55)
```

#### SN65 Remove Material Cost

SN65 removes cost from an existing material.

**SN65 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN65). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **Material** | varchar50 | yes | Material type (as defined in SigmaNEST). |
| **Thickness** | float | yes | Material thickness. |
| **Width** | float | no | Stock width. |
| **ItemData1** | varchar50 | no | The cost type. Accepted values are "Raw," "Remnant," or "Scrap" (not case-sensitive). |

**SN65 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, Material, Thickness)
VALUES ('SN65', 1, '1000', 'MS', 0.500)
```

### SN7x Transactions: Programs and Work Orders

The SN7x transactions swap sheets, update programs, archive work orders, and more. Select a transaction from the following list to view the transaction description, variables, and a sample transaction.

-   SN7A Swap Sheets (page 82)
-   SN70 Update Program (page 84)
-   SN70N Modify Program UpdateState (page 85)
-   SN71 Archive Completed Work Orders (page 86)
-   SN72 Archive Selected Work Order (page 87)
-   SN73 Run File (page 88)
-   SN73C Update Cut Time (page 89)
-   SN73N Modify Program ActualState (page 91)
-   SN74 Delete Program (page 93)
-   SN75 Update All Programs (page 94)
-   SN76 Remove Remnants from Program (page 95)
-   SN77 Clear Work Order and Stock Tables (page 96)
-   SN77A Clear Archive Tables (page 97)
-   SN77ALL Clear All SigmaNEST Tables (page 98)
-   SN78 Modify Program Part Quantity (page 99)
-   SN78R Reject Part (page 101)
-   SN79 Delete Part File (page 103)

#### SN7A Swap Sheets

SN7A swaps sheets that are in process, the same way the Swap Sheet command works in SigmaNEST.

**SN7A Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN7A). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ItemName** | varchar50 | yes | Stock name. |
| **ProgramName** | varchar50 | yes | NC program name. |
| **ProgramRepeat** | int | yes | value > 0 = specific repeat to update. 0 = update all repeats. |
| **StringData1** | varchar50 | no | Original sheet name, used in the case of Multi Sheets. |

**SN7A Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemName, ProgramName, ProgramRepeat)
VALUES ('SN7A', 1, '1000', 'Sheet1', 'Prog1', 1)
```

#### SN70 Update Program

SN70 updates the specified program. As a result, it reduces sheet inventory, increments the completed quantity of work order parts, and adds newly created remnants to the inventory, when applicable.

**SN70 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN70). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ProgramName** | varchar50 | yes | NC program name. |
| **ProgramRepeat** | int | yes | value > 0 = specific repeat to update. 0 = update all repeats. |

**SN70 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ProgramName, ProgramRepeat)
VALUES ('SN70', 1, '1000', 'Prog1', 1)
```

#### SN70N Modify Program UpdateState

SN70N modifies the UpdateState field of the specified program.

**SN70N Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN70N). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ItemType** | int | yes | UpdateState. 0 = Program_Created, 90 = Program_Finished, 100 = Program_Updated. |
| **ProgramName** | varchar50 | yes | NC program name |
| **ProgramRepeat** | int | yes | value > 0 = specific repeat to update; value <= 0 = update all repeats |

**SN70N Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemType, ProgramName, ProgramRepeat)
VALUES ('SN70N', 1, '1000', 1, 'Prog1', 90)
```

#### SN71 Archive Completed Work Orders

SN71 archives all completed work orders. A work order is considered complete when the Quantity Completed is greater than or equal to the required quantity for each part in the work order.

**SN71 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN71). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |

**SN71 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID)
VALUES ('SN71', 1, '1000')
```

#### SN72 Archive Selected Work Order

SN72 archives the specified work order. Archiving a work order removes it from the work order list in SigmaNEST.

> **Warning:** If you archive a work order that is incomplete or in-process, any data associated with the work order is deleted. Only archive completed work orders.

**SN72 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN72). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |

**SN72 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo)
VALUES ('SN72', 1, '1000', '70')
```

#### SN73 Run File

SN73 runs executables, batch (.wol) files, or script (.pas, .ipr, .ubs) files.

**SN73 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN73). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **FileName** | varchar255 | yes | Executable, batch, or script file name. |
| **StringData1-8** | varchar50 | no | If the FileName field references an executable, StringData1-8 can be used for command line parameters. |

**SN73 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, FileName)
VALUES ('SN73', 1, '1000', 'BatchFile.wol')
```

#### SN73C Update Cut Time

SN73C updates the recorded cutting time of a specified program.

**SN73C Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN73C). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ProgramName** | varchar50 | yes | NC program name. |
| **ProgramRepeat** | int | yes | value > 0 = specific repeat to update. 0 = update all repeats. |
| **Param1** | float | no | Estimated cutting time in seconds. |
| **StartDate** | datetime | no | Program start time. |
| **EndDate** | datetime | no | Program end time. |

**SN73C Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ProgramName, ProgramRepeat, Param1)
VALUES ('SN73C', 1, '1000', 'Prog1', 1, 758)
```

#### SN73N Modify Program ActualState

SN73N modifies the ActualState field of the specified program.

**SN73N Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN73N). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ProgramName** | varchar50 | yes | NC program name. |
| **ProgramRepeat** | int | yes | value > 0 = specific repeat to update. 0 = update all repeats. |
| **StringData1** | varchar50 | no | Name of machine. |
| **StringData2** | varchar50 | no | Reason program was stopped. |
| **Param1** | float | no | 0 = created, 1 = program start, 2 = reserved, 3 = program stop/pause |
| **Param2** | float | no | 0 = no update, 1 = need update (Load Manager) |
| **Param3** | float | no | Estimated cutting time in seconds. |
| **StartDate** | datetime | no | Program start time. |
| **EndDate** | datetime | no | Program end time. |

**SN73N Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ProgramName, ProgramRepeat, Param1)
VALUES ('SN73N', 1, '1000', 'Prog1', 1, 1)
```

#### SN74 Delete Program

SN74 deletes the specified program. As a result, associated stock is restored to the sheet library and associated work order parts become available for nesting.

> **Warning:** All associated in-process data and program repeats are also deleted when running transaction SN74.

**SN74 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN74). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ProgramName** | varchar50 | yes | NC program name. |

**SN74 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ProgramName)
VALUES ('SN74', 1, '1000', 'Prog1')
```

#### SN75 Update All Programs

SN75 updates all programs.

**SN75 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN75). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |

**SN75 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID)
VALUES ('SN75', 1, '1000')
```

#### SN76 Remove Remnants from Program

SN76 removes remnants from the specified program.

**SN76 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN76). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ProgramName** | varchar50 | yes | NC program name. |
| **ProgramRepeat** | int | no | value > 0 = specific repeat to update. 0 = update all repeats. |

**SN76 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ProgramName, ProgramRepeat)
VALUES ('SN76', 1, '1000', 'Prog1', 1)
```

#### SN77 Clear Work Order and Stock Tables

SN77 clears all data from the Work Order and Stock tables in the SigmaNEST database.

> **Warning:** This action cannot be undone.

**SN77 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN77). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |

**SN77 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID)
VALUES ('SN77', 1, '1000')
```

#### SN77A Clear Archive Tables

SN77A clears all data from the Archive tables in the SigmaNEST database.

> **Warning:** This action cannot be undone.

**SN77A Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN77A). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |

**SN77A Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID)
VALUES ('SN77A', 1, '1000')
```

#### SN77ALL Clear All SigmaNEST Tables

SN77ALL clears all data from the SigmaNEST database.

> **Warning:** This action cannot be undone.

**SN77ALL Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN77ALL). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |

**SN77ALL Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID)
VALUES ('SN77ALL', 1, '1000')
```

#### SN78 Modify Program Part Quantity

SN78 modifies the part quantity of a specific part in the specified program.

**SN78 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN78). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | yes | Part name. |
| **Qty** | int | yes | New part quantity. |
| **ProgramName** | varchar50 | yes | NC program name. |
| **ProgramRepeat** | int | yes | value > 0 = specific repeat to update. 0 = update all repeats. |

**SN78 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName, Qty, ProgramName, ProgramRepeat)
VALUES ('SN78', 1, '1000', '70', 'Part1', 25, 'Prog1', 1)
```

#### SN78R Reject Part

SN78R rejects a specific part in the specified program, adding that part to the Rejected Part database table.

**SN78R Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN78R). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | yes | Part name. |
| **Qty** | int | yes | Number of parts. |
| **ItemType** | int | yes | By default, 1 = wrong size, 2 = wrong material, 3 = poor edge quality, 4 = damage in cutting process, 5 = flare in sheet\plate, 6 = design flaw in part geometry. |
| **ProgramName** | varchar50 | yes | NC program name. |
| **ProgramRepeat** | int | yes | value > 0 = specific repeat to update. 0 = update all repeats. |
| **StringData1** | varchar50 | no | Comment. |
| **StringData2** | varchar50 | no | Operator name. |
| **StringData3** | varchar50 | no | 0 = not scrapped, 1 = scrapped. |
| **StringData4** | varchar50 | yes | Sheet name. |

**SN78R Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName, Qty, ItemType, ProgramName, ProgramRepeat, StringData4)
VALUES ('SN78R', 1, '1000', '70', 'Part1', 25, 4, 'Prog1', 1, 'Sheet1')
```

#### SN79 Delete Part File

SN79 deletes the specified part file from the part folder.

> **Note:** To include subfolders when searching the part folder, select **Search part library subfolders (SN79)** in the Part Transactions (page 16) section of the Global Configuration (page 15).

**SN79 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN79). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ItemName** | varchar100 | yes | Part name. |
| **FileName** | varchar255 | no | Folder to search. |
| **RevNumber** | varchar50 | no | Revision associated with the SigmaNEST part. |
| **TypeDescr** | varchar50 | no | File extension. |

**SN79 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemName)
VALUES ('SN79', 1, '1000', 'Part1')
```

### SN8x Transactions: Parts and Work Orders

The SN8x transactions create and modify work orders and parts. Select a transaction from the following list to view the transaction description, variables, and a sample transaction.

-   SN80 Add Undefined Part to Order (page 106)
-   SN81 Modify Work Order Parts (page 109)
-   SN81B Modify Work Order Parts (Balance Qty) (page 112)
-   SN82 Cancel Work Order Part (page 115)
-   SN83 Add Standard Shape Part to Order (page 116)
-   SN84 Add Existing Part to Order (page 120)
-   SN84A Add Existing Part to Order (Add Quantities) (page 123)
-   SN85 Add CAD Part to Order (page 126)
-   SN86 Add BOM to Work Order (page 130)
-   SN87 Modify Work Order (page 132)
-   SN88 Add Existing Part to New Order (page 134)
-   SN89 Cancel Work Order (page 137)
-   SN89I Cancel Work Orders (Not in Process) (page 138)
-   SN89N Cancel All Work Orders (page 139)

#### SN80 Add Undefined Part to Order

SN80 creates a work order with missing or undefined parts. After a part of the same name is added to the Parts Library, the part is defined. If the work order and/or part already exist, the existing files are overwritten.

**SN80 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN80). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | yes | Part name. |
| **Qty** | int | yes | Number of parts. |
| **Material** | varchar50 | no | Material type (as defined in SigmaNEST). |
| **Thickness** | float | no | Material thickness. |
| **DueDate** | datetime | no | Work order due date. |
| **Customer** | varchar50 | no | Customer name. |
| **DwgNumber** | varchar50 | no | Drawing number associated with the part. |
| **Priority** | int | no | Work order part priority (as defined in SigmaNEST). |
| **ProgBy** | varchar50 | no | Name of programmer associated with the part. |
| **Remark** | varchar80 | no | Remark associated with the SigmaNEST part. |
| **RevNumber** | varchar50 | no | Revision associated with the SigmaNEST part. |
| **OnHold** | bit (0,1) | no | 0 = not on hold, 1 = on hold (on hold means that the order is on hold and the parts are not available for nesting). |
| **ItemData1-18**| varchar50 | no | Extra data fields associated with SigmaNEST parts. |
| **SalesRep** | varchar50 | no | Sales representative ID. |

**SN80 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName, Qty)
VALUES ('SN80', 1, '1000', '70', 'Part1', 25)
```

#### SN81 Modify Work Order Parts

SN81 modifies parts in an existing work order.

> **Note:** SN81 modifies parts that have not yet been cut, in-process parts, and completed parts. To only modify parts which have not yet been cut (also called the "balance quantity"), use SN81B Modify Work Order Parts (Balance Qty) (page 112).

**SN81 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN81). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | yes | Part name. |
| **Qty** | int | yes | Number of parts. |
| **Material** | varchar50 | no | Material type (as defined in SigmaNEST). |
| **Thickness** | float | no | Material thickness. |
| **DueDate** | datetime | no | Work order due date. |
| **Customer** | varchar50 | no | Customer name. |
| **DwgNumber** | varchar50 | no | Cost of the part drawing. |
| **Priority** | int | no | Part priority (as defined in SigmaNEST). |
| **ProgBy** | varchar50 | no | Name of programmer associated with the part. |
| **Remark** | varchar80 | no | Remark associated with the SigmaNEST part. |
| **RevNumber** | varchar50 | no | Revision associated with the SigmaNEST part. |
| **OnHold** | bit (0,1) | no | 0 = not on hold, 1 = on hold (on hold means that the order is on hold and the part is not available for nesting). |
| **ItemData1-18**| varchar50 | no | Extra data fields associated with SigmaNEST parts. |

**SN81 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName, Qty, Priority)
VALUES ('SN81', 1, '1000', '70', 'Part1', 50, 1)
```

#### SN81B Modify Work Order Parts (Balance Qty)

SN81B modifies parts in an existing work order, similarly to SN81 Modify Work Order Parts (page 109). However, it does not affect parts which are in-process or completed, only the balance quantity (parts which have not yet been cut).

> **Note:** To allow SN81B to process transactions that result in a quantity of 0, select **Process Qty = 0 for SN81B** in the Part Transactions (page 16) section of the Global Configuration (page 15).

**SN81B Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN81B). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | yes | Part name. |
| **Qty** | int | yes | Number of parts. |
| **Material** | varchar50 | no | Material type (as defined in SigmaNEST). |
| **Thickness** | float | no | Material thickness. |
| **DueDate** | datetime | no | Work order due date. |
| **Customer** | varchar50 | no | Customer name. |
| **DwgNumber** | varchar50 | no | Drawing number associated with the part. |
| **Priority** | int | no | Part priority (as defined in SigmaNEST). |
| **ProgBy** | varchar50 | no | Name of programmer associated with the part. |
| **Remark** | varchar80 | no | Remark associated with the SigmaNEST part. |
| **RevNumber** | varchar50 | no | Revision associated with the SigmaNEST part. |
| **OnHold** | bit (0,1) | no | 0 = not on hold, 1 = on hold (on hold means that the order is on hold and the part is not available for nesting). |
| **ItemData1-18**| varchar50 | no | Extra data fields associated with SigmaNEST parts. |

**SN81B Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName, Qty, Priority)
VALUES ('SN81B', 1, '1000', '70', 'Part1', 10, 1)
```

#### SN82 Cancel Work Order Part

SN82 removes a part from a work order. This only works if the part is not already in-process.

**SN82 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN82). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | yes | Part name. |

**SN82 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName)
VALUES ('SN82', 1, '1000', '70', 'Part1')
```

#### SN83 Add Standard Shape Part to Order

SN83 creates part from a standard shape, then adds it to a work order. If the work order and/or part already exist, the existing data is overwritten.

**SN83 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN83). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | yes* | Part name. *Either the ItemName or FileName variable is required for this transaction. |
| **Qty** | int | yes | Number of parts. |
| **Material** | varchar50 | yes | Material type (as defined in SigmaNEST). |
| **Thickness** | float | yes | Material thickness. |
| **DueDate** | datetime | no | The part's due date (using the system's datetime format). |
| **Customer** | varchar50 | no | Customer name. |
| **DwgNumber** | varchar50 | no | Drawing number associated with the part. |
| **Priority** | int | no | Part priority (as defined in SigmaNEST). |
| **ProgBy** | varchar50 | no | Name of programmer associated with the part. |
| **FileName** | varchar255 | yes* | Name of the part file that will be created from the standard shape. If a path is not specified, the path from the Part and CAD Retrieval Paths (page 32) section of the District Configuration is used. *Either the ItemName or FileName variable is required for this transaction. |
| **Remark** | varchar80 | no | Remark associated with the SigmaNEST part. |
| **RevNumber** | varchar50 | no | Revision associated with the SigmaNEST part. |
| **OnHold** | bit (0,1) | no | 0 = not on hold, 1 = on hold (on hold means that the order is on hold and the part is not available for nesting). |
| **ItemData1-18**| varchar50 | no | Extra data fields associated with SigmaNEST parts. |
| **OrderShape** | varchar50 | no | Name of the SigmaNEST standard shape. |
| **BatchFile** | varchar255 | no | Batch file path to run before creating the part. |
| **Process** | varchar50 | no | Name of machine. |
| **StringData1-8**| varchar50 | no | Batch commands to run before creating the part. |
| **Param1-8** | float | no* | Parameters for the standard shape specified in the OrderShape field. *Required if using standard shapes with parameters. |
| **IDNegTol** | float | no | See Tolerance Values (page 44) for information about this variable. |
| **IDPosTol** | float | no | See Tolerance Values (page 44) for information about this variable. |
| **ODNegTol** | float | no | See Tolerance Values (page 44) for information about this variable. |
| **ODPosTol** | float | no | See Tolerance Values (page 44) for information about this variable. |

**SN83 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName, Qty, Material, Thickness, Customer, OrderShape, Param1, Param2)
VALUES ('SN83', 1, '1000', '70', 'Part1', 25, 'MS', 0.500, 'SigmaTEK', 'SHAPE1', 10, 10)
```

#### SN84 Add Existing Part to Order

SN84 adds an existing SigmaNEST part to a work order. If the part already exists and has already been added to the specified work order, the existing data is overwritten. To add the new part quantity to the existing part quantity instead of overwriting it, use SN84A Add Existing Part to Order (Add Quantities) (page 123).

> **Tip:** Part values specified in this transaction, such as material and thickness, overwrite any existing values in the part file. If you want to use values from the part file instead, leave those fields blank.

**SN84 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN84). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | yes* | Part name. *Either the ItemName or FileName variable is required for this transaction. |
| **Qty** | int | no | Number of parts. |
| **Material** | varchar50 | no | Material type (as defined in SigmaNEST). |
| **Thickness** | float | no | Material thickness. |
| **DueDate** | datetime | no | The part's due date (using the system's datetime format). |
| **Customer** | varchar50 | no | Customer name. |
| **DwgNumber** | varchar50 | no | Drawing number associated with the part. |
| **Priority** | int | no | Part priority (as defined in SigmaNEST). |
| **ProgBy** | varchar50 | no | Name of programmer associated with the part. |
| **FileName** | varchar255 | yes* | Name of the part file. If a path is not specified, the path from the Part and CAD Retrieval Paths (page 32) section of the District Configuration is used. *Either the ItemName or FileName variable is required for this transaction. |
| **Remark** | varchar80 | no | Remark associated with the SigmaNEST part. |
| **RevNumber** | varchar50 | no | Revision associated with the SigmaNEST part. |
| **OnHold** | bit (0,1) | no | 0 = not on hold, 1 = on hold (on hold means that the order is on hold and the part is not available for nesting). |
| **ItemData1-18**| varchar50 | no | Extra data fields associated with SigmaNEST parts. |
| **Process** | varchar50 | no | Machine name or ID (as defined in Load Manager). |

**SN84 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName)
VALUES ('SN84', 1, '1000', '70', 'Part1')
```

#### SN84A Add Existing Part to Order (Add Quantities)

SN84A is similar to SN84 Add Existing Part to Order (page 120), except it adds part quantities together instead of overwriting the existing part quantity.

For example, if WO1 contains Part1 with a quantity of 25, and you use SN84A to add Part1 with a quantity of 10, the quantities will be added together to equal 35. If you use SN84, the original quantity will be overwritten, resulting in a quantity of 10.

**SN84A Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN84A). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | yes* | Part name. *Either the ItemName or FileName variable is required for this transaction. |
| **Qty** | int | no | Number of parts. |
| **Material** | varchar50 | no | Material type (as defined in SigmaNEST). |
| **Thickness** | float | no | Material thickness. |
| **DueDate** | datetime | no | The part's due date (using the system's datetime format). |
| **Customer** | varchar50 | no | Customer name. |
| **DwgNumber** | varchar50 | no | Drawing number associated with the part. |
| **Priority** | int | no | Work Order part priority. |
| **ProgBy** | varchar50 | no | Programmed by field associated with SigmaNEST or CTL part. |
| **FileName** | varchar255 | yes* | Name of the part file. If a path is not specified, the path from the Part and CAD Retrieval Paths (page 32) section of the District Configuration is used. *Either the ItemName or FileName variable is required for this transaction. |
| **Remark** | varchar80 | no | Remark associated with the SigmaNEST part. |
| **RevNumber** | varchar50 | no | Revision associated with the SigmaNEST part. |
| **OnHold** | bit (0,1) | no | 0 = not on hold, 1 = on hold (on hold means that the order is on hold and the part is not available for nesting). |
| **ItemData1-18**| varchar50 | no | Extra data fields associated with SigmaNEST parts. |
| **Process** | varchar50 | no | Machine name or ID (as defined in Load Manager). |

**SN84A Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName)
VALUES ('SN84A', 1, '1000', '70', 'Part1')
```

#### SN85 Add CAD Part to Order

SN85 converts an existing geometry file into a SigmaNEST part, then adds it to a work order. If the work order and/or part already exist, the existing data is overwritten.

**SN85 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN85). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | yes | Part name. |
| **Qty** | int | yes | Number of parts. |
| **Material** | varchar50 | yes | Material type (as defined in SigmaNEST). |
| **Thickness** | float | no | Material thickness. |
| **DueDate** | datetime | no | The part's due date (using the system's datetime format). |
| **Customer** | varchar50 | no | Customer name. |
| **DwgNumber** | varchar50 | no | Drawing number associated with the part. |
| **Priority** | int | no | Part priority (as defined in SigmaNEST). |
| **ProgBy** | varchar50 | no | Name of programmer associated with the part. |
| **FileName** | varchar255 | yes* | Part or geometry file name. If a path is not specified, the path from the Part and CAD Retrieval Paths (page 32) section of the District Configuration is used. *Either the FileName or TypeDescr variable is required for this transaction. |
| **Remark** | varchar80 | no | Remark associated with the SigmaNEST part. |
| **RevNumber** | varchar50 | no | Revision associated with the SigmaNEST part. |
| **ItemType** | int | no | 0 = standard part, 1 = filler part. |
| **OnHold** | bit (0,1) | no | 0 = not on hold, 1 = on hold (on hold means that the order is on hold and the part is not available for nesting). |
| **TypeDescr** | varchar50 | yes* | Geometry type, typically the same as the file extension (DXF, DWG, IGES, etc.). *Either the FileName or TypeDescr variable is required for this transaction. |
| **ItemData1-18**| varchar50 | no | Extra data fields associated with SigmaNEST parts. |
| **OrderShape** | varchar50 | no | Name of the SigmaNEST standard shape. |
| **BatchFile** | varchar255 | no | Batch file path to run before creating the part. |
| **Process** | varchar50 | no | Machine name or ID (as defined in Load Manager). |
| **StringData1-8**| varchar50 | no | Batch commands to run before creating the part. |

**SN85 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName, Qty, Material, FileName)
VALUES ('SN85', 1, '1000', '70', 'Part1', 25, 'MS', 'C:\Public\Users\Documents\CAD\Geo1.DXF')
```

#### SN86 Add BOM to Work Order

SN86 loads a bill of materials (BOM) into the specified work order.

> **Note:** The quantities specified in the BOM file are multiplied by the work order quantity.

**SN86 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN86). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **Qty** | int | no | BOM quantity. |
| **DueDate** | datetime | no | The part's due date (using the system's datetime format). |
| **Customer** | varchar50 | no | Customer name. |
| **Priority** | int | no | Part priority (as defined in SigmaNEST). |
| **FileName** | varchar255 | yes | Path of the BOM file. |

**SN86 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, Qty, FileName)
VALUES ('SN86', 1, '1000', '70', 25, 'C:\Public\Users\Documents\BOM\BOM1.BOM')
```

#### SN87 Modify Work Order

SN87 modifies attributes of an existing work order, leaving the parts in the work order unaltered.

**SN87 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN87). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **DueDate** | datetime | no | Work order due date. |
| **Customer** | varchar50 | no | Customer name. |
| **Priority** | int | no | Work order priority. |
| **OnHold** | bit (0,1) | no | 0 = not on hold, 1 = on hold (on hold means that the order is on hold and is unavailable for nesting). |
| **ItemData1** | varchar50 | no | WO Data 1. |
| **ItemData2** | varchar50 | no | WO Data 2. |
| **ItemData3** | varchar50 | no | Customer PO#. |
| **ItemData4** | varchar50 | no | Order Number. |
| **SalesRep** | varchar50 | no | Sales representative ID. |

**SN87 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, OnHold)
VALUES ('SN87', 1, '1000', '70', 1)
```

#### SN88 Add Existing Part to New Order

SN88 is similar to SN84 Add Existing Part to Order (page 120), except it will fail if the work order already exists. It can only be used to add existing parts to new work orders.

**SN88 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN88). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | yes* | Part name. *Either the ItemName or FileName variable is required for this transaction. |
| **Qty** | int | no | Number of parts. |
| **Material** | varchar50 | no | Material type (as defined in SigmaNEST). |
| **Thickness** | float | no | Material thickness. |
| **DueDate** | datetime | no | The part's due date (using the system's datetime format). |
| **Customer** | varchar50 | no | Customer name. |
| **DwgNumber** | varchar50 | no | Drawing number associated with the part. |
| **Priority** | int | no | Part priority (as defined in SigmaNEST). |
| **ProgBy** | varchar50 | no | Name of programmer associated with the part. |
| **FileName** | varchar255 | yes* | Name of the part file. If a path is not specified, the path from the Part and CAD Retrieval Paths (page 32) section of the District Configuration is used. *Either the ItemName or FileName variable is required for this transaction. |
| **Remark** | varchar80 | no | Remark associated with the SigmaNEST part. |
| **RevNumber** | varchar50 | no | Revision associated with the SigmaNEST part. |
| **OnHold** | bit (0,1) | no | 0 = not on hold, 1 = on hold (on hold means that the order is on hold and the part is not available for nesting). |
| **ItemData1-18**| varchar50 | no | Extra data fields associated with SigmaNEST parts. |
| **Process** | varchar50 | no | Machine name or ID (as defined in Load Manager). |

**SN88 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName)
VALUES ('SN88', 1, '1000', '70', 'Part1')
```

#### SN89 Cancel Work Order

SN89 cancels an existing work order. This is the same as deleting a work order in SigmaNEST.

**SN89 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN89). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |

**SN89 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo)
VALUES ('SN89', 1, '1000', '70')
```

#### SN89I Cancel Work Orders (Not in Process)

SN89I cancels all work orders that are not currently in process. This is the same as deleting those work orders in SigmaNEST.

**SN89I Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN89I). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |

**SN89I Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID)
VALUES ('SN89I', 1, '1000')
```

#### SN89N Cancel All Work Orders

SN89N cancels all work orders, regardless of state. This is the same as deleting all work orders in SigmaNEST.

**SN89N Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN89N). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |

**SN89N Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID)
VALUES ('SN89N', 1, '1000')
```

### SN9x Transactions: Stock Management

The SN9x transactions manage sheets, coils, and remnants. Select a transaction from the following list to view the transaction description, variables, and a sample transaction.

-   SN90 Add/Remove Stock (page 141)
-   SN91 Modify Stock (page 144)
-   SN91A Modify Stock (Allow Qty = 0) (page 147)
-   SN92 Delete Stock (Except In-Process) (page 150)
-   SN93 Delete All Stock (page 151)
-   SN93R Delete All Remnants (page 152)
-   SN94 Add Stock (New Only) (page 153)
-   SN95 Delete All Stock (Except In-Process) (page 156)
-   SN95R Delete All Remnants (Except In-Process) (page 157)
-   SN96 Delete Stock (page 158)
-   SN97 Add Remnant (page 159)

#### SN90 Add/Remove Stock

SN90 adds or removes stock from the stock library.

**SN90 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN90). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | no | Work order number. |
| **ItemName** | varchar50 | yes | Stock name. |
| **Qty** | int | yes | Quantity of stock to add. Enter a negative integer to remove existing stock. |
| **Material** | varchar50 | yes | Material type (as defined in SigmaNEST). |
| **Thickness** | float | yes | Material thickness. |
| **Customer** | varchar50 | no | Customer associated with the stock. |
| **Length** | float | yes | Stock length. |
| **Width** | float | yes | Stock width. |
| **HeatNumber** | varchar50 | no | Heat number associated with the stock. |
| **ItemType** | int | no | 0 = sheet, 1 = remnant, 2 = coil. |
| **BinNumber** | varchar50 | no | Bin number associated with the stock. |
| **Location** | varchar50 | no | Location of the stock. |
| **Mill** | varchar50 | no | Mill quality associated with the stock. |
| **PrimeCode** | varchar50 | no | Prime code associated with the stock. |
| **Param1** | float | no | Actual weight. |
| **Param2** | float | no | Actual price. |
| **Param5** | float | no | 0 = none, 1 = reserved, 2 = on consignment. |
| **ItemData9** | varchar50 | no | MRP/ERP stock ID. |

**SN90 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemName, Qty, Material, Thickness, Length, Width)
VALUES ('SN90', 1, '1000', 'Sheet1', 5, 'MS', 0.500, 120, 60)
```

#### SN91 Modify Stock

SN91 modifies existing stock, but will fail if the modification will result in a quantity of 0. Use SN91A Modify Stock (Allow Qty = 0) (page 147) if you want to change the quantity to 0.

**SN91 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN91). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | no | Work order number. |
| **ItemName** | varchar50 | yes | Stock name. |
| **Qty** | int | yes | Quantity of stock to add. |
| **Material** | varchar50 | yes | Material type (as defined in SigmaNEST). |
| **Thickness** | float | yes | Material thickness. |
| **Customer** | varchar50 | no | Customer associated with the stock. |
| **Length** | float | yes | Stock length. |
| **Width** | float | yes | Stock width. |
| **HeatNumber** | varchar50 | no | Heat number associated with the stock. |
| **ItemType** | int | no | 0 = sheet, 1 = remnant, 2 = coil. |
| **BinNumber** | varchar50 | no | Bin number associated with the stock. |
| **Location** | varchar50 | no | Location of the stock. |
| **Mill** | varchar50 | no | Mill quality associated with the stock. |
| **PrimeCode** | varchar50 | no | Prime code associated with the stock. |
| **Param1** | float | no | Actual weight. |
| **Param2** | float | no | Actual price. |
| **Param5** | float | no | 0 = none, 1 = reserved, 2 = on consignment. |
| **ItemData9** | varchar50 | no | MRP/ERP stock ID. |

**SN91 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemName, Qty, Material, Thickness, Length, Width)
VALUES ('SN91', 1, '1000', 'Sheet1', 10, 'MS', 0.500, 120, 60)
```

#### SN91A Modify Stock (Allow Qty = 0)

SN91A is similar to SN91 Modify Stock (page 144), except it allows you to run transactions which result in a quantity of 0.

> **Note:** SN91A will not create new stock unless **Add sheets with SN91A if they don't exist yet** is enabled in the Sheet Transactions (page 17) section of the Global Configuration (page 15).
> 
> **Note:** Stock with a quantity of 0 is automatically deleted if **Delete sheets with 91A when Qty available = 0** is enabled in the Sheet Transactions (page 17) section of the Global Configuration (page 15).

**SN91A Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN91A). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | no | Work order number. |
| **ItemName** | varchar50 | yes | Stock name. |
| **Qty** | int | yes | Quantity of stock to add. |
| **Material** | varchar50 | yes | Material type (as defined in SigmaNEST). |
| **Thickness** | float | yes | Material thickness. |
| **Customer** | varchar50 | no | Customer associated with the stock. |
| **Length** | float | yes | Stock length. |
| **Width** | float | yes | Stock width. |
| **HeatNumber** | varchar50 | no | Heat number associated with the stock. |
| **ItemType** | int | no | 0 = sheet, 1 = remnant, 2 = coil. |
| **BinNumber** | varchar50 | no | Bin number associated with the stock. |
| **Location** | varchar50 | no | Location of the stock. |
| **Mill** | varchar50 | no | Mill quality associated with the stock. |
| **PrimeCode** | varchar50 | no | Prime code associated with the stock. |
| **Param1** | float | no | Actual weight. |
| **Param2** | float | no | Actual price. |
| **Param5** | float | no | 0 = none, 1 = reserved, 2 = on consignment. |
| **ItemData9** | varchar50 | no | MRP/ERP stock ID. |

**SN91A Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemName, Qty, Material, Thickness, Length, Width)
VALUES ('SN91A', 1, '1000', 'Sheet1', 0, 'MS', 0.500, 120, 60)
```

#### SN92 Delete Stock (Except In-Process)

SN92 deletes the specified stock from the stock library, unless the stock is currently in-process. To delete in-process stock, use SN96 Delete Stock (page 158).

**SN92 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN92). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ItemName** | varchar50 | yes | Stock name. |

**SN92 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemName)
VALUES ('SN92', 1, '1000', 'Sheet1')
```

#### SN93 Delete All Stock

SN93 deletes all stock (including in-process stock) from the stock library. To delete only stock that is not in-process, use SN95 Delete All Stock (Except In-Process) (page 156).

> **Warning:** This action cannot be undone.

**SN93 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN93). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |

**SN93 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID)
VALUES ('SN93', 1, '1000')
```

#### SN93R Delete All Remnants

SN93R deletes all remnants (including in-process remnants) from the stock library. To delete only remnants that are not in-process, use SN95R Delete All Remnants (Except In-Process) (page 157).

> **Warning:** This action cannot be undone.

**SN93R Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN93R). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |

**SN93R Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID)
VALUES ('SN93R', 1, '1000')
```

#### SN94 Add Stock (New Only)

SN94 is similar to SN90 Add/Remove Stock (page 141), except it only adds new stock, and cannot modify existing stock. If the specified stock already exists, this transaction will fail.

**SN94 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN94). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | no | Work order number. |
| **ItemName** | varchar50 | yes | Stock name. |
| **Qty** | int | yes | Quantity of stock to add. |
| **Material** | varchar50 | yes | Material type (as defined in SigmaNEST). |
| **Thickness** | float | yes | Material thickness. |
| **Customer** | varchar50 | no | Customer associated with the stock. |
| **Length** | float | yes | Stock length. |
| **Width** | float | yes | Stock width. |
| **HeatNumber** | varchar50 | no | Heat number associated with the stock. |
| **ItemType** | int | no | 0 = sheet, 1 = remnant, 2 = coil. |
| **BinNumber** | varchar50 | no | Bin number associated with the stock. |
| **Location** | varchar50 | no | Location of the stock. |
| **Mill** | varchar50 | no | Mill quality associated with the stock. |
| **PrimeCode** | varchar50 | no | Prime code associated with the stock. |
| **Param1** | float | no | Actual weight. |
| **Param2** | float | no | Actual price. |
| **Param5** | float | no | 0 = none, 1 = reserved, 2 = on consignment. |
| **ItemData9** | varchar50 | no | MRP/ERP stock ID. |

**SN94 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemName, Qty, Material, Thickness, Length, Width)
VALUES ('SN94', 1, '1000', 'Sheet2', 10, 'MS', 0.500, 120, 60)
```

#### SN95 Delete All Stock (Except In-Process)

SN95 is similar to SN93 Delete All Stock (page 151), except it only deletes stock that is not in-process.

> **Warning:** This action cannot be undone.

**SN95 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN95). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |

**SN95 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID)
VALUES ('SN95', 1, '1000')
```

#### SN95R Delete All Remnants (Except In-Process)

SN95R is similar to SN93R Delete All Remnants (page 152), except it only deletes remnants that are not in-process.

> **Warning:** This action cannot be undone.

**SN95R Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN95R). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |

**SN95R Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID)
VALUES ('SN95R', 1, '1000')
```

#### SN96 Delete Stock

SN96 is similar to SN92 Delete Stock (Except In-Process) (page 150), except it also deletes in-process stock.

**SN96 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN96). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ItemName** | varchar50 | yes | Stock name. |

**SN96 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemName)
VALUES ('SN96', 1, '1000', 'Sheet1')
```

#### SN97 Add Remnant

SN97 adds remnants to the inventory. The remnant can be defined by a standard shape or a CAD file. If there is an existing remnant of the same name, it is overwritten with the new remnant data.

**SN97 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (SN97). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ItemName** | varchar50 | yes | Remnant name. |
| **Qty** | int | yes | Number of remnants. |
| **Material** | varchar50 | yes | Material type (as defined in SigmaNEST). |
| **Thickness** | float | yes | Material thickness. |
| **FileName** | varchar50 | yes* | Name of the geometry file used to define the remnant. *Required only if remnant is defined from a CAD file. |
| **Length** | float | no | Remnant length. |
| **Width** | float | no | Remnant width. |
| **Cost** | float | no | Cost of the remnant. |
| **HeatNumber** | varchar50 | no | Heat number associated with the stock. |
| **TypeDescr** | varchar50 | yes* | Enter "Shape" to create the remnant from a standard shape. *Required only if remnant is created from the shape library. |
| **BinNumber** | varchar50 | no | Bin number associated with the stock. |
| **Location** | varchar50 | no | Location of the stock. |
| **Mill** | varchar50 | no | Mill quality associated with the stock. |
| **PrimeCode** | varchar50 | no | Prime code associated with the stock. |
| **ItemData1-4** | varchar50 | no | Sheet data from SigmaNEST. |
| **OrderShape** | varchar50 | yes* | Name of the SigmaNEST standard shape. *Required only if the TypeDescr is "Shape". |
| **BatchFile** | varchar225 | no | Batch file path to run. |
| **StringData1-8**| varchar50 | no | Batch commands to run. |
| **Param1-8** | float | yes* | Parameters for the standard shape specified in the OrderShape field. *Required only if the TypeDescr is "Shape." **Param3-4 can be used as standard shape parameters OR the parameters listed below. They cannot be used for both. |
| **Param3** | float | no | Actual weight OR standard shape parameter, as noted above. |
| **Param4** | float | no | Actual price OR standard shape parameter, as noted above. |
| **ItemData9** | varchar50 | no | MRP/ERP stock ID. |

**SN97 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemName, Qty, Material, Thickness, FileName)
VALUES ('SN97', 1, '1000', '70', 'Remnant1', 1, 'MS', 0.500, 'C:\Users\Public\Documents\CAD\Geo1.DXF')
```

### QTx Transactions: Quote Management

The QTx transactions manage quotes and work orders. Select a transaction from the following list to view the transaction description, variables, and a sample transaction.

-   QT10 Add Customer (page 164)
-   QT11 Modify Customer (page 166)
-   QT12 Delete Customer (page 168)
-   QT20 Add Address (page 169)
-   QT21 Modify Address (page 171)
-   QT22 Delete Address (page 173)
-   QT80 Add New Quote (page 174)
-   QT81 Modify Quote (page 176)
-   QT82 Mark Quote as Lost (page 178)
-   QT83 Add Standard Shape Part to Quote (page 179)
-   QT84 Add Existing Part to Quote (page 183)
-   QT85 Add CAD Part to Quote (page 186)
-   QT86 Add BOM to Quote (page 190)
-   QT88 Submit Quote (page 191)
-   QT89 Archive Quote (page 192)

#### QT10 Add Customer

QT10 adds new customers.

**QT10 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (QT10). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **Customer** | varchar50 | yes | Customer name. |
| **Remark** | varchar80 | no | Customer comment. |
| **Location** | varchar50 | no | The customer location. |
| **StringData1**| varchar50 | no | Customer description. |
| **StringData2**| varchar50 | no | Account Manager. |
| **StringData3**| varchar50 | no | Owner. |
| **StringData4**| varchar50 | no | Tax Number. |
| **StringData5**| varchar50 | no | External Reference Number. |
| **ItemID** | varchar50 | no | Unique customer ID. If an ID is not assigned, SigmaNEST automatically generates this number. |
| **TaxRate** | varchar50 | no | Tax rate as a percentage. |

**QT10 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, Customer)
VALUES ('QT10', 1, '1000', 'SigmaTEK')
```

#### QT11 Modify Customer

QT11 modifies existing customers.

**QT11 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (QT11). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **Customer** | varchar50 | yes* | Customer name. *Either the Customer or ItemID variable is required for this transaction. |
| **Remark** | varchar80 | no | Customer comment. |
| **Location** | varchar50 | no | The customer location. |
| **StringData1**| varchar50 | no | Customer description. |
| **StringData2**| varchar50 | no | Account Manager. |
| **StringData3**| varchar50 | no | Owner. |
| **StringData4**| varchar50 | no | Tax Number. |
| **StringData5**| varchar50 | no | External Reference Number. |
| **ItemID** | varchar50 | yes* | Unique customer ID. *Either the Customer or ItemID variable is required for this transaction. |
| **TaxRate** | varchar50 | no | Tax rate as a percentage. |

**QT11 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, Customer, StringData2)
VALUES ('QT11', 1, '1000', 'SigmaTEK', 'John Doe')
```

#### QT12 Delete Customer

QT12 deletes existing customers. This transaction also deletes all customer-related information, such as addresses and contacts.

**QT12 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (QT12). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **Customer** | varchar50 | yes* | Customer name. *Either the Customer or ItemID variable is required for this transaction. |
| **ItemID** | varchar50 | yes* | Unique customer ID. *Either the Customer or ItemID variable is required for this transaction. |

**QT12 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, Customer)
VALUES ('QT12', 1, '1000', 'SigmaTEK')
```

#### QT20 Add Address

QT20 adds an address to an existing customer's profile.

**QT20 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (QT20). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **Customer** | varchar50 | yes | Customer name. |
| **ItemType** | int | no | Address type. 0 = bill to, 1 = ship to. |
| **StringData1**| varchar50 | no | Address 1. |
| **StringData2**| varchar50 | no | Address 2. |
| **StringData3**| varchar50 | no | City. |
| **StringData4**| varchar50 | no | State. |
| **StringData5**| varchar50 | no | Zip Code. |
| **StringData6**| varchar50 | no | Country. |
| **ItemID** | int | no | Unique address ID. If an ID is not assigned, SigmaNEST automatically generates this number. |

**QT20 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, Customer, ItemType, StringData1, StringData3)
VALUES ('QT20', 1, '1000', 'SigmaTEK', 0, '1445 Kemper Meadow Drive', 'Cincinnati')
```

#### QT21 Modify Address

QT21 modifies an existing customer address.

**QT21 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (QT21). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **Customer** | varchar50 | yes | Customer name. |
| **ItemType** | int | no | Address type. 0 = bill to, 1 = ship to. |
| **StringData1**| varchar50 | no | Address 1. |
| **StringData2**| varchar50 | no | Address 2. |
| **StringData3**| varchar50 | no | City. |
| **StringData4**| varchar50 | no | State. |
| **StringData5**| varchar50 | no | Zip Code. |
| **StringData6**| varchar50 | no | Country. |
| **ItemID** | int | yes | Unique address ID. |

**QT21 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, Customer, StringData4, StringData5, ItemID)
VALUES ('QT21', 1, '1000', 'SigmaTEK', 0, 'OH', '45251', 12)
```

#### QT22 Delete Address

QT22 deletes an existing customer address.

**QT22 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (QT22). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ItemID** | int | yes | Unique address ID. |

**QT22 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemID)
VALUES ('QT22', 1, '1000', 12)
```

#### QT80 Add New Quote

QT80 creates a new quote.

**QT80 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (QT80). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Quote Number. |
| **Customer** | varchar50 | yes* | Customer name. *Either the Customer or ItemID variable is required for this transaction. |
| **Location** | varchar50 | no | The customer location. |
| **StringData1**| varchar50 | no | Quote comments. |
| **ItemID** | int | yes* | Unique customer ID. *Either the Customer or ItemID variable is required for this transaction. |
| **SalesRep** | varchar50 | no | Sales representative ID. |

**QT80 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, Customer)
VALUES ('QT80', 1, '1000', 'Q23', 'SigmaTEK')
```

#### QT81 Modify Quote

QT81 modifies information associated with an existing quote, such as customer name, sales rep, location, or due date.

**QT81 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (QT81). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Quote Number. |
| **DueDate** | datetime | no | Customer due date. |
| **Customer** | varchar50 | yes* | Customer name. *Either the Customer or ItemID variable is required for this transaction. |
| **Location** | varchar50 | no | The customer location. |
| **ItemID** | int | yes* | Unique customer ID. *Either the Customer or ItemID variable is required for this transaction. |
| **SalesRep** | varchar50 | no | Sales representative ID. |

**QT81 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, Customer, Location)
VALUES ('QT81', 1, '1000', 'Q23', 'SigmaTEK', 'Midwest')
```

#### QT82 Mark Quote as Lost

QT82 marks an existing quote as lost.

**QT82 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (QT82). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Quote Number. |

**SN82 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo)
VALUES ('QT82', 1, '1000', 'Q23')
```

#### QT83 Add Standard Shape Part to Quote

QT83 creates a part from a standard shape, then adds it to a quote.

**QT83 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (QT83). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Quote Number. |
| **ItemName** | varchar100 | yes | Part name. |
| **Qty** | int | yes | Number of parts. |
| **Material** | varchar50 | yes | Material type (as defined in SigmaNEST). |
| **Thickness** | float | yes | Material thickness. |
| **DueDate** | datetime | no | Customer due date. |
| **Customer** | varchar50 | yes* | Customer name. *Either the Customer or ItemID variable is required for this transaction. |
| **DwgNumber** | varchar50 | no | Drawing number associated with the part. |
| **Priority** | int | no | Part priority (as defined in SigmaNEST). |
| **ProgBy** | varchar50 | no | Name of programmer associated with the part. |
| **FileName** | varchar255 | yes | Path to the part file that will be created from the standard shape. |
| **Remark** | varchar80 | no | Customer comment. |
| **RevNumber** | varchar50 | no | Revision associated with the SigmaNEST part. |
| **OnHold** | bit | no | 0 = not on hold, 1 = on hold (on hold means that the order is on hold and the part is not available for nesting). |
| **ItemData1-18**| varchar50 | no | Extra data fields associated with SigmaNEST parts. |
| **OrderShape** | varchar50 | yes | Name of the SigmaNEST standard shape. |
| **BatchFile** | varchar225 | no | Batch file path to run before creating the part. |
| **Process** | varchar50 | no | Machine name or ID (as defined in Load Manager). |
| **StringData1-8**| varchar50 | no | Batch commands to run before creating the part. |
| **Param1-8** | float | no* | Parameters for the standard shape specified in the OrderShape field. *Required if using standard shapes with parameters. |
| **ItemID** | int | yes* | Unique customer ID. *Either the Customer or ItemID variable is required for this transaction. |

**QT83 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName, Qty, Material, Thickness, Customer, FileName, OrderShape, Param1, Param2)
VALUES ('QT83', 1, '1000', 'Q23', 'Part1', 25, 'MS', 0.500, 'SigmaTEK', 'C:\Users\Public\Documents\SNDATA\Parts\Part1.prs', 'Shape1', 10, 10)
```

#### QT84 Add Existing Part to Quote

QT84 adds an existing SigmaNEST part to a quote.

**QT84 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (QT84). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Quote Number. |
| **ItemName** | varchar100 | yes | Part name. |
| **Qty** | int | yes | Number of parts. |
| **Material** | varchar50 | no | Material type (as defined in SigmaNEST). |
| **Thickness** | float | no | Material thickness. |
| **DueDate** | datetime | no | Customer due date. |
| **Customer** | varchar50 | yes* | Customer name. *Either the Customer or ItemID variable is required for this transaction. |
| **DwgNumber** | varchar50 | no | Drawing number associated with the part. |
| **Priority** | int | no | Part priority (as defined in SigmaNEST). |
| **ProgBy** | varchar50 | no | Name of programmer associated with the part. |
| **Remark** | varchar80 | no | Customer comment. |
| **RevNumber** | varchar50 | no | Revision associated with the SigmaNEST part. |
| **OnHold** | bit | no | 0 = not on hold, 1 = on hold (on hold means that the order is on hold and the part is not available for nesting). |
| **ItemData1-18**| varchar50 | no | Extra data fields associated with SigmaNEST parts. |
| **Process** | varchar50 | no | Machine name or ID (as defined in Load Manager). |
| **Param1** | float | yes | 0 = use specified part quantity, 1 = use original part quantity. |
| **ItemID** | int | yes* | Unique customer ID. *Either the Customer or ItemID variable is required for this transaction. |

**QT84 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName, Qty, Customer, Param1)
VALUES ('QT84', 1, '1000', 'Q23', 'Part1', 25, 'SigmaTEK', 0)
```

#### QT85 Add CAD Part to Quote

QT85 converts an existing geometry file into a SigmaNEST part, then adds it to a quote.

**QT85 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (QT85). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Quote Number. |
| **ItemName** | varchar100 | yes | Part name. |
| **Qty** | int | yes | Number of parts. |
| **Material** | varchar50 | yes | Material type (as defined in SigmaNEST). |
| **Thickness** | float | yes | Material thickness. |
| **DueDate** | datetime | no | Customer due date. |
| **Customer** | varchar50 | yes* | Customer name. *Either the Customer or ItemID variable is required for this transaction. |
| **DwgNumber** | varchar50 | no | Drawing number associated with the part. |
| **Priority** | int | no | Part priority (as defined in SigmaNEST). |
| **ProgBy** | varchar50 | no | Name of programmer associated with the part. |
| **FileName** | varchar255 | yes | Path to the geometry file used to create the part. |
| **Remark** | varchar80 | no | Customer comment. |
| **RevNumber** | varchar50 | no | Revision associated with the SigmaNEST part. |
| **ItemType** | int | no | 0 = standard part, 1 = filler part. |
| **OnHold** | bit | no | 0 = not on hold, 1 = on hold (on hold means that the order is on hold and the part is not available for nesting). |
| **TypeDescr** | varchar50 | yes | Geometry type, typically the same as the file extension (DXF, DWG, IGES, etc.). |
| **ItemData1-18**| varchar50 | no | Extra data fields associated with SigmaNEST parts. |
| **OrderShape** | varchar50 | no | If the file extension does not match the geometry type (specified in TypeDescr), use this variable to specify the file extension. |
| **BatchFile** | varchar255 | no | Batch file path to run before creating the part. |
| **Process** | varchar50 | no | Machine name or ID (as defined in Load Manager). |
| **StringData1-8**| varchar50 | no | Batch commands to run before creating the part. |
| **ItemID** | int | yes* | Unique customer ID. *Either the Customer or ItemID variable is required for this transaction. |

**QT85 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName, Qty, Material, Thickness, Customer, FileName)
VALUES ('QT85', 1, '1000', 'Q23', 'Part1', 25, 'MS', 0.500, 'SigmaTEK', 'C:\Public\Users\Documents\CAD\Geo1.DXF')
```

#### QT86 Add BOM to Quote

QT86 loads a BOM file into the specified quote.

**QT86 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (QT86). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Quote Number. |
| **Qty** | int | yes | BOM quantity. |
| **FileName** | varchar255 | yes | Path to the BOM file. |

**QT86 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, Qty, FileName)
VALUES ('QT86', 1, '1000', 'Q23', 25, 'C:\Public\Users\Documents\BOM\BOM1.BOM')
```

#### QT88 Submit Quote

QT88 submits an existing quote to a customer. This is the same as clicking Submit in the SigmaNEST Info Manager.

**QT88 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (QT88). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | int | yes | Quote Number. |

**QT88 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo)
VALUES ('QT88', 1, '1000', 'Q23')
```

#### QT89 Archive Quote

QT89 archives an existing quote. This is the same as clicking Archive in the SigmaNEST Info Manager.

**QT89 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (QT89). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | int | yes | Quote Number. |

**QT89 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo)
VALUES ('QT89', 1, '1000', 'Q23')
```

### CTLx Transactions: Cut-to-Length

The CTLx transactions manage Cut-to-Length orders, parts, and stock. Select a transaction from the following list to view the transaction description, variables, and a sample transaction.

-   CTL10 Add CTL Part to Work Order (page 194)
-   CTL11 Modify CTL Work Order Parts (page 196)
-   CTL12 Cancel CTL Work Order Part (page 198)
-   CTL13 New CTL Shape (page 199)
-   CTL14 Add Profile to CTL Shape (page 201)
-   CTL15 Add Material to CTL Shape (page 203)
-   CTL21 Create CTL Cut Plan (page 205)
-   CTL22 Update CTL Cut Plan (page 206)
-   CTL24 New CTL Task (page 208)
-   CTL25 Modify CTL Task (page 209)
-   CTL26 Delete CTL Task (page 210)
-   CTL27 Update CTL Task (page 211)
-   CTL28 Add CTL Parts to Task (page 212)
-   CTL29 Remove CTL Parts from Task (page 213)
-   CTL30 New CTL Stock (page 214)
-   CTL31 Modify CTL Stock (page 216)
-   CTL32 Delete CTL Stock (page 218)
-   CTL33 Add CTL Stock to Task (page 219)
-   CTL34 Remove CTL Stock from Task (page 220)

#### CTL10 Add CTL Part to Work Order

CTL10 adds a CTL part to a work order. If the work order and/or part already exist, the existing data is overwritten.

**CTL10 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL10). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | no | CTL part name (automatically increments if not specified). |
| **Qty** | int | yes | Number of parts. |
| **Material** | varchar50 | no | Material type (as defined in SigmaNEST). |
| **DueDate** | datetime | no | The part's due date (using the system's datetime format). |
| **Customer** | varchar50 | no | Customer name. |
| **Length** | float | no | CTL part length. |
| **ItemData1-5**| varchar50 | no | Extra data fields associated with SigmaNEST parts. |
| **OrderShape** | varchar50 | yes | CTL profile name. |
| **StringData1**| varchar50 | yes | Units. Accepted values are "Imperial" and "Metric"(not case-sensitive). |

**CTL10 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName, Qty, OrderShape, StringData1)
VALUES ('CTL10', 1, '1000', '70', 'CTLPart1', 25, 'M4X6', 'Imperial')
```

#### CTL11 Modify CTL Work Order Parts

CTL11 modifies CTL parts in an existing work order.

**CTL11 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL11). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | yes | CTL part name (automatically increments if not specified). |
| **Qty** | int | no | Number of parts. |
| **Material** | varchar50 | no | Material type (as defined in SigmaNEST). |
| **DueDate** | datetime | no | The part's due date (using the system's datetime format). |
| **Length** | float | no | CTL part length. |
| **ItemData1-5**| varchar50 | no | Extra data fields associated with SigmaNEST parts. |

**CTL11 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName, Qty)
VALUES ('CTL11', 1, '1000', '70', 'CTLPart1', 5)
```

#### CTL12 Cancel CTL Work Order Part

CTL12 removes a CTL part from a work order.

**CTL12 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL12). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | yes | CTL part name (automatically increments if not specified). |

**CTL12 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName)
VALUES ('CTL12', 1, '1000', '70', 'CTLPart1')
```

#### CTL13 New CTL Shape

CTL13 creates a new CTL shape.

**CTL13 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL13). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **TypeDescr** | varchar50 | yes | CTL standard shape type, as listed in the SigmaNEST CTL Setup dialog box. |
| **OrderShape** | varchar50 | yes | CTL profile name. |
| **StringData1**| varchar50 | yes | Units. Accepted values are "Imperial" and "Metric"(not case-sensitive). |
| **Param 1-8** | float | no | Parameters for the specified standard shape type. |

**CTL13 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, TypeDescr, OrderShape, StringData1, Param1, Param2, Param3, Param4, Param5)
VALUES ('CTL13', 1, '1000', 'Miscellaneous Beams (M-Shapes)', 'M4X6', 'Imperial', 3.8, 3.8, 0.13, 0.16, 0.5)
```

#### CTL14 Add Profile to CTL Shape

CTL14 adds a new profile to an existing CTL shape.

**CTL14 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL14). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderShape** | varchar50 | yes | CTL profile name. |
| **Param1** | float | yes | Weight of the CTL shape. |
| **Param2** | float | yes | Edge distance of the CTL shape. |
| **Param3** | float | yes | Minimum remnant length of the CTL shape. |
| **StringData1**| varchar50 | yes | Units. Accepted values are "Imperial" and "Metric"(not case-sensitive). |

**CTL14 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderShape, Param1, Param2, Param3, StringData1)
VALUES ('CTL14', 1, '1000', 'M4X6', 6, 0, 0, 'Imperial')
```

#### CTL15 Add Material to CTL Shape

CTL15 assigns a material to an existing CTL shape.

**CTL15 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL15). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderShape** | varchar50 | yes | CTL profile name. |
| **Material** | varchar50 | yes | Material type (as defined in SigmaNEST). |
| **Cost** | float | no | The cost of the material. |
| **Param1** | float | yes | Density of the material. |
| **Param2** | float | yes | Cutting time. |
| **StringData1**| varchar50 | yes | Units. Accepted values are "Imperial" and "Metric"(not case-sensitive). |

**CTL15 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderShape, Material, Param1, Param2, StringData1)
VALUES ('CTL15', 1, '1000', 'M4X6', 'A36', 0.0975, 0, 'Imperial')
```

#### CTL21 Create CTL Cut Plan

CTL21 creates a new CTL cut plan for a task.

**CTL21 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL21). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **StringData3**| varchar50 | yes | Task name. |

**CTL21 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, StringData3)
VALUES ('CTL21', 1, '1000', 'Task1')
```

#### CTL22 Update CTL Cut Plan

CTL22 updates an existing CTL cut plan.

**CTL22 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL22). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ProgramName**| varchar50 | yes | Cut plan name. |

**CTL22 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ProgramName)
VALUES ('CTL22', 1, '1000', 'CutPlan1')
```

#### CTL23 Delete CTL Cut Plan

CTL23 deletes an existing CTL cut plan.

**CTL23 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL23). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ProgramName**| varchar50 | yes | Cut plan name. |

**CTL23 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ProgramName)
VALUES ('CTL23', 1, '1000', 'CutPlan1')
```

#### CTL24 New CTL Task

CTL24 creates a new CTL task.

**CTL24 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL24). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **StringData1**| varchar50 | no | Machine name or ID. |
| **StringData2**| varchar50 | no | true = create remnant, false = do not create remnant. |
| **StringData3**| varchar50 | yes | Task name. |
| **Param1** | float | no | Kerf. |

**CTL24 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, StringData3)
VALUES ('CTL24', 1, '1000', 'Task1')
```

#### CTL25 Modify CTL Task

CTL25 modifies an existing CTL task.

**CTL25 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL25). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **StringData1**| varchar50 | no | Machine name or ID. |
| **StringData2**| varchar50 | no | true = create remnant, false = do not create remnant. |
| **StringData3**| varchar50 | yes | Task name. |
| **Param1** | float | no | Kerf. |

**CTL25 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, StringData2, StringData3)
VALUES ('CTL25', 1, '1000', 'True', 'Task1')
```

#### CTL26 Delete CTL Task

CTL26 deletes an existing CTL task.

**CTL26 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL26). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **StringData3**| varchar50 | yes | Task name. |

**CTL26 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, StringData3)
VALUES ('CTL26', 1, '1000', 'Task1')
```

#### CTL27 Update CTL Task

CTL27 updates an existing CTL task.

**CTL27 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL27). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **StringData3**| varchar50 | yes | Task name. |

**CTL27 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, StringData3)
VALUES ('CTL27', 1, '1000', 'Task1')
```

#### CTL28 Add CTL Parts to Task

CTL28 adds a CTL part to a task.

**CTL28 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL28). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | yes | CTL part name (automatically increments if not specified). |
| **OrderShape** | varchar50 | yes | CTL profile name. |
| **StringData3**| varchar50 | yes | Task name. |

**CTL28 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName, OrderShape, StringData3)
VALUES ('CTL28', 1, '1000', '70', 'CTLPart1', 'M4X6', 'Task1')
```

#### CTL29 Remove CTL Parts from Task

CTL29 removes a CTL part from a task.

**CTL29 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL29). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **OrderNo** | varchar50 | yes | Work order number. |
| **ItemName** | varchar100 | yes | CTL part name (automatically increments if not specified). |
| **OrderShape** | varchar50 | yes | CTL profile name. |
| **StringData3**| varchar50 | yes | Task name. |

**CTL29 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, OrderNo, ItemName, OrderShape, StringData3)
VALUES ('CTL29', 1, '1000', '70', 'CTLPart1', 'M4X6', 'Task1')
```

#### CTL30 New CTL Stock

CTL30 adds new CTL stock. If the specified stock already exists, the quantity entered is added to the stock library.

**CTL30 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL30). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ItemName** | varchar50 | no | CTL stock name. |
| **Qty** | int | no | Quantity of stock to add. |
| **Material** | varchar50 | no | Material type (as defined in SigmaNEST). |
| **Length** | float | no | CTL stock length. |
| **HeatNumber** | varchar50 | no | Heat number associated with the stock. |
| **BinNumber** | varchar50 | no | Bin number associated with the stock. |
| **Location** | varchar50 | no | Location of the stock. |
| **Mill** | varchar50 | no | Mill quality associated with the stock. |
| **PrimeCode** | varchar50 | no | Prime code associated with the stock. |
| **ItemData1-5**| varchar50 | no | Extra data fields associated with the CTL stock. |
| **OrderShape** | varchar50 | yes | CTL profile name. |
| **StringData1**| varchar50 | yes | Units. Accepted values are "Imperial" and "Metric"(not case-sensitive). |

**CTL30 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemName, Qty, OrderShape, StringData1)
VALUES ('CTL30', 1, '1000', 'CTLStock1', 5, 'M4X6', 'Imperial')
```

#### CTL31 Modify CTL Stock

CTL31 modifies existing CTL stock.

**CTL31 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL31). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ItemName** | varchar50 | no | CTL stock name. |
| **Qty** | int | no | Quantity of stock to add. |
| **Material** | varchar50 | no | Material type (as defined in SigmaNEST). |
| **Length** | float | no | CTL stock length. |
| **HeatNumber** | varchar50 | no | Heat number associated with the stock. |
| **BinNumber** | varchar50 | no | Bin number associated with the stock. |
| **Location** | varchar50 | no | Location of the stock. |
| **Mill** | varchar50 | no | Mill quality associated with the stock. |
| **PrimeCode** | varchar50 | no | Prime code associated with the stock. |
| **ItemData1-5**| varchar50 | no | Extra data associated with the CTL stock. |
| **OrderShape** | varchar50 | yes | CTL profile name. |
| **StringData1**| varchar50 | yes | Units. Accepted values are "Imperial" and "Metric"(not case-sensitive). |

**CTL31 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemName, Qty, OrderShape, StringData1)
VALUES ('CTL31', 1, '1000', 'CTLStock1', 10, 'M4X6', 'Imperial')
```

#### CTL32 Delete CTL Stock

CTL32 deletes the specified CTL stock.

**CTL32 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL32). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ItemName** | varchar50 | yes | CTL stock name. |
| **OrderShape** | varchar50 | yes | CTL profile name. |
| **StringData1**| varchar50 | yes | Units. Accepted values are "Imperial" and "Metric"(not case-sensitive). |

**CTL32 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemName, OrderShape, StringData1)
VALUES ('CTL32', 1, '1000', 'CTLStock1', 'M4X6', 'Imperial')
```

#### CTL33 Add CTL Stock to Task

CTL33 adds CTL stock to a task.

**CTL33 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL33). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ItemName** | varchar50 | yes | CTL stock name. |
| **OrderShape** | varchar50 | yes | CTL profile name. |
| **StringData3**| varchar50 | yes | Task name. |

**CTL33 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemName, OrderShape, StringData3)
VALUES ('CTL33', 1, '1000', 'CTLStock1', 'M4X6', 'Task1')
```

#### CTL34 Remove CTL Stock from Task

CTL34 removes CTL stock from a task.

**CTL34 Variables**

| Variable | Type | Required | Definition |
| :--- | :--- | :---: | :--- |
| **TransType** | varchar10 | yes | Transaction number (CTL34). |
| **District** | int | yes | Unique database identifier. |
| **TransID** | varchar10 | no | Any value provided by an external system. Referred to when logging successes and failures. |
| **ItemName** | varchar50 | yes | CTL stock name. |
| **OrderShape** | varchar50 | yes | CTL profile name. |
| **StringData3**| varchar50 | yes | Task name. |

**CTL34 Example**
```sql
INSERT INTO [SimTrans].[dbo].[TransAct] (TransType, District, TransID, ItemName, OrderShape, StringData3)
VALUES ('CTL34', 1, '1000', 'CTLStock1', 'M4X6', 'Task1')
```

## Chapter 4: Resources

This section contains the following additional resources for SimTrans:

-   FAQs/Troubleshooting
-   Technical Support
-   About Us

### FAQs/Troubleshooting

**How do I contact technical support?**

SigmaTEK's Technical Support Team is available Monday through Friday from 8:00 AM to 7:00 PM EST, excluding nationally recognized holidays. Support is available to trained users with a current maintenance subscription only. Please have your SimTrans version number ready before calling support.

-   **Phone:** 513.595.2002
-   **Email:** support@sigmanest.com

**How do I report a problem with SimTrans?**

1.  Restart SimTrans and recreate the conditions that caused the problem.
2.  If the issue occurs again, contact Technical Support (page 223). Explain how they can reproduce the problem, and provide any other required information.
3.  The SigmaTEK Support Team will work with you to troubleshoot and resolve the issue, or submit a bug to our development team.

Examples of errors that should be reported:

-   Access violation
-   List index out of bounds
-   Invalid pointer operation
-   Integer overflow
-   Out of memory

**I have a great idea for a new feature. How do I share it with you?**

Please contact Technical Support (page 223) to submit a feature request. We are always adding new features and improving SimTrans to meet our customers' needs, so we welcome and encourage constructive feedback.

### Technical Support

SigmaTEK's Technical Support Team is available Monday through Friday from 8:00 AM to 7:00 PM EST, excluding nationally recognized holidays. Support is available to trained users with a current maintenance subscription only. Please have your SimTrans version number ready before calling support.

-   **Phone:** 513.595.2002
-   **Email:** support@sigmanest.com

[Image: A friendly technical support representative at her desk, ready to assist customers.]

> **Tip:** Visit http://www.sigmanest.com/services/training/ to learn more about user training classes.

### About Us

SigmaTEK Systems, LLC provides robust CAD/CAM, nesting, and automation software solutions for every size business, from new job shops to established manufacturers.

[Image: The exterior of the SigmaTEK headquarters building.]

Since our founding in 1993, we have been dedicated to research, development, and extensive support for our products, including SigmaNEST, SigmaTUBE, SigmaBEND, SimTrans, SigmaMRP, and SigmaNEST SX.

SigmaNEST leads the world in nesting systems for fabrication, providing unsurpassed material utilization, motion optimization, manpower efficiency, manufacturing automation, and data management.

Supported by an expert team of mathematicians and engineers, SigmaTEK reaches the globe from its headquarters in Cincinnati, Ohio, with branches in Europe, Asia, Australia, Africa, and South America.

You can learn more about SigmaTEK at www.sigmanest.com.

---
**SIGMANEST software**
Nest with the Best®
