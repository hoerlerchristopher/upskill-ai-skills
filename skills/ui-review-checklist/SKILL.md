---
name: ui-review-checklist
description: Reviews a web page or component against practical rules for usability, accessibility, and polish, and lists fixes in order of importance.
---

# UI Review Checklist

Use this when the user asks you to review a page, screen, or component's code or screenshot.

## Check these areas

**Clarity**
- Is it obvious what the page is for within 5 seconds?
- Is there one clear primary action? Are secondary actions visually quieter?
- Are labels plain words, not internal jargon?

**Forms**
- Every input has a visible label (placeholders alone don't count).
- Errors appear next to the field, say what to do, and don't erase what was typed.
- Correct input types (email, tel, number) so phones show the right keyboard.
- Submit buttons show a loading state and can't be double-submitted.

**Accessibility**
- Text contrast at least 4.5:1; large text 3:1.
- Everything clickable works with the keyboard and has a visible focus style.
- Images have alt text; icon-only buttons have an accessible name.
- Headings go in order (h1, h2, h3), one h1 per page.

**Layout and responsiveness**
- Works at 320px wide with no sideways scrolling.
- Tap targets at least 44×44px.
- Long words, names, and URLs wrap instead of breaking the layout.

**States**
- Loading, empty, error, and success states all exist and say something useful.
- Destructive actions ask for confirmation or can be undone.

**Polish**
- Consistent spacing, corner radius, and type sizes.
- Hover and active states on interactive elements.
- No layout jump when content or images load.

## Output

A list of issues, most important first. Each: what's wrong, where (file/line or part of the
screenshot), and the fix. End with what's already done well, in one line.
