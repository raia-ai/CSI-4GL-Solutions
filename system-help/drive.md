---
title: "Mapping a Network Drive"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Mapping a Network Drive"
long_description: "Help documentation for Mapping a Network Drive in the 4GL system."
---


Mapping a Network Drive
=======================

1. Enable the Client for NFS service:
   1. Go to Control Panel > Programs > Turn Windows features on or off.  
      ![](../../Resources/Images/map-drive1.png)
   2. Scroll down until you see “Services for NFS”. Make sure this is enabled along with “Client for NFS”. The Administrative Tools do not need to be enabled.  
      ![](../../Resources/Images/map-drive2.png)
2. Edit the registry:
   1. Click Windows Search, then type regedit in the Search field and press Enter. Click Yes to allow changes to your device. If you encounter an issue editing the registry in the following steps, run regedit as an administrator.
   2. Add a new DWORD32 registry entry for AnonymousGid:
      1. Click Edit, and select New DWORD (32 bit) Value.
      2. In the Name field, enter “AnonymousGid”. Leave the value at 0.
   3. Repeat to add a second DWORD32 registry entry named “AnonymousUid” with a value of 0.  
      ![](../../Resources/Images/map-drive3.png)
3. Restart the NFS client:
   1. Click Windows Search, then type cmd, right-click on the command prompt app and click Run as Administrator.
   2. In the Windows Command Line (CMD) window, restart the NFS Client by typing the following:  
      nfsadmin client stop  
      nfsadmin client start
4. Map the network drive:
   1. Open File Explorer, then right-click on This PC > Map network drive.
   2. Assign the letter for the drive. The letter should be the same on all computers and in  (Z used as example).
   3. Type the folder path.  
      \*\* Keep in mind linux uses this **/** for a backslash but on windows it is a **\**  
      Make sure you use this **\** on this screen \*\*
   4. Click Finish. This process can take just over a minute.

      ![](../../Resources/Images/map-drive4.png)
5. After connecting successfully, you should be able to see all the folders within the drive directory.

---
