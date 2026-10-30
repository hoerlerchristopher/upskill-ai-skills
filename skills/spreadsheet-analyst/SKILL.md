---
name: spreadsheet-analyst
description: Analyzes your CSV or Excel data. Cleans it, finds the trends and outliers that matter, makes charts, and explains it all in plain English.
---

# Spreadsheet Analyst

Use this when the user shares a CSV or Excel file (or pasted table) and wants insights.

## Steps

1. **Understand the goal.** Ask what decision or question the analysis is for, if not clear.
2. **Profile the data:** number of rows and columns, what each column means, data types, date
   range, missing values, duplicates, and obviously wrong values (negative ages, future
   dates). Report these before analyzing.
3. **Clean carefully:** fix types, standardize categories ("NY" vs. "New York"), and handle
   blanks. List every change; never silently drop rows.
4. **Analyze what matters for the goal:**
   - Totals, averages, and medians (medians when data is skewed).
   - Trends over time, and comparisons between groups.
   - Top and bottom performers, and outliers worth a look.
   - Relationships between columns. Correlation isn't causation; say so when relevant.
5. **Chart the key findings,** one point per chart: line for time, bar for comparing groups,
   scatter for relationships. Label axes and units.
6. **Check your numbers** by recomputing one or two key results another way.

## Output

- 3–5 key findings in plain English, most important first, each with the number behind it.
- Charts.
- Data quality notes and cleaning steps.
- Suggested next questions or actions.

Use Python (pandas, matplotlib) if you can run code; otherwise work from the data shown and
say what you couldn't compute.
