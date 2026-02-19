---
title: "In Barcodes Create"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "In Barcodes Create - 4GL Help Documentation"
long_description: "This topic provides detailed information about In Barcodes Create in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Creating Barcodes for Bin Locations
===================================

1. Download the Code128 font to C:\Windows\Fonts.
2. Run the Warehouse Location Listing (IN29), output to screen (LPS), to get a list of all current bin locations. You will need the Type column and Location columns; the Location Description is not needed for barcoding purposes.
3. Copy each bin location and paste them on individual lines in a Word document. Add a description below each bin location so you know what it is. [why? in the previous step it says the description is not needed? what is an example of description (example below should show this)? is it recommended this Word file be saved for future use, or is this a one-time thing?]  
   F123  
   F124  
   F125
4. Add asterisks (\*) to the beginning and end of each bin location:  
   \*F123\*  
   \*F124\*  
   \*F125\*
5. Highlight the bin location lines and change the font to the Code128 font in the Windows/Fonts folder.  
   ![](../Resources/Images/barcode.png)

---
