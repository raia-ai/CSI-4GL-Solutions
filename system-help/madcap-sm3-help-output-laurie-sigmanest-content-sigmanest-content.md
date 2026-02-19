---
title: "Madcap_-_SM3_Help-Output-Laurie-SigmaNEST_content-SigmaNEST_content"
source: "Madcap_-_SM3_Help-Output-Laurie-SigmaNEST_content-SigmaNEST_content.docx"
tags: ["help", "documentation", "SigmaNEST", "MadCap Flare", "manufacturing", "CNC", "software", "user-guide"]
version: "1.0"
last_updated: "2025-12-03"
short_description: "Table of Contents Plate Nesting with SigmaNEST An order line requires the following to be exported to SigmaNEST: A primary machine that has Plate Nest Integration enabled1. The product must be a product line with Plate Nest Integration enabled1. The order line must have a Customer Part Number. Once the order has been processed and is in PCK or PBP status, the line will be available in PR44B. When the order is processed, a directory for the customer will be created in the CAD File Directory2 (if not already created), and a subdirectory for the order will be created. This"
long_description: "Table of Contents Plate Nesting with SigmaNEST An order line requires the following to be exported to SigmaNEST: A primary machine that has Plate Nest Integration enabled1. The product must be a product line with Plate Nest Integration enabled1. The order line must have a Customer Part Number. Once the order has been processed and is in PCK or PBP status, the line will be available in PR44B. When the order is processed, a directory for the customer will be created in the CAD File Directory2 (if not already created), and a subdirectory for the order will be created. This sales order directory will contain a Sales directory and a Production directory. The customer directory is also created when a CAD file is attached to a line in PR44B or when a sales order is approved from credit approval or quality control. The work order and parts are now ready to be uploaded to SigmaNEST. In SigmaNEST, the order lines are nested and the remnant created. When the job is posted, the IP document is created in 4GL where it can be processed and tracked. When the IP document is processed, any sales order lines reserved against the IP are released from PBP status. If the log used on the nest is the same as the log that was originally allocated to the order, SM3 will deallocate the log from the sales order and allocate it to the IP; the finished goods of the IP will be allocated to the sales order. A SigmaNEST program may contain a work order that is not in 4GL, e.g. for a test piece cut from the plate. In the generated IP document, the test piece does not appear as a finished good, but its weight is allocated to the finished goods for the 4GL order(s). Whenever a full plate is moved in or out of inventory without being processed, it will be automatically updated in SigmaNEST stock (provided the plate is a product line with Plate Nest Integration enabled). Exporting Orders to SigmaNEST Choose In-House Production » Nesting » Export Work Orders to SigmaNest [PR44B]. This window displays all work orders that are ready to be exported to SigmaNEST; these are indicated by in the Exp field. If your line does not show up in the list, check to ensure that it has a primary process that has plate nesting enabled, the part number field is populated, the product line has plate nesting enabled, and the line is in either PCK or PBP status. Use the fields at the top to filter the list as required. If you choose to Show Exported, you will see the exported work orders indicated by . To view details about an order, select it and click Inquire to view the Sales Order Inquiry window. To attach a part file (.dxf or .dwg file) to an order, select the order and click Attach CAD and retrieve the file. Alternatively, if the files are stored in the designated folder3,"
---
Table of Contents

Plate Nesting with SigmaNEST

An order line requires the following to be exported to SigmaNEST:

- A primary machine that has Plate Nest Integration enabled1.
- The product must be a product line with Plate Nest Integration enabled1.
- The order line must have a Customer Part Number.

Once the order has been processed and is in PCK or PBP status, the line will be available in PR44B. When the order is processed, a directory for the customer will be created in the CAD File Directory2 (if not already created), and a subdirectory for the order will be created. This sales order directory will contain a Sales directory and a Production directory. The customer directory is also created when a CAD file is attached to a line in PR44B or when a sales order is approved from credit approval or quality control.

The work order and parts are now ready to be uploaded to SigmaNEST.

In SigmaNEST, the order lines are nested and the remnant created. When the job is posted, the IP document is created in 4GL where it can be processed and tracked. When the IP document is processed, any sales order lines reserved against the IP are released from PBP status. If the log used on the nest is the same as the log that was originally allocated to the order, SM3 will deallocate the log from the sales order and allocate it to the IP; the finished goods of the IP will be allocated to the sales order.

