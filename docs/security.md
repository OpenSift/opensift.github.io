---
title: Security
nav_order: 5
parent: Documentation
---

# Security

OpenSift is built for **local use**.

## Localhost-only
The UI server is intended to bind to:
```
- `127.0.0.1` (IPv4 loopback)
- `::1` (IPv6 loopback)
```

This prevents access from your LAN.

**Run like this:**
```
bash
uvicorn ui_app:app --reload --host 127.0.0.1 --port 8001
```

Authentication

OpenSift supports two auth paths:
	1.	Generated token (printed on startup; valid until restart)
	2.	Password (stored locally as a salted PBKDF2 hash)

Rate limiting

Rate limiting helps prevent spam and brute forcing:
	•	/login and /set-password POST are limited
	•	/chat/stream is limited (prevents runaway loops)
	•	ingest endpoints are limited

Recommendations
	•	Keep OpenSift local (don’t expose to the internet)
	•	Avoid ingesting sensitive materials if prohibited by policy
	•	Treat provider keys/tokens as secrets