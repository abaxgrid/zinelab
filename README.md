# Skylux Zine Lab

A browser tool for laying out a one-sheet zig-zag ("maze") zine: one printed sheet, a few slits, and accordion folds turn it into a small book.

Everything runs in a single file, `index.html`. There is no build step and no server; open it in a browser or host it on GitHub Pages.

## What it does

- **Sheet setup**: A3, Legal, Letter, A4, Tabloid, A2 or a custom size, portrait or landscape. Choose the number of strips (columns) and pages per strip (rows), the paper margin and the white border around photos.
- **Photos**: drop in JPG, PNG or WebP files, drag them onto pages, drag one page onto another to swap them, or fill empty pages in reading order. Each page shows whether its photo has enough resolution to print sharply.
- **Per-page styling**: background color, patterns (checks, stripes, dots, grid), vignette strength and color, black and white, zoom and crop position, and text with font, size, color, alignment and rotation.
- **Cut and fold guides**: the sheet shows cut slits, valley and mountain folds, and page numbers in reading order. A guide panel lists the tools and steps for the current layout.
- **Flip-through preview**: read the zine as spreads or single pages, with an option to show pages as they turn out after folding.
- **Print-ready PDF**: export at 150, 200 or 300 dpi with optional cut lines, fold and trim marks, and a second page of cutting and folding instructions.
- **Projects**: save a project file (`.json`, photos included) and open it later. A draft is also kept in the browser.

## Use it

1. Open `index.html` in a recent desktop browser (Chrome, Edge, Firefox or Safari).
2. Pick the paper size and grid, add photos, arrange and style the pages.
3. Check the result with **Preview zine** and **Cut and fold guide**.
4. **Export PDF**, then print at 100% (Actual size), single-sided, with "Fit to page" turned off.

Print one copy on plain paper and fold it before printing on photo paper.

## Hosting on GitHub Pages

Settings → Pages → Deploy from a branch → `main`, folder `/ (root)`. The tool is then served at `https://abaxgrid.github.io/zinelab/`.

## Notes

- Fonts load from Google Fonts and the PDF library (jsPDF 2.5.1) from cdnjs, so the first load needs an internet connection.
- RAW camera files don't open in a browser. Export JPGs from your editor first; 2400 px on the long edge is plenty for an A3 3 × 6 layout.
- Photos never leave your computer. They stay in the page and in the browser's local storage.
