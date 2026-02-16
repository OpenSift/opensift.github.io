---
title: Ingestion
nav_order: 3
parent: Documentation
---

# Ingestion

OpenSift supports ingestion via:

- URLs (web pages / articles)
- PDF uploads
- Text uploads (.txt, .md)

## URL ingestion
Paste a URL in the ingest panel. OpenSift fetches text, chunks it, embeds it, and stores it for retrieval.

## PDF ingestion
Upload a PDF file. OpenSift extracts text and ingests it.

> If a PDF is scanned images, text extraction may be empty (OCR is not enabled by default).

## Chunking & embeddings
Ingested content is:
1. chunked
2. embedded
3. stored in the local vector database

Queries retrieve the top matching chunks.