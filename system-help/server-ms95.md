---
title: "Restarting the License Server"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Restarting the License Server"
long_description: "Help documentation for Restarting the License Server in the 4GL system."
---

Restarting the License Server
=============================

[deprecated as of 3.15 - BG 38123]

Sometimes the  license usage number goes out of sync and licenses are being consumed “in error”. Restarting the license server releases these licenses without killing valid sessions.

There are two ways to restart the server:

* From within :  
  Choose Administration » Administration » Restart License Server [MS95]
* From the command prompt on the Linux server (must be done as root):  
  cd /usr/dev81/ManagementServices/bin  
  ./managementServices restart

---