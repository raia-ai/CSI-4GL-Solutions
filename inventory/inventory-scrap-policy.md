---
title: "Inventory-scrap_policy"
source: "Inventory-scrap_policy.docx"
tags: ['inventory', 'scrap policy', 'revaluation', 'log split', 'IN6C', 'IN1T', 'IN16', 'picking confirmation', 'ERP', 'inventory inquiry']
version: "1.0"
last_updated: "2025-12-03"
short_description: "This policy note outlines how to configure and apply inventory scrap policies using Scrap Types “T” and “R” and revaluation percentages. It explains where to review re‑valued amounts after a split log (Split Log Inquiry, IN6C), and clarifies that the scrap type and percent can be overridden at the time of Log Split. An example illustrates that a Scrap Type “T” with a 98% revalue charges 2% to the order and 98% to the scrap (“G”) log. It also summarizes the differences between IN1T (product/spec‑specific) and IN16 (product‑line level) options, noting that IN1T supersedes IN16."
long_description: "This document provides practical guidance for setting and using inventory scrap policies in the system. It centers on the two supported Scrap Types—“T” and “R”—and how the revalue percentage determines the split of costs when a log is split and either returned to stock or routed to a scrap log. The content also identifies where users can verify the results of a revaluation in the user interface and explains the ability to override policy settings at the time of Log Split.

Scrap Type “T” revalues and returns the drop to a dedicated scrap log, while Scrap Type “R” revalues and returns the log to inventory stock. An illustrative scenario shows that if a policy is configured with Scrap Type “T” and a 98% revalue, the system charges 2% to the log on the order and 98% to the scrap (“G”) log. Users can review these revalued amounts after picking confirmation by opening Split Log Inquiry (menu path: Main Menu → Inventory Inquiry Menu → Log Split IN6C) and checking the “Rvl” (Inventory Re‑evaluation) field.

Operational flexibility is supported through on‑the‑fly overrides: both scrap type and percentage can be changed during the Log Split itself, eliminating the need to repeatedly adjust the underlying policy for one‑off situations. For example, if the intent is to return the log on order with an extra 5% of cost and return the drop to inventory at 95%, the user can select Scrap Type “R” on the split log and set the Percentage to 95%.

The document also distinguishes configuration scope and precedence across two setup areas. IN1T (scrap policy) is more specific—to a product and its specifications—whereas IN16 (product line scrap options) provides only percentage or cost scrap and revalue code options at the product‑line level. Importantly, settings on IN1T supersede those on IN16, ensuring that product‑level policy details take precedence over any broader, line‑level defaults."
---

## Example: Revaluation with Scrap Type 'T'

- if you set up your scrap policy, with ‘T' as your Scrap Type, and and the revalue % to 98%, then yes the log on the order would be charged 2% and the scrap log ('G' log) would be 98%

## Viewing Re-valued Amounts After Split Log

- After a split log is done in picking confirmation, you can see the re-valued amounts if you look at the Split Log Inquiry screen, and look in the ‘Rvl' field (Inventory Re-evaluation)
- Main Menu-->Inventory Inquiry Menu-->Log Split IN6C

## Overriding Scrap Policy at Log Split

- You can override your scrap policy type and % at the time of Log Split, so you don’t have to keep changing your policy.
- if you wanted to return the log on order with an extra 5% of cost, and return the drop to inventory at 95%, then change your Scrap Type to “R” on the split log, and your Percentage to 95%

## Scrap Types

- Scrap Type 'T' - revalues and returns drop to a scrap log
- Scrap Type 'R' - revalues and returns log to inventory stock

## Selecting a Scrap Type

- ‘T’
- OR  ‘R’

## Configuration Scope: IN1T vs IN16

- Diff between IN1T (scrap policy) and IN16 product line scrap options, is that IN1T is more specific to a product and specs, where IN16 scrap options ONLY gives you ‘percentage’ or ‘cost’ scrap and revalue code options, and is applied to all product line
- IN1T supersedes what is set up on IN16