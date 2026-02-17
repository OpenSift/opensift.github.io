---
title: Documentation
nav_order: 2
has_children: true
---

# Documentation

OpenSift documentation aligned to the main OpenSift project repository.

## Start here
- [Quick Start](quickstart.md)
- [Using the Chat UI](ui.md)
- [Ingestion (PDFs + URLs)](ingestion.md)
- [Providers](providers.md)
- [Troubleshooting](troubleshooting.md)
- [Security](security.md)
- [Roadmap](roadmap.md)
- [Release Notes](release-notes.md)

## Runtime modes
OpenSift supports multiple launch modes from `backend/opensift.py`:
- `setup`: interactive first-run configuration and launch chooser
- `gateway`: supervised UI process plus optional MCP server
- `ui`: UI server only
- `terminal`: terminal chat only

## Mental model
OpenSift runs as a retrieval-grounded workflow:

1. **Ingest**: URL or file content is chunked and embedded.
2. **Retrieve**: semantic search returns relevant local context.
3. **Generate**: provider-backed responses stream from grounded context.

By default, deployment is local-first and optimized for study workflows.
