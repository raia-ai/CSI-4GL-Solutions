---
title: "Stock Management System IS-200 Host Connection Specifications [Disk Sharing Type]"
source: "madcap-sm3-help-content-externalfiles-toyota-stockmanagementsystem.md"
tags: ['SM3', 'System Help']
version: "1.0"
last_updated: "2026-02-19"
short_description: "Stock Management System IS-200 Host Connection Specifications [Disk Sharing Type]"
long_description: "This document provides detailed information about stock management system is-200 host connection specifications [disk sharing type] in the 4GL system. It includes procedures, reference information, and best practices for users and administrators."
---
**Unauthorized Reproduction Prohibited**

# Stock Management System IS-200 Host Connection Specifications [Disk Sharing Type]
## Second Edition

**TOYOTA INDUSTRIES CORPORATION**
**Toyota Material Handling Japan**
**Logistics System Engineering Dept.**

| Approved by | Examined by | Prepared by |
| :---: | :---: | :---: |
| [Stamp] | [Stamp] | [Stamp] |

---

## Revision History

| Edition | Symbol | Change | Changed page | Date | Examined by | Prepared by |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| First | | Newly prepared | | April 25, 2022 | Katou | Tsuzuki |

---

## Contents

1.  **Introduction**
2.  **Basic Specifications**
3.  **Data Transmission/Receipt Method**
    3.1 Setting Items
    3.2 File Transfer Specifications
    3.3 Transfer Sequence
    3.4 Other
4.  **Transmission/Receipt Data**
5.  **Data Specifications**
    5.1 Storage and retrieval order data
    5.2 Item# Master
    5.3 Storage and Retrieval Results Data
    5.4 Stock Data

---

## 1. Introduction

The optional functions for the “Stock Management System IS-200 (hereinafter referred to as the system)” include a host communication function for sending and receiving data to and from the customer's computer.

(Disk sharing format is the preferred form of operation)

*   It is possible to share disks (folders) between the customer's computer and this system using the network function of Windows Server 2019.
*   Purpose of this system is to reduce the workload of creating applications on the customer's side by simply copying instructions from the customer's system to this system without using FTP or other commands.

---

## 2. Basic Specifications

The basic specifications and operating environment are described below.

**System Diagram**

