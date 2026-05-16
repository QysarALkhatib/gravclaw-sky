# Firebase Integration — GravClaw Sky

## Architecture Role
Firebase serves as the **live infrastructure layer** (Layer 4) in OpenClaw v2:

1. **Firestore Vector Search** — Semantic memory across sessions
2. **Cloud Functions** — Text chunking + summarization pipeline
3. **Real-time DB** — Instant agent-to-agent communication
4. **Tavily/Serper** — Clean web search via Firebase Extensions
5. **Gemini API (2M tokens)** — Extended context window

## Connection Points
- **n8n → Firebase:** REST API or Admin SDK
- **Antigravity → Firebase:** MCP Firebase Server (direct)
- **GitHub ↔ Firebase:** Webhook sync for research outputs

## Collections
| Collection | Purpose |
|---|---|
| `memory` | Vector embeddings for semantic search |
| `agent-bus` | Real-time task dispatch & results |
| `queue` | Task state tracking (todowrite) |
| `research` | Deep research intermediate files |