---
title: "Linear Nesting During Order Entry"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Linear Nesting During Order Entry"
long_description: "This topic provides detailed information about Linear Nesting During Order Entry in the 4GL system."
---


Linear Nesting During Order Entry
=================================

This function allows you to nest selected line items on an order, or import line items into a new sales order and nest them at the same time. Nesting projects created in this way are linked to the order and can be viewed during order inquiry (on the Reserves tab).

You can also create a linear nesting job from documents already in .   
Use the Linear Nesting Production Inquiry [IN6H] to view the status of linear nesting projects.

1. Prepare your Excel spreadsheet [recording says it's “similar to the regular excel import” - is it actually the same, generated via OE3Q?]. Make sure you have at least populated the Product or Pseudo Code, Length, SUM Quantity, Primary Process; optionally enter a Group to group lines into different nesting projects.
2. Create a new sales order.
3. On the Details tab, click ![](../Resources/Images/i_arrow_down.png) and then click Nest.
4. Select the Data Source: the selected order lines or import from Excel. If you are importing, click the File icon to retrieve the spreadsheet.
5. When prompted, enter or select the Machine Code that you will be using to cut the product. In the Nesting Requirements window, a line is created for each group from the spreadsheet. For each group you can:
   * Select a different machine to be used.
   * Click + in the D column to view the details:
   + To see the order requirements for individual lines, click … beside the first Pieces number to display the “Cut To” Details window. The lengths from the original documents are converted to a common unit. Each line is selected for inclusion in the nesting project; if you decide you want to exclude a line, clear the S check box. You can also add another line, e.g. if you want to create additional pieces for stock. Click Close to return to the Linear Nesting Requirements window.
   + To see the inventory to be considered, click … beside the second Pieces number to display the “Cut From” Details window. This shows all inventory of the product. Each log is selected, meaning  can consider using any of the logs when processing the nesting project, but you may be able to reserve specific logs for the nest1. If you prefer to select logs manually, e.g. to use up your smaller lengths, click Unsel All and then select the logs to be considered. You can add another line, e.g. if there is product incoming that you want to be factored into the nesting algorithm. [there's no Close button - click Cancel to return? or F3 only?]* Select the S check box for each product you want to process, then click Process.
6. performs the nesting and displays the groups in separate nesting projects in the Import and Nest Project Maintenance window. Click + in the D column to view the cutting schedule for the group. This window displays the log(s) that will be used, how many pieces of each will be cut, and any drop left over.
   * If you want to ship the drop to the customer, select the S check box; this will add a line to the order for the drop.
   * If you want to return all or a portion of the drop to stock, change the Drop value to what you want to remain as scrap (or ship to the customer); the balance of the original drop is added to the RTS field. For example, if a calculated drop is 13.75 and you want to return a 10 inch piece to stock, change the Drop to 3.75. The RTS field will show 10.
   * The customer may be charged1 for the scrap whether the drop is being shipped to the customer or not, but they will not be charged for any pieces returned to stock.
   * Click Preview to view the Production Order document; the operator will use this document and the handheld Linear Nesting Log Split function to cut the logs.
   * Click Close to return to the Project Maintenance window where you can select a different group to view the details for.

   If you want to view a nesting summary of all of the groups/projects, click the ![](../Resources/Images/i_excel.png) in the Project Maintenance window. The nesting summary will display the feed pieces, feed material, feed length, scrap, RTS, scrap %, cutting pieces, cutting length, gross quantity and IUM, and will print the total gross quantity for each project. It will also print the processing totals at the bottom of the report; these include the process along with the pricing quantity.
7. When you are ready, click Process. All of the order requirements from the selected nesting lines are added as line items on the Details tab of the order. If configured2, the Pricing Qty field takes into account any scrap being charged to the customer. Raw materials on IP orders may be costed using average cost or replacement cost3.
8. If you specified grouping of the line items in the nesting project, when you open a line item you will see the group in the Form Group field. If the Form Grouping field on the Header tab is set to **G**roup, when you preview the order you will see one price for each group.

If the “Print Nesting Summary When Previewing In Order Entry” switch = “Y”, clicking the Preview button in OE31 will print a Nesting Summary report to Excel in addition to the sales order preview to PDF. If the switch = “N”, clicking the Preview button in OE31 will only print the sales order preview to PDF.

When a sales order is processed in OE31, or released in OE3L if batch printing is turned on, or approved from credit approval in the Task Manager, the linear nest production order for each nesting document that belongs to the sales order will print with the picking slips, based on the form printer options in IN19 for form 57.

Configuration


1 If  > Linear Nesting by Product Availability = “Y”: the list includes cut products as well; or “L”: same as “Y” but also enables selection of individual logs to be reserved for the nest. In the case of a linear nest log split, the reservation would be removed from the log that is being split.

2 [is this referring to this switch?:] > Scrap Revaluation for Inhouse Production

The scrap value is calculated from the inventory based on the average or actual cost depending on the costing method of that product. The cost code is defined in   > Linear Nesting Scrap Allocation Code

3  > Processing Raw Material Costing Method

---