*   **Host computer (customer's)** connects via **Ethernet** to a **HUB**.
*   **Stock management computer (TOYOTA INDUSTRIES)** also connects via **Ethernet** to the **HUB**.
*   **Data Flow:**
    *   (1) Receiving storage and retrieval order (Host -> Stock Mgmt)
    *   (2) Receiving Parts# master (Host -> Stock Mgmt)
    *   (3) Sending storage and retrieval result (Stock Mgmt -> Host)
    *   (4) Sending stock data (Stock Mgmt -> Host)

**Connection Specifications**
*   **Protocol**: TCP/IP, NetBIOS
*   **Line**: Ethernet

**Inventory management computer specifications**
*   **OS**: Windows Server 2019

### Items to be prepared by customer beforehand

| No | Category | Item | Details |
| :-- | :--- | :--- | :--- |
| 1 | Communication | Ethernet HUB | • A LAN connection should be possible using Ethernet.<br>• The hub should be installed near the stock management computer (within 10 m), and network wiring work should be carried out between the hub and host computer. (Wiring between hub and stock management computer carried out by TOYOTA INDUSTRIES.)<br>• The above hub installation and network wiring work should be completed before making final adjustments to the entire system. |
| 2 | Registration | Host name<br>Work group name<br>User registration<br>IP address | • Stock management computer, host computer host name (computer name) should be decided by customer first, and notified prior to TOYOTA INDUSTRIES.<br>• User information should be registered to allow the TOYOTA INDUSTRIES stock management computer and host equipment to access one another.<br>• The stock management computer and host computer IP addresses should be decided and notification given beforehand. |

---

## 3. Data Transmission/Receipt Method

### 3.1 Setting Items

**(1) Stock management computer settings**
*(When TOYOTA INDUSTRIES' stock management computer shares its folder to customer's computer)*

*   **Host name**: Decided by customer (Default name: ISMAIN)
*   **IP address**: Decided by customer
*   **Protocol used**: TCP/IP, NetBIOS
*   **Services**: Server services and workstation services are used.
*   **Work group name**: Decided by customer (Default name: ISGROUP)
*   **Common name**: Decided by customer (Default name: ZAIKO)
*   **User name**: Decided by customer (Default name: isuser)
*   **Password**: Decided by customer (Default password: is200)

**(2) Host computer (customer's) setting**
*(When customer's computer shares its folder to TOYOTA INDUSTRIES' stock management computer)*

*   **Host name**: Please let us know.
*   **IP address**: Please let us know.
*   **Protocol used**: TCP/IP, NetBIOS
*   **Services**: Server services and workstation services are used.
*   **Work group name**: Please let us know.
*   **Common name**: Decided by customer (Default name: JOUI)
*   **User name when accessing customer's computer**: Please let us know.
*   **Password when accessing customer's computer**: Please let us know.

### 3.2 File Transfer Specifications

*   **File type**: Standard sequential text files
*   **Data transmission method**: Data is transmitted by preparing a shared disk (=shared folder) on the host computer and/or the stock management computer and copying the files onto that disk. *Usually, a shared disk is created on either computer.
*   **Transfer directory**: Please let us know the shared name for the shared disk, and the directory used for sending and receiving files. If the shared disk is created at the stock management computer, by default, folder (`d:\pgm\dat\joui`) will be named as "ZAIKO" and used for sharing.
*   **Transmission/receipt start method**: Data transmission and receipt is started from the stock management computer operation screen.

### 3.3 Transfer Sequence

(In the following description, the shared disk is located in TOYOTA INDUSTRIES' stock management computer.)

**(1) Storage and retrieval order data**

1.  Storage and retrieval order data is edited and files are saved by screen operation at the host computer.
2.  The above files are copied to the shared disk on the stock management computer by screen operation at the host computer.
3.  Files transferred, by screen operation at the stock management computer, are read.
4.  If necessary, the host computer checks the success or failure of the assignment process.
    *   The stock management computer transmits the success or failure of the assignment process only when it is set to "Transmit result file".
    *   When the inventory control computer is set to "With automatic assignment" and "Transmit result file" it will not receive the data for the storage (retrieval) orders, if there are any unsent results of the storage (retrieval) assignment.
    *   ※If the stock management computer performs automatic assignment, and host computer does not check the success or failure of the assignment, inventory discrepancies may occur when the storage assignment fails.

*Diagram: Storage and Retrieval Order Data Flow*
1.  *Host computer creates and saves the order file.*
2.  *Host computer copies the order file to the shared disk on the Stock Management computer.*
3.  *Stock Management computer reads and processes the file.*
4.  *Host computer checks the result (optional).*

**(2) Item# master**

1.  Data is edited and files are saved by screen operation at the host computer.
2.  The above files are copied to the shared disk on the stock management computer by screen operation at the host computer.
3.  Files transferred, by screen operation at the stock management computer, are read.
4.  The stock management computer writes the update result to a file, and then copies the file to the shared disk.
5.  The update result is then checked at the host computer.

*Diagram: Item Master Data Flow*
1.  *Host computer creates and saves the item master file.*
2.  *Host computer copies the file to the shared disk on the Stock Management computer.*
3.  *Stock Management computer reads and processes the file.*
4.  *Stock Management computer writes a result file and copies it to the shared disk.*
5.  *Host computer reads the result file to check the update status.*

**(3) Storage and retrieval results data, stock data**

1.  Files are copied to the shared disk by screen operation at the stock management computer.
2.  Shared disk files are read at the host computer.

*Diagram: Results/Stock Data Flow*
1.  *Stock Management computer writes data (results, stock info) to a file on the shared disk.*
2.  *Host computer reads the file from the shared disk.*

### 3.4 Other

*   The following two items must be possible in order to send and receive the data.
    *   If the shared disk is located on the host computer, the shared disk must be configurable as a Windows Server 2019 or Windows 10 network drive when the stock management computer starts.
    *   When a shared disk is located on the stock control computer, it must be possible to connect to the shared disk from the host computer side.
    Communication is possible if the above two conditions are met. If you wish to connect using another method, please consult us separately.

*   Data can be transferred using either of the following two methods:
    1.  By stock management computer screen operation or host computer screen operation
    2.  Automatic transfer at a fixed time or interval, or when files are written (*1)

*   The success of data transfer can be checked using either of the following two methods:
    1.  By checking at the operation screen when transferring data
    2.  By checking the results file (*2) or error log

*   Storage and retrieval order data files (`F01`, `F02`) on the data receipt disk are deleted once they have been read by the stock management computer. To check the result, results file (`F01`, `F02`) is written to the transmission directory. (*3)

*   Furthermore, if older files with the same name as new files, that has created by the stock management computer (Assignment result file, Item# Master receipt results, results data, stock data), already exist at that location, no further data will be written until these files have been deleted.

---
**Footnotes:**

*   **\*1: If data is transferred automatically when files are written:**
    1.  Communication is performed using data files only, or
    2.  Communication is performed using data files and a trigger file.

    In the case of 2), perform communication using the following procedure.
    *   **Transmission processing**: Data is written in the order of data file, then trigger file.
    *   **Receipt processing**: Data files are read when both the data files and the trigger file have been prepared, and the data files and trigger file are then deleted. Furthermore, to prevent communication stopping when only the trigger file remains for some reason, the trigger file is forcibly deleted if the trigger file only continues to exist for a fixed period of time when no data files exist.

*   **\*2: The results file is written only if "Transmit result file" is set.** If "Transmit result file" is set, and assignment fails at F01, assignment is not performed for that data anymore. Operations such as re-assignment and maintenance should be performed at the screen for data for which assignment has failed.

*   **\*3: Delete the results file at the host computer.** If a results file remains on the stock management computer, the next results file will not be sent.

---

## 4. Transmission/Receipt Data

The transmission/receipt data types and an overview of processing are described below.

| No | Data name | Details |
| :-- | :--- | :--- |
| 1 | Storage and retrieval order data | Storage and retrieval order data created by the customer is received, and storage and retrieval is performed at the auto-stacking warehouse managed by the TOYOTA INDUSTRIES stock management system. |
| 2 | Item# master | Item# master data created by the customer is received, and Item# master data managed by the TOYOTA INDUSTRIES stock management system is updated. |
| 3 | Storage and retrieval results data | Results data of the storage and retrieval performed at TOYOTA INDUSTRIES auto-stacking warehouse will be provided. |
| 4 | Stock data | Stock information managed by the TOYOTA INDUSTRIES stock management system will be provided. |

---

## 5. Data Specifications

### 5.1 Storage and retrieval order data

Storage and retrieval order data received from the host computer is registered in the stock management system, and the storage and retrieval assignment and storage and retrieval operations are performed. Refer to the separate document "Screen Layout" for screen images. Processing is performed by carrying out the following operations at the host order screen.

*   Start reading host order data.
*   Display the read storage and retrieval order data, select the storage and retrieval order for parts to be stored and retrieved, and start storage and retrieval.
    *When automatic storage and retrieval processing is performed, the above operation is usually not necessary. Only for data that fails to be assigned, an operation on the screen is required.

**(1) File name, file format**
*   **File name**:
    *   `F01.CSV` (Storage order data)
    *   `F02.CSV` (Retrieval order data)
*   **File format**: Sequential text file
*Refer to the separate document "File Design Sheet" for details on data items.*

**(2) Storage order data**
One or more Item# unit data records are continuously set in file `F01`. Storage assignment is processed in units of the same storage order No. Storage locations are determined in units of the same pallet No. in each storage order No. When data with the same No. as the already registered storage order No. is received, the previous data is discarded and the newly received data will be validated. In this case, all previously received data is returned as an assignment failure.

*Diagram: `F01` Storage Order Data Processing*
*   *A received file (`F01.CSV`) contains multiple records, grouped by `Storage order No.`.*
*   *Storage assignment is performed per `storage order No.` unit.*
*   *Within a `Storage order No.`, storage location assignment is performed for each `pallet unit No.`.*
*   *This results in a `Storage order` being created in the system.*

**(3) Retrieval order data**
One or more BOX ID unit data records are continuously set in file `F02`. Retrieval assignment is processed in units of the same retrieval order No. Retrieval locations are determined in units of the same sequential No. in each retrieval order No.
When data with the same No. as the already registered retrieval order No. is received, the previous data is discarded and the newly received data is validated. In this case, all previously received data is returned as assignment failure.
If there is data with the same "retrieval order No. + sequential No." in one file, the data after the second data will not be processed anymore.

*Diagram: `F02` Retrieval Order Data Processing*
*   *A received file (`F02.CSV`) contains multiple records, grouped by `Retrieval order No.`.*
*   *Retrieval assignment is performed per `retrieval order No.` unit.*
*   *Within a `Retrieval order No.`, retrieval location assignment is performed for each `sequential No.` (which corresponds to a `BOX ID`).*
*   *This results in a `Retrieval order` being created in the system.*

**(4) Data setting restrictions**
1.  A single file can hold up to 1,000 records.
2.  If storage and retrieval order No. data with the same number as a storage and retrieval order No. that has already read previously but not yet been erased (not yet assigned) has been registered, the previously registered storage and retrieval order No. data is erased, and new data will be registered.
3.  Continuously set same storage and retrieval order No. in one file.
4.  Use "Item#" that have already been registered at the TOYOTA INDUSTRIES stock management computer.
5.  Line break codes [`0x0D`, `0x0A`] are required at the end of the file.

**(5) Notes during the storage and retrieval operations (when operating the host order automatically)**
1.  Returns the results of successful or failed assignment, and file read failure, to the host computer.
2.  If assignment fails in the middle of host order data, the failed host order data is deleted. (If the configuration is set to manually assign host order data from the screen, the data that failed to be assigned will not be deleted. The data that failed to be assigned can be assigned again from the screen.)
3.  For details on assignment errors, please check TOYOTA INDUSTRIES stock management computer.
4.  Results are returned by file unit basis, if multiple orders are received in a single file, the results will not be returned until all assignments are completed.

### 5.2 Item# Master

The Item# Master is received from the host computer, and the Item# Master is updated inside the stock management computer. Batch update or differential update can be specified for the update process. Batch update is a method which involves replacing all Item# data to a new data, and differential update involves adding, deleting, or updating data for each Item#. The update processing method can be switched by the data. Refer to the separate document “Screen Layout" for screen images. Processing is performed by carrying out the following operations at the "Receive Item# Master" screen.
*   Start reading Item# Master data from the host computer.
    *   ※ If processing is performed automatically, the above operation is unnecessary.
    *   ※ A timeout may occur if attempting to receive large quantities of Item# data at one time. Be sure to receive no more than 1,000 items of Item# data at a time.

**(1) File name, file format**
*   **File name**: `F03.CSV` (Item# Master)
*   **File format**: Sequential text file
*Refer to the separate document “File Design Sheet" for details.*

**(2) Data setting restrictions**
1.  Item#s with processing class “A” (add) must be unregistered. Item#s are updated if they have already been registered.
2.  Item#s with processing class “U” (update) must have been registered beforehand. If not registered, the Item#s will be handled as error data, and updating or deleting will not be performed.
3.  If performing a batch update, set data with processing class "Z" (delete all) as dummy data in the first record, and then set the new data with which it is to be replaced as “A” (add). If performing a batch update, Item#s that cannot be deleted for reasons such as they still exist in the stock data are recorded in the error log, even if they have not been specified in the new data for replacement.
4.  The meaning of all items is the same as those for the system's Item# Master. Refer to the relevant manual for details.
5.  The edit class is a setting used to specify whether changes can be made with Item# Master inquiries (maintenance). The edit class should normally be set to "0"(editing possible).
6.  The "Update result" records whether the TOYOTA INDUSTRIES stock management system has successfully updated the Item# Master, and therefore the space should be filled in.
7.  Ensure that the same Item#s do not exist in the same file.
8.  Line break codes [`0x0D`, `0x0A`] are required at the end of the file.
