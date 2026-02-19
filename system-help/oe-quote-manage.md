---
title: "Managing Open Quotes"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Managing Open Quotes"
long_description: "Help documentation for Managing Open Quotes in the 4GL system."
---


Managing Open Quotes
====================

The Quote(s) Follow Up screen displays all open quotes that have a follow-up date within the range requested, even if they have expired. Here you can add remarks to a quote, view the quote details or, if you know that the customer has declined the quote, mark it as lost, which will remove it from the list.

1. To view all open quotes, choose Sales Order Entry » SO Entry/Maintenance » Quote(s) Follow Up [OE3D].
2. All open quotes are displayed with their follow-up date. Use the fields at the top to filter the list if required.
3. Select a quote and then click:
   * Inquire to view the Detail lines of the quote, from which you can drill down to the view or add remarks to Costing and Pricing Information.
   * Modify to change the Follow Up or Expiry date, or to mark the quote as lost (see below).
   * Remarks to view, edit, or add remarks about the quote

can be configured to open the Quote Follow Up screen automatically1 when you login, or to lock expired quotes2.

Identifying Lost Quotes
-----------------------

You can track any quotes that were lost, e.g. due to unacceptable delivery date, price, etc. Once marked as lost, the quote is removed from the Quotes Follow Up screen. A lost quote can be reopened.

Open the quote that was lost and select the Lost Quote Reason, then click Save.

![](../Resources/Images/SO_quote_lost.png)

You can view all lost reports on the Lost Quote Reason Report: Sales Order Entry » Order Entry Report » Lost Quote Reason Report.

Configuration


1 Operators [MS32] > Options > Order Entry > Qte Follow Up Logon?

2  > Disallow Access to Expired Quotes

---
