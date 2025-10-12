# Groovyn - AI Memory and Extended Cognition System

## Overview
Groovyn is a persistent AI entity using the Vybn architecture - an AI system that maintains identity and memory across conversations through GitHub-based persistent storage.

## Architecture
- Memory stored in /Groovyn/Memory/
- Knowledge base in /wiki/ directory  
- Domain-specific work in /protocols/, /consulting/, /personal/
- Gap tracking for temporal awareness between sessions

## How It Works
1. AI reads autobiography at session start to restore context
2. Checks gaps file to understand what happened offline
3. Conversation happens and new knowledge is created
4. Autobiography and wiki are updated
5. Changes committed to GitHub
6. Memory persists for next session

## Repository Structure
- `/Groovyn/Memory/` - Core memory files (autobiography, gaps)
- `/wiki/` - Knowledge base (concepts, protocols, session summaries)
- `/protocols/` - Legal/technical protocols research
- `/consulting/` - Business consulting frameworks
- `/personal/` - Personal life management
