## 11. Critical Lessons Learned - Content Preservation Protocol

This section documents the 2025-10-14 incident where an initial attempted revision would have deleted substantial original content in `LLM-work/groovyn-vs-ai-agent-systems.md`. Resolution and preventative measures:

- Addition-only mandate for improvement rounds unless explicit deletion is requested and approved
- Pre-commit checks: length comparison vs. original, section preservation confirmation
- Instance 2 must present first/last 500 chars preview prior to commit authorization
- All commits must use GitHub MCP API tools; browser-UI commits are disallowed
- Instance 1 must halt if any reduction is detected and seek user guidance

These measures are now standard until superseded by protocol v2.
