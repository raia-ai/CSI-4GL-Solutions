---
title: "Madcap_-_SM3_Help-Content-ExternalFiles-EFT_CKV-CKV_-_WFG_-_source_for_PDF"
source: "Madcap_-_SM3_Help-Content-ExternalFiles-EFT_CKV-CKV_-_WFG_-_source_for_PDF.docx"
tags: ["MadCap", "4GL", "Help Content", "EFT", "CKV", "WFG", "User Guide", "Documentation", "External Files", "PDF Source"]
version: "1.0"
last_updated: "2025-12-04"
short_description: "Consolidated help content for 4GL covering EFT CKV/CKV and WFG workflows and references. This source document is structured for PDF export and has been converted to Markdown with headings, lists, and tables preserved."
long_description: "This document originates from a MadCap Flare source used to produce a PDF for the 4GL help system. It aggregates external files and topics related to electronic funds transfer (EFT), CKV/CKV processes, and WFG-specific guidance. The conversion presented here restructures the original DOCX into standards-compliant Markdown suitable for vector indexing and downstream publishing. Main sections from the original are mapped to second-level headers (##), while subsections use third-level headers (###) for consistency. Bulleted and numbered lists are preserved using GitHub-flavored Markdown, and tables are rendered as Markdown tables with header separators. Where the original used inline formatting (bold, italics, underline), those styles are translated into Markdown emphasis. Obvious encoding artifacts were cleaned, and sequential duplicate lines removed to improve readability without altering meaning. The resulting file retains the logical content order of the source, including headings, narrative paragraphs, procedures, callouts, and tabular data where applicable. This Markdown is intended for ingestion into OpenAI’s vector store and for reuse in documentation workflows that prefer plain-text, version-control-friendly formats."
---
## Inputfilerecord types

## File header Record

## Detailrecord

## Trailerrecord

## Transaction code table
*0300XXX00XXXXXXXXXXXXX0
---------1---------2----
1. 123456789012345678901234
| Sample data | *03 | 00259 | 000009610XXXXXX | 0 |  |
| --- | --- | --- | --- | --- | --- |
| Field name | *03 | Bank ID | Account number | 0 | Unused |
| Field position | 1-3 | 4-8 | 9-23 | 24 | 25-85 or 165 |
| Description | Always *03 | Bank ID provided by Wells Fargo. Right justified, zero filled, numeric. | Right justified, zero filled, numeric | Always zero | Spaces |

There should be only one detail record for each check issued. Each detail record must be in the same format and contain an account number.

000000100102280200XXXXXXXXXXXXX3200000026420MARY MOORE
---------1---------2---------3---------4---------5---------6---------7---------8
1. 12345678901234567890123456789012345678901234567890123456789012345678901234567890
| Sample data | 0000001001 | 022802 | 00XXXXXXXXXXXXX | 320 | 0000026420 | MARY MOORE |  |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Fieldname | Check serial no. | Issue date | Account number | Transaction code | Amount | Additional data/payee information | Unused |
| Fieldposition | 1-10 | 11-16 | 17-31 | 32-34 | 35-44 | 45-84 (or 45-164)** | To 85 or 165 |
| Description | Rightjustified, zerofilled, numeric.<br>Each serial number must be unique. | Format MMDDYY, numeric.<br>Note: issue date can be all zeros for stop payment transaction codes. | Wells Fargo account number, right justified, zero filled, numeric | Transaction code*(see Transaction code t**able)* | Format ($$$$$$$$cc). Right justified, zerofilled, numeric | Leftjustified, alphanumeric, may contain special characters.<br>**Payee Validation n****otes:**<br>If using the Payee Validation service, payee information must match check issue payee information exactly. Do not use carriage returns between payee names.Thepayee name ends at the beginning ofthe legal street address or P.O. box number, unless you authorize the bank to verify the first line only.Do notinclude address in your issue file. | Spaces |

&00000040000000116564
---------1---------2---------3---------4---------5---------6---------7---------8
1. 12345678901234567890123456789012345678901234567890123456789012345678901234567890
| Sampledata | & |  | 0000004 |  | 0000000116564 |  |
| --- | --- | --- | --- | --- | --- | --- |
| Field name | & | Spaces | Detail record count | Spaces | Total amount | Unused |
| Field position | 1 | 2-15 | 16-22 | 23-25 | 26-38 | 39-85 or 165 |
| Description | Always & | 14 spaces | Totalcount of detail records. Right justified, zerofilled, numeric. | 3 spaces | Total dollar amount of detail records. Format ($$$$$$$$$$$cc). Rightjustified, zerofilled, numeric. | Spaces |
