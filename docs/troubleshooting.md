---
title: Troubleshooting
nav_order: 6
parent: Documentation
---

# Troubleshooting

## I cannot access the UI from another device
Expected. OpenSift is localhost-only by design.

## Login fails
- Use the startup token printed in server logs, or
- set a password via `/set-password`

## Rate limit exceeded
Wait for the retry window (typically 60 seconds) and retry.
Limits are configurable in `backend/ui_app.py`.

## URL ingest fails
You should now see a specific ingest error message in chat.

Common causes:
- page blocks scraping
- page requires JavaScript rendering
- URL is invalid or missing scheme
- page contains too little extractable text

Try:
- a different article URL
- uploading a PDF copy of the content
- copying content into `.txt`/`.md` and ingesting that file

## PDF shows little or no text
The PDF may be scanned. OCR fallback may help, but quality depends on local OCR dependencies and source quality.

## Retrieval says nothing found after ingest
Check:
- you are in the same owner namespace used for ingestion
- ingest completed successfully (look for the success message)
- your query terms are present in the ingested material

## Provider errors
Confirm:
- key/token is set correctly
- selected provider matches available credentials
- required local CLI is installed for Claude Code mode

## Gateway exits early
Check UI health endpoint:
- `http://127.0.0.1:8001/health`

Increase startup timeout if needed:

```bash
python opensift.py gateway --health-timeout 30
```
