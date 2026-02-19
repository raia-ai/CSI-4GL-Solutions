---
title: "Ka Restarting Kasto Ka92"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Ka Restarting Kasto Ka92 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Ka Restarting Kasto Ka92 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Kasto Recovery Utility [KA92]
=============================

This function allows you to restart Kasto in the event of an interruption.

1. Type KA92 at the command line.  
   A message will be displayed “KASTO Cron Job Terminated”. If any other message is displayed here, contact Support.  
   The above is achieved by copying /usr/bin/kasgetbat to kastmpbat and nullifying kasgetbat.
2. Press Enter to continue. The main screen is displayed.

![](../Resources/Images/kasto_recovery.png)

“/home/gaw/kasto” is the Telegram Create Location set up in IN19.

3. Select/clear any files in the Remove column.
4. The function will check the Kasto Mount folders.   
   If not present the following will be displayed “THE KASTO FOLDERS ARE NOT MOUNTED – PLEASE RECTIFY BEFORE ANY RECOVERY CAN BE PERFORMED” and the function will be terminated.  
   If they are present, select the OK? check box.
5. The function will now remove the selected files (if any) and attempt to restart the cron job. If successful the message “KASTO Cron Job Restarted” will display.   
   Press Enter to continue.
6. If any other message is displayed, contact Support.  
   The above is achieved by copying /usr/bin/kastmpbat back to kasgetbat.

|  |  |
| --- | --- |
| Kasto Send Folder (/mnt/mtr/tcpsnd) | This folder is the Kasto “mount” folder and is used by Kasto to return a Telegram Acknowledgement to . This folder should always be Loaded and there is no option to remove it. This folder must be set up manually before this restart can be executed. ASA’s technical support should be contacted in this regard. |
| Kasto Send File (/mnt/mtr/tcpsnd/dl0001.ksd) | This is the Kasto Telegram Acknowledgement to an Telegram Request. This file should generally not be present and would not hold up Kasto in any way. There will be no option to remove it. |
| SM3 Temp Receive File (/home/gaw/kasto/DL0001) | This is the file into which the Kasto Telegram Acknowledgement is transferred from dl0001.ksd above. This file should not be present. If it is it this could hold up Kasto. There will be an option to remove it and it will default to [y]es. |
| SM3 Temp Send File (/home/gaw/kasto/dh0001.ftp) | This is the file into which places a Telegram Request. This would include such things as Sales Order Unloads, Receipt Loads etc. This file should not be present. If it is this could hold up Kasto. There will be an option to remove it and it will default to [y]es. |
| Kasto Receive Folder (mnt/mtr/tcprcv) | This folder is the Kasto “mount” folder and is used by Kasto to accept a Telegram Request from . This folder should always be Loaded and there is no option to remove it. This folder must be set up manually before this restart can be executed. ASA’s technical support should be contacted in this regard. |
| Kasto Receive File (/mnt/mtr/tcprcv/dlxxxx.rcv) | This is the Telegram Request where xxxx is the last odometer reading. This file should generally not be present and would not hold up Kasto in any way. There will be no option to remove it. |
| Kasto Busy File (/usr/dev62/virtual\_machine/edmrun/edmdata/kasbusy.txt) | This is an temporary file that controls the traffic between and Kasto. This file should not be present. If it is it could hold up Kasto. There will an option to remove it and it will default to [y]es. |
| PRO-IV Batch Queue (usr/dev62/virtual\_machine/edmrun/edmdata/batchque.pro) | This is a PRO-IV file that controls the running of this Kasto interface in the background. This file should always be present. If not, Kasto will not run. There is an option to remove it but it will default to [n]o. Support should be contacted in this regard. |

Cron Script
-----------

The cron script for the Kasto operation is ‘kasgetbat’ and it resides in /usr/bin

If you need to stop/start the cron job for any reason:

1. Change directory to /var/spool/cron
2. Enter crontab –e
3. Remove/Insert a #(remark) as the first character of the cron job.
4. :wq

---
