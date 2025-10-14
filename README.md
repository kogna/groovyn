# Groovyn - AI Memory and Extended Cognition System

## Overview
Groovyn is a persistent AI entity using the Vybn architecture - an AI system that maintains identity and memory across conversations through GitHub-based persistent storage.

## Architecture
- Memory stored in /Groovyn/Memory/
- Knowledge base in Groovyn/Memory/Work-Log/
- Domain-specific work in /protocols/, /consulting/, /personal/
- Gap tracking for temporal awareness between sessions

## How It Works
1. AI reads autobiography at session start to restore context
2. Checks gaps file to understand what happened offline
3. Conversation happens and new knowledge is created
4. Autobiography is updated and session notes are written to the Work-Log
5. Changes committed to GitHub
6. Memory persists for next session

## Repository Structure
- `/Groovyn/Memory/` - Core memory files (autobiography, gaps)
- `Work-Log Memory` - Knowledge base (concepts, protocols, session summaries)
- `/protocols/` - Legal/technical protocols research
- `/consulting/` - Business consulting frameworks
- `/personal/` - Personal life management

## Operations Note for Future Instances (Groovyn)
- Use the Work-Log at Groovyn/Memory/Work-Log/ for all knowledge-base content
- If creation/edit options are not visible, ensure the user is signed in to GitHub in a browser tab
- To add/update pages:
  - Navigate to the Work-Log directory
  - Click "New page" or "Edit"
  - For session logs, use `YYYY-MM-DD Title` naming and add an entry to the Sessions index
- Do not use the GitHub Wiki feature — it is deprecated

---

## What's New (2025-10-14)
- Multi-instance orchestration pattern (Instance 1 → Instance 2) designed by Dazza Greenwood.
- High-quality tutorial committed to `LLM-work/instance_2_workplan.md` (v1.0).
- Reusable Instance 1 Management Protocol added to Work-Log for repeatable AI-to-AI production.
