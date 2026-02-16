---
title: Troubleshooting
nav_order: 6
parent: Documentation
---

# Troubleshooting

## I can’t access the site from another device
That’s expected — OpenSift is localhost-only by design.

## Login fails
- Use the token printed in server logs, or
- Set a password via `/set-password`

## Rate limit exceeded
Wait for the retry window (usually 60 seconds) and try again.
If needed, you can adjust the limits in `ui_app.py`.

## PDF shows no text
Scanned PDFs may have no extractable text. OCR is not enabled yet.

## Provider errors
If generation fails, confirm:
- your key/token is correct
- the provider selection matches your credentials