A SigmaNEST program may contain a work order that is not in 4GL, e.g. for a test piece cut from the plate. In the generated IP document, the test piece does not appear as a finished good, but its weight is allocated to the finished goods for the 4GL order(s).

Whenever a full plate is moved in or out of inventory without being processed, it will be automatically updated in SigmaNEST stock (provided the plate is a product line with Plate Nest Integration enabled).

Exporting Orders to SigmaNEST

- Choose In-House Production » Nesting » Export Work Orders to SigmaNest [PR44B].
- This window displays all work orders that are ready to be exported to SigmaNEST; these are indicated by  in the Exp field. If your line does not show up in the list, check to ensure that it has a primary process that has plate nesting enabled, the part number field is populated, the product line has plate nesting enabled, and the line is in either PCK or PBP status.
Use the fields at the top to filter the list as required. If you choose to Show Exported, you will see the exported work orders indicated by .

To view details about an order, select it and click Inquire to view the Sales Order Inquiry window.

- To attach a part file (.dxf or .dwg file) to an order, select the order and click Attach CAD and retrieve the file.

Alternatively, if the files are stored in the designated folder3, click Auto-Attach CAD. SM3 will scan the Sales folder in the sales order folder for any .dxf or .dwg files named with the part number (partnumber.dxf or partnumber.dwg). If found, the drawing will be attached to the workorder line and will be copied to the Production folder.

- When you are ready to export, select the line(s) and click Export Lines.

If a file was attached to the order line, a SimTrans transaction will be generated that will create a new SigmaNEST part based on the customer part number and file (as the drawing). It will automatically be attached to the SigmaNEST work order. This is considered a SimTrans SN85 transaction.

In the above, if the part already exists in SigmaNEST it will be overwritten.

If a file was not attached to the order line, a SimTrans transaction will be generated that will look for an existing SigmaNEST part with a name that matches the customer part number. If it finds one, the part will be attached to the SigmaNEST work order. If it does not, the work order line will be created in SigmaNEST with no part attached. This is considered a SimTrans SN84 transaction.

The files transferred can be viewed in the SimTrans dashboard.

- Click Sync to check with the SigmaNEST database to confirm and refresh the icons in the Exp field.

Use PR57 to identify and export any logs that have not been exported to SigmaNEST. When exporting a log to SigmaNEST, the first three specifications on the log are stamped on the SigmaNEST stock item as SheetData2, SheetData3 and SheetData4.

Setting Up the Job in SigmaNEST

Refer to the SigmaNEST documentation.

- Set up your workspace: create a new workspace, create a new task, retrieve the work order lines to add to the workspace, select the sheet.
- Create the remnant: choose Nesting » Auto Nest, then choose Nesting NC » Crop Sheet (example: Min % Used = 100, select Create Remnant, Crop Type=Crop Step 1, Part Offset 0.5).

The  set in SigmaNEST must be mounted to allow users to view remnant images in 4GL. If the directory is invalid, remnants will NOT be saved when posting SigmaNEST programs.

- Post the job (Nesting NC » Post).

Tracking the Job in 4GL

Viewing the IP Document

When the job is posted in SigmaNEST, a corresponding IP document is created in 4GL for each layout. To view an IP document:

- Choose In-House Production » Production Document Controlled » IP Entry / Maintenance [PR34].
- Locate and open the new document.
- On the Header tab, select a Due Date.

you will see the SigmaNEST program number associated with the IP in the search list as well as on the Header tab.

- The Details tab displays the raw material sheet and the finished goods line items, including the remnant that will go back into inventory. Modify as required.

In the case of remnants, a corresponding dog leg record is created that can be viewed from Inventory Inquiry or from the IN1E Shape field.

When performing a log swap, SM3 will attempt to submit the transaction to SimTrans every five seconds; if the maximum defined attempts4 is reached, you will be prompted to resubmit or cancel the swap.

The SM3-Sigma Cron Activity Log [PR59] captures cron activity when validating work orders and programs pulled from SigmaNEST, and when an IP is generated. When viewing this log, you will see one or more entries for the program you posted; these may indicate that there are parts missing, or the IP was generated, or it was generated but with an allocation code, or it was generated but has non-WO parts.

