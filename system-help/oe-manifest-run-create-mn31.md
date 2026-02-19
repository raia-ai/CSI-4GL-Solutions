---
title: "Managing Manifest Runs"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Managing Manifest Runs"
long_description: "Help documentation for Managing Manifest Runs in the 4GL system."
---

Managing Manifest Runs
======================

The Manifest/Load Planning feature facilitates the manifest and load planning process to manage runs. A run represents an outbound truck which will be delivering or picking up material to or from a customer or supplier. Information captured on each run may include the driver's name and mobile phone number, truck description and maximum weight, departure time, etc.

The manifest system is driven by day: runs will be created, documents scanned, and documents assigned to runs for a particular day.

If automatic assignment to the manifest is enabled1, when a sales order goes to PCK status it will be added to the manifest based on the required date on the order lines (creating a manifest if one doesn't already exist for that date).

If the route on an order matches the route of a default run2, the order lines will be automatically assigned to that run, provided it's the only run associated with that route. If there are multiple runs associated with the route on a document, you must manually assign the document to a run. The manifest run for branch transfers will use the route code from the destination warehouse customer.

The high-level process is as follows:

1. Retrieve the documents (orders, purchase orders, processing POs etc.) that represent the material to be delivered or picked up on that day.
2. Assign the material (document line level) to a run. You can assign a partial line item, e.g. to break up a larger weight line item across multiple trucks.

   As data changes, you can click the Refresh icon ![](../Resources/Images/i_refresh.png) at the bottom of any tab to refresh the page results. The time the data was last built is also displayed.
3. After the material has been picked/processed in the warehouse, generate the loading report for each run that includes the details of the material allocation.
4. Warehouse operator uses the loading report and the handheld Manifest Load Confirmation to scan the material as it is loaded onto the truck.
5. Process the run to generate all the shipping paperwork including packing slips, MTRs, and run sheets.

ensures that the loaded material coincides with what was physically picked against a particular run.

Manifests can be searched and reviewed in the Manifest Inquiry screen [MN61].

Creating or Managing a Manifest
-------------------------------

1. Choose Sales Order Entry » SO Entry/Maintenance » Manifest / Load Planning [MN31].
2. Clear the Run Date filter on the left to see all open manifests, or enter a run date to view, or click New to create a manifest for a different date3.

You can choose to view manifests for ALL warehouses, but you cannot enter a Document number or click New until you select a specific warehouse.

3. The Runs tab displays any default runs2 but you can also create a new run here for this date. When you select a run on the left, its run info is displayed and editable on the right (changes are not updated in the template). The Route field will only display those assigned to the same warehouse as the manifest as well as routes that are not assigned to a warehouse. Select Omit Pick Slips for a run to skip that run when printing picking slips from the Process page; this may be set by default2 but can be overwritten for a run. The Assigned, Picked, and Loaded weights will update as document lines are assigned and loaded to a run throughout the day. Optionally click Document to attach a generic document to the manifest; for example, the run summary with the signature of the person who loaded the truck, the run sheet with the customer's signature or the driver's “arrived” and “departed” times, etc. You cannot delete a run if documents are assigned to it; they must be removed on the Assign tab first.
4. The Documents tab displays all orders assigned to this manifest. Line items from these documents will be available to assign to runs on the Assign tab. If automatic assignment to the manifest is disabled1, you must manually add the orders to a manifest. Your options here include:
   * In the Document Id field, scan or input the document numbers to add.
   * Click … to open the document selection screen where you can search and filter documents that have not been assigned to a manifest. If you select a Run ID before selecting a document it will automatically assign the document to that run. The Total Weight in the top right corner reflects all documents that match the selection criteria; to see the weight of one or more documents, select them and click Total.
   * Select a document in the list and click Inquire to view the source document (e.g. the sales order).
   * To add an item that does not have a corresponding document (e.g. a customer appreciation promo gift), click Misc Doc to create a “dummy” document and input the customer, route and weight. These miscellaneous documents are identified as XX document type, and are loaded automatically as they are assigned to a run.
   * To create miscellaneous documents from other documents in  (e.g. sales orders and delivery dockets), click Generate Misc. Change the Manifest if necessary, and select the Run if you are ready to do so. Select the Source Document: this document can be from a different warehouse than the manifest. When you click Save, a miscellaneous document will be created for each “package” that was originally created on the source document, i.e. delivered on the delivery note or picked against the order. Packages could either be logs, packages, or multi-part packages. The miscellaneous document will include a Scan field containing the value of the package's barcode.  
     These generated miscellaneous documents are identified as XD document type, and are NOT loaded automatically as they are assigned to a run.

   These miscellaneous documents may also be generated outside of a manifest via MN34.
   * To remove a document from this day's manifest, select it and click Delete. You cannot delete a document if any of its line items have been picked or loaded for a truck; the items would have to be unloaded first (on the Pick/Load tab).

   An order document may appear on multiple manifests if its line items have different required dates. The Assign tab will only display the line items to be shipped on that date.
5. The Assign tab is used to assign line items to runs. The Unassigned Items table displays any document lines (from those on the Documents tab for this manifest) that have not been assigned to a run.
   * Select a Run ID from available runs on this day. The selected run may already contain documents that were automatically assigned when the order was processed (see Tips above).
   * Select an unassigned item and click Assign to assign it to the selected run. The maximum weight defined for the truck will be highlighted in red. While you can assign greater than the maximum weight, you will not be allowed to process a run that has more than the maximum weight loaded.
   * To remove an item from a run and make it available to assign to a different run, click Unassign. You cannot unassign an item if it has been loaded on a truck; the item would have to be unloaded first (on the Pick/Load tab).
   * To move an unassigned item to a different manifest, select it and click Move, then select the manifest it should move to.
   * If you have assigned logs to a run and later assign the corresponding order line to a different run, the logs will be also be reassigned to the new run.
   * You may need to split a line item onto different runs, e.g. if the weight exceeds the truck maximum: select the line item, click Assign Partial, and enter the quantity to be assigned to the selected run. The document line is added to the Run Items table, but the line with the updated quantity also remains in the Unassigned Items table; both lines include a “P” indicating that it has been partially assigned.

   You can reassign a document line from one manifest to another: On the Assign tab, select the Run ID and then scan a document into the Scan field. The line will be assigned to the selected run, even if it has no logs picked or was previously assigned to another run (unless it has been loaded, is closed, or belongs to a different warehouse).  
   A magnifying glass icon at the bottom left of the Unassigned and assigned Run Items sections allows you to open the inquiry window for the selected item (there is no inquiry for miscellaneous documents).
6. The Pick/Load tab is used to manage quantities that have been picked against a document in the manifest, e.g. in Picking Confirmation [OE41] or the handheld Picking Confirmation or Package Maintenance. When items are picked the weight could change from what was ordered, so this tab allows you to review and manage the picked weights by run. When a line item is picked in OE41/WF11 and has only been assigned to one manifest and run, the log will automatically be picked against a run. If a line item is split over multiple runs, the log will not be automatically picked and you will need to manually pick the log onto a run.

See below for information about picking or assigning packages.

The Pick/Load tab also reflects when line items have been loaded onto the truck via the handheld Manifest Load Confirmation (in the Loaded column). You cannot load packaged logs unless all the logs from the package are on the same run. If a log is added to a package after the log was loaded, the log will be unloaded.

Any generated miscellaneous docs must be manually loaded on this tab: scan the original package label to load confirm the misc document that was created from that package.

7. The On Hold tab displays any orders that have not yet reached the picking stage (PCK status), or that have unreleased picking slips but are currently awaiting some kind of approval (e.g. Quality, Credit, Pricing). This information provides some insight as to what orders will most likely need to be incorporated into the planning process.
8. Review the Runs tab through the day to monitor each run's Assigned, Picked, and Loaded weights.
   * When the run is fully picked and ready to load: click Process, select the Run Id, enter “R” and select the Loading Report (see below for details). Provide this to the warehouse who will use it and the handheld Manifest Load Confirmation to load the truck. The load progress is updated on the Runs tab in real-time.
   * When the run is fully loaded:
     + If you want to generate reports, click Process select the Run Id, and enter “R”. You can produce a Run Sheet (a summary at the order header level of what's on the truck, to be signed by the customer as proof of delivery) and Picking Slips if necessary. You can also select the Run Summary to export a summary of all runs (at the truck level) to an Excel spreadsheet—you can generate this while selecting other reports or click the button at the bottom of the Process Document page at any time.

     To print picking slips for all runs, click Picking Slips at the bottom of the Process Document page. This will release all order lines that are assigned to unprocessed runs that are in PBP status for the whole manifest. Picking slips will not print for any run that has the Omit Pick Slips check box selected on the Runs tab.
     + If you're ready to finalize the run, click Process and enter “P” to process it. For sales orders, branch transfers, consignments and outside processing documents, this processes the document from picking confirmation. It also generates the final shipping paperwork to accompany the delivery: packing slip, MTRs, and run sheet.

     You can select a previously processed run to reprint the run sheet or delivery notes.

     You will not be able to process the run if any packages are partially assigned; use View Packages to review the package assignments. If processing is interrupted for a run, its status will be PAR and the documents are locked until the processing is restarted and completed.  
     A warning may appear4 if reserved logs have zero picked quantity.

Managing the Order in which Items are Loaded and Delivered
----------------------------------------------------------

When a document is assigned to a run, the ship-to address is added to a list of a drops. Each drop has a sequence to indicate the order in which the drop will be performed on the run.

To view or change the drop sequence, on the Assign tab click Drop Seq. You will see the list of addresses with their drop sequence on the right. You can change the sequence but you cannot introduce a gap or enter duplicates or zeros. Click Save.

If all documents in a manifest sharing the same delivery address are removed from a run, the drop is removed from the list of available drops. The sequences of the remaining drops are updated (to remove gaps in the sequence) but the order remains the same.

If the shipping address of an order is changed, a drop is added for the new address if it is unique to the run. If a delivery address is unused, the drop for that address will be removed from the run. Similarly, for POs, if you modify the ship-from info on the vendor, this will update drops for all POs that reference that vendor ship-to.

The loading report is sorted in reverse drop order, so that the last drop items are loaded on the truck first, and the first drop items are loaded last.

Picking and Assigning Packages
------------------------------

* From the Logs subtab on the Pick/Load tab:
  + If a sales order log belonging to a package is assigned to (or unassigned from) a run, all other logs belonging to the same package will be automatically assigned to/from the run.
  + If the load status for a log belonging to a package is toggled, the load status for all other logs belonging to the same package will be automatically toggled.
  + You can assign packaged logs to a run even if the entire package is not yet on the manifest; however, you cannot load packaged logs until the entire package has been assigned to the run.
* From the Packages subtab on the Pick/Load tab:
  + If a package is assigned to (or unassigned from) a run, all the logs belonging to that package will be automatically assigned to/unassigned from the run.
  + You can assign a package to a run even if the entire package is not yet on the manifest. It will only assign the logs that are available on the current manifest. However, you cannot load packaged logs until the entire package has been assigned to the run.

To view packages with logs assigned to the current, or all, runs, click Packages on the Pick/Load or Assign tab. If the package contents have been assigned to multiple runs, a red X will be shown in the Asg column.

What's On the Loading Report?
-----------------------------

The loading report is used by the warehouse staff to load the truck (and confirm the loading with the Manifest Load Confirmation). It shows exactly which products are to be loaded and where to find them:

* Grouped by drop, presented in descending order, with the address for each drop only showing once.
* One line per package; for multi-packs, one line will show per sequence but the product descriptions and quantities will show on the first sequence.
* Bin location, log number, package ID, package type (bundle, skid, etc.)
* The item description will be a concatenation of the product descriptions of all unique product codes. For example, if you have 20 order lines that belong to the same product code but only the length varies, the report will only show one product description.
* The quantity shows the quantity of the pack (total of all logs in pack).
* Assigned outbound lines with no logs picked show the current ordered pieces.

The Loading Report can be reprinted, from the manifest process tab, with the same data as the original report. You can select the documents you want to reprint (except the Picking Slip).  
The Manifest Loading Summary Report [MN71] is an Excel report that can include multiple runs, including completed runs, from one or more routes. You can choose the regular detailed report or a summary that prints one row for each document as well as the freight cost of the selected cost code and the margin and margin% of the invoice.

Recording Trip Times for Drops
------------------------------

You can go into a manifest run after it has been processed to enter the trip times for each customer delivery.

1. Choose Sales Order Entry » SO Entry/Maintenance » Manifest Drop Time Tracking [MN32].
2. Enter or select the Date of the manifest or enter the Manifest number, then select the Run.
3. All the drops for that run are listed. Enter the Trip Start and Trip End times for each drop.
4. Optionally, click Inquire to view the manifest.

The trip start and end times are displayed on the Manifest Loading Summary Report [MN71].

Configuration


1  > Manifest Automatic Routing

2 Manifest Run Template Maintenance [MN33]

3  > Allow Multiple Manifests for a Day; if this switch is enabled, multiple manifests may be created for the same date; if switch is disabled, “New” button is disabled if there is already a manifest for the day

4 MS32>Options>OE>Additional Options>Warning If Used Logs Not Picked:  
- If set to “N” (no warning) - the order is processed without any warning  
- If set to “S” (soft warning) - a message will appear but the order can be processed.  
- If set to “H” (hard warning) - a message will appear and the order cannot be processed.

---