---
title: "Using the Browser Version"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Using the Browser Version"
long_description: "This topic provides detailed information about Using the Browser Version in the 4GL system."
---


Using the Browser Version
=========================

[use “browser version”, not “Open Client”]

Our web browser version allows users to connect to  from any device, anywhere in the world with an internet connection.

**When you want to disconnect, be sure to use the Logoff button.** If you simply close the tab your session will be left hanging which will hold onto record locks until the session times out or until you recover the session (see below) and log off properly.   
**Also, do not allow your browser to remember passwords for .**

Some limitations of the browser version:

* After you log off, you will be left with a blank tab. This is a ProIV limitation; you can just close the tab.
* Duplicating tabs is not supported.
* Double-click doesn’t work in product select. You must press Enter or click the select button to select a product.
* When entering the body of an email or remarks, use Shift+Enter to create a new line (not Ctrl+Enter as in the Windows version).
* The session timeout default is 30min but this can be overridden at the user level (MS32).

Settings Specific to the Browser Version


In order to upload generic documents to sales orders or purchase orders, you must set the “AP Document Attachments” and “AR Document Attachments” directories in IN19, for each warehouse.   
You should also set the “AR Generic Document File Path Linux” or “AP Generic Document File Path Linux” switches (in  or via MS33 > Accounts Receivable [Payable] > Additional Options) to store system-wide files associated with customers, vendors, and products.



Changing the Screen Size


To change the size of the screen in your browser, hold your Ctrl button and use the scroll wheel on your mouse to make it larger or smaller.



Making Sure Column Position and Width Changes Persist


### Chrome

1. Open your Chrome Settings and choose Settings.

![](../Resources/Images/chrome_settings.png)

2. Open the **Privacy and Security** page and click Site Settings.
3. Scroll down to the bottom and click Additional content settings.
4. Scroll down again to On-device site data.
5. Select Allow sites to save data on your device.

   ![](../Resources/Images/Chrome-privacy-allow-sites-save-data.png)

### Edge

1. Open your Edge Settings and choose Settings.
2. On the Privacy, search and services page, click Cookies.
3. Enable Allow sites to save and read cookie data (recommended).

   ![](../Resources/Images/Edge-privacy-allow-sites-save-cookie-data.png)

Alternatively, if you don’t want to allow all sites to save and read cookie data, you can set the  URL as an exception:

1. Open your Edge Settings and choose Settings.
2. On the Privacy, search and services page, click Cookies.

   ![](../Resources/Images/Edge-privacy-allow-1site-save-cookie-data1.png)
3. Next to Allowed to save cookies, click Add site. Enter the URL you use to connect to , select the Include third-party cookies on this site checkbox, and click Add.

   ![](../Resources/Images/Edge-privacy-allow-1site-save-cookie-data.png)
4. You now have to make sure that these cookies are not cleared when you close Edge.  
   Click the Privacy, search and services page again and then click Clear browsing data.

   ![](../Resources/Images/Edge-privacy-allow-1site-save-cookie-data2.png)
5. Click Choose what to clear every time you close the browser.
6. If you don’t want to clear any cookies and site data, turn off the Cookies and other site data option.   
   If you want to clear all cookies and site data except for : next to Don’t clear, click Add. Enter the URL you use to connect to , select the Include third-party cookies on this site checkbox, and click Add.

   ![](../Resources/Images/Edge-privacy-allow-1site-save-cookie-data3.png)


Printing to PDF


If you are printing forms to PDF, normally the PDF will open in the Adobe viewer in Chrome. If you want to download the PDF to open in the Adobe application instead, change your settings in Chrome as follows:

1. Open your Chrome Settings and choose Settings.

![](../Resources/Images/chrome_settings.png)

2. In the “Privacy and Security” section, click Site Settings.
3. Scroll down to the bottom and click Additional content settings.
4. Click PDF Documents and enable the switch:

![](../Resources/Images/chrome_settings_PDFdocs.png)

If your browser is set to download PDF files, any PDF reports generated in  will be saved to your Downloads folder.



Recovering Sessions


If you inadvertently close a session (close the browser tab) without logging off properly, you can recover the session (start right where you left off) without missing a beat.

You can only recover sessions if the whole browser isn’t closed, unless you have your browser settings set to “Continue where you left off”.  
![](../Resources/Images/ADM_browser-settings.png)

When you start , if there is a session to recover you will be presented with a recoverable session window:

![](../Resources/Images/ADM_browser-recoverable-session.png)

To recover the session, click the link (RM5010S1 in the example above). This will open a new tab with the recovered session but will leave the previous tab on the login page: you can close that tab.



Mac OS Keyboard Shortcuts


and this help system are based on Windows conventions. However, it is possible to use the browser version of  on Mac OS. While the experience would largely be the same on both platforms, there are some keyboard shortcuts that are different between Windows and Mac OS. For the most part you can just swap the Command key wherever you see Ctrl.

| Function | Windows | Mac OS |
| --- | --- | --- |
| Select multiple entries in a list | Shift+click (for contiguous entries) Ctrl+click (for non-contiguous entries) | Shift+click Command+click |
| Add a new line (e.g. Remarks) | Ctrl+Enter (Shift+Enter in the browser version) | Shift+Command+Enter |

---
