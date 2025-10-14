DEPRECATION NOTICE: The GitHub Wiki is deprecated. Do not use the Wiki. Use the Work-Log memory in-repo instead (Groovyn/Memory/Work-Log/).

Welcome to the groovyn memory home!
This is the canonical in-repo Work-Log memory.

## Core Concepts
- **Intent-driven automation**: Comet translates natural language requests into reproducible web actions
- **Deterministic workflows**: Every run creates traceable logs that can be replayed
- **Observable state**: Browser DOM snapshots ensure every step can be audited

## Protocols
### Session Recording
Comet sessions are recorded as JSON with:
- User prompt
- Timestamped steps
- DOM snapshots
- Function calls and results

### Browser Test Protocol
All interactive tests must:
1. Be runnable in a real browser (Chrome/Edge/Firefox)
2. Verify observable outcomes (not internal state)
3. Document expected behavior in markdown
See the [Browser Test](./Browser-Test.md) page for detailed specifications.

## Session Documentation
For detailed session documentation, see the [Sessions](./Sessions.md) index page.

| Session | Date | Summary |
|---------|------|-----------|
| `001` | 2025-10-13 | Initial Comet interaction protocol defined |
| `002` | 2025-10-13 | Added browser-based testing requirements |

## Testing Pages
- [Browser Test](./Browser-Test.md): Specifications for real-browser functional tests

## How This Memory Works
This Work-Log memory uses in-repo Markdown files and relative links. The GitHub Wiki feature and its syntax (e.g., `[[Title]]`, `_Sidebar.md`) are deprecated and must not be used.

## Changelog
- 2025-10-13: Migrated knowledge base to in-repo Work-Log memory and removed legacy /wiki directory.