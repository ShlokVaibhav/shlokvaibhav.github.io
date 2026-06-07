# shlokvaibhav.github.io

My personal site. Plain HTML + CSS, no build step, no JavaScript.

## Files
```
index.html      Home — Sapere Aude, intro, recent writing & tech digest
writing.html    Essays (cards link to Substack)
books.html      Book reviews — visual archive (cards link to Substack)
notes.html      Tech Digest — DSP notebooks (link out to the DSP site)
hobbies.html    Off the clock — playlist, origami photos, cafés, blogroll
research.html   Research + publication
cv.html         Web CV + PDF download
styles.css      All styling, one file (sectioned, with a table of contents up top)
thumbs/         Local thumbnails for Tech Digest cards (bpsk, dsss, costas)
media/          Your own photos for the Hobbies page (create when needed)
Shlok-Vaibhav-Singh-CV.pdf   Résumé, linked from cv.html
docs/ADR.md     The handful of decisions behind the build
AGENTS.md       House rules for AI assistants editing this repo
```

## Edit
- **Colours / fonts / widths:** the `:root` variables at the top of `styles.css`. Change once, applies everywhere.
- **Header & footer:** copied into each page between `<!-- shared … -->` comments. Editing the nav = the same change in all 7 pages (find-and-replace).
- **Add an essay:** copy one `<a class="card">` block in `writing.html` (+ the home row), point it at the post URL and cover image.
- **Add a book:** copy a card in `books.html`; swap the `<span class="c-img ph">` placeholder for the cover `<img>` (see the comment in the file).
- **Add a digest entry:** copy a card in `notes.html`; drop a square image in `thumbs/`.
- **Add a hobby item:** in `hobbies.html`, copy a card / photo `<figure>` / `linklist` row. Photos go in `media/`; placeholders (`c-img ph`) show until you swap in a real `<img>`.
- **Add a CV row:** copy a `<div class="cv-row">` block in `cv.html`.

## Run & deploy
Open any `.html` locally — no server needed. To publish: push to a repo named `shlokvaibhav.github.io`, enable GitHub Pages on `main` (root). No Jekyll/Node.
