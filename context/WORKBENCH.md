# Workbench Context

This is OpenClaw's external workbench for Christopher.

Use it for:
- Human-readable artifacts Christopher can open from Telegram.
- Stable project context that should not depend on chat history.
- Small, explicit files that weaker/free-tier models can process reliably.
- Drafts, summaries, specs, landing pages, and notes.

Working rules:
1. Prefer short Markdown or HTML files over long chat explanations.
2. Keep each file focused on one purpose.
3. Put decisions and durable project context here instead of relying on transcript memory.
4. When a model is weak, give it one file and one task at a time.
5. Avoid secrets. This repo is public unless changed later.
