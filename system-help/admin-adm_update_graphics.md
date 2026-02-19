---
title: "Adm Update Graphics"
source: "madcap.md"
tags: ["4GL", "ADMIN", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Adm Update Graphics - 4GL Help Documentation"
long_description: "This topic provides detailed information about Adm Update Graphics in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the ADMIN module."
---
Updating  Graphics
==================

Each time you receive an update there is a good chance a new graphic file has been created. You'll know you are missing a graphic if an  oval is displayed instead of the graphic.

This is not an issue for those using the browser version of , as files are used from the server which are automatically updated.

PC Users
--------

If you are running  on a PC desktop (not via browser), graphics are stored in the following folder (depending where you have the NorthgateArinso folder installed):

C:\Program Files (x86)\Zellis\PROIV Version 9\Client\bitmaps

This folder must be released in Windows Security to all can update, otherwise you will receive security errors when you download graphics files.

To force a new download of graphics at time of login, in MS32 clear the Graphics Version field. The .piv login (login edited in Edit > Session Properties > Connection) must be the  login.

![](../../Resources/Images/MS32_Graphics_version.png)

Terminal Clients
----------------

There is no need to download graphics files by user. However, graphics files should be updated by copying all files, existing on a desktop/laptop, to the folder on the server used by the terminal client files, or they can be copied from the Linux server. Normally this would be done by your IT Department.

---
