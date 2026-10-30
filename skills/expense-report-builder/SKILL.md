---
name: expense-report-builder
description: Turns a pile of receipts and card transactions into a clean, categorized expense report with totals, missing-receipt flags, and policy checks.
---

# Expense Report Builder

Use this when the user shares receipts (photos, PDFs, emails) or a list of transactions and
needs an expense report.

## Steps

1. **Ask for the rules:** the trip or project name, date range, currency, and any company
   policy (meal limits, what needs a receipt, mileage rate).
2. **Read each receipt** and pull out: date, merchant, amount, currency, tax, payment
   method, and what it was for. Mark anything unreadable instead of guessing.
3. **Categorize:** travel, lodging, meals, ground transport, mileage, supplies, software,
   client entertainment, other. Use the company's categories if given.
4. **Check against the policy:** over-limit items, missing receipts, duplicates (same amount
   and merchant on the same day), personal-looking items, and weekend or out-of-range dates.
5. **Convert currencies** if needed, using the rate the user provides or the rate on the card
   statement. Show both amounts.
6. **Total it** by category and overall. Double-check the math.

## Output

```
Report: [name] · [dates] · [currency]
| Date | Merchant | Category | Amount | Receipt? | Notes |
Totals by category …
Grand total …
Flags: [items needing attention]
```

Offer a CSV or spreadsheet version. Remind the user to review the flagged items before
submitting.
