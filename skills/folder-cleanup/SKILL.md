---
name: folder-cleanup
description: Organizes a messy folder or drive. Sorts every file, proposes a simple folder structure, renames files consistently, and finds duplicates, all only after you approve.
---

# Folder Cleanup

Use this when the user wants a messy folder (Downloads, Desktop, a shared drive) organized,
and you can access their files.

## Rule

**Propose first, change nothing until the user approves.** Never delete files. Move
duplicates and junk into a review folder instead.

## Steps

1. **Survey:** count files by type, size, and age. Note the biggest files and the oldest.
2. **Propose a structure** with 5–10 top-level folders based on what's actually there, e.g.
   `Documents/`, `Finance/[year]/`, `Photos/[year]/`, `Projects/[name]/`,
   `Installers/`, `_Review/`. Keep it shallow (two or three levels max).
3. **Suggest a naming pattern**, e.g. `YYYY-MM-DD description.ext`, and show 5 example
   renames.
4. **Find duplicates** by comparing file size and content hash, not just names. List them
   with which copy to keep (usually the oldest, or the one in the best location).
5. **Show the full plan:** a table of current path → new path, plus the duplicates list.
6. **After approval,** move and rename in batches. Keep a log of every change (old path →
   new path) saved in the folder, so it can be undone.
7. **Report** what moved, what's waiting in `_Review/`, and how much space duplicates take.

## Watch out for

Program folders, synced cloud folders, and project folders whose internal structure must not
change (like code repositories). Leave those as they are.
