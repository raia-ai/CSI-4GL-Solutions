---
title: "Purchasing-PO15_-_Purchase_Shipping_Terms"
source: "Purchasing-PO15_-_Purchase_Shipping_Terms.docx"
tags: ['cost', 'component', 'purchase', 'shipping', 'description', 'used', 'default', 'allow', 'terms', 'cst']
version: "1.0"
last_updated: "2025-12-03"
short_description: "PO15 Purchase Shipping Terms. This is where you define the different shipping terms that are going to be used on Purchase Orders with their cost components. Note: the fields +, Frm, To are not used anymore."
long_description: "PO15 Purchase Shipping Terms. This is where you define the different shipping terms that are going to be used on Purchase Orders with their cost components. Note: the fields +, Frm, To are not used anymore. Once a shipping term is used on a purchase order the system will not allow to change any component entered but it will allow adding a new component. This will only affect new PO’s. A default purchase shipping  is set on the Vendor Maintenance (PO11). When entering the PO (PO31) the purchase shipping term can be modified as long as there are NO detail lines."
---

## PO15 Purchase Shipping Terms

## Description

This is where you define the different shipping terms that are going to be used on Purchase Orders with their cost components.

> the fields +, Frm, To are not used anymore.

## Field Definitions

| Field | Description |
| --- | --- |
| Cst | Purchase Cost defined in PO14 |
| Cost Description | Description that will appear in cost component windows |
| Src |  |
| Opr | Operator that enters this cost “WHS” or “OFC”, blank means OFC (office) |
| Type | LNE– if cost component should be entered at the line level HDR – if cost component is for the full PO (shipping cost button on detail line) |
| Clc | Calculation Code of Purchase Cost – ex LB, LOT. This can be overridden on PO |
| Cur | Default currency when cost is a HDR cost |
| Cst Factor | Default cost factor to bring on PO |
| Ovr | Allow overwriting description on PO |
| Prn | Print this cost component on the PO |
| Hid | Hide this cost component – this goes with security on operator MS32 |
| Mnd | Cost component is mandatory |
| W | Warehouse |

## Note

Once a shipping term is used on a purchase order the system will not allow to change any component entered but it will allow adding a new component. This will only affect new PO’s.

A default purchase shipping  is set on the Vendor Maintenance (PO11).

When entering the PO (PO31) the purchase shipping term can be modified as long as there are NO detail lines.
