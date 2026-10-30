---
name: docs-seo-check
description: Audits your README, docs, or help pages for search visibility, covering titles, descriptions, headings, keywords, readability, and broken links, with fixes ready to paste.
---

# Docs SEO Check

Use this when the user wants their documentation, README, or help center to be easier to
find in search (and in AI search).

## Check each page for

1. **Title** — unique, under ~60 characters, starts with the main topic ("Install the CLI
   on Windows", not "Getting started (2)").
2. **Description** — a meta description or opening paragraph of 120–160 characters that says
   what the page helps with.
3. **Headings** — one H1, then H2/H3 in order. Headings phrased the way people search ("How
   to reset your API key").
4. **Keywords** — the words users actually type, used naturally in the title, first
   paragraph, and a heading. Product jargon is explained the first time.
5. **Answer first** — the solution near the top; background after.
6. **Readability** — short paragraphs, steps as numbered lists, code in code blocks, and
   images with alt text.
7. **Links** — no broken links; descriptive link text (not "click here"); related pages
   linked to each other.
8. **Duplicates** — pages covering the same thing, which should be merged or point to one
   main version (canonical).
9. **Freshness** — outdated versions, screenshots, or commands.

## Output

A table: page, issue, priority (high/medium/low), and the fix. Then rewritten titles,
descriptions, and opening paragraphs for the top pages, ready to paste.
