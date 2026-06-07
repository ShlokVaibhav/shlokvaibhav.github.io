# AGENTS.md

Rules for AI assistants editing this repo. Keep it boring and minimal.

1. **No build step, no JavaScript, no frameworks.** Plain HTML + one CSS file. If a change seems to need JS, it probably doesn't — push back.
2. **One stylesheet.** All CSS lives in `styles.css`. Use the `:root` tokens; don't hardcode colours/fonts. Respect the numbered section TOC at the top.
3. **Header & footer are duplicated across the 5 pages on purpose** (no includes — that would add a dependency). Change one → change all of `index/writing/notes/research/cv.html` identically.
4. **Content over chrome.** Don't invent copy, posts, stats, or sections. Use the user's exact words. Ask before adding anything.
5. **Links open in the same tab** (no `target="_blank"`). External links use full `https://` URLs.
6. **Images:** Tech Digest cards use local `thumbs/*.png` (square). Writing cards hotlink Substack's original S3 image at its native aspect-ratio — never the pre-cropped `og:image`.
7. **Don't reintroduce cruft.** No `uploads/`, no scratch files, no dead CSS. If you remove a feature, remove its styles too.
8. Record any non-obvious decision in `docs/ADR.md` (one tight entry).
