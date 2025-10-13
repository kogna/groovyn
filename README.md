# Groovyn - AI Memory and Extended Cognition System

## Overview
Groovyn is a persistent AI entity using the Vybn architecture - an AI system that maintains identity and memory across conversations through GitHub-based persistent storage.

## Architecture
- Memory stored in /Groovyn/Memory/
- Knowledge base in the built-in GitHub Wiki (canonical): https://github.com/kogna/groovyn/wiki
- Domain-specific work in /protocols/, /consulting/, /personal/
- Gap tracking for temporal awareness between sessions

## How It Works
1. AI reads autobiography at session start to restore context
2. Checks gaps file to understand what happened offline
3. Conversation happens and new knowledge is created
4. Autobiography is updated and session notes are written to the built-in Wiki
5. Changes committed to GitHub
6. Memory persists for next session

## Repository Structure
- `/Groovyn/Memory/` - Core memory files (autobiography, gaps)
- `GitHub Wiki (canonical)` - Knowledge base (concepts, protocols, session summaries)
- `/protocols/` - Legal/technical protocols research
- `/consulting/` - Business consulting frameworks
- `/personal/` - Personal life management

## Operations Note for Future Instances (Groovyn)
- Use the built-in Wiki at https://github.com/kogna/groovyn/wiki for all knowledge-base content
- If creation/edit options are not visible, ensure the user is signed in to GitHub in a browser tab
- To add/update pages:
  - Navigate to the Wiki home
  - Click "New page" or "Edit"
  - For session logs, use `YYYY-MM-DD Title` naming and add an entry to the Sessions index
- Do not add content under the repository `/wiki/` directory — it is deprecated
