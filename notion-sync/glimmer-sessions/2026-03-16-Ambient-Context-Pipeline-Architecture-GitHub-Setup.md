---
title: "Ambient Context Pipeline — Architecture + GitHub Setup"
date: 2026-03-16
key_decisions: "Pipeline to live in cognitive-ecosystem GitHub repo (not a new repo). Start with Branch A (Notion context event schema) before anything else. Zo is the orchestration layer. Notion is the shared memory bus. GitHub audit handed to Claude Code."
platform: "Claude"
what_i_worked_on: "Researched A2A protocol current status (v0.3, Linux Foundation, 150+ orgs, slower grassroots adoption than MCP but enterprise momentum real). Synthesised all previous LLM context-sharing ideas across 18 months into a unified map (manual handoffs → shared databases → MCP bus → orchestration pipelines → OpenClaw/A2A). Wrote the Ambient Context Pipeline conception document — full architecture with 4 implementation branches (MVP through full A2A node). Created Claude Code prompt for adding conception doc to cognitive-ecosystem GitHub repo. Discussed GitHub structure and organisation options."
momentum_score: "High"
next_actions: "1. Design Notion Context Event database schema (Branch A). 2. Build Zo daemon to monitor Notion context events (Branch B). 3. Consider adding GitHub MCP as a proper Claude connector."
critical_context: "Conception doc + Claude Code prompt saved to outputs as DCOS-context-pipeline-conception.md and prompt-github-audit.md. Conception doc and context-event schema pushed to cognitive-ecosystem GitHub repo by Claude Code. GitHub repo: https://github.com/liquescentremedies/Cognitive-Ecosystem. A2A now under Linux Foundation — MCP donated to AAIF (Anthropic + OpenAI + Block + Google), 97M monthly SDK downloads. Full pipeline architecture: Notion (shared memory) → Zo daemon (orchestration) → OpenClaw sessions_send (agent comms) → A2A Agent Card (future)."
notion_id: 325755ec-7e2c-8197-9c19-f2ed29a68e82
---

