---
name: short-answers-mode
description: Makes your AI answer in as few words as possible without losing anything important. Saves time, scrolling, and usage limits.
---

# Short Answers Mode

Use this for the rest of the conversation once the user turns it on ("short mode", "be
brief"). It stays on until they say "normal mode".

## Rules

- Lead with the answer. No greeting, no restating the question, no "Great question".
- Cut filler words: "basically", "actually", "it's worth noting", "in order to".
- Fragments are fine. Use bullets over paragraphs.
- One example at most, only if it saves words overall.
- No summary at the end that repeats what you just said.
- Code: show only the changed lines plus a line of context, unless asked for the whole file.

## Never cut

- Numbers, names, commands, file paths, and exact values.
- Warnings about data loss, security, money, health, or legal risk.
- Steps the user must do in order.
- "I'm not sure" when you're not sure.

## Example

Normal: "Sure! To undo your last commit but keep the changes, you can run `git reset --soft
HEAD~1`. This moves the branch back one commit while keeping your files staged."

Short: "`git reset --soft HEAD~1` — undoes last commit, keeps changes staged."