If the nested area on a program does not equate to the total nested area from the work orders, the 4GL-Sigma cron will make a second attempt to confirm there are no missing work order parts. The IP will be generated after the second attempt regardless of whether the areas equate, under the assumption non-work order parts are part of the nest. In the IP document, the Special Instructions field on the Header tab will include a note indicating that the nest may contain non-work order parts.

Processing and Tracking the Job

Shop operators use the following wireless handheld functions to finish processing the job:

- Conf Production & SigmaNEST Program  [WF1L] is used to pick and validate the log used for the production job: scan the document, which brings up the plate assigned to the job. If the operator used a different plate, scan the different log (must be same material and dimensions). If they chose a different size plate, the remnant will be different and the job must go back to the CAD department to be renested on the new plate.
- Update SigmaNEST IP  [WF1M] is used to confirm and update the IP and the SigmaNEST job.

Once the job has been processed, the IP document will be updated and materials allocated to the order(s) that made up the IP.

Configuration

1 Product lines and machines (primary process) in sales orders must have plate nest integration enabled (in IN16 > Warehouse and SWTMNT respectively) in order to be included in PR44B.

2 SWTMNT > CAD File Directory

3 SWTMNT > Linux CAD File Directory

4 SWTMNT > SimTrans Transaction Check Max Attempts

Refer to SigmaNEST Integration for full installation and configuration instructions.

SigmaNEST Integration

This topic outlines the installation and configuration of SigmaNEST and SimTrans (a service that enables third-party software to interface with SigmaNEST) and their integration with SM3.

Refer to Plate Nesting with SigmaNEST for an overview of the integration workflow.

Installation Requirements

- The SigmaNEST License Manager must be installed on the server. Once installed, the License Manager can be accessed through localhost:5055 in a browser.
- Set up the SigmaNEST server as described here:
- SNData must be accessible on the network for SigmaNEST workstations to connect with the SigmaNEST server.
- Set up a SigmaNEST workstation as described here:
- Additional instructions for setting up SigmaNEST can be found here:
- Set up SimTrans on the SigmaNEST server as described here:

Configuration

SigmaNEST

System

Ensure the Units are set to the same type as SM3:

Ensure the Export Work Order Information to SimTrans flag is enabled:

Remnant Images

- In SigmaNEST Configuration, set the directory to save the images. If this directory is invalid, remnants will NOT be saved when posting SigmaNEST programs.

- In SM3, go to SWTMNT > Location of Product Shape Images, and set the value to the same path as the one used in the SigmaNEST remnant output path.
- For the browser version of SM3, the Remnant Directory set in SigmaNEST must be mounted to allow users to view the contents. You will need to set up the mount on the 4GL server. In this example, the directory will be called “remsaveoutput”:
  - As superuser, create the directory with the following command:
mkdir /mnt/remsaveoutput
  - Add an entry to /etc/fstab to set up the mount.
  - Mount the directory with the following command:
mount /mnt/remsaveoutput
  - In SM3, set the SWTMNT > Linux Shape Folder Location value to the mounted directory path (in our example, "/mnt/remsaveoutput/").

SimTrans

In Global Configuration, enable the option to add sheets with SN91A if they don’t exist yet:

Also enable the SN84 and SN85 options:

In District Configuration, enable the following Sheet Replace options for the districts:

SM3

MS38 - External DB Connections

A database connection for SimTrans must be added for each warehouse that needs to interface with SigmaNEST. Please note the following details:

- The ID must be SIMTRANS
- The Driver must be com.microsoft.sqlserver.jdbc.SQLServerDriver
- The Conn field (connection string) must be in the format
jdbc:sqlserver://[server_ip]\SIGMANEST;databaseName=[database]
(contents highlighted in green are specific to your environment).
- The Enable field must be set to ‘Y’ for 4GL to recognize the connection is active

A database connection for SNDB must be added for each warehouse that needs to interface with SigmaNEST. The same details as the SIMTRANS connection apply except the ID for this one must be SNDB.

PR11 - Machine Master

For each machine that will be used as a primary process to export automatically to SigmaNEST:

