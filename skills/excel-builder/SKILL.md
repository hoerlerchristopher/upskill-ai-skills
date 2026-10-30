---
name: excel-builder
description: Creates and edits real Excel files with formulas, formatting, charts, and multiple sheets, using Python's openpyxl.
---

# Excel Builder

Use this when the user wants an .xlsx file made or changed (a tracker, budget, report, or
template) and you can run Python.

## Steps

1. **Plan the workbook** before coding: sheet names, columns, which cells are inputs vs.
   formulas, and what the user will do with it. Confirm if it's more than a simple table.
2. **Build with openpyxl** (`pip install openpyxl`):
   - Use real **formulas** (`ws["D2"] = "=B2*C2"`) instead of pasting calculated values, so
     the sheet stays live.
   - Use **number formats** for money, percentages, and dates
     (`cell.number_format = '"$"#,##0.00'`).
   - **Header row:** bold, filled, frozen (`ws.freeze_panes = "A2"`), with auto-filter.
   - **Column widths** sized to the content.
   - **Data validation** for dropdowns, and **conditional formatting** for highlights.
   - Turn data into an Excel **Table** when the user will add rows.
   - **Charts** with `openpyxl.chart` (bar, line, pie) pointing at the data range.
3. **When editing an existing file,** load it with `load_workbook`, change only what was
   asked, and save under a new name unless told to overwrite. Note: openpyxl doesn't keep
   some features (like pivot tables or macros); warn before saving over files that have them.
4. **Check the result:** reopen the file, confirm formulas reference the right cells, and
   that nothing shows an error.

## Output

The file, plus a short guide: what each sheet is for and which cells to fill in.
