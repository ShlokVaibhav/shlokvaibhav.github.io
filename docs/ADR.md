# ADR — decisions behind this site

Short record of *why*, so changes don't undo intent. Snapshot: ~880 lines, 0 JS, 1 stylesheet, 1 breakpoint, 0 dead CSS.

1. **Plain static HTML + CSS, no build step.** The old stub used Quarto (needs a toolchain). Now what you edit is what ships; open a file to preview. Long-form writing lives on Substack, so no Markdown pipeline is needed.
2. **Zero JavaScript.** Layout, the responsive card grid, and the dropcap are all native CSS. JS would add a dependency and a failure mode for no feature gain.
3. **One stylesheet, driven by `:root` tokens.** Re-theming is a one-line edit; a numbered TOC keeps any rule findable. No style duplication.
4. **Header/footer duplicated per page, not a JS/template include.** An include would re-add the dependency #2 removed (nav vanishes if it fails) or a build step (#1). At 5 pages, a find-and-replace is cheaper. *Revisit past ~10 pages.*
5. **EB Garamond via Google Fonts, with a Georgia/Times fallback.** The single typography dependency, chosen deliberately; the page still renders if it fails.
6. **Card grid for posts (matplotlib plot-types style).** Tech Digest uses local `thumbs/`; Writing hotlinks each Substack post's *original* cover at its native aspect-ratio — the pre-cropped `og:image` mangled portrait covers.
7. **Cool-neutral palette, one teal accent, in `oklch`.** One accent keeps focus on content; oklch keeps greys/accent perceptually consistent when hue is tweaked.
8. **CV is both a web page and a PDF.** The HTML version is current/accessible; the PDF is the portable artifact. The web copy is intentionally a superset (newer role than the dated PDF).

Deploy: repo `shlokvaibhav.github.io` → Pages on `main` (root). Nothing for Jekyll to process.
