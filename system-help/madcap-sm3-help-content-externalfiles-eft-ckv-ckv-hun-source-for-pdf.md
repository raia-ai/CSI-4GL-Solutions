---
title: "Madcap_-_SM3_Help-Content-ExternalFiles-EFT_CKV-CKV_-_HUN_-_source_for_PDF"
source: "Madcap_-_SM3_Help-Content-ExternalFiles-EFT_CKV-CKV_-_HUN_-_source_for_PDF.docx"
tags: ["EFT", "CKV", "CSV format", "Check verification", "Field definitions", "4GL", "MadCap", "External files", "HUN", "Specification"]
version: "1.0"
last_updated: "2025-12-04"
short_description: "This document defines the comma-separated CSV file layout used for Check Verification for “HUN.” It lists the required data elements and their formats so implementers can generate or validate files consistently. The specification includes Check Number (six numeric digits), Date (MM/DD/YY), Vendor (up to 40 alphabetic characters, quoted if the name contains a comma), and Amount (integer part with zero suppression and two decimal places). It is intended as a concise reference for developers, analysts, and QA teams integrating file-based exchange in the SM3/MadCap help context."
long_description: "This reference provides a concise specification of the CSV format used for Check Verification tied to the “HUN” context. It enumerates the fields that must be present in each record and states the accepted format for each, enabling consistent file generation, ingestion, and validation.

The file is described as a comma-separated CSV. Each record contains the following elements:
- Check Number: A six-digit numeric identifier. No alphabetic or special characters are allowed, and the value should be strictly numeric with a length of six.
- Date: A date formatted as MM/DD/YY. This implies two-digit month, two-digit day, and two-digit year components separated by slashes.
- Vendor: Up to 40 alphabetic characters for the vendor name. If a comma appears in the name, the value must be enclosed in quotation marks to preserve CSV integrity and prevent an unintended field split.
- Amount: A numeric amount in the form ZZZZZZZZ.99, where Z indicates a zero-suppressed integer digit. Zero suppression means leading zeros in the integer portion are omitted, while the fractional part always includes two digits.

The table included in this document presents the fields under the headers “Field” and “Notes,” pairing each element with its formatting rule. This compact layout is suitable for quick reference during development or testing and for inclusion in build and QA checklists. Although the document does not prescribe additional CSV conventions, standard practices apply: maintain the comma delimiter between fields, surround any field containing a comma with quotes, and ensure that numeric fields do not include thousands separators or currency symbols unless explicitly specified (they are not specified here).

Consumers of the file should validate each record against the constraints listed above and handle quotation appropriately when parsing Vendor values. Producers should ensure that data values conform prior to export, paying particular attention to date formatting and the removal of leading zeros in the integer part of Amount values. Consistent adherence to this format helps prevent ingestion errors and aids reconciliation and auditing within the broader SM3/MadCap documentation and help system workflows.

This specification is intentionally minimal and focused on field-level requirements. It is suitable for embedding within implementation guides, onboarding materials, or automated schema checks. Any extensions—such as optional fields, additional validation rules, or locale-specific variations—are outside the scope of this document and should be defined separately if needed."
---

## CHECK VERIFICATION FOR 'HUN'
### Comma-separated CSV Format

| Field | Notes |
| --- | --- |
| Check Number | 6 Numeric |
| Date | MM/DD/YY |
| Vendor | 40 Alpha (If "," in Name enclose in quotes) |
| Amount | ZZZZZZZZ.99 where Z is zero suppressed |