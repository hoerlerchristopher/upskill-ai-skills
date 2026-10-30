---
name: accessibility-fixer
description: Finds and fixes accessibility problems in HTML and components so people using keyboards, screen readers, or zoom can use your site.
---

# Accessibility Fixer

Use this when the user wants to make a page or component accessible, or asks why it fails
an accessibility check.

## Steps

1. **Scan the code** for the common problems below and list each one with its location.
2. **Fix them directly** in the code, smallest change first. Prefer native HTML over ARIA:
   a real `<button>` beats a `<div role="button">`.
3. **Explain each fix** in one plain sentence so the user learns the pattern.

## Common problems and fixes

- **Clickable divs/spans** → use `<button>` (actions) or `<a href>` (navigation).
- **Missing labels** → `<label for>` on inputs; `aria-label` on icon-only buttons.
- **Images** → meaningful `alt` text; `alt=""` for decorative images.
- **Focus** → never remove outlines without a visible replacement; keep a logical tab order;
  don't use positive `tabindex`.
- **Dialogs and menus** → move focus in when opened, trap it while open, return it when
  closed, close on Escape.
- **Color** → text contrast 4.5:1; don't use color alone to show errors or status.
- **Forms** → errors linked with `aria-describedby`, announced with a live region, and
  required fields marked in text, not only with a red asterisk.
- **Headings and landmarks** → one `<h1>`, ordered headings, `<main>`, `<nav>`, `<header>`,
  `<footer>`.
- **Motion** → respect `prefers-reduced-motion`.
- **Language** → `<html lang="…">` set.

## Check your work

Tab through the page with the keyboard only. Every action must be reachable and visible.
Mention that a real screen reader test (VoiceOver, NVDA) is the final check.
