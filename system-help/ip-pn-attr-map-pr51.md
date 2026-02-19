---
title: "Plate Nest Attribute Mapping"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Plate Nest Attribute Mapping"
long_description: "Help documentation for Plate Nest Attribute Mapping in the 4GL system."
---

Plate Nest Attribute Mapping
============================

In-House Production » Nesting » Plate Nest Attribute Mapping [PR51]

This screen allows you to specify a product line, thickness or specification (grade) from  and assign it a value that will be recognized by SigmaNEST. These recognizable values come into effect when exporting inventory and work orders from  to SigmaNEST. If these values are not specified, the  will be used by default.

Product lines are mapped to materials. Grades are mapped to materials as well to cater for the scenario where SigmaNEST inventory is defined at the grade level.

Thicknesses and grades can be defined specifically for product lines, but this is not necessary. Defining thicknesses or grades for the Default line will work as well. Product line-specific attributes allow for cases where the standard thickness value for certain products does not properly represent the actual value. For example, product lines where gauges are used might have a thickness of 11 for 11GA, but the thickness is not 11”.

will use the Grade if a mapping is defined for it in PR51. If no grade is defined, it will use the Material if a mapping is defined for it in PR51. If no material is defined,  will default to the product line.

You can add, modify and delete materials, thicknesses and gauges. Deleting materials will delete all thicknesses and gauges entered against that material.

You cannot enter duplicate values for the same material.

In the following example, CPL in  is mapped to MS in SigmaNEST, and SPL in  is mapped to SS in SigmaNEST:

![](../Resources/Images/PR51_PN_attribute_map.png)
![](../Resources/Images/PR51_PN_attribute_map2.png)

---