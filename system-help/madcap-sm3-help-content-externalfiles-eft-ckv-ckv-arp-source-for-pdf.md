---
title: "Madcap_-_SM3_Help-Content-ExternalFiles-EFT_CKV-CKV_-_ARP_-_source_for_PDF"
source: "Madcap_-_SM3_Help-Content-ExternalFiles-EFT_CKV-CKV_-_ARP_-_source_for_PDF.docx"
tags: ["MadCap Flare", "4GL", "EFT", "CKV", "ARP", "Accounts Receivable", "Help Content", "External Files", "User Guide"]
version: "1.0"
last_updated: "2025-12-04"
short_description: "This document provides the 4GL Help reference for Check Verification under Accounts Receivable Positive Pay (ARP) within the EFT CKV/CKV context. It has been converted from the original DOCX into structured Markdown with clean, UTF-8–compliant text, normalized headings, preserved lists, and GitHub‑style tables. The specification defines a space‑delimited file format—including field names, lengths, and data rules—for exchanging ARP check verification data. All content has been retained while broken formatting and encoding artifacts were corrected. Logical section breaks were inferred where appropriate to improve clarity and enable reliable vector‑store ingestion and retrieval. The resulting file is suitable for governance, audit, and knowledge reuse across implementation and support teams."
long_description: "This Markdown file is a faithful, structured conversion of the MadCap Flare–derived SM3 Help topic describing the Check Verification interface for Accounts Receivable Positive Pay (ARP) in the EFT CKV/CKV domain. The original DOCX content has been semantically reconstructed to provide consistent and machine‑friendly formatting without altering the underlying information. Main sections are represented by double‑hash headers (##), with subordinate information expressed as body text, lists, or GitHub Flavored Markdown tables. Numbered and bulleted items are preserved according to the source document’s numbering definition whenever available; otherwise, list semantics are retained as unordered items.

The central specification defines a space‑delimited external file format used to convey ARP check verification details. It enumerates the required fields and their constraints, including: Record Type (1 alphanumeric character, with ‘V’ indicating a void or debit and null indicating a regular check), Bank (concatenation of Bank Branch Transit, 5 numeric, and CDA Account Number, 7 numeric), Check Date (6 numeric, MMDDYY), Check Number (10 numeric, right‑justified and zero‑filled), Check Amount (10 numeric with an implied decimal), Spare (15 alphanumeric as literal Xs for padding), and Vendor Name (40 alphanumeric). These constraints clarify allowable values, lengths, alignment, and formatting so that generating and consuming systems can validate and parse records reliably.

During conversion, text encoding anomalies were normalized to ensure UTF‑8 compliance, duplicate lines were removed, and spacing was standardized. The table structure from the source was preserved and rendered as a Markdown table with clear header and body rows, which improves readability in plain‑text contexts and enables accurate tokenization for vector databases. Where the original layout indicated logical grouping—such as the prominent topic title followed by a concise description and tabular field specification—this structure was made explicit through headings and section breaks to aid downstream indexing, chunking, and retrieval.

This artifact is intended for use in OpenAI‑compatible vector stores and similar retrieval‑augmented generation (RAG) pipelines. It enables precise, field‑level question answering—for example, querying valid lengths, alignment rules (right‑justified, zero‑filled), or date formats (MMDDYY). It also supports broader tasks such as onboarding developers to the ARP interface, validating integration payloads, and aligning upstream and downstream systems on canonical field definitions. The combination of descriptive prose and tabular schema ensures both human‑readable guidance and machine‑parsable structure.

Overall, the result balances readability and rigor: it remains a faithful representation of the original help content while being optimized for search accuracy, content chunking, and embedding‑based retrieval in production workflows.

In addition to preserving the final specification, the conversion process emphasizes future maintainability. Headings, lists, and tables follow consistent Markdown idioms so additions and revisions can be diffed and reviewed cleanly in source control. This consistency also minimizes fragmentation when chunking content for embeddings, supporting stable document IDs and traceable updates across releases."
---
## CHECK VERIFICATION FOR “ARP”

Space-delimited format (one space between fields)

|**Field**|**Notes**|
|---|---|
|Record Type|1A (‘V’ is Void or Debit; Null if regular Check)|
|Bank|Bank Branch Transit(5N) + CDA Account Number(7N)|
|Check Date|6N as MMDDYY|
|Check Number|10N RJ zero-filled|
|Check Amount|10N implied decimal|
|Spare|15A as ‘XXXXXXXXXXXXXXX’|
|Vendor Name|40A|
