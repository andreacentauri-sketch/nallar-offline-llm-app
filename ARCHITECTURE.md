# Architecture

## High-level flow

```text
User / UI
   |
   v
FastAPI typed request surface
   |
   v
MessageInput(content, ...)
   |
   v
NALLAR orchestration / retrieval / quality logic
   |
   v
Local LLM adapter
   |
   v
Local model runtime (for example Ollama when configured)
   |
   v
Streaming response
```

## Key engineering properties

- Typed API boundary rather than unstructured request parsing.
- Local-first inference path.
- Separation between API/orchestration code and local model adapter.
- Explicit source identity and package manifest.
- Existing correctness/evaluation work is kept separate from packaging claims.

## Security / governance boundary

This portfolio package is a documentation and reproducibility artifact. It does not alter canonical application source, model weights, registry state, or production promotion status.
