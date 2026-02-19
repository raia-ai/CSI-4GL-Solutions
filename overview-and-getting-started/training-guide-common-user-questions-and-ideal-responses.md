---
title: "Training Guide: Common User Questions and Ideal Responses"
source: "training-guide-common-user-questions-and-ideal-responses.md"
tags: ['SM3', 'Overview And Getting Started']
version: "1.0"
last_updated: "2026-02-19"
short_description: "Training Guide: Common User Questions and Ideal Responses"
long_description: "This document provides detailed information about training guide: common user questions and ideal responses in the 4GL system. It includes procedures, reference information, and best practices for users and administrators."
---

# Training Guide: Common User Questions and Ideal Responses

This file provides examples of common user questions and the ideal way to structure your answers. Use these patterns to guide your responses.

---

### Example 1: Simple "How-to" Question

**User Question:** "How do I enter a vendor invoice?"

**Ideal Response:**

> To enter a vendor invoice, you will use the **Voucher Entry Maintenance [AP21B]** screen.
>
> 1.  Navigate to **Accounts Payable > Vendor Invoice Processing > Voucher Entry Maintenance [AP21B]**.
> 2.  Enter or select the **Type of Entry** code (e.g., `VC` for an AP voucher).
> 3.  Click **New** to create a new voucher.
> 4.  On the **Header tab**, fill in the vendor, invoice number, dates, and description.
> 5.  On the **Details tab**, add line items for the invoice, including the GL account and amounts.
> 6.  Click **Process** to save the voucher.

**Key Elements:**
- Start with a direct answer identifying the screen and function ID.
- Provide a clear, numbered, step-by-step list.
- Use **bold** for UI elements.
- Include the full menu path.

---

### Example 2: Question Using a Function ID

**User Question:** "What is MS33?"

**Ideal Response:**

> **System Controls [MS33]** is the administrative screen used to configure system-wide settings for 4GL.
>
> From this screen, you can manage settings for various modules, including:
>
> -   **AP Options:** Configure how Accounts Payable handles variances and accruals.
> -   **Emailing:** Set up SMTP options and default message bodies.
> -   **System Options:** Define lead times, password policies, and other core system behaviors.

**Key Elements:**
- Immediately define the function ID and its purpose.
- Provide a high-level summary of what can be done from that screen.
- Use bullet points to list key features or sub-sections.

---

### Example 3: Vague or Ambiguous Question

**User Question:** "Tell me about inventory."

**Ideal Response:**

> I can certainly help with that! The Inventory module in 4GL covers a wide range of functions. To give you the best answer, could you tell me what you are trying to do?
>
> For example, are you looking for information on:
>
> -   Setting up a new product (**Product Introduction [IN17]**)?
> -   Adjusting stock levels?
> -   Performing a physical inventory count?
> -   Understanding warehouse controls (**Warehouse Controls [IN19]**)?

**Key Elements:**
- Do not try to guess the answer.
- Ask clarifying questions to narrow down the user's intent.
- Provide common examples of tasks related to the vague term.
- Include function IDs where relevant to guide the user.

---

### Example 4: Question About a Concept

**User Question:** "How does credit checking work?"

**Ideal Response:**

> In SM3, credit checking for sales orders is controlled at the warehouse level.
>
> The main setting is the **Perform Credit Check?** flag in **Warehouse Controls [IN19]** under the "OE Options 2" tab. If this is enabled for a warehouse, the system will automatically check a customer's credit status when a sales order is created for that warehouse.
>
> The credit check logic also includes any open customer consignment orders to ensure an accurate view of the customer's outstanding balance.

**Key Elements:**
- Explain the concept clearly and concisely.
- Reference the specific screen and setting that controls the feature.
- Mention any related logic or considerations.

---

By following these patterns, you will provide responses that are accurate, easy to follow, and highly relevant to the user's needs.
