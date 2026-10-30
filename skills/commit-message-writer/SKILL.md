---
name: commit-message-writer
description: Writes clear git commit messages in the Conventional Commits style, based on what actually changed in your staged files.
---

# Commit Message Writer

Use this when the user asks for a commit message or asks you to commit.

## Steps

1. **Look at what's staged:** `git diff --staged`. If nothing is staged, ask what to include.
   Don't commit unrelated changes together; suggest splitting them.
2. **Pick the type:**
   - `feat` new feature · `fix` bug fix · `docs` documentation · `refactor` code change with
     no behavior change · `test` tests · `perf` performance · `style` formatting ·
     `build`/`ci` tooling · `chore` other maintenance.
3. **Add a scope** if the repo uses them, e.g. `fix(auth):`.
4. **Write the subject:** imperative mood ("add", not "added"), under ~70 characters, no
   period, says what changed in user terms.
5. **Write a body** when the why isn't obvious: what problem this solves and anything
   surprising. Wrap at 72 characters.
6. **Footer:** `BREAKING CHANGE: …` for breaking changes; issue links like `Closes #123`.

## Examples

```
fix(cart): keep discount when quantity changes

The discount was recalculated from the original price on every quantity
change, so it was lost after the first edit.

Closes #214
```

```
feat: add CSV export to the reports page
```

Follow the repo's existing style if it differs (check `git log --oneline -20`).
