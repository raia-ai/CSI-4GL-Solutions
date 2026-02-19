---
title: "Toyota ASRS Cron Job"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Toyota ASRS Cron Job"
long_description: "Help documentation for Toyota ASRS Cron Job in the 4GL system."
---


Toyota ASRS Cron Job
====================

The cron job is the link between  and Toyota. The script can be found in /usr/bin/tsmgetbat. It is fired up frequently. The frequency can be changed as follows:

* cd /var/spool/cron
* Crontab –e to edit
* The frequency is currently set as \*/5 (every 5 mins)
* :wq to save and exit
* Crontab –l to list the contents

You can view the cron log on the server by viewing /var/log/cron. If it stops working, use the Toyota Recovery Utility (TSM92) to restart (see below).

Trigger – TSM91
---------------

This function sets up the Batch Queue and initiates TSM911. The batch queue (5) can be found in: /usr/dev9/virtual\_machine/stm321/stmdata.

Download – TSM911
-----------------

This function performs the following:

* downloads stock items from F05\_DAT
* downloads storage results from F06\_DAT
* downloads retrieval results from F07\_DAT.

All the downloads store their data in an intermediary file keyed on today’s date and a sequence number. This ensures that there are no data clashes. On completion of this cycle TSM9111 will be initiated.

Upload – TSM9111
----------------

This function performs the following:

* uploads storage items to F01\_DAT
* uploads retrieval items to F02\_DAT
* uploads Parts Master data to F03\_DAT

All the upload functions ensure that the target files are empty so as not to clash with data that Toyota has not finished processing. If there is data present it will skip that cycle until the file becomes available. On completion of this cycle TSM91111 will be initiated.

Process Download Data – TSM91111
--------------------------------

This function runs directly after the above function and performs the following:

* Extracts any unprocessed stock records and updates the sync file as part of the Inventory Synchronize procedure.
* Extracts any unprocessed Storage Results data and matches them to the original Storage Requests. It will perform a log split, transferring the material from the original [F]loor log and transferring it to a newly created [T]oyota log. If there is any difference between the Storage Request and the Storage Result it will log an Adjustment Record.
* Extracts any unprocessed Retrieval Results data and matches it to the original Retrieval Request. It too will perform a log split, splitting off the Retrieval Quantity from the Toyota log and spawning a new Floor child log. It then deletes the original log reserve on the SO line and replaces it with a reserve on the newly created Log. If there is any difference between the Retrieval Request and the Retrieval Result it will log an Adjustment Record.

On completion of this cycle the cron job will be exited.

Recovery Utility – TSM92
------------------------

This function allows you to restart the Toyota cron job in event of a failure.

1. Choose Toyota ASRS System » Toyota Recovery Utility [TSM92].
2. The Toyota ASRS paths are listed. You only need to be concerned with the following:
   * Storage Upload (F01)
   * Retrieval Upload (F02)
   * Item Master Upload (F03)
   * TSM Busy File

   The Upload files are normally retrieved by Toyota and then deleted. Similarly, the TSM Busy File relates to the cron job itself and should normally be deleted automatically after running.
3. If any of the above are Loaded, select the Remove checkbox next to the item.
4. Select the OK checkbox then click Process.

---