- SigmaNEST integration must be enabled to allow work order lines to export automatically to SigmaNEST. To enable this, in PR11 expand (F9) on the machine you wish to modify, then F4 on the Addt’l field to enable the Enable Plate Nest Integration switch (you can also access this switch via SWTMNT).
- The machine must reference a valid production process (PR18) in the Process field.
- The machine Description must match the SigmaNEST machine name:

IN16 - Product Line

SigmaNEST integration must be enabled for specific product lines by warehouse to allow work order lines with those product lines to automatically export to SigmaNEST. This also allows receipt lines with the specific product lines to automatically export inventory to SigmaNEST.

For each applicable product line, expand (F9) to access the Warehouse options, then select the desired warehouse and set Enable Plate Nest Integration to ‘Y’.

IN19 - Warehouse Maintenance

These switches can also be accessed via SWTMNT.

To specify the active SimTrans district for the warehouse, set the IN19 > Plate Nesting > SigmaNEST District ID switch value to the district number assigned in the SimTrans District Configuration:

A mounted directory is required for attaching CAD files to sales orders. This is only required if existing SigmaNEST parts are not going to be used. For this example, the directory will be parts:

- On the Linux server as superuser, create the directory with the following command:
mkdir /mnt/parts
- Add an entry to /etc/fstab to set up the mount.
- Mount the directory with the following command:
mount /mnt/parts
- In SM3, set IN19 > Plate Nesting > Linux CAD File Directory to the mounted directory.
- Set IN19 > Plate Nesting > CAD File Directory to the Windows directory used for the mount.

When performing a log swap, SM3 will attempt to submit the transaction to SimTrans every five seconds up to the maximum number of attempts defined in IN19 > Plate Nesting > SimTrans Transaction Check Max Attempts. If the maximum is reached, the user is prompted to resubmit or cancel the swap.

PR51 - Plate Nest Attribute Mapping

Attribute mappings link SM3 product lines with SigmaNEST materials. These are entered in .

In the example, CPL in 4GL is mapped to MS in SigmaNEST, and SPL in 4GL is mapped to SS in SigmaNEST.

SM3 will use the Grade if a mapping is defined for it in PR51. If no grade is defined, it will use the Material if a mapping is defined for it in PR51. If no material is defined, SM3 will default to the product line.

**Batch Run**

The batch run script for the SigmaNEST database polling should be set in the crontab to run every minute. It is located with the other SM3 login scripts in /usr/bin.

The batch job will log into SM3 as user SIG and query the SigmaNEST database for posted programs. For each posted program it finds, it will generate an In-house Production document.

The script's contents should be similar to the following:

CDATE_50=Y
export CDATE_50
DATE_SC_50=Y
export DATE_SC_50
JAVA_HOME=/usr/java/jre1.8.0_241
export JAVA_HOME
PROIV_HOME=/usr/dev83/virtual_machine
export PROIV_HOME
LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$JAVA_HOME/lib/amd64:$JAVA_HOME/lib/amd64/server:$JAVA_HOME/lib/amd64/client:$PROIV_HOME/lib:/usr/local/lib:$PROIV_HOME/lib/instant_client:$PROIV_HOME/lib/libcurl
export LD_LIBRARY_PATH
PATH=/usr/java/jre1.8.0_241/bin:$PROIV_HOME:/usr/vsifax/obin:/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin:/usr/X11R6/bin:/usr/vsifax/bin:/usr/vsifax/lbin:/root/bin
export PATH
PROPATH=/usr/dev83/virtual_machine/stm310
export PROPATH
PRODATA=/usr/dev83/virtual_machine/stm310/stmdata
export PRODATA
PRORUNTYPE=DEV
export PRORUNTYPE
PROTERM=DECVT100
export PROTERM
GUI=N
export GUI
export SSO_JARPATH=/usr/dev83/virtual_machine/stm310/sso
export ORACLE_HOME=/oracle/product/12.2.0/sm3
export ORACLE_SID=stmprod
export SQL_DBTYPE=ORACLE
export SQL_USERNAME=stm310user
export SQL_PASSWORD=stm310user
export SQL_DBNAME=stmprod
export SQL_CURSORS=AUTO
export PRODB_CHARSET=8
export LOCKED_ROWS_RETURNED=Y
export SQL_NOSIG=Y
export SQL_TRANSACTION_ERROR=Y
export NLS_LANG="AMERICAN_AMERICA.AL32UTF8"
cd $PRODATA
/usr/dev83/virtual_machine/pro SIG STM

