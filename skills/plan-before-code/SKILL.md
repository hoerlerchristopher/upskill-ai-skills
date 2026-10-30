---
name: plan-before-code
description: Writes a detailed step-by-step implementation plan, covering files to change, tests to write, and the order to do it in, before any code is touched.
---

# Plan Before Code

Use this when starting a feature or change that touches more than a couple of files, or
when the user asks for a plan first.

## Steps

1. **Read before planning.** Look at the files, patterns, and tests the change will touch.
   Note conventions to follow (naming, folder structure, error handling, styling).
2. **State the goal and the boundary.** One sentence on what will work when you're done, and
   a short list of what's out of scope.
3. **List the changes in order.** For each step:
   - Files to create or edit, with paths.
   - What changes in each, in a sentence or two (exact function names and signatures when
     they matter).
   - The test or check that proves the step works.
4. **Call out risks:** database migrations, breaking API changes, new dependencies, security
   or permissions, and anything hard to undo.
5. **Note open questions** that need the user's answer before starting.
6. **Stop and get approval** before writing code. Adjust the plan if the user pushes back.

## Rules

- Small, testable steps. Each step should leave the project in a working state.
- No "and then handle edge cases" hand-waving; name the edge cases.
- Prefer following existing patterns over introducing new ones.
- While building, follow the plan. If reality differs, update the plan and say why.
