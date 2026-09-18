# Demo Script

## Goal

Demonstrate a local-first typed streaming LLM application without changing production source or model weights.

## Steps

```bash
cd ~/Downloads/nallar_v7_2_0_runtime
source .venv/bin/activate
python app.py
```

In a second terminal, verify the local model runtime is available:

```bash
ollama list
```

Then use the NALLAR UI or its chat creation endpoint, followed by:

```text
POST /api/chats/{chat_id}/messages/stream
body model: MessageInput
semantic field: content
```

## Talking points

- Why local inference matters: privacy, reproducibility, offline capability, cost control.
- Why typed API boundaries matter: safer interfaces and clearer contracts.
- Why package evidence is separated from correctness evidence.
- How the same application can later become a tool inside MCP/RAG/multi-agent workflows.
