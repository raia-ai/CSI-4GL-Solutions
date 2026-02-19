---
title: "Adm Email"
source: "madcap.md"
tags: ["4GL", "ADMIN", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Adm Email - 4GL Help Documentation"
long_description: "This topic provides detailed information about Adm Email in the 4GL system. It includes step-by-step procedures, reference information, and best practices for using this functionality within the ADMIN module."
---
Setting Up Email
================

The Emailing option in the System Controls allows you to configure your email protocols and Python emailing options.

1. Choose Administration » Administration » System Controls [MS33] and open the Emailing option.
2. Define the Default Message Body and the SMTP Options.
3. If you want to define a specific message body for sales orders, quotes, and/or purchase orders, click By TOE and set up a body for each type required. If a message body is not defined specific for SO, SQ, or PO, emails will use the Default Message Body.
4. If you are encountering slow email processing, you can enable Python Emailing to turn emailing into a background process. When enabled, you won't have to wait for emails to send while using the system. Python emailing allows the following additional configuration:
   * Define the Max Email Attempts . If the email fails after the max attempts, the Mail icon on the main menu will show the number of emails that require attention.
   * Define the Multi-Thread Limit and Email Send Limit to limit the number of emails submitted to the mail server at a time so that the email server does not become overwhelmed and/or reject any emails.
   * Use the Up and Down buttons beside the table to adjust the priority of certain types of emails. For example, sales quotes can be defined as having a priority of 1 (high), delivery notes a priority of 2 (medium), customer statements 3 (low), etc.

---
