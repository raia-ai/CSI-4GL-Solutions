---
title: "KASTOlogic Storage Computer Link"
source: "Madcap_-_SM3_Help-Content-ExternalFiles-KastoDocs.pdf"
tags: ["KASTO", "KASTOlogic", "WMS", "Computer Link", "Telegram", "FTP", "TCP/IP", "Database Interface", "API", "Automation"]
version: 1.0
last_updated: 2025-12-04
short_description: "Technical specification for the KASTO Computer Link, detailing the interface between a KASTOlogic Warehouse Management System (WMS) and a host computer system. It covers various data transmission methods like file transfer (FTP, SMB), TCP/IP sockets, and direct database interaction. The document outlines the structure and purpose of different telegram types used for order processing, inventory management, and master data synchronization."
long_description: "This document provides a comprehensive technical specification for the KASTO Computer Link, Version 2.20.1. It serves as a guide for integrating a KASTOlogic Storage Computer and Warehouse Management System (WMS) with an external host (customer's) data processing system. The specification details multiple methods for data transmission, including file-based transfers via FTP (active and passive modes) and SMB shared folders, real-time communication using TCP/IP sockets with a 'STOP AND GO' acknowledgement mechanism, and a database interface using Oracle tables. The document meticulously defines the structure of various 'telegrams'—data packets used for specific functions. These include order entry (HLAU), order acknowledgements (LHAU), inventory inquiries (HLBM), master data maintenance (HLST), and machine status updates (HLMS). For each telegram, the guide provides a field-by-field breakdown, specifying data type, length, and purpose, ensuring seamless and error-free communication between the KASTO system and the host."
---
# KASTO – Computer Link for the Storage Computer
## Warehouse Management System (WMS)"
> **Note: ** Yellow text has to be translated or are new feature since later version
**Data Flow: **
HOST (WMS) <--> KASTOlogic KASTO Storage Computer (Transfer of data)
| | |
|: --- | :--- | :--- | :--- | :--- |
| 1 | Telegram-Type | 4 | alpha | `LHST` |
| 2 | Sequence no. | 6 | num | |
| **Project: ** | KASTO – Standard |
| **Telegram exchange: ** | KASTO <-> HOST |
| **Type of link: ** | DB, SMB share, FTP, Socket |
| **Physical link: ** | ETHERNET |
| **Protocol: ** | TCP/IP |
**Project Modifications**
| Date | Last project modifications | Writer |
The computer link is the connection between the LVR and the production control system respectively the material scheduling level of the customer's data processing system. It enables data exchange for the following tasks: - Order processing
- Inventory management
- Master data management
The data transfer (per data transfer / per TCP-socket) is determined project-specifically depending on customer request.
### 1.2 Mode of link
- **Physical link: ** ETHERNET-network
- **Hardware: ** RJ-45- jack (10 Base T, UTP)
- **Transmission: ** by TCP/IP - protocol
- **Transmission protection: ** by protocol
- On user side there is no further installations necessary.
### 1.3 Telegrams
| Category | Description |
| **Field types** | **Alphanumerical fields: **<br>Enter values or text left justified, unoccupied digits have to be filled with blanks.<br><br>**Numerical fields:**<br>Enter values right justified, zeroize to the left (leading zeros). Length in meter, weight in kg. |
| **Examples for field values** | **Type: ** NUM, **Length:** 5, **Value:** 800, **Field:** `00800`<br>**Type:** NUM, **Length:** 12.4, **Value:** 6.5 m, **Field:** `000000065000`<br>**Type:** NUM, **Length:** 12.4, **Value:** 24.5 kg, **Field:** `000000245000`<br>**Type:** NUM, **Length:** 12.4, **Value:** 18 pcs, **Field:** `000000180000` |
| **Length** | Details to length of telegrams and end-sign depend on operating system. Date-transmission principle and operating system, see following chapter. |
The field length can be configured for only following fields: 
- **order number**: 10 to 24 characters (see for example AU or BK telegrams)
- **order position**: 10 to 24 characters (see for example AU or BK telegrams)
- **order info data**: 1 to 2000 characters (best for database), or more
- **stock quality**: 1 to 24 characters, standard 16 characters
- **info data**: 1 to 2000 characters (best for database), or more for compartments, article, or charge data
## 2. Different methods of transmitting data
### 2.1 Transfer of data via files-transfer
Messages/telegrams from HOST to KASTOlogic or reverse are defined in a specified format (ASCII-Format). Before transmitting all of them are combined in a text-file.
One line-item is one message/telegram. This line-item must be ended with the Operating system defined line-end sign (CR/LF, ASCII 13/10).
One file can include more than one line-item (messages/telegrams).
The sequence of processing is line-item by line-item.
Line-Item starting with “#” will not be read.
#### 2.1.1 Conversion of file-naming
| Filename | Direction & Purpose |
| **Notes** | - The file name may only consist of letters or numbers since no special characters are accepted by the LVR to designate a file.<br>- The total length of the file name must not exceed 16 characters.<br>- **Important: ** Suffix 'rcv'. The LVR, when receiving data, only accepts this type of files as transfer files. |
| **Alternatives** | - See process chart REKO TCP/IP.<br>- Other transmission alternatives subject to agreement. |
#### 2.1.2 File transfer via shared folders (SMB)
A folder to receive KASTO-data is shared on the Host computer. A folder to receive HOST data is shared on the KASTOlogic. The data transfer runs similarly to the FTP-transfer (including file renaming).
#### 2.1.3 Process Chart REKO-TCP/IP via active FTP
**HOST to LVR**
1.  **HOST: ** Creates acknowledgement file `dhxxxx.ftp` (with telegram type `HLQU`) and transmits it.
2.  **LVR: ** Saves `dhxxxx.ftp` in `d:\host\tcprcv`.
3.  **HOST: ** Renames `dhxxxx.ftp` to `dhxxxx.rcv` using FTP command "rename".
4.  **LVR: ** Reads and then erases `dhxxxx.rcv`.
### 2.2 Data transmission per TCP/IP socket
#### 2.2.1 Telegram format
1.  **LVR: ** After processing, creates file `dlyyyy.ksd` (e.g., with telegram type `LHAU`) in `d:\host\tcpsnd`.
2.  **HOST: ** Checks in cycles (e.g., 1/min) if `dlyyyy.ksd` is available, then fetches it from `d:\host\tcpsnd`.
3.  **LVR: ** Renames `dlyyyy.ftp` to `dlyyyy.ksd` using FTP command "rename".
4.  **HOST: ** Erases `dlyyyy.ksd` from `d:\host\tcpsnd` using FTP command "delete".
**LVR to HOST (Data Processing)**
Each telegram consists of: 
- **Telegram head: ** (consisting of telegram type and sequence number)
- **Data fields**
- **Mark for telegram end: ** `<Carriage Return>`
The length and number of data fields depend on the telegram type. The end of each telegram is signaled with a `<Carriage Return>`. Due to the variable number of data fields, the transmitted telegrams are also of a variable length.
#### 2.2.2 Link
Two separate TCP links are used, one link for each direction. The TCP/IP addresses and the port numbers are determined after consultation with the customer.
- **Default: **
- HOST = 20000
- KASTO = 20001
**2.2.2.1 Receiver**
The receiver of the telegrams is the **TCP server**. This receiver receives the data telegrams via the port assigned to it and transmits acknowledgement telegrams for the received data telegrams via the same link.
**2.2.2.2 Sender**
The sender of data telegrams is the **TCP client**. This client sends data telegrams via its sending port and receives the acknowledgement telegrams via the same link. The sender opens the link.
#### 2.2.3 Data transmission
Each data telegram must be acknowledged. A positive acknowledgement is given if the data on the received system have a correct format and have been saved. The report for both directions of the data exchange is the same. The sending system may only send the next data telegram after it has received an acknowledgement (**STOP AND GO mechanism**). The inspection and processing of the contents are carried out at a later time. All received and sent telegrams are recorded.
#### 2.2.4 Transmission security
In order to realize telegram repetitions or losses, a sequence number will be assigned to the telegram head. An acknowledgement always has the same sequence number as the data telegram to be acknowledged.
- **Sequence number: ** '000001' - '999999'. If '999999' is reached, the next sequence number will be '000001'. Sequence numbers are always assigned continuously.
- The sequence number **'000000'** is used for adjusting the sequence numbers of sender and receiver. The sequence number '000000' in a data telegram is always accepted by the receiver. The next expected sequence number is '000001'.
**2.2.4.1 Sender**
- The sender sets up the link to the receiver. If the 'Connect' is successful, transmission starts.
- If no acknowledgement is received in time, the data telegram is repeated. After a given number of repetitions, the sender closes the link and tries again.
- The next data telegram is only sent after an acknowledgement is received. The sequence number increments with each acknowledged telegram.
- If acknowledged with a sequence number error, the sender repeats the telegram with sequence number '000000'.
- If acknowledged with a telegram error (form error code = 1), the process is recorded, and it continues with the next data telegram.
- Unexpected acknowledgements are rejected.
**2.2.4.2 Receiver**
- The receiver waits for a link set-up from the sender.
- If a link exists and another is set up, the existing link is closed, and the process continues with the new one.
- A received telegram is acknowledged positively if it is a known type with the expected sequence number.
- If the telegram type is unknown, it's acknowledged with a telegram error (code = 1).
- If the sequence number is not expected, it's acknowledged with a sequence error. The sequence number '000000' is always accepted.
- A repeated telegram (same sequence number as the previously acknowledged one) is acknowledged positively but not processed.
#### 2.2.4.3 Sequence diagrams
**2.2.4.3.1 Data telegram received without errors**
1.  **HOST -> KASTOlogic: ** `Data (SEQ: 000006)`
2.  **KASTOlogic -> HOST: ** `QU (FE: 1, SEQ: 000006)` (Data telegram received with errors, process recorded)
3.  **HOST -> KASTOlogic: ** `Data (SEQ: 000007)` (Continue with next data telegram)
4.  **KASTOlogic -> HOST: ** `QU (FE: 0, SEQ: 000007)` (No error)
### 2.3 Data base interface
#### 2.3.1 Data base user
The tables are created in the database under "rekohost". The user "rekohost" is only used by the Host system.
| Table | User | Rights |
5.  **HOST -> KASTOlogic: ** `Data (SEQ: 000000)` (Compensation sequence no.)
6.  **KASTOlogic -> HOST: ** `QU (FE: 0, SEQ: 000000)` (Repetition accepted)
**2.2.4.3.4 Data telegram received with errors**
**Table: T_KASTO_SND**
| Column | Data Type | Description |
- **KASTOlogic with inventory administration: ** Organizes master data (articles) and their inventory. Appointments (WE / WA) state the article and nominal amount.
- **KASTOlogic with cassette number administration: ** Does not organize inventory, only cassettes and their locations. Appointments are transport orders (bring cassette to station and back).
Some telegrams (or individual fields) are only used as project-specific options.
**Optional Modules: **
| Option | Project-specific use | Name |
**Telegram-Type: LHST (LVR → HOST)**
| Field N° | Description | Length | Type | Comment |
| 4b | Host-Ref-No. | 20 | alpha | no | Option: Content of field "Host-Ref-No" from telegram HOST → LVR |
| 5 | Tele-form-fault-code | 2 | num | yes | `0`: no fault<br>`1`: telegram received with fault<br>`2`: sequence nº fault, next sequence nº see field 6 (With socket only)<br>`3`: telegram can not be used |
| 6 | Next sequence nº | 6 | num | no | With socket only: HOST expects this nº as next sequence nº from LVR. (Required if fault-code == 2) |
| | **Total length: ** | | | |
| | EOS | | | End-Of-String / end mark |
### 3.10 HLSA Master data inquiry
| | EOS | | | | End-Of-String: `\n` or LF (file) |
### 3.11 HLST Master Data maintenance
| 6 | Next sequence no | 6 | num | no | With socket only: LVR expects this nº as next sequence nº from HOST. (Required if fault-code == 2) |
| | **Total length** | | | | |
| 3 | Function | 2 | num | yes | | `1`: Add and change master data. Data is integrated/overwritten in LVR database.<br>`2`: Erase master data. Master data of the article will be erased. |
| 3b | Host ref no. | (20) | alpha | | | Host-Reference No. (optional field) |
| 4 | Article | 24 | alpha | yes | | |
| 5 | Description | 64 | alpha | yes | | Article description |
| 6 | Date of first entry | 8 | num | no | actual | YYYYMMDD |
| 7 | Change Date | 8 | num | no | actual | YYYYMMDD |
| 4 | Order-Type | 2 | num | yes | | `1`: Commissioning (cass.system)<br>`10`: Input order<br>`11`: Store Cassette (cass.system)<br>`12`: Bring Cassette (cass.system)<br>`13`: View cassettes (cass.system)<br>`15`: Removal (with KASTOcenter)<br>`18`: Shipping order<br>`20`: Production order (cut optimization)<br>`21`: Sawing (with KASTOcenter)<br>`22`: Sawing Manuel (with KASTOcenter) |
| 5 | Urgent order | 1 | num | no | 0 | `0`=no, `1`=yes |
| 6 | Station | 2 | num | no | 0 | `0`=Transfer pool, >0=Station |
| 7 | Order-No. | 10-24 | alpha/num | yes | | Unique for all orders. `Order-N°` and `Order position` must be unique. (KASTOcenter: Only type num) |
| 8 | Order-position | 10-24 | alpha/num | yes | | |
| 9 | Order-Pos.-Total | 5 | num | no | 0 | |
| 10 | Due date Sequence | 14 | num | no | Actual time | YYYYMMDDhhmmss e.g., 20001231085930 |
| 11 | Article | 24 | alpha | yes | | |
| 12 | Heat | 24 | alpha | no | | |
| 13 | Heat monitoring | 1 | num | yes | 0 | Binary value: `0`=None, `1`=Heat-trueness, `2`=Heat2-trueness, `4`=Heat3-trueness (for commissioning/production) |
| 14 | Heat2 | 24 | alpha | no | | Info field |
| 15 | Required amount | 12.4 | num | yes | | |
| 16 | Actual amount | 12.4 | num | no | 0.0 | |
| 17 | Required pieces | 10 | num | no | 0 | Cutting order: Number of required pieces |
| 18 | Actual pieces | 10 | num | no | 0 | Cutting order: Number of actual pieces |
| 19 | Cut piece (Cut-off length) | 12.4 | num | no | 0.0 | Cutting order: Cut-off length |
| 20 | Store length | 12.4 | num | no | 0.0 | Storage: Length from data base. Removal: `0` all allowed, >`0` storage length. |
| 21 | Info | 255 | alpha | no | | |
| 22 | Cassette type | 2 | num | no | 0 | Storage (for cass.system) |
| 23 | Field-type | 6 | alpha | no | | Storage (for cass.system) |
| 24 | Quantity of Cassettes | 2 | num | no | 1 | Storage: Number of cassettes (for cass.system) |
| 25 | Cassettes no. | 10 | num | no | 0 | Number of requested cassette (for cass.system) |
| 26 | Compartment no | 5 | num | no | 0 | Number of requested compartment (for cass.system) |
| 27 | Container area | 2 | alpha | no | | Cutting order (KASTOcenter): for cut-offs 'A' |
| 28 | Container no | 2 | num | no | 0 | Cutting order (KASTOcenter): for cut-offs '1' |
| 29 | Saw until out of material | 1 | num | no | 0 | Cutting order (KASTOcenter): `0`=no, `1`=yes |
| 30 | Marking | 1 | num | no | 0 | Cutting order (KASTOcenter, marker): `0`=no, `1`=yes |
| 31 | Marking selection | 1 | num | no | 0 | Cutting order (SSZ,marker): `0`: Only mark 1st good cut piece, `1`: Mark each good cut piece |
| 32 | Bar order | 1 | num | no | 0 | Storing/removal from/to (KASTOcenter): `0`: Cassette location, `1`: Bar location |
| 33 | Storage number (Manual) | 3 | num | no | 0 | `0`: Order entry in automatic storage system, >`0`: Order entry in manual storage system |
| 34 | Cut piece (Cut-off width) | 12.4 | num | no | 0.0 | If article type 'plate': Cutting order: Cut-off width |
| 35 | Store width | 12.4 | num | no | 0.0 | If article type 'plate': Storage width from DB. Removal: `0` all allowed, >`0` storage width. |
| 36 | Required amount pieces | 5 | num | no | 0 | Piece managed in compartments (Option: Cass-Systems) |
| 37 | Actual amount pieces | 5 | num | no | 0 | Piece managed in compartments (Option: Cass-Systems) |
| 38 | Heat3 | 24 | alpha | no | | Info field |
| 39 | Packing tare | 12.4 | num | no | 0.0 | Default when storing, always as weight value |
| 40 | Handling location | 2 | num | no | 0 | `00`: Automatic station, `01-49`: outside, `50`: manual removal (free), `51-69`: manual removal (fixed) |
| 41 | Shipping Pallet Type | 1 | num | no | 0 | `0`: without, `1`: small, `2`: medium, `3`: large (Option, auto commissioning) |
| 42 | Cardboard before first sheet | 1 | num | no | 0 | `0`: without, `1`: small, `2`: medium, `3`: large (Option, auto commissioning) |
| 43 | Cardboard after last sheet | 1 | num | no | 0 | `0`: without, `1`: small, `2`: medium, `3`: large (Option, auto commissioning) |
| 44 | Paper layer | 1 | num | no | 0 | Manually place paper layer (Option): `0`: No, `1`: Yes |
| 45 | Amount OS REQU. | 12.4 | num | no | 0.0 | Req. Amount for Order/Sales quantity |
| 46 | Amount_OS_ACTUAL | 12.4 | num | no | 0.0 | Actual Amount for Order/Sales quantity |
| 47 | Amount_OS_UoM | 3 | alpha | no | Empty string | Unit of Measure for Order/Sales quantity |
| 48 | Miter left | 4.1 | num/alpha | no | 0 or empty | Miter left, as angle 0.0-359.9° or chart index Axxx-Zxxx |
| 49 | Miter right | 4.1 | num/alpha | no | 0 or empty | Miter right, as angle 0.0-359.9° or chart index Axxx-Zxxx |
| 50 | Miter Shape | 4 | alpha | no | Empty | Miter shape for left and right |
| 51 | Rolling Direction | 1 | num | no | 0 | `0`: Item - Direction of rolling, `1`: Lengthwise, `2`: Across, `3`: Uniform, `9`: Turnable |
| 52 | Bar number | 9 | num | no | 0 | Actual bar number |
| 53 | Product | 24 | alpha | no | | |
| 54 | Quality | 16 | alpha | no | | |
| 55 | Systemnumber | 2 | num | no | 0 | |
| 56 | Store height | 12.4 | num | no | 0 | |
| 57 | Owner | 24 | alpha | no | | Or company name |
| 58 | Search criteria | 20 | alpha | no | | Search criteria for storage, separated by '|' for OR logic. E.g.: `D|M` |
| 59 | Bundle status | 1 | num | no | 0 | Input order: `0`=no bundle, `1`=closed, `2`=opened. Commissioning: `0`=not important, `1`=only closed, `2`=only opened, `9`=only bundle. |
| 60 | Bundle type | 4 | num | no | 0 | `0000`=no bundle or not important, `0001`=bundle type 1, ... |
| | EOS | | | | | End-Of-String: `\n` or LF (file) |
*Article unit is not overwritten when article master record is changed.*
### 3.12 LHST Master Data feedback
| 3 | Fault-Code | 2 | num | `0`: no fault<br>`51`: Function unknown<br>`52`: Record not found<br>`53`: Can't read record<br>`54`: Can't insert record<br>`55`: Can't change record<br>`56`: Can't erase record<br>`57`: used Data not allowed (i.e. unit, article-type) |
| 3b | Host ref no. | (20) | alpha | Host-Reference No.(optional field) |
| 4 | Article | 24 | alpha | |
| 5 | Description | 64 | alpha | |
| 6 | Date of first entry | 8 | num | |
| 7 | Change-date | 8 | num | |
| 8 | Material form | 2 | num | |
| 9 | Width | 12.4 | num | |
| 10 | Height | 12.4 | num | |
| 11 | Wall width | 12.4 | num | |
| 12 | I-beam width | 12.4 | num | |
| 13 | Standard length | 12.4 | num | |
| 14 | Weight per unit | 12.4 | num | |
| 15 | Weighingtolerance | 5 | num | |
| 16 | Minimum 1 | 12.4 | num | |
| 17 | Minimum 2 | 12.4 | num | |
| 18 | Amount unit | 3 | alpha | |
| 19 | Storage area | 2 | num | |
| 20 | Quality-Info | 16 | alpha | |
| 21 | PreferenceStation | 2 | num | |
| 22 | Date of reset | 8 | num | YYYYMMDD. Date when following fields have been set to zero. |
| 23 | Added Amount | 12.4 | num | Added quantity, since last 'Date of reset' |
| 24 | Removal Amount | 12.4 | num | Removal amount, since last 'Date of reset' |
| 25 | Access Counter | 10 | num | Accesses, since last 'Date of reset' |
| 26 | Article-Key | 24 | alpha | Second key for article (Option, KASTOcenter) |
| 27 | Heat management | 1 | num | |
| 28 | Separation Amount | 12.4 | num | Option |
| 11 | Heat-Control | 1 | num | with control of Heat: `0` = no, `1` = yes |
| 12 | Heat2 | 24 | alpha | Info field |
| 13 | Registration Quantity | 12.4 | num | Quantity of this registration(booking amount) |
| 14 | Required Quantity | 12.4 | num | Host-required amount |
| 15 | Actual Quantity | 12.4 | num | Cumulative actual amount in LVR |
| 16 | Required Pieces | 10 | num | Cutting order: Host-required pieces |
| 17 | Actual Pieces | 10 | num | Cumulative actual pieces in LVR |
| 18 | Cut-off length | 12.4 | num | Cutting order: Cut-off length |
| 19 | Store Length | 12.4 | num | Storage: Length from data base. Removal: `0` all allowed, >`0` storage length |
| 20 | Order End | 1 | num | `0` = no, `1` = yes |
| 21 | Position End | 1 | num | `0` = no, `1` = yes |
| 22 | Cassette nº | 10 | num | Requested cassette nº (with cass.system) |
| 23 | Compartment N° | 5 | num | Requested compartment nº (with cass.system) |
| 24 | Container Area | 2 | alpha | Cutting order (SSZ): for cut-offs |
| 25 | Container nº | 2 | num | Cutting order (SSZ): for cut-offs |
| 26 | Bar Order | 1 | num | In/out storage from/to (SSZ): `0`: Cassette location, `1`: Bar location |
| 27 | Info | 255 | alpha | |
| 28 | Total amount | 12.4 | num | Actual amount plus waste pieces |
| 29 | Order duration | 12.4 | num | Processing duration of cutting order (SSZ) in minutes (1/100) |
| 30 | Storage number (Manual) | 3 | num | Option: Storage number of manual storage system |
| 31 | Material inventory | 12.4 | num | Total material inventory of this article (with cass.system) |
| 32 | Material inventory(Heat) | 12.4 | num | Total material inventory of this article per heat (with cass.system) |
| 33 | Order from HOST | 1 | num | `0`: Order created manually, `1`: Order inserted from HOST |
| 34 | Cut-off width | 12.4 | num | If article type 'plate': Cutting order: Cut-off width |
| 35 | Store width | 12.4 | num | If article type 'plate': Storage width from data base. Removal: `0` all allowed, >`0` storage width |
| 36 | Bar length | 12.4 | num | Actual bar length, if feed back by every bar |
| 37 | Bar number | 9 | num | Actual bar number, if feed back by every bar |
| 38 | Bar state | 1 | num | If feed back by every bar (KASTO center): `0`: bar in process, `1`: bar will be restored, `2`: bar will be eliminated |
| 39 | Station | 2 | num | `0` = Transfer pool, >`0` = Station |
| 40 | Required amount pieces | 5 | num | Piece managed in compartments (Option: Cass-Systems) |
| 41 | Actual amount pieces | 5 | num | Piece managed in compartments (Option: Cass-Systems) |
| 42 | Heat3 | 24 | alpha | Info field |
| 43 | Packing tare | 12.4 | num | Added/removed packing tare. Always as weight value. (Option) |
| 44 | Handling location | 2 | num | `00`: Automatic station, `01-49`: outside, `50`: manual removal (free), `51-69`: manual removal (fixed) |
| 45 | Shipping pallet type | 1 | num | `0`: without, `1`: small, `2`: medium, `3`: large (Option, auto commissioning) |
| 46 | Cardboard before first sheet | 1 | num | `0`: without, `1`: small, `2`: medium, `3`: large (Option, auto commissioning) |
| 47 | Cardboard after last sheet | 1 | num | `0`: without, `1`: small, `2`: medium, `3`: large (Option, auto commissioning) |
| 48 | Paper layer | 1 | num | Manually place paper layer (Option): `0`: No, `1`: Yes |
| 49 | Booking_Piece | 10 | num | Booked amount of pieces (see fields 40,41) |
| 50 | Booking_OS | 12.4 | num | Booked Order/Sales quantity |
| 51 | Amount_OS_REQU. | 12.4 | num | Req. Amount for Order/Sales quantity |
| 52 | Amount_OS_ACTUAL | 12.4 | num | Actual Amount for Order/Sales quantity |
| 53 | Amount_OS_UOM | 3 | alpha | Unit of Measure for Order/Sales quantity |
| 54 | Amount_Bypass | 12.4 | num | Bypass Amount in booking unit |
| 55 | Sub-Compartment ID | 1 | num | Storing: depending on New Storing Amount. Commissioning: depending on Removal-Material Amount. `0`: None, `1`: Rest |
| 56 | Requ. Date | 14 | num | YYYYMMDDhhmmss e.g., 20001231085930 |
| 57 | User name | 20 | alpha | |
| 58 | Product | 24 | alpha | |
| 59 | Quality | 16 | alpha | |
| 60 | Systemnumber | 2 | num | |
| 61 | Store height | 12.4 | num | |
| 62 | Client | 24 | alpha | Or company name |
| 63 | Bundle status | 1 | num | `0`=no bundle, `1`=closed bundle, `2`=opened bundle |
| 64 | Bundle type | 4 | num | `0000`=no bundle, `0001`=bundle type 1, ... |
| | **Total Length: ** | | | |
| | EOS | | | End-Of-String: `\n` or LF (file) |
**Fault codes: **
- `51`: Function unknown
- `52`: Record not found
- `53`: Can't read record
- `54`: Can't insert record
- `55`: Can't change record
- `56`: Can't erase record
- `57`: Record already existing (Option)
- `61`: Article unknown
- `62`: Order type unknown
- `63`: Cassette nº missing
- `64`: Order returned (other)
- `65`: Order n
- `66`: Order-position
- `67`: Article not suited for cutting
- `68`: Article / compartment blocked
- `69`: Unit for Order/Sales quantity not allowed
- `70`: Storing, Charge 1, 2 or 3 already exists in storage
- `71`: Storing, Charge 1, 2 or 3 already exists in an order
- `72`: commissioning, Charge 1, 2 or 3 not present in storage
- `73`: Wrong cutting/production data
- `74`: Wrong Search criteria
- `75`: Client is missing or unknown
### 3.5 LHBK Inventory correction messages
| 20 | Separation | 1 | num | Separation possibility (option): `0`: No, `1`: Yes, with suction type 1, `2`: Yes, with suction type 2, `3`: Yes, with suction type 3 |
| 21 | Paper layer | 1 | num | Paper layer in sub-compartment (option): `0`: No, `1`: Yes (can be blown out), `2`: Yes (can only be removed manually) |
| 22 | Storage height | 12.4 | num | Item height or thickness |
| 23 | Sub-Compartment ID | 1 | num | `0`: None, `1`: Rest |
| 24 | Order from Host | 1 | num | `0`: not from Host system, `1`: Order from Host system (fields 25+26 are filled) |
| 25 | Order No. | 10 | alpha | Order number |
| 26 | Order Pos. | 10 | alpha | Order position |
| 27 | Package support | 1 | num | Package support in sub-compartment (option): `0`: No, `1`: Yes with protective cover sheet, `2`: Yes with pick-up pallet |
| 28 | Quality | 16 | alpha | |
| 29 | User name | 20 | alpha | |
| 30 | Systemnumber | 2 | num | |
| 31 | Client | 24 | alpha | Or company name |
| 32 | Bundle status | 1 | num | `0`=no bundle, `1`=closed bundle, `2`=opened bundle |
| 33 | Bundle type | 4 | num | `0000`=no bundle, `0001`=bundle type 1, ... |
| 34 | Layout-Id | 10 | Num | Layout-Identnumber |
| | **Total length** | | | |
LVR answers to HLBM with: `LHBM`.
| Field No. | Description | Length | Type | Reqd Field | Default | Comment |
| 7 | Sub-compartment ID | 2 | num | no | 00 | `00`: all (obliging for functions 4, 9 and 10)<br>`01`: only rest<br>`02`: only special rest<br>`10`: select no rest<br>`11`: select all rest |
| 8 | Systemnumber | 2 | num | yes | 00 | `00`: all systems |
| 9 | Client | 24 | alpha | no | | Or company name |
| 10 | Heat1 | 24 | alpha | no | | |
| 11 | Heat2 | 24 | alpha | no | | |
| 12 | Heat3 | 24 | alpha | no | | |
| 13 | Quality | 16 | alpha | no | | |
| 17 | End of material list recognition | 1 | num | `0`: Further return messages will follow to HLBM<br>`1`: Last return message to HLBM |
| 18 | Storage number | 3 | num | With function 7, 8, 9, 10 only |
| 19 | Storage row | 3 | num | With function 7, 8, 9, 10 only |
| 20 | Storage height | 3 | num | With function 7, 8, 9, 10 only |
| 21 | Sequence in shelf | 5 | num | KASTOcenter: Sequence of bars in storage shelf |
| 22 | Stored width | 12.4 | num | If article type 'sheet' or 'plate': With function 7 or 8 only |
| 23 | Bar number | 9 | num | Actual bar number if feed back by every bar (KASTOcenter) |
| 24 | Bar state | 1 | num | If feed back by every bar: `0`: next bar (without trim cut), `1`: bar (with trim cut) |
| 25 | Compartment State | 1 | num | With function 7 or 8 only (see HLBM): `0`: available, `1`: blocked, `2`: defect |
| 26 | Heat3 | 24 | alpha | Info field, With function 7, 8, 9, 10 only |
| 27 | Fieldname | 6 | alpha | Fieldname, with function 7 or 8 only (see HLBM) |
| 28 | Field-type | 6 | alpha | Fieldtype, with function 7 or 8 only (see HLBM) |
| 29 | Field-State | 1 | num | Occupation-Status: `0`: empty, `1`: occupied, `2`: full (no storing) |
| 30 | 0-Date | 8 | num | Zero-cross-date, YYYYMMDD, with function 7 or 8 only |
| 31 | Separation | 1 | num | Separation possibility (Option, auto commissioning): `0`:No, `1`:suction type 1, `2`:suction type 2, `3`:suction type 3 |
| 32 | Paper layer | 1 | num | Paper layer in sub-compartment (Option, auto commissioning): `0`:No, `1`:Yes (can be blown out), `2`:Yes (manual removal) |
| 33 | Sub-compartment ID | 1 | num | `0`: None, `1`: Rest |
| 34 | Package support | 1 | num | Package support in sub-compartment (O_Sheetcom): `0`:No, `1`:Yes with protective cover sheet, `2`:Yes with pick-up pallet |
| 35 | Quality | 16 | alpha | With function 7 or 8 only |
| 36 | Amount of pieces | 10 | num | Only with piece management (Option) |
| 37 | Stored height | 12.4 | num | |
| 38 | Systemnumber | 2 | num | |
| 39 | Client | 24 | alpha | Or company name |
| 40 | Bundle status | 1 | num | `0`=no bundle, `1`=closed bundle, `2`=opened bundle |
| 41 | Bundle type | 4 | num | `0000`=no bundle, `0001`=bundle type 1, ... |
| 42 | Reserved amount | 12.4 | Num | Reserved material (filled only if option O_Reserv delivered) |
| 43 | Reserved pieces | 10 | Num | (filled only if option O_Reserv delivered) |
| | **Total length** | | | |
**Telegram type: LHMS (LVR → HOST)**
| Field no. | Description | Length | Type | Comment / admissible values |
| 3 | Function | 2 | Num | `1`: Set Status (Response to 'Set')<br>`2`: Machine status (Response to 'Request')<br>`3`: Machine status modified (asynchronous) |
| 4 | Machine type | 3 | Alpha | Machine type: RBG' (Gantry crane), 'RFZ' (Gantry crane), 'UMS' (Rotary Station), 'UFW' (Under floor carrier), 'STA' (Station), 'SAE' (Saw) |
| 5 | Machine number | 3 | Num | Machine number (000 = all machines of selected machine type) |
| 6 | Status | 2 | Num | Machine Status: `00`: not to be modified, `01`: set to 'available', `02`: set to 'not available'. Status is set at KASTOvr level, not PLC level. |
| 7 | Permission for distribution | 2 | Num | Permission for distribution of pick orders: `00`: not to be changed, `01`: set to 'permitted for distribution', `02`: set to 'denied for distribution'. Used if destination is unknown (station=0). |
| 4 | Error-Code | 2 | Num | `00`: no error<br>`31`: Function unknown<br>`41`: Machine status not set<br>`42`: Permission for distribution not set<br>`51`: Request not possible |
| 5 | End characteristic | 1 | Num | Status request: `0`: Further feedbacks will follow, `1`: Last feedback concerning the request |
| 6 | Machine type | 3 | Alpha | Machine type: RBG', 'RFZ', 'UMS', 'UFW', 'STA', 'SAE' |
| 7 | Machine number | 3 | Num | Machine number (000 = all machines) |
| 8 | Status | 2 | Num | Machine status: `01`: available, `02`: not available |
| 9 | Permission for distribution | 2 | Num | Permission for distribution of pick orders: `01`: permitted for distribution, `02`: denied for distribution |
LVR answers to HLSA with: `LHST`.
| Field No | Description | Length | Type | Reqd Field | Comment |
| 3 | Function | 2 | num | yes | `1`: All articles: Master Data of all articles will be returned.<br>`2`: One article: Master Data of article 'Article-1' will be returned.<br>`3`: Area: Master Data of all articles from 'Article-1' to 'Article-2' will be returned.<br>`4`: Article matching: select Master Data of article matching 'Article-1' will be returned. |
| 3b | Host ref no. | (20) | alpha | no | Host-Reference No. (optional field) |
| 4 | Article 1 | 24 | alpha | no | |
| 5 | Article 2 | 24 | alpha | no | |
| | **Total Length** | | | | |
On fault, LVR answers to HLST with: `LHST`.
| Field No. | Description | Length | Type | Reqd Field | Default | Comment |
| 8 | Material Form | 2 | num | yes | | `1`: Round-Solid, `2`:Rectangle–Solid, `3`:Round-Tube, `4`:Rectangle-Tube, etc. |
| 9 | Width | 12.4 | num | yes | | |
| 10 | Height | 12.4 | num | yes | | |
| 11 | Web width | 12.4 | num | no | 0.0 | |
| 12 | I-beam width | 12.4 | num | no | 0.0 | |
| 13 | Standard Length | 12.4 | num | yes | 65000 | Example: System with standard length of 6.5 m |
| 14 | Weight per unit | 12.4 | num | no | 0.0 | weight per unit |
| 15 | Weighing Tolerance | 5 | num | no | 0 | |
| 16 | Minimum 1 | 12.4 | num | no | 0.0 | for display in dialogue |
| 17 | Minimum 2 | 12.4 | num | no | 0.0 | for display in dialogue |
| 18 | Amount Unit | 3 | alpha | yes | | Example: KG, PC |
| 19 | Storage Area | 2 | num | no | 0 | |
| 20 | Quality-Info | 16 | alpha | no | | KASTOtec: 0' wrought, '1' peeled |
| 21 | Preference Station | 2 | num | no | 0 | For storing in |
| 22 | Article-Key | 24 | alpha | no | | Second key for article (Option, KASTOcenter) |
| 23 | Heat management | 1 | num | no | 0 | Binary values: `0`:no heat mgmt, `1`:heat mgmt 1, `2`:heat mgmt 2, `4`:heat mgmt 3 |
| 24 | Separation Amount | 12.4 | num | no | 0.0 | Option: Quantity from which order from manual storage needs processing. |
| 25 | Cassette-field type | 6 | alpha | no | | Cassette field type for this material. |
| 26 | Carbide | 1 | num | no | 0 | KASTOcenter: `0`:Not Suited for Carbide, `1`:Suited for Carbide |
| 27 | Article-Type | 10 | alpha | no | | Article-type, e.g., `BARS`, `PLATES` |
| 28 | Alloy | 10 | alpha | no | | Alloy |
| 29 | Separation | 1 | num | no | 0 | `0`: No, `1`:suction type 1, `2`:suction type 2, `3`:suction type 3 |
| 30 | Suction Pressure Reduction | 1 | num | no | 0 | `0`: No, `1`:Yes |
| 31 | Fanning | 1 | num | no | 0 | `0`: No, `1`:fanning magnet, `2`:spreader airblast, `3`:both |
| 32 | Paper layer | 1 | num | no | 0 | `0`: No, `1`:Yes (can be blown out), `2`:Yes (manual removal) |
| 33 | Sheet Format | 1 | num | no | 0 | O_Sheetcom: `1`:small, `2`:medium, `3`:large |
| 34 | Rolling Direction | 1 | num | no | 0 | `0`: Default, `1`:Lengthwise, `2`:Across, `9`:Turnable |
| 35 | Minimum remnant length | 12.4 | num | no | INI-Default | Smallest remnant length (for manufacturing orders) |
| 36 | Minimum remnant width | 12.4 | num | no | INI-Default | Smallest remnant width (for manufacturing orders) |
| 37 | Info data | 255 | alpha | no | | Project-specific info data. Field length can be adjusted. |
| 38 | Package support | 1 | num | no | 0 | O_Sheetcom: `0`:No, `1`:protective cover sheet, `2`:pick-up pallet |
| 39 | System number | 2 | num | no | 1 | Primary system |
| 40 | Storage number | 3 | num | no | 0 | Base location |
| 41 | Storage row | 3 | num | no | 0 | |
| 42 | Storage height | 3 | num | no | 0 | |
| 43 | Material | 48 | alpha | no | | Material name |
| 44 | Inventory amount | 12.4 | num | no | 0 | In article base unit of measure |
| 45 | Article area | 12.4 | num | no | 0 | Article area in m² |
| 46 | Maximum1 | 12.4 | num | no | 0 | In article base unit of measure |
| 47 | Maximum2 | 12.4 | num | no | 0 | In article base unit of measure |
| 48 | End of life | 8 | num | no | 0 | End of article life (YYYYMMDD) |
| 49 | Pickstation | 2 | num | no | 0 | Preference station for storing out |
| 50 | Article class 1 | 1 | alpha | no | | Article class A, B or C (empty=not defined) |
| 51 | Article class 2 | 1 | alpha | no | | Article class A, B or C (empty=not defined) |
| 52 | Replenishment min | 12.4 | num | no | 0 | Target location replenishment minimum quantity |
| 53 | Replenishment max | 12.4 | num | no | 0 | Target location replenishment maximum quantity |
| 54 | Replenishment amount | 12.4 | num | no | 0 | Target location replenishment default needed amount |
| 55 | Symmetry | 1 | num | no | 0 | `1`=symmetry, `2`=no symmetry |
| | **TotalLength: ** | | | | | |
| 29 | End of material recognition | 1 | num | Option: `0`: More return messages to HLSA follow, `1`: Last return message to HLSA |
| 30 | Cassette field-type | 6 | alpha | Cassette field type allocated to this material. |
| 31 | Carbide | 1 | num | KASTOcenter: `0`: Not suited for Carbide, `1`: Suited for Carbide |
| 32 | Article-type | 10 | alpha | e.g., `BARS`, `PLATES` |
| 33 | Alloy | 10 | alpha | Alloy |
| 34 | Separation | 1 | num | `0`: No, `1`:suction type 1, `2`:suction type 2, `3`:suction type 3 |
| 35 | Suction Pressure Reduction | 1 | num | `0`: No, `1`:Yes |
| 36 | Fanning | 1 | num | `0`: No, `1`:fanning magnet, `2`:spreader airblast, `3`:both |
| 37 | Paper layer | 1 | num | `0`: No, `1`:Yes (can be blown out), `2`:Yes (manual removal) |
| 38 | Sheet Format | 1 | num | `1`: small, `2`:medium, `3`:large |
| 39 | Rolling Direction | 1 | num | `1`: Lengthwise, `2`:Across, `9`:Turnable |
| 40 | Minimum remnant length | 12.4 | num | Smallest remnant length |
| 41 | Minimum remnant width | 12.4 | num | Smallest remnant width |
| 42 | Info data | 255 | alpha | Project specific info data. Field length can be adjusted. |
| 43 | Package support | 1 | num | O_Sheetcom: `0`:No, `1`:protective cover sheet, `2`:pick-up pallet |
| 44 | System number | 2 | num | Primary system |
| 45 | Storage number | 3 | num | Base location |
| 46 | Storage row | 3 | num | |
| 47 | Storage height | 3 | num | |
| 48 | Material | 48 | alpha | Material name |
| 49 | Inventory amount | 12.4 | num | |
| 50 | Area | 12.4 | num | Article area in m² |
| 51 | Maximum1 | 12.4 | num | (in article unit of measure) |
| 52 | Maximum2 | 12.4 | num | (in article unit of measure) |
| 53 | End of life | 8 | num | End of article life (YYYYMMDD) |
| 54 | Pickstation | 2 | num | Preference station for storing out |
| 55 | Article class 1 | 1 | alpha | Article class A, B or C (empty=not defined) |
| 56 | Article class 2 | 1 | alpha | Article class A, B or C (empty=not defined) |
| 57 | Replenishment min | 12.4 | num | Target location replenishment minimum quantity |
| 58 | Replenishment max | 12.4 | num | Target location replenishment maximum quantity |
| 59 | Replenishment amount | 12.4 | num | Target location replenishment default needed amount |
| | **Total length** | | | |
---

# KASTOlogic Storage Computer Link
