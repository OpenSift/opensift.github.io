---
title: Documentation
nav_order: 2
has_children: true
---

# Documentation

Welcome to the OpenSift docs.

## Start here
- [Quick Start](quickstart.md)
- [Using the Chat UI](ui.md)
- [Ingestion (PDFs + URLs)](ingestion.md)
- [Providers](providers.md)
- [Security](security.md)
- [Troubleshooting](troubleshooting.md)

## Mental model
OpenSift works in three steps:

1. **Ingest**: PDF or URL content is chunked and embedded.
2. **Retrieve**: queries fetch the most relevant chunks.
3. **Generate**: optional provider turns retrieved context into study output.

Everything is optimized for **fast study workflows**.