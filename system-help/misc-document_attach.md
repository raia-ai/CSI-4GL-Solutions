---
title: "Document Attach"
source: "madcap.md"
tags: ["4GL", "MISC", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Document Attach - 4GL Help Documentation"
long_description: "This topic provides detailed information about Document Attach in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the MISC module."
---
Attaching a Document to a Record
================================

The Document Attachment function allows you to attach related documents to a record so that they are accessible to other users. This function is available in many areas of the system, such as order entry, purchase order entry, etc. — wherever you see the Document button at the bottom of the form:

![](../Resources/Images/doc_attach1.png)

*Browser Version:* In order to upload generic documents to sales orders or purchase orders, you must set the “AP Document Attachments” and “AR Document Attachments” directories in IN19, for each warehouse.   
You should also set the “AR Generic Document File Path Linux” or “AP Generic Document File Path Linux” switches (in  or via MS33 > Accounts Receivable [Payable] > Additional Options) to store system-wide files associated with customers, vendors, and products.

To attach a document to a record:

1. When you are in a record, click Document.
2. Press F5 or click Add File.
3. Locate the file and click Open. The file is uploaded to SM3 and is available to anyone viewing this record.

Note that for Vendor Invoice Inquiry, to attach a document, click the button in the G column for the record that you want to attach the document to:

![](../Resources/Images/doc_attach2.png)

It's possible to import multiple generic documents which can be attached to customers or vendors; please  for assistance.

---
