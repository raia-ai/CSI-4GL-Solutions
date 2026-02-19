---
title: "Understanding How  Handles Sales Taxes"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Understanding How  Handles Sales Taxes"
long_description: "Help documentation for Understanding How  Handles Sales Taxes in the 4GL system."
---


Understanding How  Handles Sales Taxes
======================================

applies sales taxes based on the customer's ship-to address. These taxes are applied on a hierarchical nature in the order shown:

* City
* County
* Province/State
* Country

provides a table at each level; for each individual entry (e.g. each city in the City table) you can define the default tax rate and whether that level's tax should be applied in *addition* to a tax at a higher level, and whether the tax is the *last* tax to be considered (ignoring a tax at a lower level).

Some examples:

* **Ship-to = Ontario, Canada**
    
  Corresponding table entries:  
  City = blank  
  County = blank  
  Province/State = blank  
  Country = GST  

  ► Only the country tax (GST) will be charged.
* **Ship-to = New Brunswick, Canada**Corresponding table entries:  
  City = blank  
  County = blank  
  Province/State = HST, last tax  
  Country = GST  

  ► Because the Province/State tax is set as the last tax, the system will not look further to the Country level.  
  Only one level of tax (HST) will be charged.

* **Ship-to = New Orleans, Orleans Parish (county), Louisiana, USA**
    
  Corresponding table entries:  
  City = city tax, additional  
  County = county tax, additional  
  Province/State = state tax, additional  
  Country = federal tax, additional  

  ► Because taxes are defined at all four levels, and each is defined to be charged in addition to others, all four levels of tax will be charged.

* **Ship-to = Kansas City, Kansas, USA**
    
  Corresponding table entries:  
  City = city tax, additional  
  County = blank  
  Province/State = state tax  
  Country = federal tax, additional  

  ► Because a City tax is applicable and the State tax is not set to be applied in addition to previous level taxes, the State tax will be bypassed. Two levels of tax (city, country) would be charged.

A customer can have one or more ship-to addresses defined in their customer file, or a one-time ship-to address may be recorded at time of order entry. If a customer should be charged a specific tax even if their address would otherwise preclude it, the tax code should be added to their ship-to details in their customer file, or it may be added to the quote/order. Sales staff may be able to change the taxes on a quote/order.1

includes a built-in table of postal/zip codes; whenever you enter a postal code (in customer maintenance or order entry),  populates the city, county, state and country based on the postal/zip code entered. You may edit this table [MS45] if you wish to customize the city alias associated with the postal/zip code. Alias City names are used at time of printing of documents.

Setting Up the Tax Types and Rates
----------------------------------

Default tax types and rates are defined in the Tax Jurisdiction file. One or more rates from this table are applied to the quote/sales order at time of entry according to the ship-to address, as illustrated above. Sales staff may be able to change the taxes on a quote/order.1

In the event of a change in a rate at any government level, the rate can be changed in the Tax Jurisdiction table. Products shipped prior to the change of rate will be charged at the rate in effect when the quote/order was created.

1. Choose Sales Order Entry » File Maintenance » Tax Jurisdiction [OE12].
2. Enter all tax types that you expect to require, at all levels, and their current rate.
3. Assign these tax types to individual cities, counties, provinces/states, and countries in their respective maintenance tables: Choose the appropriate table in the Administration » Regional Maintenance menu:
   * City Maintenance [MS42]
   * County Maintenance [MS46]
   * Province/State Maintenance [MS41]
   * Country Maintenance [MS43]
4. For each individual entry in a table (e.g. each province/state), select the tax code (from the Tax Jurisdiction table) and indicate if this tax should be applied in Addition to any taxes at a higher level, and if this tax should be considered Last in the hierarchy (i.e. any taxes at a lower level will not be applied). The Country table does not include the Last option because it is already the last in the hierarchy.
5. Repeat steps 3 and 4 as required for different levels and entries.

Basing Taxes on the Warehouse Location
--------------------------------------

While normally taxes are assigned and calculated based on the Ship-To address, if a customer pays or arranges the freight or pick-up of material at the warehouse, taxes should be based on the location of the warehouse instead. This requires two areas to be set up in :

* Warehouse Maintenance [IN19] - the appropriate tax code(s) for the warehouse address must be defined in the Taxes field.
* Sales Shipping Terms [OE15] - the shipping term associated with pickup/customer-paid freight (e.g. Your Truck) must have the “T” check box selected. This directs the tax code to be pulled from the warehouse definition.

Configuration


1  > Can Tax Codes be Modified at Time of Order Entry

---
