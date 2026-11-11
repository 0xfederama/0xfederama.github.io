# CLAUDE.md

Personal website/blog built with Hugo (extended) + the `cactus` theme.

## Layout
- `config.toml` — site config (menu, home description, socials, `[params]` for the theme).
- `content/posts/` — blog posts, named `YYYY-MM-DD-slug.md`; `content/about/` — about page.
- `data/projects.json` — projects list shown on the home page.
- `static/` — files copied as-is (images).
- `layouts/` — **overrides of theme templates**. Put any theme customization here (copy the file from `themes/cactus/layouts/...` to the same path under `layouts/`). Currently overridden: `partials/head.html` (`css.Sass`, no Google Analytics, no cactus.chat), `index.html` (`hugo.Data`), `_default/baseof.html` and `posts/single.html` (`.Site.Language.Locale`, author without `isset .Site`).
- `themes/cactus/` — git submodule of upstream monkeyWzr/hugo-theme-cactus. **Never edit files inside it**: changes there are not committed in this repo and CI would not see them.

## Commands
- `hugo server` — local dev server with live reload.
- `hugo --gc --minify` — production build into `public/` (gitignored).
- `git submodule update --init` — fetch the theme after cloning.

## Deploy
GitHub Actions (`.github/workflows/gh-pages.yml`) builds on push to `main` and deploys to GitHub Pages. The Hugo version is pinned via `HUGO_VERSION` there; keep it in sync with the local Hugo (`hugo version`) when upgrading.

