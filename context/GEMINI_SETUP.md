# Gemini / Lighter Model Setup

OpenClaw is being migrated from the very strong Codex 5.5 brain to Google AI Studio / Gemini free-tier models.

## Configured default chain

Primary:
- `google/gemini-3.1-pro-preview`

Fallbacks:
- `google/gemini-3-flash-preview`
- `google/gemini-3.1-flash-lite-preview`
- `google/gemini-2.5-flash`
- `openai-codex/gpt-5.5` as emergency fallback while migration is still being hardened

## Available Google models added to OpenClaw catalog

- `google/gemini-3.1-pro-preview`
- `google/gemini-3-pro-preview`
- `google/gemini-3-flash-preview`
- `google/gemini-3.1-flash-lite-preview`
- `google/gemini-2.5-pro`
- `google/gemini-2.5-flash`
- `google/gemini-2.5-flash-lite`
- `google/gemini-2.0-flash`
- `google/gemini-2.0-flash-lite`
- `google/gemma-4-31b-it`
- `google/gemma-4-26b-a4b-it`

## Operating pattern for weaker/free-tier models

1. Keep boot context small.
2. Put project context in small focused files.
3. Give one job per turn.
4. Use explicit input/output formats.
5. Publish artifacts here instead of relying on chat history.
6. Use checklists and scripts to reduce reasoning load.
7. Escalate only hard planning/debugging to stronger fallback models.

## Secret handling

Google API key lives locally in Christopher's Linux secrets area and is mirrored into OpenClaw's private `.env`. Do not commit keys to this repo.
