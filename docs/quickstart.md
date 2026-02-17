---
title: Quick Start
nav_order: 1
parent: Documentation
---

# Quick Start

From the OpenSift app repository root, enter:

```bash
cd backend
```

## 1. Create a virtual environment

```bash
python3.13 -m venv .venv
source .venv/bin/activate
```

Recommended: Python 3.12 or 3.13.

## 2. Install dependencies

```bash
pip install -U pip setuptools wheel
pip install openai
pip install anthropic
pip install sentence-transformers
pip install -r requirements.txt
```

## 3. Configure provider credentials (optional)

Supported providers:
- Claude Code (setup token)
- Claude API (Anthropic key)
- OpenAI API key

Examples:

```bash
export OPENAI_API_KEY="your-key"
export ANTHROPIC_API_KEY="your-key"
```

Claude Code users:

```bash
claude setup-token
export CLAUDE_CODE_OAUTH_TOKEN="..."
unset ANTHROPIC_API_KEY
```

If no provider is configured, OpenSift still ingests/retrieves context but generation will be limited.

## 4. Run OpenSift

From `backend/`:

### Guided setup (recommended)

```bash
python opensift.py setup
```

Setup flow can:
- save keys/tokens to `backend/.env`
- choose launch mode (`gateway`, `ui`, `terminal`, `both`)

### Gateway runner (recommended day-to-day)

```bash
python opensift.py gateway --with-mcp
```

Gateway mode:
- supervises UI and optional MCP server
- performs health check on `/health`
- gracefully shuts down managed processes on Ctrl+C

### UI only

```bash
python opensift.py ui --reload
```

### Terminal only

```bash
python opensift.py terminal --provider claude_code
```

Open:

```text
http://127.0.0.1:8001/
```
