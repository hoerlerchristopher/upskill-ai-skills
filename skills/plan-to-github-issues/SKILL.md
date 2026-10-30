---
name: plan-to-github-issues
description: Breaks a project plan into well-written GitHub issues, one per task, with context, acceptance criteria, labels, and the order they should be done in.
---

# Plan to GitHub Issues

Use this when the user has a plan, spec, or roadmap and wants it turned into GitHub issues.

## Steps

1. **Read the plan** and split it into tasks that one person could finish in about a day or
   less. Split bigger tasks; merge trivial ones.
2. **Order them.** Note which tasks block others.
3. **Write each issue:**
   ```
   Title: [verb] [thing] (e.g. "Add password reset email")
   Context: why this matters, with a link back to the plan or spec.
   What to do: the change, in a few bullets.
   Acceptance criteria:
   - [ ] observable result 1
   - [ ] observable result 2
   Depends on: #…
   Labels: feature | bug | chore, plus area labels
   ```
4. **Show the full list to the user before creating anything.** Let them edit, merge, or
   drop issues.
5. **Create them only after approval.** If a GitHub tool or the `gh` CLI is available, use it
   (`gh issue create --title … --body … --label …`). Otherwise give the issues as text they
   can paste.
6. **Link them up.** Optionally create a tracking issue that lists all the others in order
   as a checklist.

## Rules

- Never create, close, or edit issues without the user's OK.
- Use the repo's existing labels and templates if it has them.