If the cd $PRODATA line is not there, batch6.out may be found in $PROPATH instead $PRODATA.

The SIG batch run user must exist as an operator in MS32, and the company code must match the one used in the script:

For Developers, SIG must be a standard batch run user with STPOLL as the Logon and Default function links:

All activity for the batch run is logged in $PRODATA/batch6.out.

Troubleshooting

If batch6.out is not being updated, you may need to run the Reset SigmaNEST Cron [PR58]. This utility recreates the batchque.pro file with the required permissions, and archives the batch log file (batch6.out).

The following are some common messages you may encounter in batch6.out that will prevent the IP from being generated:

- Failed to acquire licence - 'Could not acquire licence of type 'PROIV Runtime' from licence group ''. Insufficient free licences available.'

This will completely stop the batch run from proceeding and will cause a build-up in the batch queue.
As root, you will need to first restart the PROIV license server, then recreate $PRODATA/batchque.pro.
If the problem persists, there may be an issue with the number of available licenses, or the PROIV installation.

- DIM NOT DEFINED, DROP SHAPE: ''
015 - SUBSCRIPT VALUE NOT WITHIN RANGE OF DIMENSION - $UOMS_CONVERSION_TYPE 0

This likely indicates the log that was used for the nesting could not be found in 4GL, or the shape is not a sheet type. This can also occur if SheetData1 for the sheet in SigmaNEST is not prefixed with the warehouse code, or is an invalid log number. The nest will have to be redone with an appropriate plate.

- IP generated with no set

This likely indicates either the machine that was used in SigmaNEST could not be found in 4GL based on the machine description, or the machine that was used did not have a valid Process set in PR18.

Plate Nest Attribute Mapping

In-House Production » Nesting » Plate Nest Attribute Mapping [PR51]

This screen allows you to specify a product line, thickness or specification (grade) from SM3 and assign it a value that will be recognized by SigmaNEST. These recognizable values come into effect when exporting inventory and work orders from SM3 to SigmaNEST. If these values are not specified, the 4GL will be used by default.

Product lines are mapped to materials. Grades are mapped to materials as well to cater for the scenario where SigmaNEST inventory is defined at the grade level.

Thicknesses and grades can be defined specifically for product lines, but this is not necessary. Defining thicknesses or grades for the Default line will work as well. Product line-specific attributes allow for cases where the standard thickness value for certain products does not properly represent the actual value. For example, product lines where gauges are used might have a thickness of 11 for 11GA, but the thickness is not 11”.

SM3 will use the Grade if a mapping is defined for it in PR51. If no grade is defined, it will use the Material if a mapping is defined for it in PR51. If no material is defined, SM3 will default to the product line.

You can add, modify and delete materials, thicknesses and gauges. Deleting materials will delete all thicknesses and gauges entered against that material.

You cannot enter duplicate values for the same material.

In the following example, CPL in 4GL is mapped to MS in SigmaNEST, and SPL in 4GL is mapped to SS in SigmaNEST:

Conf Production & SigmaNEST Program

This function is used to pick and validate the log used for the production job.

Scan the document, which brings up the plate assigned to the job. If the operator used a different plate, scan the different log (must be same material and dimensions). If they chose a different size plate, the remnant will be different and the job must go back to the CAD department to be renested on the new plate.

After this is completed, use Update SigmaNEST IP  to confirm and update the IP and the SigmaNEST job.

When performing a log swap, SM3 will attempt to submit the transaction to SimTrans every five seconds; if the maximum defined attempts1 is reached, you will be prompted to resubmit or cancel the swap.

Configuration

1 SWTMNT > SimTrans Transaction Check Max Attempts

Update SigmaNEST IP

This function is used to confirm and update the IP and the SigmaNEST job. It is used after the Conf Production & SigmaNEST Program function is used to pick and validate the log used for the production job.

Configuration

IN19 > Label Options > Function Label Usages - Set up a label usage for a shipping label (SL types) and select the "O" column to set a shipping label to print for finished goods reserved against an order. When the IP is confirmed, if there are finished good logs allocated to the order the user will be asked if they want to print shipping labels.
Optionally set up label usages for Parent logs and Drop logs; if these are not set, no label will print for them.
