# Dr. Ohad Elishco — Academic Portfolio

Personal academic website for Dr. Ohad Elishco (Ben-Gurion University of the Negev),
covering research, publications, teaching, and team. The site is a static,
multi-page website hosted on **GitHub Pages**.

🌐 **Live site:** https://elishco-ohad.github.io

## Pages

| File | Description |
|------|-------------|
| `index.html` | Home — bio, overview, and contact |
| `Research.html` | Research areas and interests |
| `Publications.html` | Publication list (rendered from a JavaScript data array, filterable by year) |
| `Teaching.html` | Courses and mentorship |
| `People.html` | Research team members |

## Tech stack

- **Static HTML** — no build step; each page is a standalone file.
- **[Tailwind CSS](https://tailwindcss.com/)** via the CDN (`cdn.tailwindcss.com`), configured inline per page through `tailwind.config`.
- **Google Fonts** — *Newsreader* (serif headings) and *Inter* (body/labels).
- **Material Symbols** — icon font for UI glyphs.
- Publications are stored as a JS array inside `Publications.html` and rendered to the DOM on load.

## Assets

- `CV_Ohad.pdf` — downloadable CV (linked from the header "CV" button on each page).
- `Ohad.jpg` — profile photo.

## Local development

No tooling or dependencies are required — just open the files in a browser:

```bash
open index.html
```

Or serve the folder over a local HTTP server (recommended, so relative links behave like production):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

The site deploys automatically via **GitHub Pages** from the `main` branch.
Pushing to `main` publishes the changes:

```bash
git add -A
git commit -m "Your message"
git push
```

Changes typically go live within a minute. If updates don't appear in the
browser, do a hard refresh to bypass the cache (in Safari: **Cmd + Option + R**,
or open a private window).

## Maintenance notes

- The header (navigation, **CV** and **Contact** buttons) is duplicated across
  every page. When editing it, apply the same change to all five HTML files to
  keep them consistent.
- Button styling relies on custom Tailwind utilities (`font-label-md`,
  `text-label-md`). Each page must define these in its inline `tailwind.config`
  for the buttons to render identically.
- To add a publication, edit the `publications` array in `Publications.html`.
