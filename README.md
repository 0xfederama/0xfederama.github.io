# My portfolio

Source of my personal website, live at [federama.dev](https://federama.dev) (also served at [0xfederama.github.io](https://0xfederama.github.io)).

Built with [Hugo](https://gohugo.io) (extended edition) and the [hugo-theme-cactus](https://github.com/monkeyWzr/hugo-theme-cactus) theme, included as a git submodule. My customizations live in this repo's `layouts/` folder, which overrides the theme's files, so the submodule itself stays unmodified.

## Run locally

```bash
git clone --recursive https://github.com/0xfederama/0xfederama.github.io.git
cd 0xfederama.github.io
hugo server
```

If you cloned without `--recursive`, run `git submodule update --init` first.

## Write a post

```bash
hugo new content posts/YYYY-MM-DD-my-post.md
```

## Deploy

Pushing to `main` builds and deploys the site to GitHub Pages via `.github/workflows/gh-pages.yml`. No manual step needed; `public/` is build output and is not committed.
