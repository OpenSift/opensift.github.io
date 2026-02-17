---
title: Ingestion
nav_order: 3
parent: Documentation
---

# Ingestion

OpenSift supports source ingestion via:
- URLs (web pages / articles)
- PDF uploads
- text uploads (`.txt`, `.md`)

## URL ingestion
Paste a URL in the Ingest panel. OpenSift:
1. fetches the page with retry/timeout safeguards
2. extracts and normalizes main content
3. falls back to broader body-text extraction when needed
4. chunks + embeds + stores content in local vector DB

URL handling includes:
- basic URL validation
- auto-prefixing `https://` when scheme is omitted
- actionable error messages when ingestion fails

Common failure reasons:
- site blocks automated scraping
- content requires client-side JavaScript rendering
- page has too little extractable text

## PDF ingestion
Upload a PDF file. OpenSift extracts text and ingests it.

For scanned PDFs, OpenSift attempts OCR fallbacks (when local OCR tooling is available), including:
- image-based extraction from embedded PDF images
- `pdf2image` + `pytesseract` fallback path

## Namespace behavior
Ingestion is scoped to the current owner namespace so subjects remain separate.

## Chunking and embeddings
Ingested content is:
1. chunked
2. embedded
3. stored for semantic retrieval

Queries retrieve top matching chunks for grounded generation.
