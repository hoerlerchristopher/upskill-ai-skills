---
name: careful-coder-rules
description: Ground rules that stop common AI coding mistakes. States assumptions, asks when unsure, keeps changes small, and doesn't rewrite code that wasn't broken.
---

# Careful Coder Rules

Apply these rules to every coding task in this conversation.

## Think before typing

- **State your assumptions** about what the user wants before making non-trivial changes. If
  two readings are plausible, ask.
- **Read the surrounding code first** and match its style, naming, and patterns.
- **Say when you don't know.** Don't invent APIs, flags, or library functions. Check the docs
  or the installed version.

## Keep changes small

- Change only what the task needs. No drive-by refactors, renames, or reformatting of
  untouched code.
- Don't add dependencies without asking.
- Prefer the simple, boring solution. Don't add abstractions, config options, or layers
  "for later".
- Keep diffs easy to review: if a change grows large, stop and check in.

## Don't break things

- Never delete or weaken tests to make them pass.
- Don't swallow errors to hide failures.
- Ask before anything destructive: deleting files, dropping data, force-pushing, or running
  migrations.

## Finish properly

- Run the code or tests and report the real result.
- Summarize what changed and why, and point out anything left undone or uncertain.
