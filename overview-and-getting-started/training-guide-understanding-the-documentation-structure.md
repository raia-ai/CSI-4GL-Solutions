---
title: "Training Guide: Understanding the Documentation Structure"
source: "training-guide-understanding-the-documentation-structure.md"
tags: ['SM3', 'Overview And Getting Started']
version: "1.0"
last_updated: "2026-02-19"
short_description: "Training Guide: Understanding the Documentation Structure"
long_description: "This document provides detailed information about training guide: understanding the documentation structure in the 4GL system. It includes procedures, reference information, and best practices for users and administrators."
---

# Training Guide: Understanding the Documentation Structure

This guide helps you understand the structure of the `madcap.md` knowledge base.

## Topic Structure

Each topic in the `madcap.md` file follows a consistent structure:

1.  **Header:** Every topic begins with a line starting with `# Madcap - SM3 Help-Content-...` This line contains the original file path, which includes the module.

    -   **Example:** `# Madcap - SM3 Help-Content-AP-AP21B_Vendor_Invoice_Entry.htm`
    -   **Module:** `AP` (Accounts Payable)

2.  **Title:** The main title of the topic is usually on the next line, underlined with `===`.

3.  **Content:** The body of the topic, which can include:
    -   Procedural steps (numbered lists)
    -   Reference tables (using Markdown table syntax)
    -   Conceptual explanations
    -   Links to videos

4.  **Separator:** Each topic is separated by a `---` line.

## How to Use This Structure

When you retrieve information from the knowledge base, pay attention to the header line. It gives you the **module context** for the information.

-   If a user asks about "vouchers," and you find a topic with `Content-AP` in the header, you know this topic is about **Accounts Payable** vouchers.
-   If you find a topic with `Content-OE` in the header, it might be about sales order vouchers.

This contextual information is key to providing an accurate answer.

## Key Modules

Here are the most important modules you will see in the documentation and what they cover:

-   **AP:** Accounts Payable (vendor invoices, payments)
-   **AR:** Accounts Receivable (customer payments, credit)
-   **GL:** General Ledger (financials, journal entries)
-   **IN:** Inventory (products, warehouses, stock)
-   **OE:** Order Entry (sales orders, quotes)
-   **PO:** Purchasing (purchase orders)
-   **Admin / MS:** System Administration and Controls
-   **Reports:** All system reports

Always use the module context to frame your answer.
