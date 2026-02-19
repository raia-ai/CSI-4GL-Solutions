---
title: "Ap Refund Customer"
source: "madcap.md"
tags: ["4GL", "AP", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Ap Refund Customer - 4GL Help Documentation"
long_description: "This topic provides detailed information about Ap Refund Customer in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the AP module."
---
Refunding a Customer
====================

1. In AP do a direct check (AP21B\_D) for a Cash vendor touching 9999-00 (clearing account).
2. On the Heading tab:
   * Overwrite name and address
   * Enter credit refund information in description
   * If you need more description, press F4 on the … to open remarks
   * Select payment type C – check
   * In invoice# enter the customers c/n#
3. On the Details tab:
   * Delete GL default accounts
   * Click Add item:
     + Select dummy-clearing account
     + Enter check amount
     + In the Description field, enter a note such as “Refund CR#123”.
4. Click Process. This will automatically link to the print check (AP3661).
5. Check Register and Update (AP37), then Post.
6. Go to the GL and enter a J journal to reverse (credit) the amount out of 9999-00 and close off the AR C/N (GL31). You can close off the credit note directly here or create an open transaction in AR.
   * To create an open transaction, stop here. You can apply the open transaction in AR33.
   * To close off the credit note, click E Applications and select c/n. Be sure to enter the proper “to be applied”.

---
