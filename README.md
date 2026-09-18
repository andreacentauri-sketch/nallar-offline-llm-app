# Offline LLM App

> Recruiter-facing public presentation generated from the verified local NALLAR portfolio package.

## 30-second summary

This project is presented around four questions: **what was built, how it was tested, what was measured, and what is not being claimed**.

## Evidence model

- Runnable implementation or portfolio artifact.
- Executable tests and/or quantitative evaluation.
- Reproducible local commands.
- Explicit limitations.

## Proof points

- Local-first LLM application packaging.
- Typed API / local-model integration boundaries.
- Architecture, evaluation, demo, and case-study documentation.

## Evidence boundary

Portfolio packaging and source-integrity evidence do not by themselves establish production readiness.

---

## Reproduce locally

See the project files and original run notes below. Use the repository's own test/evaluation commands and inspect the generated evidence artifacts rather than relying on screenshots alone.


### Original run notes

# NALLAR Offline LLM App

## Portfolio status

This package is the recruiter-facing packaging artifact for the NALLAR Offline LLM App workstream.

**Verified package gate:** generated from the exact NALLAR source identity recorded in `SOURCE_MANIFEST.json`.

## What it demonstrates

- Local-first LLM application architecture.
- FastAPI/Starlette-style typed API surface.
- Typed streaming endpoint: `POST /api/chats/{chat_id}/messages/stream`.
- Typed message body model with semantic input field `content`.
- Local LLM adapter status: **present**.
- Source integrity and reproducible package manifest.

## Run locally

From the original NALLAR runtime directory:

```bash
cd ~/Downloads/nallar_v7_2_0_runtime
source .venv/bin/activate
python app.py
```

If the runtime is normally started with ASGI instead, use the project's installed ASGI server against the `app` object.

Before sending prompts, ensure the configured local model runtime is available. Ollama binary detected; non-mutating `ollama list` probe executed.

## Demo flow

1. Start the local model runtime.
2. Start NALLAR.
3. Create a chat through the NALLAR API/UI.
4. Send a message through the typed streaming route.
5. Observe streamed/local response behavior.
6. Review `EVALUATION.md` for evidence boundaries.

## Evidence boundary

This package does **not** claim O6 production correctness closure, HOLDOUT80 performance, or production promotion. The historical O6 correctness lane remains open and source-scoped.


## Public claim boundary

This repository is published as an evidence-backed portfolio artifact. Test and evaluation results apply to the documented local/bundled scope. No production deployment, foundation-model training, or other unverified capability is implied.
