# Pain Discovery — Field Manual

A single-file, bilingual (English / Russian) web app for running **customer-pain discovery interviews**. Fill in answers as you talk, then export the whole thing as a dark "dossier" PDF.

Built as one self-contained `index.html` — no build step, no dependencies, works offline (just double-click it).

## Features

- **Fill-in template** for all five interview phases, the operating doctrine, and the make-or-break principles.
- **Language switch** (flag button, top-right) — English ⇄ Russian. Your typed answers stay put when you switch languages.
- **Auto-save** — answers persist in your browser (`localStorage`); nothing is sent anywhere.
- **Export PDF** — keeps the dark espionage theme. In the print dialog, choose **Save as PDF**.
- **Save / Load file** — export your answers as a `.json` you can back up or reopen later.
- **Design** — minimalist-luxury / espionage aesthetic: deep blacks, charcoal panels, crimson + gold accents, Swiss-inspired typography.

## Use it locally

Double-click `index.html`, or serve the folder:

```bash
python -m http.server 8000
# then open http://localhost:8000
```

## Publish to GitHub Pages

From this folder:

```bash
git init
git add .
git commit -m "Pain Discovery field manual"
git branch -M main
# create an empty repo on github.com first, then:
git remote add origin https://github.com/<you>/<repo>.git
git push -u origin main
```

Then on GitHub: **Settings → Pages → Source: `main` / root**. Your app goes live at
`https://<you>.github.io/<repo>/`.

## Customize

All text (both languages) lives in the `I18N` object inside `index.html`. Edit a question or note there and it updates everywhere. The `[the thing]` placeholder in Phase 1 is meant to be swapped for the activity you're investigating (or filled into the "Activity" field in the case-file header).

## License

MIT — see [LICENSE](LICENSE).
