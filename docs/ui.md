---
title: Chat UI
nav_order: 2
parent: Documentation
---

# Chat UI

OpenSift UI is chat-first: ingest, ask, review, and save in one workspace.

## Core flow
- Select an owner namespace
- Choose output mode (`study_guide`, `key_points`, `quiz`)
- Choose provider (`claude_code`, `claude`, `openai`)
- Ask questions and stream grounded responses

## Layout
- Left sidebar:
  - owner selector
  - chat history list
  - new chat creation (inline naming, no popup)
  - session open/delete actions
- Main chat workspace:
  - streaming chat transcript
  - composer with mode/provider/k controls
- Tool panel:
  - Ingest
  - Study Library
  - Quiz Attempts
  - Flashcards

## Sidebar tools
- Ingest URL
- Upload and ingest files
- Browse saved study items
- Track quiz attempts
- Manage flashcards

## Owners (namespaces)
Use owners to isolate classes/topics, for example:
- `bio101`
- `chem-midterm`
- `cs-finals`

Each owner maintains separate:
- session history
- retrieval context
- saved study assets

Owner names are normalized to a safe format to avoid retrieval/session mismatches.

## Streaming responses
Responses stream incrementally so you can read output as generation happens.
