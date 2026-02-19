---
title: "Adm Rec Lock"
source: "madcap.md"
tags: ["4GL", "ADMIN", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Adm Rec Lock - 4GL Help Documentation"
long_description: "This topic provides detailed information about Adm Rec Lock in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the ADMIN module."
---
Viewing or Releasing Locked Records
===================================

Various Oracle and  records are locked when being edited, and are released when the user is finished with them. Sometimes a record can get stuck in locked status if the connection is interrupted, e.g. through a power failure or fluctuation, internet connection issues, etc. If you try to open a record that is in use by another user, a message briefly flashes indicating the file name that is locked:

![](../../Resources/Images/ADM_reclocks.png)

To view locked records, choose Administration » Administration » View Record Locks [RECLOCKS].

The Record Locks form displays two types of files in use: the top table displays Oracle tables and the bottom table displays  files. The *Primary Key* column displays the key of the record that is locked — typically the warehouse and document number.

If you are encountering locks while attempting to edit data in , you can use this form to see who else might be locking the record you are trying to edit.

If you are locked out of a document or even  entirely, you can start a new session and use this form to unlock (kill) the record that is locked in the previous session.

If your operator is configured with the appropriate security permission (in MS32), you can kill another user's session from RECLOCKS or from the Logged On Operators screen (RM5010S1).

Other Types of Locked Records
-----------------------------

### OE42 Locks

If any tables used during invoicing are locked and invoice is processed in OE42, invoicing will be locked until released in OE9AD or RECLOCKS.

### Generic Locks

If any tables used during manifest update or check register/update are locked and those documents are processed, they will be locked until released in MS98 or RECLOCKS.

---
