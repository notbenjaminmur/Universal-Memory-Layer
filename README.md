# Universal Memory Layer (UML)

The **Universal Memory Layer (UML)** is a standardized JSON format designed to export and import a user’s memory across different AI models and platforms.

## Why?
Today, when switching LLMs (GPT, Claude, Mistral, Gemini…), users lose their history.  
UML allows you to **save your conversational memory** and reuse it anywhere.

## Goals
- Provide a **universal format** to store AI interaction history.
- Ensure **portability** across models and platforms.
- Build **privacy and consent** into the design.

## Key Features
- **JSON Schema (Draft-07)**: strict, open, extensible.
- Supports:
  - User profile
  - Conversations with metadata
  - Facts, short/long-term memories, preferences
  - Knowledge graphs
  - Artifacts (files, links)
  - Embeddings
- Handles **PII annotations** and **redactions** for compliance.

## Quick Example
```json
{
  "uml_version": "1.0.0",
  "user_profile": {
    "id": "user:123",
    "display_name": "User 123"
  },
  "memories": {
    "facts": [
      {
        "id": "mem-f-1",
        "kind": "fact",
        "value": "Demo user for UML specification",
        "confidence": 0.99,
        "first_seen_at": "2025-01-01T00:00:00Z"
      }
    ]
  }
}
