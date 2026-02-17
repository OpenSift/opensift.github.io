---
title: Home
nav_order: 1
---

# OpenSift

[![Build / Smoke Tests](https://github.com/OpenSift/OpenSift/actions/workflows/ci.yml/badge.svg)](https://github.com/OpenSift/OpenSift/actions/workflows/ci.yml)
[![Release](https://img.shields.io/github/v/release/OpenSift/OpenSift?label=release)](https://github.com/OpenSift/OpenSift/releases)
[![Release Date](https://img.shields.io/github/release-date/OpenSift/OpenSift?label=released)](https://github.com/OpenSift/OpenSift/releases)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/OpenSift/OpenSift/blob/main/LICENSE)

**Sift faster. Study smarter.**

OpenSift is an AI-powered, local-first study assistant for working through large source sets (PDFs, URLs, notes) with grounded retrieval and generation.

Core workflow:
1. Ingest content (URL, PDF, TXT, MD)
2. Retrieve relevant chunks from local vector search
3. Generate study output with your selected provider

Outputs include:
- Study guides
- Key points and summaries
- Quizzes
- Flashcards

## Quick links
- [Documentation](docs/index.md)
- [Quick Start](docs/quickstart.md)
- [Chat UI](docs/ui.md)
- [Ingestion](docs/ingestion.md)
- [Providers](docs/providers.md)
- [Troubleshooting](docs/troubleshooting.md)
- [Security](docs/security.md)

## Notes
- OpenSift is currently a hobby proof-of-concept project.
- The UI is designed for localhost usage.
- Recommended runtime is the gateway runner: `python opensift.py gateway --with-mcp`.

## Screenshots
![Demo](assets/images/screenshot.png)
![Study Guide](assets/images/study_guide.png)
![Key Points](assets/images/key_points.png)
![Quiz Me](assets/images/quiz_me.png)
