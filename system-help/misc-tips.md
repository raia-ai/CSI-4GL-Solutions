---
title: "Tips"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Tips - 4GL Help Documentation"
long_description: "This topic provides detailed information about Tips in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Data Entry Tips
===============

* Accelerator keys are underscored letters on tabs and buttons that serve as shortcuts to invoke a command or action without having to tab to it or use your mouse to click on it. Pressing Alt+the letter is the same as clicking on the button or tab; for example, if you're on the Billing tab of a sales order, you can press Alt+U to attach a document without having to navigate down to the Document button:  
  ![](../Resources/Images/accelerator-keys.png)
* selecting multiple items in a list:
  + if the items are all together (adjacent), click the first item, then press Shift and click the last item
  + if the items are not all together, press and hold Ctrl (Command) and click each item
* when you see Y/N options, blank=N
* lists that have a ![](../Resources/Images/i_reset_4_arrows.png) at the bottom right - click this icon to restore the default columns if you have resized or rearranged columns
* use **%** as a wildcard in any string search (searching for customers, vendors, or products) to take the place of any number of characters. For example, **m%r** will find results that start with **m** and have any number of characters between **m** and **r**: Mac Service, Maverick Metal, Metal For All, etc.

Function Keys
-------------

| Key | Mode | Description |
| --- | --- | --- |
| ESC | Escape | Cancel what you are currently working on. Note there may be times when you cannot cancel as records have been processed. |
| F3 | End of Data | Saves and exits the screen you are currently in. You may be asked if you would like to Process, Hold, or Abort the current document. Depending where you are in the screen you may not be able to exit the screen until remaining fields have been completed. |
| F4 | Open Window | Fields that have + or … can be opened to see more options -- press F4 (or double-click) to open the additional window. |
| F5 | Add | Add a new line (record) to the screen. Can only be done in paging screens. |
| F6 | Change / Select | In paging screens, pressing <F6> while on sequence number (Seq) of a line will select it for changing. In select windows, pressing <F6> will select the line you are on and return data from it to previous screen. |
| F7 | Delete | Pressing <F7> while on a line in a paging screen will select it for deletion. You can then use the up and down arrow keys to select additional lines. Once you have selected all the lines you would like to delete, the system will open confirmation window. |
| F8 | Lookup | Lookup mode. |
| F9 | Expand / Contract | Some paging screens have “hidden” details for each line. Press <F9> (or click  at the bottom right) to view these additional details. Press <F9> again (or click ) to hide the details. |
| / | Exit | Exits out of current screen. |

If Your PC is Using a Comma Instead of a Period for Decimals
------------------------------------------------------------

1. Open the Control Panel and open the Region settings.
2. Click Additional settings.
3. On both the Numbers and Currency tabs, change the Decimal symbol to a period.  
   ![](../Resources/Images/decimal-symbol.png)
4. If you are using the non-browser version of :
   * Choose Edit » Session Properties (at the top of the window).
   * On the Regional Settings tab, choose “ProivRes\_French\_Canadian.dll”.
   * Click Apply, then OK to close the properties.

   ![](../Resources/Images/decimal-symbol-PIVsession-prop.png)

---
