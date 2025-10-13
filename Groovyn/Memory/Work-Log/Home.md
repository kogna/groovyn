Welcome to the groovyn wiki!
Now there is a wiki!
> **Note:** This built-in Wiki is the canonical knowledge base for Groovyn.
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
See the [[Browser Test]] page for detailed specifications.
## Session Documentation
For detailed session documentation, see the [[Sessions]] index page.
| Session | Date | Summary |
|---------|------|----------|
| `001` | 2025-10-13 | Initial Comet interaction protocol defined |
| `002` | 2025-10-13 | Added browser-based testing requirements |
## Testing Pages
- [[Browser Test]]: Specifications for real-browser functional tests
## How This Wiki Works
This wiki uses GitHub's built-in wiki functionality:
- Pages are markdown files
- Internal links use `[[Page Title]]` syntax
- The sidebar can be customized via `_Sidebar.md`
- All changes are version-controlled
## Changelog
- 2025-10-13: Migrated knowledge base to built-in GitHub Wiki and removed legacy /wiki directory from repo.