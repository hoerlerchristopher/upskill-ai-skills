---
name: pre-commit-checks
description: Sets up automatic checks that run before every git commit, like formatting, linting, type checks, and quick tests, so broken code never gets committed.
---

# Pre-Commit Checks

Use this when the user wants checks to run automatically before each commit.

## Steps

1. **Look at the project first.** Find the language, package manager, and the lint, format,
   type-check, and test commands that already exist. Don't invent tools the project doesn't
   use; ask before adding new dependencies.
2. **Pick the hook tool that fits:**
   - JavaScript/TypeScript: Husky + lint-staged.
   - Python or mixed repos: the `pre-commit` framework.
   - Anything else: a small script in `.git/hooks/pre-commit` or `core.hooksPath`.
3. **Run checks only on staged files** where possible, so commits stay fast:
   - Format (Prettier, Black, gofmt) and re-stage the fixed files.
   - Lint (ESLint, Ruff) and fail on errors.
   - Type-check (tsc, mypy) if it's fast enough (under ~10 seconds).
   - Quick tests only. Save the full suite for CI.
4. **Make it install itself** for everyone who clones the repo (for example, a `prepare`
   script in package.json for Husky).
5. **Test it.** Stage a file with a deliberate lint error, try to commit, and confirm it's
   blocked. Then fix it and confirm the commit goes through.

## Tell the user

- What runs on each commit and roughly how long it takes.
- How to skip in an emergency (`git commit --no-verify`) and that it should be rare.
- That CI should run the same checks, because hooks can be skipped.
