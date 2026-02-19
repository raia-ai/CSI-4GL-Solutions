---
title: "Setting Up Pick Slip Print Options"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Setting Up Pick Slip Print Options"
long_description: "Help documentation for Setting Up Pick Slip Print Options in the 4GL system."
---


Setting Up Pick Slip Print Options
==================================

This topic applies to setting up the regular picking list (form 05); there are separate forms for other types of pick slips (24-OP Pickslip, 55-Branch Transfer Picking Slip, 56-Customer Consignment Picking Slip, 59-Linear Nesting Picking Slip).

See Setting Up Form and Label Print Options for additional form printing options you may want to define.

Configuring Print Options
-------------------------

The print options allow you to control which printer or which printer tray to send different pick slip types to, the number of copies to print, if it should print in landscape orientation, etc. For example, you may want to print regular pick slips from tray 1 with white paper but print backorder pick slips from tray 2 with yellow paper.

To access the print options, open IN19 > Forms > press F4 on the P column beside Picking List.

![](../Resources/Images/ADM_whse-form-mtce.png)

On the print options screen, create an entry for each type of order that you print pick slips for, using the W column to specify the order type, as shown in the image above.

* blank - default option for regular sales and POS orders
* K - back orders1
* O - OP document reserves - this setting is used if there are any OP/IP documents reserved on the order

Printing by Primary Process or Bin Location
-------------------------------------------

may be set up2 to print a pick slip for each unique primary process and/or bin location on an order, in addition to the master copy of pick slips defined on the main print options screen above.

Printing by primary process allows you to segregate a single order into logical groups. For example, an order could require saw cutting, straight stock pulls, and plate cutting. By printing by primary process you could end up with three picking slips (for the same order)—one for each process described in the example.

Printing by bin location allows you to segregate a single order into picking areas of the warehouse. Typically, printing by bin location facilitates picking functions and not production functions. For this function to work you must assign products in a warehouse to a bin location (using function IN9ZZ [xref]). These locations can either be broadly defined, like bay 1, bay 2 etc. in which case you would print out a separate picking slip per bin location OR, if you have specific “homes” for products in your warehouse, bins can be defined in a way that allows you to sort a single picking slip by location providing you with an efficient picking path.

A switch option allows for printing by either machine or bin location: this would print by machine for lines that have a machine on them (as long as the machine is not marked as stock in PR11) and would print by bin location for lines that do not have a machine on them or the machine is marked as stock in PR11.

If you do not want a master copy to print, set the printer to NUL in the main print options:  
![](../Resources/Images/ADM_whse-form-mtce-null.png)

You can also choose to define print options by Operator, i.e. if you want a user to print to a different printer than other users. Machine, Bin Location, and Operator settings are not mutually exclusive and just allow for additional outputs of pick slips. For example you could print a copy with just the lines associated with the machine code, and also a copy for the operator with all open lines.  
A form option for the pick slip allows you to print the bin location below the order line (enter “N” in the “Additional Details Print Order”).

### Printing By Machine

On the print options screen, click Machine to define the options for each machine process that you want to print separately. If a machine process is not specified, it will use the default print options.

Machine pick slips only print the order lines associated with the defined machine processes. For example, a “SAW” pick slip will only have order lines associated with the “SAW” machine.

### Printing By Bin Location

On the print options screen, click Bin Location to define the options for each bin location3 that you want to print separately. If a bin location is not specified, it will use the default print options.

If bin locations are defined, those pick slips will only print order lines associated with the defined bin locations. For example, an “A1” pick slip will only have order lines with bin location “A1”.

These instructions provide separate picking slips for each bin location. If you want a single picking slip sorted by bin location you would instead set the Sort by Bin Location option in the form options (press F4 on the O column beside Picking List).

Configuration


1 For backorders that are released through the Task Manager, this setting is only used if the Backorder Method switch is set to “A”.

2  > Print Separate Pickslip For Each Unique Machine/Bin On Order

3 Products are assigned to a warehouse and bin location in IN18 > Warehouse

---
