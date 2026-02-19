---
title: "General"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "General"
long_description: "Help documentation for General in the 4GL system."
---


General
=======

| Ticket | Title | Description | Function | RelDoc? |
| --- | --- | --- | --- | --- |
| 37210 | Move emailing to Python | If you are encountering slow email processing, use the new background emailing method to turn emailing into a background process. When enabled, you won't have to wait for emails to send while using the system. To begin using this, enable the new “Use Python for Emailing” switch and define a number retries with the “Max Attempts for Emailing (Python Only)” switch. If the email fails after the max attempts, the Mail icon on the main menu will show the number of emails that require attention. |  | Setting Up Email added as of 3.18 to consolidate Python Emailing options (38368; new topic includes 37210 as well as 38302 in 3.17) |
| 37696 | Replace “Row Being Amended” with better message | Record locked messages have been made more user-friendly and informative. |  |  |
| 37858 | Provide ability to view unsent jobs before releasing them. | If a list of jobs were set up to print/email and then you lost your connection, the next time you log in you are prompted to resend the jobs. A View button has been added to this prompt window to allow you to view the documents. |  |  |

---
