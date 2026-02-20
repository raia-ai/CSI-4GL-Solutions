---
title: General_Metals_Knowledge-Metals_Order_Lifecycle
source: General_Metals_Knowledge-Metals_Order_Lifecycle.docx
tags:
  - metals
  - order lifecycle
  - sales order
  - procurement
  - manufacturing
  - logistics
  - ERP
  - inventory management
  - quality control
  - operations
version: '1.0'
last_updated: '2025-12-03'
short_description: >-
  This document outlines the end-to-end Metals Order Lifecycle, detailing key
  processes, roles, and data flow from inquiry and quotation through order
  entry, production, fulfillment, invoicing, and post-delivery activities. It
  consolidates operational steps, decision points, and handoffs across sales,
  procurement, manufacturing, logistics, and finance to provide a unified
  reference for execution and training.
long_description: >-
  This internal knowledge document provides a structured, step-by-step view of
  the Metals Order Lifecycle used by the organization. It describes how customer
  demand is captured and translated into executable orders, how materials and
  production are planned and executed, and how goods are delivered, invoiced,
  and reconciled. The content aligns cross-functional responsibilities spanning
  sales/customer service, procurement and supplier coordination, shop-floor
  manufacturing processes (cutting, processing, fabrication), inventory control
  and warehousing, quality checks and documentation, logistics and shipping, and
  finance for billing and cash application. Where applicable, the document notes
  upstream and downstream dependencies, data and document artifacts (e.g.,
  quotes, sales orders, MTRs/COCs, pick lists, BOLs, invoices), system
  interactions within the ERP and related tools, and exception handling patterns
  for changes, returns, or quality holds. The purpose is to provide a reliable
  reference for onboarding, compliance, and continuous improvement, ensuring
  consistent terminology, clear inputs/outputs for each step, and visibility
  into ownership and controls throughout the quote-to-cash lifecycle. 
---

# General Metals Knowledge Metals Order Lifecycle

\*\*Title: \*\* Metals Order Lifecycle \*\*Description: \*\*This document outlines the key stages and workflows involved in the typical lifecycle of a metals industry order. It is intended to help IT support teams better understand operational processes to more effectively support SM3 configuration, automation, and user support.

### 1. Quote to Order Conversion

* Customer requests a quote(SQ) for specific materials, dimensions, and finishes.
* Sales team prepares a quote including pricing, lead time, and specs.
* Quote may include custom processing or certifications.
* Upon approval, quote is converted to a Sales Order ( SM3 creates Work Order #).

### 2. Sales Order & Work Order Creation

* Sales Order triggers internal review and scheduling.
* For processed material, Internal (IP) or Outside(OP) processes are generated.
* WO/IP may involve saw cutting, shearing, nesting, or outside processing(OP).
* Material is allocated from inventory or reserved for future delivery.

### 3. Inventory Allocation & Processing

* Items are pulled from stock or coils are slitted to size.
* Inventory is often managed by weight, dimension, or piece count.
* Remnants and drops may be recorded for future reuse.
* SM3 tracks heat numbers, lot numbers, and traceability details.

### 4. Quality Control & Certifications

* MTRs (Mill Test Reports) are matched with each Log number.
* Processing certs or inspection logs are appended where needed.
* Oracle Cloud or Customer server must support document storage and customer-specific attachments.

### 5. Shipping & Fulfillment

* Pack lists, BOLs, and customer-specific documents are generated.
* Labels may include barcodes or tags.
* SM3 updates inventory levels and marks order as shipped.
* Shipment data may be shared via EDI or customer portal.

### 6. Invoicing & Order Close

* Invoice is generated automatically or manually upon shipment.
* SM3 links invoice with original order and shipment records.
* Final reporting includes gross margin, delivery KPIs, and compliance data.

### 7. Recommended SM3 Fields and Flags

To support the above lifecycle, consider implementing the following fields or flags:

* Quote Expiration Date
* Sales Order Type (Standard, Blanket, Processed, etc.)
* Work Order Status (PBP, ASG, PCK, Scheduled, In Progress, Complete)
* Processing Requirements (e.g., Nesting, Outsourcing)
* Heat/Lot Number Tracking/Country of Origin
* Certification Document Links
* Shipping Method and Carrier Info
* Invoice Status and Payment Terms

### Figures
