---
title: "Task Mgr Using Tk1"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Task Mgr Using Tk1 - 4GL Help Documentation"
long_description: "This topic provides detailed information about Task Mgr Using Tk1 in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---


Using the Task Manager
======================

The Task Manager displays tasks that you may need to review or approve before they can move to their next stage in . Task types are assigned to users with appropriate security, or to groups that the user may be part of.

The Task Manager must be enabled for your user ID. In addition, 4GL and/or your system administrator must configure task types and relationships, groups, etc. These configurations are described in Setting Up the Task Manager.

The Task Manager may open automatically upon login if your user ID is configured to do so1. To open it manually, click Tasks (beside the Logoff button) or enter the screen ID [TK1].

The User tab displays tasks assigned to a selected user or to a group that the user is assigned to. You can filter tasks by type of entry (TOE), and/or by who owns the task (the user, a group or both). The header area also displays the selected user's contact phone number, the user's supervisor and the dates the user is absent (if defined for the user). You may view, approve, disapprove, reassign, or edit tasks for another user if you are identified as their supervisor (or if you are granted “full control” Task Manager security)1, or if their tasks have been forwarded to you.

The Group tab allows you to view tasks for a specific group that you are a member of. If you are granted “full control” security1, you can see all group tasks even if you are not a member of the group.

The tasks will be grouped by their Feature (task type):

|  |  |
| --- | --- |
| Backorder Review | The Backorder Method switch must be set to A or N to activate this task.  When activated, if there is a backorder the salesperson on that order will receive a task notification. When they approve the task, they will be presented with all lines that were backordered AND were contained on the packing slip. For example, if there were five lines on the original order and only lines 1 and 2 were shipped on a packing slip and only line 2 had a backorder (line 1 was a complete shipment), the backorder review window would only show line 2.   * If the switch is set to A (On Approval Keep B/O Doc Open), the salesperson would have the option to create a backorder for each line or close it out. If a backorder is created the lines on the original sales order would just remain open. * If the switch is set to N (On Approval Create Doc as B/O), the salesperson would have the option to create a backorder for each line or close it out. For those lines where they want to create a backorder they can decide to either leave the original order open or move them to a new sales order. The user may want to leave the original order open if there is already a picking slip out in the warehouse for that item. This could happen if a portion of the material was picked or produced and they needed to ship that to the customer but also need to keep the original picking slip to fulfill the remaining quantities. For lines that are left open or moved, the delivery date can be modified; if automatic assignment to manifests is enabled, these lines will automatically be assigned to a manifest for the specified dates.  Refer to the following flowchart:   When approving a backorder task:   * The delivery date is blank for all backordered lines and must be populated in order to approve the task. * If the pickslip is produced it will only include the backordered lines. |
| Buyout Approval | Buyouts are used in situations where a sales order has insufficient inventory to execute, so a purchase order is automatically triggered to execute, pending approval. It allows the salesperson to seamlessly act as a reseller beyond their own stock.  An MTRNOTFOUND task may or may not be created for buyout lines that do not have MTRs2. |
| CM/DM Approval | Credit and debit memos are used to reverse the dollar value and inventory changes associated with an invoiced account. For example, customer returns can be processed via a credit memo. Only credit and debit memos processed via Credit/Debit Note Entry Maintenance [OE45] will be available for approval in the Task Manager; Quick Credit Notes [OE45A] do not require approvals so no tasks are associated with them. You will only see approval tasks for sales warehouse(s) that your security class has CM/DM Approval for.  A user must be identified as a CM/DM Manager3 in order to approve credit/debit memos, and they may or may not be able to approve CM/DMs they created4. When approving a credit note, a return slip will only print if there are inventory lines.  The override limit5 for inventory and non-inventory items must either be set to zero, or the value of the inventory (or non-inventory) lines on the CM/DM must be less than or equal to the limit value. |
| Documents Approved | Allows you to process any approvals under your own user ID/name; for example, if you don't have authority to approve $5k, after it is approved it comes back to you to send the email to the customer under your own name. |
| Intercompany Approval | After an intercompany order request (e.g. PQ) is processed, an intercompany approval task will be generated for the selling warehouse.  The approver can view/edit the intercompany sales order. The pricing of the item defaults to the average cost of the product’s inventory in the selling warehouse, but it can be edited.  If the task is approved, the Intercompany Picking Slip will be printed for the selling warehouse to fill, and an intercompany PO is created for the purchasing warehouse.  If the task is disapproved, the status of the intercompany sale order document will be “BAD”; there is no task notification to the purchasing warehouse to indicate that their request is disapproved. |
| Inventory Adjustment Approval | This is connected with the Adjustment Authorization (IN32); approval in the Task Manager will remove the request from IN32 and vice versa. |
| MTR Not Found | If you pick a log with an invalid MTR filename (in PO41), an MTR Not Found task is created. In the Task Manager comment field, if there is only one log with missing MTR the product description is shown and you can inquire on the log using the Inventory>Log Inquiry dropdown. |
| Orders Req. Credit Approval | If the customer file is set to credit hold, or their order meets any of the other credit hold criteria, the order is placed on hold and must be approved before it can be processed.  If an order is disapproved after the credit check, its status will be set to “BAD”; the order cannot be copied and must be re-entered. |
| PO Delivery Date Change | This message task will advise you if someone changed the delivery date on an incoming PO that you have a sales or OP order against. |
| Pricing Approval | If a quote or order fails configured pricing checks it will go on pricing approval hold and will not be released to the customer or warehouse. Once approved, the order/quote goes to Documents Approved status for final approval. |
| Purchase Order Approval | If you select multiple PQs and they are all the same currency, you will be asked if you want to consolidate them into one PO. If you choose Yes, you are prompted to select a vendor.  If a PQ was generated from an order, a "Buyout Approval" task must be approved before the "Purchase Order Approval" task. If you add other task types when selecting the PQs you will not be provided with the option to consolidate and you can only generate one PO from each PQ. |
| Quality Control Approval | Customers may be flagged (in AR17) as requiring an extra quality control check. Any sales orders processed for these customers are sent (after passing the credit check and pricing check) to the Task Manager in QCH status for approval.  If approved, the documents will print and the order status will change to PCK or PBP, depending on whether the warehouse is set for batch print.  If disapproved, the sales order status is set to BAD and a new order will be required.  In Order Entry, when you enter a sales order number for a document in QCH status, you will have the option to withdraw the sales order from the approval process, after which you can edit the sales order and process it again. |
| Receipt Confirmation | During Handheld Receiving if a pre-receipt record is not found after scanning the supplier label, a receipt confirmation task will be created so that the issue can be reviewed and rectified.  A receipt confirmation task is also created from PO41 if a sales order has the same product reserved as the received product on the PO. |

