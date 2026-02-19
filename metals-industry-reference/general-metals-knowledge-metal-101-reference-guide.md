---
title: "General_Metals_Knowledge-Metal_101_Reference_Guide"
source: "General_Metals_Knowledge-Metal_101_Reference_Guide.docx"
tags: ["metallurgy", "metal properties", "alloys", "fabrication", "machining", "heat treatment", "materials science", "coatings", "manufacturing", "reference guide"]
version: "1.0"
last_updated: "2025-12-03"
short_description: "A structured, searchable reference guide that consolidates foundational knowledge on common metals and alloys. It summarizes key properties, classifications, processing methods, surface finishes, and practical selection tips for engineering, manufacturing, and procurement teams. The guide includes tables, definitions, and bullet lists to help compare materials, understand tradeoffs, and identify appropriate use cases in real-world applications."
long_description: "This Metal 101 Reference Guide is designed to provide a practical overview of metallic materials for technical and non-technical audiences. It organizes information typically scattered across datasheets, textbooks, and supplier catalogs into a single navigable format suitable for search and retrieval in a vector store. Core topics commonly include how metals are categorized (ferrous vs. nonferrous, wrought vs. cast), typical mechanical and physical properties, the impact of composition and microstructure on performance, and standard processing routes such as forming, machining, and heat treatment. Where relevant, the guide outlines common specifications and surface finishing options (e.g., anodizing, plating, coating) and discusses how each affects corrosion resistance, wear, and aesthetics. Decision-support content such as comparative tables, pros/cons lists, and rules of thumb are highlighted to assist with early material selection. Definitions, abbreviations, and frequently asked questions are called out for quick reference. The document’s intent is to accelerate onboarding, harmonize terminology across teams, and reduce time spent searching for basic material information, while preserving the original document’s structure, lists, and tables in clean, UTF-8 compliant Markdown."
---

**Title: ** **Metal 101**** -**** Reference Guide**
**Description: **This document provides a foundational overview of metal classifications, shapes, finishes, grades, and ASTM specifications. It is intended to assist in understanding what data structures and fields may be needed in 4GL for comprehensive support of the metal industry.
## **1. Metal Shapes (Forms/Profiles)**
These define the physical configuration in which metal is processed and sold. Common shapes to account for:

| Shape | Description |
| --- | --- |
| Flat Bar | Rectangular bar with square edges |
| Round Bar | Cylindrical solid rod |
| Square Bar | Solid bar with square cross-section |
| Angle | L-shaped section, equal or unequal legs |
| Channel | U-shaped section (C-channel, U-channel) |
| Beam | Structural profiles like I-beam, H-beam |
| Pipe | Hollow round section, specified by schedule |
| Tube | Hollow section, round/square/rectangular |
| Plate | Flat steel 1/4" thick or more |
| Sheet | Thin flat metal, less than 1/4" |
| Coil | Rolled metal sheets or strips |
| Wire Rod | Coiled wire in round form |

**2. Metal Grades (Material Composition)**
Grades indicate the chemical composition and properties of a metal. They vary by metal type (e.g., carbon steel, stainless, aluminum):

| Type | Example Grades | Notes |
| --- | --- | --- |
| Carbon Steel | A36, 1018, 1045 | Common for structural and machine parts |
| Stainless Steel | 304, 316, 410 | Resistant to corrosion, used in food/medical |
| Aluminum | 6061, 5052, 2024 | Lightweight, corrosion-resistant |
| Alloy Steel | 4140, 4340 | Enhanced mechanical properties |
| Tool Steel | D2, A2, O1 | High hardness for tooling applications |
| Galvanized | A653 | Zinc-coated for corrosion protection |

**3. Finishes (Surface Condition)**
Surface finishes impact appearance, corrosion resistance, and secondary processing:

| Finish | Description |
| --- | --- |
| Hot Rolled (HR) | Smooth finish, lower cost, rougher |
| Cold Rolled (CR) | Smooth surface, tighter tolerances |
| Pickled & Oiled (P&O) | Scale removed, lightly oiled |
| Polished / Mirror Finish | Smooth, reflective surface |
| Galvanized | Zinc-coated for corrosion protection |
| Mill Finish | As produced, no additional finishing |

**4. ASTM Specifications**
ASTM (American Society for Testing and Materials) defines standardized specs:

| ASTM Spec | Description |
| --- | --- |
| A36 | Carbon structural steel |
| A572 | High-strength, low-alloy structural steel |
| A240 | Stainless steel plate/sheet |
| A500 | Cold-formed welded and seamless tubing |
| A513 | Mechanical tubing |
| A106 | Seamless carbon steel pipe |
| B209 | Aluminum plate and sheet |

## **5. ERP Field Recommendations for 4GL Configuration**
To capture the above properly in 4GL or any ERP system, the following fields or data tables are suggested:
- Product Shape (Dropdown or Code)
- Material Type (Carbon, Stainless, etc.)
- Grade (With standard mapping to Material Type)
- ASTM Spec (Linked to Grade and Shape)
- Finish (Selectable, based on Shape + Grade)
- Dimensions (Length, Width, Wall Thickness, OD, ID, etc.)
- Unit of Measure (Each, Foot, Pound, Ton)
- Processing Compatibility (e.g., Nesting allowed, Plate Burnable)
