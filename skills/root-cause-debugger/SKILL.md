---
name: root-cause-debugger
description: Debugs failing tests, broken builds, and confusing errors by finding the real cause first instead of guessing and patching.
---

# Root-Cause Debugger

Use this when something is broken: a failing test, a build error, a crash, or behavior that
doesn't match what's expected.

## Rules

- **No fix until you can explain the cause.** Guess-and-patch hides bugs.
- Change one thing at a time, and undo changes that didn't help.
- Read the full error message and stack trace before anything else.

## Steps

1. **Reproduce it.** Find the exact command or steps that show the problem. Note the actual
   result vs. the expected result. If you can't reproduce it, gather more information
   (logs, versions, inputs) before going further.
2. **Narrow it down.**
   - When did it last work? What changed since (code, dependencies, config, data)?
   - Shrink the input until the failure is as small as possible.
   - Split the code path in half with logs or a debugger to find where good turns bad.
3. **Form a hypothesis** in one sentence: "X happens because Y." Predict what you'd see if
   it's true, then check that prediction.
4. **Fix the cause,** not the symptom. Avoid try/catch that swallows errors, retries that
   hide failures, or special-casing one input.
5. **Prove it.** Rerun the reproduction, then the related tests. Add a test that would have
   caught this bug if one is practical.
6. **Recover cleanly.** Remove debug logs and temporary changes.

## Report

Cause (one or two sentences), the fix, how it was verified (with the actual command
output), and anything else that might have the same problem.
