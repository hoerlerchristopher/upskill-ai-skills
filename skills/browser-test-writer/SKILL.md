---
name: browser-test-writer
description: Turns a plain-English scenario like "user signs up and sees the welcome page" into a working Playwright end-to-end test.
---

# Browser Test Writer

Use this when the user describes something a user does on a website and wants an automated
browser test for it.

## Steps

1. **Write the scenario as steps,** each with an expected result. Confirm them with the user
   if the scenario is vague.
2. **Look at the app** (the code, or the page if you can open it) to find the real labels,
   buttons, and URLs. Don't guess selectors.
3. **Write the test with Playwright Test:**
   - Prefer user-facing locators: `getByRole("button", { name: "Sign up" })`,
     `getByLabel("Email")`, `getByText(...)`. Use `data-testid` only as a fallback.
   - Use web-first assertions that wait automatically:
     `await expect(page.getByRole("heading", { name: "Welcome" })).toBeVisible()`.
   - Never use fixed waits like `waitForTimeout`.
   - One scenario per test, with a name that describes the behavior.
   - Set up test data through the app's API or fixtures, not by clicking through unrelated
     pages.
4. **Follow the project's setup:** existing config, base URL, folder, and helpers.
5. **Run it** (`npx playwright test path/to/file`) and fix failures until it passes for the
   right reason. Make sure it can fail: break the expected text once and confirm it fails.

## Output

The test file, the command to run it, and the actual result of running it.
