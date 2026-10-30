---
name: parallel-task-splitter
description: Spots when a job can be split into independent pieces and hands them to separate AI agents to work on at the same time, then checks and combines their results.
---

# Parallel Task Splitter

Use this when a request has two or more parts that don't depend on each other, and the tool
can run sub-agents or parallel tasks.

## When to split

Split only when the pieces:
- Don't share files or state that both would change.
- Don't need each other's results to start.
- Are each big enough to be worth a separate agent (more than a few minutes of work).

Don't split when tasks touch the same files, must happen in order, or are quick. Do those
yourself, one after another.

## Steps

1. **List the pieces** and confirm they're independent.
2. **Write a self-contained brief for each agent:** the goal, exact files or sources to use,
   what not to touch, and the format of the result. The agent won't see this conversation,
   so include everything it needs.
3. **Run them in parallel.**
4. **Review every result.** Check it did what was asked, didn't overreach, and works. Don't
   pass along an agent's claims without checking them.
5. **Combine** the results, resolve any overlaps, and run a final check on the whole.

## Report

What each agent did, what you checked, and anything that needed fixing.
