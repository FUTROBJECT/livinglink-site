# LivingLink — Landing Site

Static marketing site for LivingLink (speculative concept, FutureObjects Research).

| File | What it is |
|---|---|
| `index.html` | Landing page |
| `design-system.html` | Brand book / design system |
| `demo.html` | Live working demo (local-store build — comments persist per-visitor in their browser) |
| `assets/brand/` | Canonical logo files |

Everything is self-contained static HTML — no build step, no dependencies.

## Deploy to GitHub Pages (GitHub Desktop)

1. GitHub Desktop → **File → Add Local Repository…** → choose this `site` folder. Desktop will say it isn't a repo and offer **"create a repository here instead"** — click that.
2. In the create dialog, **don't change the Name field** (changing it makes Desktop create a subfolder); leave **Git ignore: None** and **License: None** — the folder is already complete.
3. Commit: all files will be listed → summary "LivingLink landing site" → **Commit to main**.
4. Click **Publish repository** (top bar). In that dialog set **Name: `livinglink-site`** (this names the GitHub repo, independent of the folder), Account: **futrobject**, and uncheck **"Keep this code private"** (Pages on the free plan needs a public repo) → Publish.
5. On github.com, open the repo → **Settings → Pages → Source: Deploy from a branch → `main` / `(root)` → Save**.

Live in ~a minute at `https://futrobject.github.io/livinglink-site/`.

To update later: change files, GitHub Desktop will show the diff → commit → **Push origin**. Pages redeploys automatically.

## Notes

- `demo.html` is fully client-side: visitors can comment, but comments live in *their* browser (localStorage). Real two-way review with shared comments needs the Yjs sync server — see `docs/shared-demo-runbook.md` in the main project, which can't run on GitHub Pages (static hosting only).
- `.nojekyll` is included so Pages serves files as-is.
- To refresh the site after design changes in the main project, re-copy: `landing.html → index.html`, `design-system.html`, `demo-metrics-commented.html → demo.html`, and `assets/brand/`.
