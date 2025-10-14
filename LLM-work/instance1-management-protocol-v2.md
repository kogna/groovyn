# Instance 1 Management Protocol v2 (Additive-Only Guarantee)

This document updates Instance 1 orchestration steps to prevent content loss during iterative improvements.

## Key Additions
- Step 9a: Instance 1 Content Review (preview + length check)
- Step 10a: Content Preservation Verification (addition-only rule)
- Step 10: Commit authorization with preservation constraints
- MCP API requirement for all commits
- Enhanced Step 11 and Step 12 verification/reporting

## Insertions (ready-to-paste snippets)

### Step 9a: Instance 1 Content Review
Before authorizing final commit:
1. Request first 500 and last 500 characters of enhanced version
2. Compare length vs. original; flag significant reductions
3. Verify all original sections remain
4. Only proceed if preservation confirmed

### Step 10a: Content Preservation Verification
Mandatory:
- Length maintained or increased
- Section-by-section intact
- Additions/Enhancements only
- If any reduction: STOP and request guidance

### Step 10 (Rewritten): Authorize Final Commit with Content Preservation
- Reiterate preservation constraints
- Require MCP API commit only
- Confirm preservation post-commit

### Step 11: Final Verification (Enhanced)
- Preservation checks (length/sections) marked ✅

### Step 12: Report (Enhanced)
- Add “Content Preservation Issues” and “Commit Method Issues” fields
