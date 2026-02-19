---
title: "SigmaNEST Integration"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "SigmaNEST Integration"
long_description: "This topic provides detailed information about SigmaNEST Integration in the 4GL system."
---


SigmaNEST Integration
=====================

This topic outlines the installation and configuration of SigmaNEST and SimTrans (a service that enables third-party software to interface with SigmaNEST) and their integration with .

Refer to Plate Nesting with SigmaNEST for an overview of the integration workflow. Click here to view the SimTrans User Manual.

Installation Requirements
-------------------------

* The SigmaNEST License Manager must be installed on the server. Once installed, the License Manager can be accessed through localhost:5055 in a browser.
* Set up the SigmaNEST server as described here:  
  https://SigmaNEST.zendesk.com/hc/en-us/articles/360002094754-Install-a-SigmaNEST-server
* After installing SigmaNEST, you must install Microsoft SQL Server 2014 Service Pack 3 (assuming you are using SQL Server 2014) which can be found here:  
  https://www.microsoft.com/en-us/download/details.aspx?id=57474
* SNData must be accessible on the network for SigmaNEST workstations to connect with the SigmaNEST server.
* Set up a SigmaNEST workstation as described here:  
  https://SigmaNEST.zendesk.com/hc/en-us/articles/360002093073-Install-SigmaNEST-on-a-workstation
* Additional instructions for setting up SigmaNEST can be found here:  
  https://products.SigmaNEST.com/Knowledge%20Base/PDFs/SigmaNEST-installation-guide.pdf
* Set up SimTrans on the SigmaNEST server as described here:  
  https://www.SigmaNEST.com/wp-content/uploads/2017/10/SimTransManual.pdf

Configuration
-------------

SigmaNEST


System

Ensure the Units are set to the same type as :

![](../../Resources/Images/SigmaNEST_config1.png)

Ensure the Export Work Order Information to SimTrans flag is enabled:

![](../../Resources/Images/SigmaNEST_config2.png)

Remnant Images

1. In SigmaNEST Configuration, set the directory to save the images. If this directory is invalid, remnants will NOT be saved when posting SigmaNEST programs.

   ![](../../Resources/Images/IP_SigmaNEST_Config.png)
2. In , go to  > Shape Images, and set the value to the same path as the one used in the SigmaNEST remnant output path.
3. For the browser version of , the Remnant Directory set in SigmaNEST must be mounted to allow users to view the contents. You will need to set up the mount on the  server. In this example, the directory will be called “remsaveoutput”:

   1. As superuser, create the directory with the following command:  
      mkdir /mnt/remsaveoutput
   2. Add an entry to /etc/fstab to set up the mount.
   3. Mount the directory with the following command:  
      mount /mnt/remsaveoutput
   4. In , set the  > Shape Image to the mounted directory path (in our example, “/mnt/remsaveoutput/”).


SimTrans


In Global Configuration, enable the option to add sheets with SN91A if they don’t exist yet:

![](../../Resources/Images/SigmaNEST_config3.png)

Also enable the SN84 and SN85 options:

![](../../Resources/Images/SigmaNEST_config4.png)

In District Configuration, enable the following Sheet Replace options for the districts:

![](../../Resources/Images/SigmaNEST_config5.png)








MS38 - External DB Connections

A database connection for SimTrans must be added for each warehouse that needs to interface with SigmaNEST. Please note the following details:

* The ID must be SIMTRANS
* The Driver must be com.microsoft.sqlserver.jdbc.SQLServerDriver
* The Conn field (connection string) must be in the format   
  jdbc:sqlserver://[server\_ip]\SIGMANEST;databaseName=[database]  
  (contents highlighted in green are specific to your environment).
* The Enable field must be set to ‘Y’ for SM3 to recognize the connection is active

A database connection for SNDB must be added for each warehouse that needs to interface with SigmaNEST. The same details as the SIMTRANS connection apply except the ID for this one must be SNDB.

![](../../Resources/Images/MS38_externalDB.png)

PR11 - Machine Master

For each machine that will be used as a primary process to export automatically to SigmaNEST:

![](../../Resources/Images/PR11_plasma_expanded.png)

* SigmaNEST integration must be enabled to allow work order lines to export automatically to SigmaNEST. To enable this, in PR11 expand (F9) on the machine you wish to modify, then F4 on the Addt’l field to enable the Enable Plate Nest Integration switch (you can also access this switch via ).
* The machine must reference a valid production process (PR18) in the Process field.
* The machine Description must match the SigmaNEST machine name:

![](../../Resources/Images/SigmaNEST_config6.png)

IN16 - Product Line

SigmaNEST integration must be enabled for specific product lines by warehouse to allow work order lines with those product lines to automatically export to SigmaNEST. This also allows receipt lines with the specific product lines to automatically export inventory to SigmaNEST.

For each applicable product line, expand (F9) to access the Warehouse options, then select the desired warehouse and set Enable Plate Nest Integration to ‘Y’.

IN19 - Warehouse Maintenance

![](../../Resources/Images/IN19_Plate_Nesting_options.png)

These switches can also be accessed via .

To specify the active SimTrans district for the warehouse, set the IN19 > Plate Nesting > SigmaNEST District ID switch value to the district number assigned in the SimTrans District Configuration:

![](../../Resources/Images/SigmaNEST_config7.png)

A mounted directory is required for attaching CAD files to sales orders. This is only required if existing SigmaNEST parts are not going to be used. For this example, the directory will be parts:

