---
title: "Oe Inq Manifest Mn61"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Oe Inq Manifest Mn61 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Oe Inq Manifest Mn61 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Manifest Inquiry
================

This function is used to look up manifest runs.

1. Choose Sales Order Entry » Order Entry Inquiries » Manifest Inquiry [MN61].
2. Use the fields at the top to filter your search. All documents that match your criteria are listed in the table.
3. Select a manifest and open it either by double-clicking, pressing Enter, or clicking Inquire. The Inquiry opens on the Run tab, mirroring what can be seen in MN31.
4. If you select a run and press Enter, you will be taken to the Assign tab for that run. The data mirrors what can be seen in MN31, but the following values will not be displayed: Picked and Loaded weight, and Unassigned weight in the Run Items section.
5. The Documents tab mirrors what can be seen in MN31:

   * Inbound documents will not factor in received weight when calculating the ordered weight. For example, if a PO line is received (partially or completely), the ordered weight of the PO will still show in the Documents list in the Inquiry.
   * You can select a document and click Inquire to open the corresponding inquiry window.
   * If the document has been assigned to any other manifests and runs, they are listed in the Other Manifests section; you can highlight one of these and click Inquire to open a manifest inquiry window for that other manifest line.
6. On the Pick/Load tab, the logs on the selected run appear even if the run has been processed (UPD). The data mirrors the data displayed in MN31, but the Runs column in the Unassigned Logs will not be displayed.

---
