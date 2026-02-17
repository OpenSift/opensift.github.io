---
title: Security
nav_order: 5
parent: Documentation
---

# Security

OpenSift is designed for local use.

## Localhost-only
The UI server is intended to bind to:
- `127.0.0.1` (IPv4 loopback)
- `::1` (IPv6 loopback)

This prevents access from your LAN.

**Run like this:**
```bash
python opensift.py ui --host 127.0.0.1 --port 8001
```

## Authentication

OpenSift supports two auth paths:
1. Generated token (printed on startup; valid until restart)
2. Password (stored locally as a salted PBKDF2 hash)

## Rate limiting

Rate limiting helps prevent spam and brute forcing:
- `/login` and `/set-password` POST are limited
- `/chat/stream` is limited
- Ingest endpoints are limited

## Recommendations
- Keep OpenSift local (do not expose to the internet)
- Avoid ingesting sensitive content when policy disallows it
- Treat provider keys and tokens as secrets
