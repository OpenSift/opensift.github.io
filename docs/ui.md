---
title: Chat UI
nav_order: 2
parent: Documentation
---

# Chat UI

OpenSift’s UI is designed to work like a chatbot.

## All-in-one flow
From the chat page you can:

- Ingest URLs
- Upload and ingest PDFs / text files
- Ask questions
- Generate study guides / quizzes

## Owners (namespaces)
Use **owners** to keep topics separate:

- `bio101`
- `chem-midterm`
- `cs-finals`

Each owner keeps its own chat history + retrieval context.

## Streaming responses
Responses stream live while generating. This makes it easy to read as the model writes.