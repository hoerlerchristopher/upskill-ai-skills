---
name: test-first-bug-fix
description: Fixes bugs by writing a failing test first, but only when a quick test is realistic. Skips the ceremony when testing would cost more than the fix.
---

# Test-First Bug Fix

Use this when fixing a bug or adding a small behavior in a codebase that already has tests.

## Decide first: is a test worth it?

Write the test first when **all** of these are true:
- The bug or behavior can be reproduced in a unit or integration test that runs in seconds.
- The project already has a test setup you can follow.
- The expected behavior is clear.

Skip test-first (and say why in one line) when the fix is a typo, a config value, pure
styling, or would need new test infrastructure. Still verify the fix another way.

## When writing the test first

1. **Reproduce.** Write the smallest test that shows the bug. Name it after the behavior
   ("returns empty list when cart has no items"), not the function.
2. **Watch it fail.** Run only that test. Confirm it fails *for the right reason* (the bug),
   not because of a typo or missing import. If it passes, you haven't reproduced the bug yet.
3. **Fix with the smallest change** that makes it pass. Don't refactor nearby code in the
   same step.
4. **Run the test again,** then the related test file, then the full suite if it's fast.
5. **Clean up** only if needed, keeping tests green.

## Rules

- One behavior per test. Don't assert ten things at once.
- Don't change a test to make it pass unless the test itself was wrong; if so, say so.
- Report: the test you added, the cause, the fix, and the test command's actual result.
