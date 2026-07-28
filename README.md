# Higher Applications of Maths — RStudio Workbook

Interactive workbook teaching statistics with RStudio for the Higher
Applications of Mathematics course. Live at
**[rstudio.clellandmaths.com](https://rstudio.clellandmaths.com)**.

Code blocks run **in the browser** via [webR](https://docs.r-wasm.org/webr/latest/),
so learners need nothing installed to try the examples.

## ⚠️ `index.html` is generated — do not edit it

`index.qmd` is the source. `index.html` and `index_files/` are Quarto build
output. Editing the HTML directly means your change is lost the next time
anyone renders.

```
index.qmd        ← edit this
index.html       ← generated, committed so the site can be served statically
index_files/     ← generated assets, committed for the same reason
*.csv            ← datasets the workbook loads
logo.webp        ← used as the favicon
```

## Building

Requires [Quarto](https://quarto.org) and the webR extension. **The extension is
not optional** — the workbook has 85 `{webr-r}` blocks and the render fails
without it:

```bash
quarto add coatless/quarto-webr   # creates _extensions/ — commit that folder
quarto render                     # regenerates index.html + index_files/
```

> **Not yet committed:** `_extensions/`. Until it is, a fresh clone cannot
> render this workbook — you have to run `quarto add` first. Committing the
> folder is Quarto's own recommendation and makes the repo self-contained.

Commit the regenerated `index.html` and `index_files/` along with your `.qmd`
change, or the published site will not reflect the edit.

## Contents

Loading a dataset · descriptive statistics · boxplots · tables · histograms ·
scattergraphs · correlation and linear regression · t-tests · z-tests · past
paper questions with worked solutions · troubleshooting · the Data Booklet
command reference.

## Where this is used

- **`rstudio.clellandmaths.com`** — this repo, deployed directly.
- **`clellandmaths.com`** — the main site links here from the Higher
  Applications *Software Skills → RStudio Workbook* topic. If a copy is ever
  served from the main domain, **this repo stays the source of truth** and that
  copy is a deployment artefact — never edit it there.

The favicon is loaded from this repo's raw GitHub URL, so the repository needs
to stay public and keep its current name for the icon to resolve.
