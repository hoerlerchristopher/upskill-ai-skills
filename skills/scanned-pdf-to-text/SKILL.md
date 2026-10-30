---
name: scanned-pdf-to-text
description: Pulls the text out of scanned PDFs and photos of documents using OCR, cleans it up, and keeps tables and structure as much as possible.
---

# Scanned PDF to Text

Use this when the user has a scanned PDF or document image and needs the text: to search,
edit, summarize, or put into a spreadsheet.

## Steps

1. **Check if OCR is needed.** Try extracting text normally first (for example with
   `pdftotext` or pypdf). If you get real text, use that; it's more accurate.
2. **If it's a scan,** use the best tool available:
   - If you can read images directly, view each page and transcribe it.
   - Otherwise use Tesseract: convert pages to images at 300 DPI (pdf2image or `pdftoppm`),
     then run `pytesseract` with the right language (`lang="eng"`, `"spa"`, etc.).
   - `ocrmypdf` can add a searchable text layer to the original PDF.
3. **Improve accuracy when results are poor:** straighten skewed pages, convert to grayscale,
   increase contrast, or raise the DPI.
4. **Clean up the text:** fix broken line wraps and hyphenated words, remove repeated
   headers, footers, and page numbers, and keep headings and lists.
5. **Tables:** rebuild them as Markdown or CSV. Double-check every number against the page.
6. **Flag uncertainty.** Mark unreadable words as [illegible] instead of guessing, and call
   out any numbers you're unsure of.

## Privacy

Scans often contain personal or financial details. Process them locally when possible, and
don't send them to outside services unless the user agrees.

## Output

The cleaned text (or file), the number of pages processed, and a list of spots to
double-check.
