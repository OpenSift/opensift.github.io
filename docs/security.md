---
title: Security
nav_order: 5
parent: Documentation
---

# Security

OpenSift is local-first and designed primarily for localhost use.

## Localhost-only model
The UI server is intended to bind to:
- `127.0.0.1` (IPv4 loopback)
- `::1` (IPv6 loopback)

Run like this:

```bash
python opensift.py ui --host 127.0.0.1 --port 8001
```

## Security hardening status

1. **Persistent XSS in chat tool rendering**
- Status: Addressed
- Notes: untrusted content paths use safe DOM patterns (`textContent`), not unsafe interpolation.

2. **URL ingest SSRF surface**
- Status: Addressed
- Notes: localhost/private targets are blocked; DNS targets and redirects are validated; redirect loops and non-http(s) targets are rejected.

3. **Event-loop blocking in heavy ingest paths**
- Status: Mitigated
- Notes: heavy embedding/extraction/query paths are offloaded via worker-thread execution.

4. **No payload/upload size limits**
- Status: Addressed
- Notes: upload bytes and key payload sizes are bounded.

5. **Non-atomic/unsynchronized persistence**
- Status: Addressed
- Notes: atomic JSON writes + lock-guarded shared state and storage operations.

6. **Production auth/session hardening**
- Status: Partially open by design
- Notes: deployment assumptions remain localhost/dev-first.

7. **Shallow CI/test coverage**
- Status: Improved
- Notes: backend tests now run in CI with focused regressions for ingest/template/auth/session/streaming behavior.

## Authentication
OpenSift supports two local auth paths:
1. Generated token (valid until process restart)
2. Password (stored locally as a salted PBKDF2 hash)

## Rate limiting
Rate limiting is applied to sensitive/high-volume POST surfaces:
- `/login`, `/set-password`
- `/chat/stream`
- `/chat/ingest/*`
- other chat mutation paths

## Key controls
- `OPENSIFT_MAX_URL_REDIRECTS`
- `OPENSIFT_ALLOW_PRIVATE_URLS`
- `OPENSIFT_MAX_UPLOAD_MB`
- `OPENSIFT_MAX_CHAT_MESSAGE_CHARS`
- `OPENSIFT_MAX_SESSION_IMPORT_CHARS`
- `OPENSIFT_MAX_HISTORY_TURNS`
- `OPENSIFT_MAX_RETRIEVAL_K`

## Recommendations
- Keep OpenSift local (do not expose directly to the public internet)
- Treat provider API keys/tokens as secrets
- Restrict private-network URL ingest unless explicitly needed in trusted environments
- Keep dependencies and local OCR/runtime tools patched
