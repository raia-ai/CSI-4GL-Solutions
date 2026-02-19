---
title: "Handhelds-StayLinked_Setup"
source: "Handhelds-StayLinked_Setup.docx"
tags: ["staylinked", "handhelds", "setup", "configuration", "server", "client", "documentation"]
version: "1.0"
last_updated: "2025-12-03"
short_description: "StayLinked setup guide covering server configuration, handheld profiles, and troubleshooting for 4GL integration."
long_description: "This document provides comprehensive instructions for setting up and configuring StayLinked with 4GL. It covers adding servers to StayLinked Administrator, creating handheld profiles, understanding the technical relationship between StayLinked and the 4GL server, and troubleshooting common issues with handheld devices."
---
**StayLinked Setup**
**Download Link:**
- Selectthe download link forSmartTE Administrator and Server Software
- Login andensure to click "Administrator Downloads" on the left pane and download theFull Windows version
**Application Link:**
Overview
This documentation covers the process of adding handheld profiles to a client's StayLinked server using StayLinked Administrator.It also briefly covers theunderlying technical relationship between StayLinked, the 4GL server and the physical handheld devices. Finally, common troubleshooting scenarios are discussed.
Adding and Connecting to a Server
- To add aserver to StayLinked Administrator, simply right click on the "Server List" and then click "Add". You can also click "Servers" on the top right-hand side of the screen and select "Add"
- A window will pop-up to allow you toadd the server information. The**Server Name**should the3-character customer. The**Server IP**would be the associated IP address for that customer.Refer totheSpreadsheet for the required information
![Image](Handhelds-StayLinked_Setup_media/image_1.png)
- To connect to a server, double click on it from the list on the left pane of the screen.The credentials are:
  - User ID: administrator
  - Password:esp
![Image](Handhelds-StayLinked_Setup_media/image_2.png)
- Once connected, the following menu options will be available for that server. In the screenshot below, we are connected to the SSL_IEP server
![Image](Handhelds-StayLinked_Setup_media/image_3.png)
- **Connections > All Connections**: list all the handhelds that are connected to the server. For troubleshooting purposes, you are presented with information such as the MAC and IP addresses.
Adding Profiles
- Clicking on**Client Configuration > Scan2Command Profiles**presents you with the screen necessary to create handheld users in StayLinked
![Image](Handhelds-StayLinked_Setup_media/image_4.png)
- To create a new profile, click on the**Add**button on the top right-hand side of the screen
- A new window will pop-up to allow you to input the user information. The**Profile Name**should be the user's name
![Image](Handhelds-StayLinked_Setup_media/image_5.png)
- Once the profile name is entered, click on the**Commands**tab
![Image](Handhelds-StayLinked_Setup_media/image_6.png)
- Click on the**Add**button to add a new command
- A new window will pop-up to allow you to input the command information
![Image](Handhelds-StayLinked_Setup_media/image_7.png)
- The**Command Name**should be the user's name
- The**Command String**should be the following:
  - `telnet 192.168.1.1 23`
  - Replace the IP address with the appropriate IP address for the customer
- Click**OK**to save the command
- Click**OK**to save the profile
- The new profile should now appear in the list of profiles
Technical Overview
StayLinked acts as a middleware between the handheld devices and the 4GL server. When a user logs into a handheld device, the device connects to the StayLinked server. The StayLinked server then establishes a telnet connection to the 4GL server on behalf of the handheld device. This architecture provides session persistence and allows users to disconnect and reconnect without losing their session state.
Troubleshooting
**Handheld cannot connect to StayLinked server**
- Verify the handheld device has network connectivity
- Check that the StayLinked server is running
- Verify the IP address configured on the handheld matches the StayLinked server IP
- Check firewall settings to ensure the required ports are open
**User session is lost when disconnecting**
- This typically indicates the StayLinked server is not properly maintaining the session
- Check the StayLinked server logs for errors
- Verify the profile configuration is correct
**Cannot telnet to 4GL server**
- Verify the 4GL server is accessible from the StayLinked server
- Check that port 23 (telnet) is open on the 4GL server
- Verify the IP address in the command string is correct
