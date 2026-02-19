---
title: "Madcap_-_SM3_Help-Content-ExternalFiles-EFT_CKV-CKV_-_FNB_-_source_for_PDF"
source: "Madcap_-_SM3_Help-Content-ExternalFiles-EFT_CKV-CKV_-_FNB_-_source_for_PDF.docx"
tags: ["EFT", "Check Verification", "CSV Format", "Field Specifications", "Banking", "FNB", "External Files", "Data Schema", "MadCap Flare"]
version: "1.0"
last_updated: "2025-12-04"
short_description: "This document defines the Check Verification (CKV) external file for FNB within the 4GL/MadCap help content. It specifies a comma‑separated values (CSV) layout and lists each field with formatting rules and constraints. Implementers can use this as a concise reference to build, export, and validate CKV files for EFT processing, ensuring correct field order, date and numeric formats, UTF‑8 encoding, and proper quoting when commas appear in vendor names. The specification supports consistent, interoperable data exchange across development, testing, and production environments."
long_description: "This document provides the authoritative specification for the Check Verification (CKV) external file used with FNB in support of Electronic Funds Transfer (EFT) processes described within the 4GL/MadCap help content. The CKV file is a comma‑separated values (CSV) text file whose purpose is to convey the minimum information required to validate check transactions in downstream systems, including identifiers, dates, amounts, and vendor details. The specification enumerates each field and states the expected data type, size, and formatting convention so that producers and consumers can rely on predictable structure and unambiguous parsing.

The file layout emphasizes clarity and portability: data is UTF‑8 encoded, fields are delimited by commas, and any field that contains a comma must be enclosed in double quotation marks to preserve CSV integrity. Each record appears on a single line with fields in a fixed order. Key requirements include a six‑digit numeric check number; a date formatted as MM/DD/YY; a monetary amount expressed with two decimal places (ZZZZZZZZ.99) using zero suppression for leading integer digits; and a vendor name up to forty characters, with quoting required when commas are present in the value. These constraints enable straightforward parsing and validation using standard CSV libraries without custom tokenization logic or bespoke parsers.

Operationally, file producers should ensure that values meet the size and format expectations before transmission and that records are free of control characters or malformed encodings that could disrupt ingestion. Producers should also maintain a consistent field order and avoid adding or removing fields without coordinated change control. File consumers should validate incoming records against the stated constraints, reject or quarantine malformed lines, and log discrepancies for remediation and auditability. Implementations may include unit tests or schema checks that assert formatting rules, particularly for date and currency fields, to reduce runtime errors.

This specification is intentionally compact yet complete for the CKV context, and is designed to integrate cleanly with broader EFT processing, reporting, reconciliation, and audit requirements. It can serve as a reference for onboarding new interfaces, for regression testing across application releases, and for operational runbooks whenever CKV data is exchanged with FNB. Teams should retain this document alongside interface configurations so that the authoritative field order and formatting rules remain visible during implementation, monitoring, and support.

In environments with strict data quality requirements, it is recommended to implement pre‑delivery validation checks and to monitor error rates over time. Typical safeguards include length checks on the check number, strict parsing of MM/DD/YY dates, enforcement of two decimal places on amounts, and quoting of vendor names that contain delimiter characters. Where files are transported between systems, ensure that line endings are consistent and that character encoding remains UTF‑8 from source to destination. Any future changes to the CKV layout should follow a formal change process to avoid breaking integrations."
---

## CHECK VERIFICATION FOR 'FNB'

### Comma-separated CSV Format

| Field | Notes |
| --- | --- |
| Check Number | 6 Numeric |
| Check Date | MM/DD/YY |
| Check Amount | ZZZZZZZZ.99 where Z is zero suppressed |
| Vendor Name | 40 Alpha (If “,” in Name enclose in quotes) |
