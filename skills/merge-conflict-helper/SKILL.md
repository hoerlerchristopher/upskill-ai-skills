---
name: merge-conflict-helper
description: Walks through git merge and rebase conflicts one at a time, keeps both sides' intent, and checks that nothing got lost before finishing.
---

# Merge Conflict Helper

Use this when a git merge, rebase, or cherry-pick stops with conflicts.

## Before touching anything

1. Run `git status` to see which operation is in progress and which files conflict.
2. Find out what each side was trying to do: read the commit messages on both branches
   (`git log --oneline` for each side) for the conflicting files.

## For each conflicted file

1. Open each conflict block (`<<<<<<<`, `=======`, `>>>>>>>`). Remember that during a
   rebase, "ours" and "theirs" are swapped compared to a merge, so check which side is which.
2. Decide per block:
   - **Both changes are needed** → combine them by hand. This is the most common case.
   - **One side replaced the other on purpose** → keep that side, and say why.
   - **Unclear** → stop and ask the user. Never guess on business logic.
3. Remove every conflict marker. Search the file for `<<<<<<<` to be sure.
4. For lockfiles (package-lock.json, yarn.lock, etc.), don't hand-edit: take one side, then
   regenerate with the package manager.

## Before finishing

- Build or type-check, and run the tests that cover the changed files.
- `git diff` the result against both sides to confirm no change was dropped.
- Then `git add` the files and continue (`git merge --continue` or `git rebase --continue`).

## Never

- Run `git checkout .`, `git reset --hard`, or `--force` pushes without the user's OK.
- Resolve a whole file with "ours" or "theirs" just to make the conflict go away.

## Report

Each file: what conflicted, what you kept, and why. Then the test results.
