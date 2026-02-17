---
title: Providers
nav_order: 4
parent: Documentation
---

# Providers

OpenSift can generate output using three provider modes.

## Claude Code (recommended local workflow)
Requirements:
- Claude Code CLI installed
- token configured via `claude setup-token`
- `CLAUDE_CODE_OAUTH_TOKEN` available

Optional environment knobs:
- `OPENSIFT_CLAUDE_CODE_CMD`
- `OPENSIFT_CLAUDE_CODE_ARGS`

## Claude API (Anthropic)
Requirements:
- `ANTHROPIC_API_KEY`

## OpenAI API
Requirements:
- `OPENAI_API_KEY`

## Model defaults
- OpenAI default: `gpt-5.2`
- Claude default: `claude-sonnet-4-5`

## No-provider mode
Even without generation credentials, OpenSift can still:
- ingest
- retrieve
- return relevant passages

Generation features require one configured provider.
