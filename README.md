# Portfolio — GitHub Pages

Single-file static site. No build step, no dependencies, no server code.

## Files

```
index.html   ← the whole site (CSS + JS inlined)
me.jpg       ← your profile photo, 400×400, square crop (add this yourself)
README.md    ← this file, safe to delete after deploy
```

## Deploy (5 minutes)

**Option A — project repo (e.g. `portfolio`)**

1. Create a new public repo on GitHub, e.g. `portfolio`.
2. Upload `index.html` and `me.jpg` (drag and drop works on mobile via the "Add file → Upload files" button).
3. Go to **Settings → Pages**.
4. Under **Source**, pick `Deploy from a branch`.
5. Branch: `main`, folder: `/ (root)`. Save.
6. Wait 1–2 minutes. Your site is at
   `https://YOUR-USERNAME.github.io/portfolio/`

**Option B — user site (shorter URL)**

Name the repo exactly `YOUR-USERNAME.github.io` and push `index.html` to `main`.
The site is live at `https://YOUR-USERNAME.github.io/` with no `/repo` suffix.
Only one repo per account can use this name.

## Before you go live — 4 edits

Search `index.html` for these and replace:

| What | Where | Replace with |
|---|---|---|
| Profile photo file | `<img src="me.jpg"` | Your filename, or leave it — the icon fallback shows if the file is missing |
| GitHub URL | `github.com/Encyclo-pedia01` | Your real GitHub username |
| LinkedIn URL | `linkedin.com/in/joseph-anderson-gameli-6a4596326` | Your real LinkedIn slug |
| Email | `joegady94@gmail.com` (3 places) | Your real email |

Optional: uncomment the `<meta property="og:url">` tag and set your live URL so link
previews resolve correctly when the page is shared on WhatsApp or LinkedIn.

## Contact form

The form validates in the browser and falls back to `mailto:` — it works with zero
backend, but it opens the visitor's email client instead of sending silently.
For real in-page sending, create a free Formspree account and swap the submit handler:
the commented-out `fetch()` block is already written at the bottom of the script.

## Notes

- Everything is in one file, so there is nothing to break on deploy.
- Relative paths only — no absolute `/` roots, so the site works from a subfolder.
- Dark mode persists via `localStorage` and respects the OS preference on first visit.
- Respects `prefers-reduced-motion`.
