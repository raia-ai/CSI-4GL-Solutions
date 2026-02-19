---
title: "Madcap_-_SM3_Help-Content-ExternalFiles-SimTransManual"
source: "Madcap_-_SM3_Help-Content-ExternalFiles-SimTransManual.pdf"
tags: ["SimTrans", "SigmaNEST", "automation", "user manual", "transaction manager", "MRP", "ERP", "CAD/CAM", "SigmaTEK", "software"]
version: 1.0
last_updated: 2025-12-03
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
This manual may describe features that are not available in your version of SimTrans. To learn more about specific features or products, contact your SigmaNEST sales representative or visit www.sigmanest.com"
## Chapter 1: Get Started
Thank you for choosing to invest in SigmaNEST, the world's leading nesting solution for all fabrication machines. The opportunity to serve you as our customer is an honor for our team. We look forward to working with you and helping you get the most from your complete SigmaNEST software solution.
SimTrans is an online transaction manager that bridges the gap between SigmaNEST and your other business systems. It typically runs in the background on a SigmaNEST workstation or on a centralized server. After setup, SimTrans automatically checks for and runs new transactions as they are created.
### System Requirements
This section outlines the system requirements for SimTrans and SigmaNEST. All specifications assume that SimTrans and SigmaNEST are the primary products used on the computer on which they are installed. If other demanding products are run on the same computer, the requirements should be adjusted accordingly.
A USB port or high-speed Internet connection is required to install the software. For licensing purposes, a USB port must also be available on each workstation (for a local license) or on a computer accessible through an internal network (for a network license). A Digi Anywhere USB device can be used for network USB access.
The SigmaNEST database requires Microsoft SQL Server 2014 (64-bit). You can install the SQL server during the SigmaNEST installation, or use an existing installation of this version or higher.
#### Single system/workstation minimum requirements
-   **Operating system: ** 64-bit Windows Server 2012 R2
-   **Processor: ** Intel/AMD quad-core
-   **Memory: ** 8 GB
-   **Hard disk type: ** 3 or more drives configured as Raid 5, 7200 RPM
-   **Hard disk capacity: ** 500 GB
-   **Screen Resolution: ** 1280x1024
-   **Video card: ** Dedicated video card with Open GL version 4.0
-   **Network: ** High-speed Internet connection
### Installation
The SimTrans installation files are included with the SigmaNEST installation package. You can contact the Technical Support (page 223) team to request a USB flash drive with the installation files, or download the files directly from the SigmaTEK Connect site. Customers with a current maintenance subscription can download updates as they are released.
> **Note: ** Stock with a quantity of 0 is automatically deleted if **Delete sheets with 91A when Qty available = 0** is enabled in the Sheet Transactions (page 17) section of the Global Configuration (page 15).
**SN91A Variables**
| Variable | Type | Required | Definition |
-   **CPU: ** 1 or 2 Intel Xeon/AMD Opteron quad-core
-   **File system: ** NTFS or ReFS
> **Warning: ** This action cannot be undone.
**SN95R Variables**
| Variable | Type | Required | Definition |
11. If this is your first time installing SimTrans, enter a database name above the New Database button: -   Select **Load default data** if you want to add default values to the database.
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
> **Tip: ** Visit http://www.sigmanest.com/services/training/ to learn more about user training classes.
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
|: --- | :--- | :---: | :--- |
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
Select an existing district from the left list to view its details. You can modify the following fields as needed: 
-   **District number: ** The unique identifier associated with a district.
-   **District name: ** A memorable name that helps you associate the district number with the linked SigmaNEST profile.
-   **SigmaNEST profile: ** The exact name of the SigmaNEST profile that the district is linked to.
-   **SigmaNEST path: ** The path to the SigmaNEST executable. (This field cannot be modified.)
-   To run a batch (.wol) file before or after processing transactions, enter the name or path in the **Execute before** or **Execute after** box.
-   If you entered the batch file's name, but not the path, enter the **Batch path**.
3.  In the **Input file extension** box, enter the extension of the file(s) to be imported (for example, .csv). The following file types are currently supported: | Text | Lotus 1-2-3 | Paradox | ADO connection | HTML, XML |
14. Select **Append: add records to the destination table**, then click **Execute** to begin the import. The TransAct table will be populated with the selected data.
#### Geometry Conversion
You can set up SimTrans to automatically convert CAD files to SigmaNEST part files. To do this, use the steps below to enable geometry conversion in the District Configuration (page 18), then select a folder to be monitored. Whenever SimTrans is running, it will monitor that folder for new CAD files, immediately processing the files as they are added to the folder.
If the parts path is `C: \SNDATA\Parts` and the customer is SigmaTEK, the parts will be saved to `C:\SNDATA\Parts\SigmaTEK`.
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
The following data fields are used to specify allowed tolerances in the TransAct database: -   **ODPosTol** (outer diameter positive tolerance)
-   **ODNegTol** (outer diameter negative tolerance)
-   **IDPosTol** (inner diameter positive tolerance)
-   **IDNegTol** (inner diameter negative tolerance)
#### Example
For example, the part in the image below was created using an SN83 transaction with the following parameters: OrderShape = DISK, Param1 (diameter) = 10.00, ODPosTol = 0.040, and ODNegTol = 0.020.
-   Spreadsheet: https://goo.gl/nmxuaf
-   PDF: https://goo.gl/h8W2pM
-   [Feedback: Archived Work Orders (page 69)](#feedback-archived-work-orders)
#### Feedback: Archived Work Orders
The STWOARC feedback table contains information about archived work orders. SigmaNEST writes feedback to this table when a work order is archived.
**STWOARC Feedback Variables**
| Variable | Type | Definition |
The STPIPARC feedback table contains information about parts that are currently marked as "in process." SigmaNEST writes feedback to this table when work order parts are: -   Posted
-   Updated
-   Deleted
The following list displays all variables in the STPIPARC table.
**STPIPARC Feedback Variables**
| Variable | Type | Definition |
The STPrgARC feedback table contains information about NC programs. SigmaNEST writes feedback to this table when an NC program is: -   Posted
-   Deleted
-   Updated
The following list displays all variables in the STPrgARC table.
**STPrgARC Feedback Variables**
| Variable | Type | Definition |
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
VALUES ('SN85', 1, '1000', '70', 'Part1', 25, 'MS', 'C: \Public\Users\Documents\CAD\Geo1.DXF')
```
#### SN86 Add BOM to Work Order
SN86 loads a bill of materials (BOM) into the specified work order.
VALUES ('SN86', 1, '1000', '70', 25, 'C: \Public\Users\Documents\BOM\BOM1.BOM')
```
#### SN87 Modify Work Order
SN87 modifies attributes of an existing work order, leaving the parts in the work order unaltered.
**SN87 Variables**
| Variable | Type | Required | Definition |
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
VALUES ('SN97', 1, '1000', '70', 'Remnant1', 1, 'MS', 0.500, 'C: \Users\Public\Documents\CAD\Geo1.DXF')
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
VALUES ('QT83', 1, '1000', 'Q23', 'Part1', 25, 'MS', 0.500, 'SigmaTEK', 'C: \Users\Public\Documents\SNDATA\Parts\Part1.prs', 'Shape1', 10, 10)
```
#### QT84 Add Existing Part to Quote
QT84 adds an existing SigmaNEST part to a quote.
**QT84 Variables**
| Variable | Type | Required | Definition |
VALUES ('QT85', 1, '1000', 'Q23', 'Part1', 25, 'MS', 0.500, 'SigmaTEK', 'C: \Public\Users\Documents\CAD\Geo1.DXF')
```
#### QT86 Add BOM to Quote
QT86 loads a BOM file into the specified quote.
**QT86 Variables**
| Variable | Type | Required | Definition |
VALUES ('QT86', 1, '1000', 'Q23', 25, 'C: \Public\Users\Documents\BOM\BOM1.BOM')
```
#### QT88 Submit Quote
QT88 submits an existing quote to a customer. This is the same as clicking Submit in the SigmaNEST Info Manager.
**QT88 Variables**
| Variable | Type | Required | Definition |
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
## Chapter 4: Resources
This section contains the following additional resources for SimTrans: -   FAQs/Troubleshooting
-   Technical Support
-   About Us
### FAQs/Troubleshooting
**How do I contact technical support?**
SigmaTEK's Technical Support Team is available Monday through Friday from 8: 00 AM to 7:00 PM EST, excluding nationally recognized holidays. Support is available to trained users with a current maintenance subscription only. Please have your SimTrans version number ready before calling support.
-   **Phone: ** 513.595.2002
-   **Email: ** support@sigmanest.com
Examples of errors that should be reported: -   Access violation
-   List index out of bounds
-   Invalid pointer operation
-   Integer overflow
-   Out of memory
**I have a great idea for a new feature. How do I share it with you?**
Please contact Technical Support (page 223) to submit a feature request. We are always adding new features and improving SimTrans to meet our customers' needs, so we welcome and encourage constructive feedback.
### Technical Support
---

# Madcap_-_SM3_Help-Content-ExternalFiles-SimTransManual
