# Browser Test Specification

## Purpose
This page defines how groovyn's Comet assistant should be tested in a real browser environment.

## Requirements

### 1. Real Browser Execution
- Tests MUST run in Chrome, Edge, or Firefox
- No headless-only features
- Visual verification should be possible

### 2. Observable Outcomes
- Test assertions should check:
  - Page content changes
  - DOM structure modifications
  - URL navigation
  - Network requests (via DevTools)
- Do NOT test internal implementation details

### 3. Session Replay
- Every test run should produce a session log
- Session logs should be replayable
- Failed tests should include:
  - DOM snapshot at failure point
  - Full action history
  - Expected vs actual state

## Test Structure

```javascript
// Example test skeleton
test('Comet should complete a multi-step task', async () => {
  // 1. Setup
  const session = await comet.start({
    task: 'Find and summarize the latest GitHub release',
    startUrl: 'https://github.com/kogna/groovyn'
  });
  
  // 2. Execute
  await session.run();
  
  // 3. Verify observable outcomes
  expect(session.finalUrl).toContain('releases');
  expect(session.extractedText).toMatch(/v\d+\.\d+\.\d+/);
  
  // 4. Save session log
  await session.saveLog('./logs/github-release-test.json');
});
```

## Logging Format

Each session log should contain:

```json
{
  "sessionId": "...",
  "timestamp": "2025-10-13T14:30:00Z",
  "task": "User's original request",
  "steps": [
    {
      "stepNumber": 1,
      "action": "navigate",
      "url": "https://...",
      "domSnapshot": "<html>...</html>",
      "timestamp": "2025-10-13T14:30:01Z"
    }
  ],
  "result": "success" | "failure",
  "finalState": {
    "url": "https://...",
    "extractedData": {}
  }
}
```

## CI Integration

- Tests should run on every pull request
- Use GitHub Actions with real browser support
- Archive session logs as artifacts
- Fail builds on assertion failures

## Related Pages

- [[Home]]: Main wiki index