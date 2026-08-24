# ADR — decisions behind this site

Short record of *why*, so changes don't undo intent. Snapshot: one small audio handler, 1 stylesheet, 1 breakpoint, 0 dead CSS.

1. **Plain static HTML + CSS, no build step.** The old stub used Quarto (needs a toolchain). Now what you edit is what ships; open a file to preview. Long-form writing lives on Substack, so no Markdown pipeline is needed.
2. **JavaScript is limited to the optional article audio button.** Layout, the responsive card grid, and the dropcap are all native CSS. The small inline handler shared by the CNT and RF-network articles only toggles their existing audio element.
3. **One stylesheet, driven by `:root` tokens.** Re-theming is a one-line edit; a numbered TOC keeps any rule findable. No style duplication.
4. **Header/footer duplicated per page, not a JS/template include.** An include would re-add the dependency #2 removed (nav vanishes if it fails) or a build step (#1). At 5 pages, a find-and-replace is cheaper. *Revisit past ~10 pages.*
5. **EB Garamond via Google Fonts, with a Georgia/Times fallback.** The single typography dependency, chosen deliberately; the page still renders if it fails.
6. **Card grid for posts (matplotlib plot-types style).** Tech Digest uses local `thumbs/`; Writing/Books hotlink each Substack post's *original* cover at its native aspect-ratio — the pre-cropped `og:image` mangled portrait covers. Books and Hobbies reuse the same card/grid/list primitives (no new system); empty slots are CSS placeholder tiles, not generated images.
7. **Cool-neutral palette, one teal accent, in `oklch`.** One accent keeps focus on content; oklch keeps greys/accent perceptually consistent when hue is tweaked.
8. **CV is both a web page and a PDF.** The HTML version is current/accessible; the PDF is the portable artifact. The web copy is intentionally a superset (newer role than the dated PDF).
9. **Generated technical articles still ship as plain static HTML.** Their source-side helpers are publishing tools, not site build dependencies. Equations use native MathML, while the RF-network article deliberately shares the CNT article's compact audio control. Article builders emit absolute Open Graph and X Card image metadata so the existing Tech Digest thumbnail can also appear in link previews.

Deploy: repo `shlokvaibhav.github.io` → Pages on `main` (root). Nothing for Jekyll to process.
