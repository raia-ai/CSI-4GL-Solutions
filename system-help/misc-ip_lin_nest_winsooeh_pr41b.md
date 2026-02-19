---
title: "Ip Lin Nest Winsooeh Pr41B"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Ip Lin Nest Winsooeh Pr41B - 4GL Help Documentation"
long_description: "This topic provides detailed information about Ip Lin Nest Winsooeh Pr41B in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Linear Nesting from Existing Documents
======================================

Linear nesting allows you to optimize cutting of long products to minimize scrap, for example when many pieces of the same product are required but of different lengths.  will analyze the order requirements against the inventory and identify which inventory pieces should be used and where they should be cut.

You can create a linear nesting job from documents already in , as described below, or you can import line items into a new sales order and nest them at the same time.

Use the Linear Nesting Production Inquiry [IN6H] to view the status of linear nesting projects.

Linear Nesting by Document
--------------------------

1. Choose In-House Production » Nesting » Linear Nesting by Document [WINSOOEH].
2. Select the Machine process that you will be cutting the material on; this determines the kerf and squaring allowance.
3. Select the document, e.g. a sales order. You will only see the line items that are long products associated with the selected machine process. Select the line item(s) that you want to include in this linear nesting project.
4. Repeat as necessary to add other documents.
5. Click Submit. The Linear Nesting Requirements window opens; continue as in step 5 below to complete and process the nesting job.

Linear Nesting from the Production Schedule
-------------------------------------------

1. Choose In-House Production » Sales Order Controlled » Production Schedule [PR41B].
2. Select the machine Process, and optionally any other filters as required.
3. Sort the documents by Raw Material.
4. Select the lines that you want to include in the nesting project (these can be for different customers and different products) and click Lin Nest.
5. In the Nesting Requirements window, the lines are grouped by product:

* To see the order requirements for individual lines, click … beside the first Pieces number to display the “Cut To” Details window. The lengths from the original documents are converted to a common unit. Each line is selected for inclusion in the nesting project; if you decide you want to exclude a line, clear the S check box. You can also add another line, e.g. if you want to create additional pieces for stock. Click Close to return to the Linear Nesting Requirements window.
* To see the inventory to be considered, click … beside the second Pieces number to display the “Cut From” Details window. This shows all inventory of the product. Each log is selected, meaning  can consider using any of the logs when processing the nesting project. If you prefer to select logs manually, e.g. to use up your smaller lengths, click Unsel All and then select the logs to be considered. You can add another line, e.g. if there is product incoming that you want to be factored into the nesting algorithm.

6. In the Nesting Requirements window, select the S check box for each product you want to process, then click Process.
7. Optionally change the generated Project Name, then click Submit to create the nesting job.
8. The Linear Nesting Cutting Schedule window opens. This window displays the log(s) that will be used, how many pieces of each will be cut, and any drop left over. Click Process.
9. Enter C to print or view the linear nesting project report. The report includes the following sections:

* Cut To List - the order requirements by document
* Cut From List - all inventory that was included in the algorithm and which pieces were selected
* Cutting Schedule - how the selected pieces will be cut; for lines that involve multiple pieces, remember that the cuts refer to each of those pieces. In the following example, we are using 7 x 156" pieces of the first log. Each piece will have one cut, resulting in a 60" piece and a 96" piece. For the second log, we are using 1 piece, making one cut to get a 96" piece and a 37" drop (at 27.82% scrap).

![](../Resources/Images/IP_linear_nest_PR41B_rpt.png)

Nest by Dimension button - need info - I'm not clear how this fits into the workflow - is this done instead of any step above? Or direct me to a document that I can use to test for myself  
BG testing notes:  
When nesting rebar log numbers are not useful. They would like the nesting to be driven by length instead of being driven by log number. Give them an option to choose by length or by log in the 'create project' stage of linear nesting. The section at the top would have one line per unique length and the section at the bottom would have one section per length per order number.  
Testing Notes  
Perform a linear nesting in PR41B, PR42B or WINSOOEH. You will need a sales order with an i-line for a cut product with a machine on the line. In PR41B/PR42B you will select the order line and click on lin nest/nest. When the window appears, choose to nest either by log or dimension. You will need to perform this test for both and compare. select the logs you want to use for the nest, then click the checkbox at the far right to select the line for nesting. process it, then continue through the confirmation window that follows. Print the report to pdf. When nesting by dimension, the report should show a consolidated version of the cutting schedule. Verify this by comparing with the log version.

Other functions in the Nesting menu to be documented somewhere/maybe (?):

* IN3F - Linear Nesting Project Maintenance - Logs button allows you to delete logs picked for the project
* PLMPNI01 - Create PLM Import File From Project
* PLMPNI02 - Create PLM Import File From Order
* PR52 - Download Receipt to ProNest
* PR56 - Download Log to ProNest
* PR53 - Upload Nest to SM3
* PR54 - Takeon Pronest Inventory
* PR55 - Validate Pronest vs. SM3 Inventory
* PR57 - Plate Nest Integration - Inventory (briefly mentioned in Plate Nesting with SigmaNEST) - When exporting a log to SigmaNEST, the first three specifications on the log are stamped on the SigmaNEST stock item as SheetData2, SheetData3 and SheetData4

---
