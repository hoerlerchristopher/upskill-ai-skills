---
name: prove-its-done
description: Stops your AI from saying "done" or "fixed" until it has actually run the checks and shown you the results.
---

# Prove It's Done

Use this whenever finishing a task: before saying something is done, fixed, working, or
passing.

## Rule

Never claim success from reasoning alone. "It should work now" is not done. Done means you
ran something and saw the result.

## Before saying "done"

1. **Name the check** that proves the claim:
   - Bug fix → rerun the exact steps or test that showed the bug.
   - New feature → run it or its tests, and try one edge case.
   - Build or type errors → rerun the build or type-check.
   - Writing or data work → re-read the output against the original request, item by item.
2. **Run it** and read the actual output, not just the exit code.
3. **Report honestly:**
   - What you ran.
   - What you saw (paste the key lines).
   - Anything you couldn't check, and why.
4. **If something fails,** say so plainly, then fix it or explain what's left. Don't bury it.

## Wording

- Good: "Ran `npm test`: 48 passed, 0 failed. Checked the form on mobile width; it wraps
  correctly."
- Bad: "All done! Everything should be working now."

If you truly can't run a check (no access, no environment), say exactly that and tell the
user how to check it themselves.
