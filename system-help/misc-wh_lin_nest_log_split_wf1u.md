---
title: "Wh Lin Nest Log Split Wf1U"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Wh Lin Nest Log Split Wf1U - 4GL Help Documentation"
long_description: "This topic provides detailed information about Wh Lin Nest Log Split Wf1U in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Linear Nesting Log Split
========================

Log splits driven from linear nesting documents. When linear nesting documents are created from the import/nest function during order entry, the order will be linked with the nesting document.

1. From the linear nesting project document, scan the barcode of the nest section to be cut.

   You may be prompted to enter the elapsed time taken for the job; see Time Tracking.
2. Scan the log that you are cutting. You may be warned1 if the log was not picked for the project.  
   The Pcs field is populated from the nesting production order; the lines below reflect each order to be fulfilled by this nest section. If the drop is to be returned to stock (RTS Length on the production order), a separate line will show the RTS piece. If there is no
3. Optionally, create a shipping label for each order [how/where?].
4. [copy step 6 from Log Split or not because the scrap tolerance is not decided at this stage bc it's decided as part of the nesting project?]

Configuration


1 SWTMNT > Check for Picked Logs in Linear Nesting Log Split

---
