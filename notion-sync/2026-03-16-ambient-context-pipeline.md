---
title: Ambient Context Pipeline — Architecture + GitHub Setup
date: 2026-03-16
platform: Claude
momentum: High
---

# Ambient Context Pipeline — Architecture + GitHub Setup

**Date:** 2026-03-16  
**Platform:** Claude  
**Momentum:** High

## What I Worked On

Researched A2A protocol current status (v0.3, Linux Foundation, 150+ orgs, slower grassroots adoption than MCP but enterprise momentum real). Synthesised all previous LLM context-sharing ideas across 18 months into a unified map (manual handoffs → shared databases → MCP bus → orchestration pipelines → OpenClaw/A2A). Wrote the Ambient Context Pipeline conception document — full architecture with 4 implementation branches (MVP through full A2A node). Created Claude Code prompt for adding conception doc to cognitive-ecosystem GitHub repo. Discussed GitHub structure and organisation options.

## Key Decisions

Pipeline to live in cognitive-ecosystem GitHub repo (not a new repo). Start with Branch A (Notion context event schema) before anything else. Zo is the orchestration layer. Notion is the shared memory bus. GitHub audit handed to Claude Code.

## Next Actions

1. Design Notion Context Event database schema (Branch A)
2. Build Zo daemon to monitor Notion context events (Branch B)
3. Consider adding GitHub MCP as a proper Claude connector

## Critical Context

Conception doc + Claude Code prompt saved to outputs as DCOS-context-pipeline-conception.md and prompt-github-audit.md. Conception doc and context-event schema pushed to cognitive-ecosystem GitHub repo by Claude Code. GitHub repo: https://github.com/liquescentremedies/Cognitive-Ecosystem. A2A now under Linux Foundation — MCP donated to AAIF (Anthropic + OpenAI + Block + Google), 97M monthly SDK downloads. Full pipeline architecture: Notion (shared memory) → Zo daemon (orchestration) → OpenClaw sessions_send (agent comms) → A2A Agent Card (future).

---
*Synced from Notion Session Log*
