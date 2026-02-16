---
title: Providers
nav_order: 4
parent: Documentation
---

# Providers

OpenSift can generate output using different providers.

## Claude Code (setup-token)
Best for local dev workflows where you use a Claude setup token.

## Claude (API key)
Works if you provide an Anthropic API key.

## OpenAI (API key)
Works if you provide an OpenAI API key.

## No provider mode
Even without a provider configured, OpenSift can still:

- ingest
- retrieve
- show relevant passages

Generation features require a configured provider.