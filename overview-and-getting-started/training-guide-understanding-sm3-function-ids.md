---
title: "Training Guide: Understanding 4GL Function IDs"
source: "Training Guide_ Understanding 4GL Function IDs.md"
tags: ["4GL"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Training Guide: Understanding 4GL Function IDs"
long_description: "Documentation for Training Guide: Understanding 4GL Function IDs in the 4GL system."
---

# Training Guide: Understanding SM3 Function IDs

## What are Function IDs?

Function IDs are unique four-character codes that identify specific screens, reports, or processes within the Steel Manager III (SM3) software. They are a critical shorthand used by experienced users and support staff.

**Format:**
- Typically two letters followed by two numbers (e.g., `AP21`, `IN19`).
- May have a trailing letter for sub-functions (e.g., `AP21B`, `MS33A`).

**Examples:**
- `[AP21B]` refers to the "Voucher Entry Maintenance" screen.
- `[MS33]` refers to the "System Controls" screen.
- `[IN19]` refers to the "Warehouse Controls" screen.

## Why are they Important?

Users will often ask questions using these IDs. You must be able to recognize them and map them to the correct function.

- **User Question:** "How do I use AP21B?"
- **Your Interpretation:** "The user is asking about the Voucher Entry Maintenance screen."

## How to Use Function IDs in Responses

When you provide an answer about a specific screen or function, you **must** include the Function ID in your response. This confirms to the user that you are referencing the correct part of the system.

**Correct Response Example:**

> To enter a vendor invoice, navigate to **Accounts Payable > Vendor Invoice Processing > Voucher Entry Maintenance [AP21B]**.

## Key Function ID Prefixes (Modules)

This table maps the two-letter prefix to the corresponding SM3 module. Use this to understand the context of a user's question.

| Prefix | Module | Description |
|:---|:---|:---|
| **AP** | Accounts Payable | Vouchers, payments, vendor invoices |
| **AR** | Accounts Receivable | Customer payments, credit management |
| **GL** | General Ledger | Journal entries, financial reporting |
| **IN** | Inventory | Product setup, warehouse management, stock levels |
| **OE** | Order Entry | Sales orders, quotes, customer management |
| **PO** | Purchasing | Purchase orders, vendor management |
| **MS** | Administration | System-wide settings and controls |
| **PR** | Production | Manufacturing and processing |
| **SH** | Shipping | Manifests and logistics |
| **RP** | Reports | All system reports |

By understanding this system, you can provide more accurate and professional support to support to-the-point support.
