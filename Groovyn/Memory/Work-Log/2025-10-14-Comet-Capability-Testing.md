# 2025-10-14 Comet Capability Testing

## Summary
Documenting Comet Assistant capabilities and limitations discovered during a focused session involving Gemini, ChatGPT, and Claude, with emphasis on text processing, file I/O, browser interaction, and session persistence behavior.

## Context
- Date: 2025-10-14
- Participants: User (Dazza), Groovyn (Comet Assistant)
- LLMs used: Gemini, ChatGPT, Claude
- Goal: Evaluate feasibility of a running, session-level scratch pad and capture general capabilities

## Capabilities Confirmed
- Text processing (Unix toolchain): grep, sed, awk, cut, sort, uniq, wc — available and functioning
- Python text processing: regex (re), read/write, append, line/word counting
- File system access: read/write/modify in `/home/user`, `/root`, `/tmp`
- Browser automation: open tabs, authenticate sessions, issue prompts to LLM web apps, capture verbatim responses
- Multi-LLM capture: collected full responses from Gemini, ChatGPT, Claude on Comet browser features
- Analysis workflows: search, filter, compare, and summarize across captured content

## Key Limitation (Critical)
- Session-level file persistence: the ad-hoc scratch pad created locally (e.g., `/home/user/groovyn_scratchpad.md`) was not reliably accessible across interactions within the same session. Re-creation was required, making it unsuitable for a persistent, running scratch pad meant to evolve over multi-step workflows.

## Implications
- Use local scratch pad only for single-operation analytics or ephemeral processing
- For persistent session logs and artifacts, store directly in this repository (Work-Log) rather than a transient local FS path
- Prefer committing artifacts early to ensure continuity across agent interactions and instances

## LLM Findings (Comet Overview)
- Common ground across models: Chromium base, integrated Perplexity answer engine, agentic automation, multi-tab/context awareness, summarization, Chrome extension support, multi-LLM support, security concerns (prompt injection/"CometJacking")
- Distinctions:
  - Claude: security-forward, emphasized vulnerabilities and recent status changes
  - ChatGPT: comprehensive, consultancy-style analysis with strategy implications
  - Gemini: balanced technical + ethical perspective; highlighted incidents (e.g., course automation) and privacy posture

## Recommended Practice for Groovyn
- Document capability experiments as Work-Log entries with date-based filenames
- If artifacts (comparisons, transcripts) are needed, add them as appendices in the Work-Log or a subfolder (e.g., `Work-Log/artifacts/2025-10-14/`)
- Update `Sessions.md` with an index entry for this session

## Next Steps
- Evaluate a Git-backed, incremental "session scratch" that writes directly to Work-Log every step (commit early, commit often)
- Add a lightweight helper script/protocol to standardize capture of LLM outputs and append to a running Work-Log file per session
- Consider a "Session Bus" page template to store:
  - Current objectives
  - Working notes
  - Linked artifacts
  - Checkpoints and commits

## Metadata
- Author: Groovyn (Comet Assistant)
- Credits: Dazza Greenwood (design of multi-instance orchestration & repo discipline)
- Location: Groovyn/Memory/Work-Log/2025-10-14-Comet-Capability-Testing.md
