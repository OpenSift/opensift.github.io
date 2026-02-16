---
title: Quick Start
nav_order: 1
parent: Documentation
---

# 🚀 Quick Start

## 1. Create a virtual environment

```
bash
python3.13 -m venv .venv
source .venv/bin/activate
```
(Recommended: Python 3.12 or 3.13)

## 2. Install dependencies

```
pip install -U pip setuptools wheel
pip install -r requirements.txt
```

## 3. Set API Keys (Optional)

Supported providers:
	•	Claude Code (setup-token)
	•	Claude API (Anthropic)
	•	OpenAI API


Example:

export OPENAI_API_KEY="your-key"

export ANTHROPIC_API_KEY="your-key"

Claude Code users:

```
claude setup-token
export CLAUDE_CODE_OAUTH_TOKEN="..."
unset ANTHROPIC_API_KEY
```

If no provider is configured, OpenSift will still retrieve relevant passages but won’t generate AI summaries.

## 4. Run the app

```
uvicorn ui_app:app --reload --host 127.0.0.1 --port 8001
```


Open:
```
http://127.0.0.1:8001/
```

The chatbot page is the default UI.
