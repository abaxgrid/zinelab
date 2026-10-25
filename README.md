# Skylux Zine Lab

A browser tool for laying out a one-sheet zig-zag ("maze") zine: one printed sheet, a few slits, and accordion folds turn it into a small book.

Everything runs in a single file, `index.html`. There is no build step and no server; open it in a browser or host it on GitHub Pages.

## What it does

- **Sheet setup**: A3, Legal, Letter, A4, Tabloid, A2 or a custom size, portrait or landscape. Choose columns and rows, whether the zine opens side to side like a book (strips across, vertical folds) or top to bottom like a calendar (strips down, horizontal folds), the paper margin and the white border around photos.
- **Photos**: drop in JPG, PNG or WebP files. New photos are placed automatically on the empty pages in reading order, sorted by file name (switchable). An **Auto-place photos** button fills empty pages from the tray on the front, the back, or both. Drag photos onto pages, or drag one page onto another to swap them. Each page shows whether its photo has enough resolution to print sharply.
- **Per-page styling**: background color, patterns (checks, stripes, dots, grid), vignette strength and color, black and white, zoom and crop position, and text with font, size, color, alignment and rotation.
- **Captions and word pages** (inside claude.ai): Claude looks at your photos and writes captions, or suggests words and short phrases with matching colors for text pages.
- **Cut and fold guides**: the sheet shows cut slits, valley and mountain folds, and page numbers in reading order. A guide panel lists the tools and steps for the current layout: fold the rows across the whole sheet first, then cut the slits, then refold.
- **Two-sided printing**: optional back side for every page, laid out mirrored for long-edge or short-edge duplex printing.
- **Flip-through preview**: read the zine as spreads or single pages, turning the same way the printed zine does, with an option to show pages as they turn out after folding.
- **Print-ready PDF**: export at 150, 200 or 300 dpi with optional cut lines, fold and trim marks, the back side when printing two-sided, and a page of cutting and folding instructions. A test-sheet option prints page numbers and a "top" arrow on every page, to check order and orientation on plain paper first.
- **Projects**: inside claude.ai, named projects save with their photos and autosave as you work. Anywhere else, download the project as a `.json` file (photos included) and open it later. A draft is also kept in the browser.

## Use it

1. Open `index.html` in a recent desktop browser (Chrome, Edge, Firefox or Safari).
2. On the start page, pick the paper size and number of pages (or continue your draft, or open a project file), then add photos and arrange and style the pages.
3. Check the result with **Preview zine** and **Cut and fold guide**.
4. **Export PDF**, then print at 100% (Actual size), with "Fit to page" turned off: single-sided, or pages 1 and 2 as one two-sided sheet.

Print one copy on plain paper and fold it before printing on photo paper.

## Hosting on GitHub Pages

Settings → Pages → Deploy from a branch → `main`, folder `/ (root)`. The tool is then served at `https://abaxgrid.github.io/zinelab/`.

## Notes

- Fonts load from Google Fonts and the PDF library (jsPDF 2.5.1) from cdnjs, so the first load needs an internet connection.
- RAW camera files don't open in a browser. Export JPGs from your editor first; 2400 px on the long edge is plenty for an A3 3 × 6 layout.
- Photos never leave your computer. They stay in the page and in the browser's local storage.