Task Actions
------------

Use the buttons at the bottom of the Task Manager to perform one of the following actions:

### Viewing Tasks

* View the History of the task; for example if the task is a non-system task (e.g. message task) the task can be reassigned to other individuals; if a task is reassigned then a record of this action will be logged under history.
* View the original document that the task relates to, e.g. the sales order.

### Taking Actions on Tasks

* Approve - Processes the document to the next status in its workflow.
* Disapprove - When a document is disapproved, the task will close; the document’s status is changed to BAD and a new document will have to be entered. Before the approver disapproves, they can initiate the following:
  1. The approver highlights the task and clicks NEW to send a “Review Document” type task/message to the originator with a message stating why the document was disapproved.
  2. The originator makes the edits required (right from that task notification), and sends back another “Review Document” task to the approver letting them know that the edits are complete.
  3. When the approver receives the message back that the edits are complete, they can approve the document.

Refer to the table above for consequences of Approve/Disapprove specific to a task type.

* Amend non-system tasks (e.g. message tasks) or group tasks (modify date and comments only), or Edit a document before approving it (e.g. edit on credit check will allow you to edit the sales order before releasing).
* Reassign tasks that you own (no group tasks) to another user for review. If you are granted “full control” security1, you can reassign any user’s tasks. The recipient’s security profile1 must be configured to access the task type.

* Hold - Place a task on hold, e.g. if you are working on a credit issue and you do not want anyone to release the order; click Hold again to return the task to its original status. If you try to “Approve” a task on hold, you will receive a warning message; click Submit to continue to approve the order or Cancel to leave it on hold.
* History - View previous actions taken on the selected task, e.g. who put it on hold and any comments.

### Creating a Message Task

You can create a message task related to an existing task (except message or system-only tasks), for example to have someone else take a look at one of your tasks.

1. On the User tab, select the task for which you want to create a related message task, then click New.
2. Select the Task Type. The options available are those set up for the same warehouse (or all warehouses) as the task that was selected in step 1. [since New creates a msg task only, what is the purpose of the Task Type in the Create Task dialog?]
3. Select the Recipient Type and the Recipient. The recipients list is limited to those in the same security class as you.
4. Enter the Date  and Comments explaining the task.
5. Click Save.

Configuration


1 MS32 > [operator] > Security

2  > Skip MTR Not Found Task For Buyout Lines

3 MS32 > [operator] > Options > Order Entry > CM/DM Manager

4  > Disallow Same Salesperson CM/DM Approval

5  > CM/DM Approval Manager Override Limit for Inventory Items; CM/DM Approval Manager Override Limit for Non-Inventory Items

---
