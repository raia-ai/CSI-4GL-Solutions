---
title: "Madcap_-_SM3_Help-Content-ExternalFiles-EFT_CKV-CKV_-_KEY_-_source_for_PDF"
source: "Madcap_-_SM3_Help-Content-ExternalFiles-EFT_CKV-CKV_-_KEY_-_source_for_PDF.docx"
tags: ["Madcap", "4GL", "Help", "External Files", "EFT", "CKV", "Key", "Documentation", "User Guide"]
version: "1.0"
last_updated: "2025-12-04"
short_description: "This document is a structured transformation of the original Madcap SM3 help content for the External Files module covering EFT and CKV key-related topics. It converts the source DOCX into Markdown with clearly defined sections, lists, and tables, preserving the original text and intent while normalizing formatting for vector-store ingestion."
long_description: "This file presents the contents of the original Madcap SM3 Help document titled “ExternalFiles—EFT CKV/CKV KEY—source for PDF” in a consistent, UTF-8 clean Markdown format. It reconstructs headings, sub-sections, bullet and numbered lists, and tabular data using GitHub Flavored Markdown. The structure aims to match the semantic organization suggested by the source layout (headings by style levels, lists by numbering/bullets) to support robust chunking and retrieval in OpenAI vector stores. No new substantive content has been added; text is preserved and only reformatted for clarity, accessibility, and consistency. Where the source used typography or spacing to indicate hierarchy or emphasis, this conversion infers corresponding Markdown headers or strong emphasis. The YAML frontmatter provides metadata for indexing (title, source, tags, version, and last_updated) alongside concise descriptions of the document’s scope and purpose. The result is a clean, machine-friendly reference of the EFT/CKV key help content suitable for search, embedding, and downstream knowledge management workflows."
---
## **CHECK VERIFICATION FOR **“KEY”**

Plain text file of 136 chars; fields are not separated by any delimiter.

| **Field** | **Width** | **Justify** | **Notes** |
| --- | --- | --- | --- |
| Account Number | 17 | RFZ | 00000' + Bank Account Number(1,12) |
| Check Number | 10 | RFZ | Strip off Prefix |
| Date | 8 |  | YYYYMMDD |
| Amount | 10 | RFZ | Implied decimal |
| Void | 1 |  | Blank |
| Additional Data | 15 |  | Spaces |
| Payee | 75 | LFB |  |
