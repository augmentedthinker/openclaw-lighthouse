# Google Model Ping — 2026-05-03

Prompt used: `Reply with exactly OK.`

## Responding

| Model | Result | Latency |
|---|---:|---:|
| `google/gemini-3-flash-preview` | OK | ~0.7s |
| `google/gemini-3.1-flash-lite-preview` | OK | ~0.6s |
| `google/gemini-2.5-flash` | OK | ~0.7s |
| `google/gemini-2.5-flash-lite` | OK | ~4.6s |
| `google/gemma-4-26b-a4b-it` | Responded, but did not follow exact instruction cleanly | ~3.1s |

## Not currently usable on this key/tier

| Model | Error |
|---|---|
| `google/gemini-3.1-pro-preview` | 429 `RESOURCE_EXHAUSTED` quota |
| `google/gemini-3-pro-preview` | 429 `RESOURCE_EXHAUSTED` quota |
| `google/gemini-2.5-pro` | 429 `RESOURCE_EXHAUSTED` quota |
| `google/gemini-2.0-flash` | 429 `RESOURCE_EXHAUSTED` quota |
| `google/gemini-2.0-flash-lite` | 429 `RESOURCE_EXHAUSTED` quota |
| `google/gemma-4-31b-it` | 500 internal error |

## Current recommended default chain

Primary:
- `google/gemini-3-flash-preview`

Fallbacks:
- `google/gemini-3.1-flash-lite-preview`
- `google/gemini-2.5-flash`
- `google/gemini-2.5-flash-lite`
- `google/gemma-4-26b-a4b-it`
- `openai-codex/gpt-5.5` as emergency fallback while migration is still being hardened

## Notes

The Pro models appear present but blocked by quota on the free-tier key. For everyday Telegram work, prefer Gemini 3 Flash or 3.1 Flash Lite.
