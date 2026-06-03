## Stack

- This repo is a Jekyll site built via the `github-pages` gem in `Gemfile`, not a Node app. Use Bundler-backed commands for site work.
- There is no repo-local CI, lint, typecheck, or test config to mirror. Verification is usually a local Jekyll build/serve.

## Commands

- Install Ruby deps with `bundle install`.
- Run the site locally with `bundle exec jekyll serve -l -H localhost`.
- Use `bundle exec jekyll build` for a one-off verification build.
- Node is only used to rebuild the shipped JS bundle: `npm install` then `npm run build:js`.

## Critical Gotchas

- `_config.yml` is not hot-reloaded by Jekyll here; restart `jekyll serve` after changing it.
- The site loads `assets/js/main.min.js` from `_includes/scripts.html`. If you edit `assets/js/_main.js` or files under `assets/js/plugins/`, rebuild with `npm run build:js` or your change will not ship.
- `Gemfile.lock` is intentionally gitignored in this repo.

## Content Map

- Root site settings, author metadata, collection config, and excludes live in `_config.yml`.
- Top nav links are driven by `_data/navigation.yml`.
- The homepage is `_pages/about.md` with `permalink: /`.
- Main content collections are `_publications/`, `_talks/`, `_teaching/`, `_portfolio/`, plus regular posts in `_posts/`.
- Static downloadable files belong in `files/`.

## Templating Conventions

- Publication pages depend on custom front matter used by `_layouts/single.html` and `_includes/archive-single.html`: `author`, `venue`, `paperurl`, `codeurl`, `citation`, and optional HTML `excerpt`.
- Collection landing pages in `_pages/` usually render by looping over `site.publications`, `site.talks`, or `site.teaching`; preserve those front matter keys when adding entries.
- Custom head additions, including favicon links and MathJax, live in `_includes/head/custom.html`.

## Generators

- `markdown_generator/` contains optional Python/Jupyter generators that write markdown into `../_publications/` from TSV or BibTeX sources.
- `talkmap.py` expects to be run from the `_talks/` directory; it scans local `*.md` talk files and writes output into `../talkmap/`.