1. On the Linux server as superuser, create the directory with the following command:  
   mkdir /mnt/parts
2. Add an entry to /etc/fstab to set up the mount.
3. Mount the directory with the following command:  
   mount /mnt/parts
4. In , set IN19 > Directories > Part Drawing > mounted and Windows directories.

When performing a log swap,  will attempt to submit the transaction to SimTrans every five seconds up to the maximum number of attempts defined in IN19 > Plate Nesting > SimTrans Transaction Check Max Attempts. If the maximum is reached, the user is prompted to resubmit or cancel the swap.

PR51 - Plate Nest Attribute Mapping

Attribute mappings link  product lines with SigmaNEST materials. These are entered in PR51.

![](../../Resources/Images/PR51_PN_attribute_map.png) ![](../../Resources/Images/PR51_PN_attribute_map2.png)

In the example, CPL in  is mapped to MS in SigmaNEST, and SPL in  is mapped to SS in SigmaNEST.

will use the Grade if a mapping is defined for it in PR51. If no grade is defined, it will use the Material if a mapping is defined for it in PR51. If no material is defined,  will default to the product line.



Batch Run


The batch run script for the SigmaNEST database polling should be set in the crontab to run every minute. It is located with the other  login scripts in /usr/bin.

The batch job will log into  as user SIG and query the SigmaNEST database for posted programs. For each posted program it finds, it will generate an In-house Production document.

The script's contents should be similar to the following:

CDATE\_50=Y  
export CDATE\_50  
  
DATE\_SC\_50=Y  
export DATE\_SC\_50  
  
JAVA\_HOME=/usr/java/jre1.8.0\_241  
export JAVA\_HOME  
  
PROIV\_HOME=/usr/dev83/virtual\_machine  
export PROIV\_HOME  
  
LD\_LIBRARY\_PATH=$LD\_LIBRARY\_PATH:$JAVA\_HOME/lib/amd64:$JAVA\_HOME/lib/amd64/server:$JAVA\_HOME/lib/amd64/client:$PROIV\_HOME/lib:/usr/local/lib:$PROIV\_HOME/lib/instant\_client:$PROIV\_HOME/lib/libcurl  
export LD\_LIBRARY\_PATH  
  
PATH=/usr/java/jre1.8.0\_241/bin:$PROIV\_HOME:/usr/vsifax/obin:/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin:/usr/X11R6/bin:/usr/vsifax/bin:/usr/vsifax/lbin:/root/bin  
export PATH  
  
PROPATH=/usr/dev83/virtual\_machine/stm310  
export PROPATH  
  
PRODATA=/usr/dev83/virtual\_machine/stm310/stmdata  
export PRODATA  
  
PRORUNTYPE=DEV  
export PRORUNTYPE  
  
PROTERM=DECVT100  
export PROTERM  
  
GUI=N  
export GUI  
  
export SSO\_JARPATH=/usr/dev83/virtual\_machine/stm310/sso  
  
export ORACLE\_HOME=/oracle/product/12.2.0/sm3  
export ORACLE\_SID=stmprod  
export SQL\_DBTYPE=ORACLE  
export SQL\_USERNAME=stm310user  
export SQL\_PASSWORD=stm310user  
export SQL\_DBNAME=stmprod  
export SQL\_CURSORS=AUTO  
export PRODB\_CHARSET=8  
export LOCKED\_ROWS\_RETURNED=Y  
export SQL\_NOSIG=Y  
export SQL\_TRANSACTION\_ERROR=Y  
export NLS\_LANG="AMERICAN\_AMERICA.AL32UTF8"  
  
cd $PRODATA  
  
/usr/dev83/virtual\_machine/pro SIG STM

If the cd $PRODATA line is not there, batch6.out may be found in $PROPATH instead $PRODATA.

The SIG batch run user must exist as an operator in MS32, and the company code must match the one used in the script:

![](../../Resources/Images/MS32_SigmaNEST.png)

For developers, SIG must be a standard batch run user with STPOLL as the Logon and Default function links:

![](../../Resources/Images/SigmaNEST_config8.png)

All activity for the batch run is logged in $PRODATA/batch6.out.

Troubleshooting
---------------

If batch6.out is not being updated, you may need to run the Reset SigmaNEST Cron [PR58]. This utility recreates the batchque.pro file with the required permissions, and archives the batch log file (batch6.out).

The following are some common messages you may encounter in batch6.out that will prevent the IP from being generated:

* **Failed to acquire licence - 'Could not acquire licence of type 'PROIV Runtime' from licence group ''. Insufficient free licences available.'**

This will completely stop the batch run from proceeding and will cause a build-up in the batch queue.  
As root, you will need to first restart the PROIV license server, then recreate $PRODATA/batchque.pro.  
If the problem persists, there may be an issue with the number of available licenses, or the PROIV installation.

* **DIM NOT DEFINED, DROP SHAPE: ''**
    
  **015 - SUBSCRIPT VALUE NOT WITHIN RANGE OF DIMENSION - $UOMS\_CONVERSION\_TYPE 0**

This likely indicates the log that was used for the nesting could not be found in , or the shape is not a sheet type. This can also occur if SheetData1 for the sheet in SigmaNEST is not prefixed with the warehouse code, or is an invalid log number. The nest will have to be redone with an appropriate plate.

* **IP generated with no set**

This likely indicates either the machine that was used in SigmaNEST could not be found in  based on the machine description, or the machine that was used did not have a valid Process set in PR18.

---
