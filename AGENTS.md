# AGENTS.md

Rules for AI assistants editing this repo. Keep it boring and minimal.

1. **No build step, no JavaScript, no frameworks.** Plain HTML + one CSS file. If a change seems to need JS, it probably doesn't — push back.
2. **One stylesheet.** All CSS lives in `styles.css`. Use the `:root` tokens; don't hardcode colours/fonts. Respect the numbered section TOC at the top.
3. **Header & footer are duplicated across the 7 pages on purpose** (no includes — that would add a dependency). Change one → change all of `index/writing/books/notes/hobbies/research/cv.html` identically.
4. **Content over chrome.** Don't invent copy, posts, stats, or sections. Use the user's exact words. Ask before adding anything.
5. **Links open in the same tab** (no `target="_blank"`). External links use full `https://` URLs.
6. **Images:** Tech Digest cards use local `thumbs/*.png` (square). Writing/Books cards hotlink the Substack post's original S3 cover at its native aspect-ratio — never the pre-cropped `og:image`. The user's own photos (Hobbies) go in `media/`. Until a real cover/photo exists, use a `<span class="c-img ph">Label</span>` placeholder tile — don't invent or generate images.
7. **Don't reintroduce cruft.** No `uploads/`, no scratch files, no dead CSS. If you remove a feature, remove its styles too.
8. Record any non-obvious decision in `docs/ADR.md` (one tight entry).
