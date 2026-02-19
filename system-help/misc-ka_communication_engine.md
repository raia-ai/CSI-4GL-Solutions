---
title: "Ka Communication Engine"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Ka Communication Engine - 4GL Help Documentation"
long_description: "This topic provides detailed information about Ka Communication Engine in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Communication Engine
====================

|  |  |
| --- | --- |
| **KA4111** | Transfer any Telegram Requests in KAR\_RCV to Kasto |
| **KA411** | Retrieve any Telegram Responses from Kasto and place them in KAS\_SND |
| **KA511** | Process Telegrams returned by Kasto. The Telegrams are returned in file KAS\_SND. After each KAS\_SND Telegram is processed it will be flagged so as not to be processed more than once. These KAS\_SND records can be viewed at any time by invoking KA63 – Kasto Unload Transaction Log. |
| **LHBM** | Inventory Feed Back. This Telegram is in response to a HLBM Telegram Inventory Inquiry. The transaction then follows one of two paths:   * Non-Synchronized - will create a KAD\_DTL record for each transaction and update it with the Kasto info returned.   It will also create an Adjustment entry if there is any discrepancy. * Synchronized - will take the returned Kasto Info and update the KAS\_SNC file. |
| **LHAU** | Order Feed Back. This Telegram is in response to a HLAU Telegram Order Entry. Can either be an Order Type 01 Unload or 10 Load.  01 - Unload:   * The Unload are SO Sales Orders, BT Branch Transfers and CC Consignment * First match and update the KAD\_DTL record with ‘Kasto’ values. (The KAD\_DTL record was originally created during the Kasto Load process). * The transaction stream is now split into two paths – Sales Order and Production Order. * Sales Orders are processed as follows:   + Downdate Order Header from Order Detail.   + Spawn a Child Log from the Parent log to satisfy the Sales Order (LULITSPL).   + Disconnect any reserves for this order on Parent log (LULITDSC).   + Commit to new reserve transfer method (LULITTFR).   + Re-allocate any reserves for other orders in excess of on-hand (LULITALL).   + Create OEL\_LOG record referencing this new spawned log.   + Generate an Adjustment transaction if Kasto on-hand not equal to SM3 on-hand.   + Update Sales Order header OEH\_HDR   + Update Picked quantity on spawned INL\_LOG. * Production Orders are processed as follows:   + Downdate Production Header and Set record from Raw Material record.   + Spawn a Child log from the Parent log to satisfy the Production Order (LULITSPL).   + Disconnect any reserves for this order on Parent log (LULITDSC).   + Commit to new reserve transfer method (LULITTFR).   + Re-allocate any reserves for other orders in excess of on-hand (LULITALL).   + Create PRR\_LOG record referencing this new spawned log.   + Generate an Adjustment transaction if Kasto on-hand not equal to SM3 on-hand.   + Update Production Order Header POD\_DOC and Set record (PRL\_LNK).   + Update Picked quantity on spawned INL\_LOG.   10 - Load:   * First match and update KAD\_DTL with ‘Kasto’ values (see above). * Read the [F]loor Parent Log. * Check for Order End and if so finalize. * Split off the cumulative amount loaded (LULITSPL). * Transfer only those reserves that are necessary from the Parent to the Child (LULITTFR). * Re-allocate any reserves for other orders in excess of on-hand (LULITALL). |
| **LHST** | Master Data Feedback. This Telegram is in response to a HLST Master Data maintenance OR a HLSA Master Data Inquiry Telegram. Every KAS\_SND record received will stamp the corresponding KAM\_MFS record with its cross reference address. This will allow the Kasto Master Data to be compared in KA67 Analyse Product Master Sync. |
| **LHBK** | Inventory Correction Message. This Telegram is in response to a correction made to the Kasto Database in the Kasto System. An ‘exact’ SM3 Inventory Adjustment is set up accordingly. |

---
