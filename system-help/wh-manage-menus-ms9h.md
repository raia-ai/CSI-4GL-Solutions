---
title: "Managing Wireless Handheld Menus"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Managing Wireless Handheld Menus"
long_description: "Help documentation for Managing Wireless Handheld Menus in the 4GL system."
---

Managing Wireless Handheld Menus
================================

The Handheld Menu Type Maintenance screen allows for multiple menu templates to be created with different menu options. A menu type can be assigned to all operators at one or all warehouses, or can be selected or modified for individual operators.

Creating a Menu Type
--------------------

To view and manage handheld menu templates, choose Administration » Administration » Handheld Menu Type Maintenance [MS9H].

* To add a new menu template1, click Add and enter a Code and Title for the menu, then click Save. A new window opens where you can select up to 17 functions to be listed in the menu. You can use the default description or edit it for this menu. When you are finished adding the required functions, click **Save**.
* To copy an existing menu template1, select it and click Copy, enter a Code and Title, and click Save.
* To change the menu options for a menu template, double-click the title, or select it and click Options.

A menu type becomes available to all users as soon as you have created it.

If you have made any changes to an existing menu type and want to apply the changes to the menu type for all users, click Update.1   
Note that this will overwrite any user-specific settings for that menu type.

You cannot delete a menu template if it is the active menu for any operator.

Activating a Menu for One or All Operators
------------------------------------------

You can make a menu the active menu for one or all operators, at one or all warehouses, in MS9H:  
Select the menu and click Activate, then select All or a specific warehouse. Search for and select an operator to activate the menu for, or select all to apply it to all operators. The selected menu overwrites the previously active menu for the warehouse(s)/operator(s).

Alternatively, you can change the menu or the menu options for individual operators in MS32:  
Select an operator and go to the Options tab and click Handheld. The operator’s currently active menu is displayed. To set a different menu for this operator, select the new Menu Type and optionally change the Menu Options. Click Activate to set the new menu and/or options for this operator. To reset the menu options to those defined in the template, click Default.

An operator can select a different menu template from the handheld: In the Selection field, enter 0 then enter the menu code for the desired menu template.

Configuration


1 Add/Modify/Delete/Copy/Update functions are only available if the Template Admin checkbox is enabled for the operator (MS32>Options>Handheld). If Template Admin is not enabled, the operator can only access Options and Activate.

---