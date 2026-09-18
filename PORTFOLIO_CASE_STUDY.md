# Portfolio Case Study — NALLAR Offline LLM App

## Problem

Build a local-first AI application that can expose a typed conversational interface while preserving explicit engineering evidence and separating architecture claims from runtime-quality claims.

## Engineering work

The system uses a typed API surface, a structured message model, an orchestration layer, and a local-model integration boundary. The broader NALLAR program also contains retrieval, semantic-quality and repair logic; those capabilities are not promoted beyond their verified evidence.

## What I would show in an interview

- Typed streaming API contract.
- Local LLM adapter boundary.
- Source-integrity and reproducible packaging.
- Clear separation of implementation, evaluation, and promotion evidence.
- How this component becomes the foundation for MCP, RAG, agentic, voice, and flagship portfolio work.

## Result

The workstream is considered package-complete only when the generated manifest, documentation set, source identity checks, and package validation all pass in the same giantstep.
