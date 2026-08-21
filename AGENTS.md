# Repository Guidelines

## Project Structure & Content

This is a Jekyll-powered academic homepage deployed through GitHub Pages. Edit the page content in `index.md`; reusable sections live in `_includes/` (`publications.md`, `services.md`). Publication entries are data-driven in `_data/publications.yml`. Site settings, identity details, and theme choices belong in `_config.yml`.

Layout and styling are in `_layouts/homepage.html`, `_sass/`, and `assets/css/`. Put images in `assets/img/`, documents such as a CV in `assets/files/`, and small browser scripts in `assets/js/`. `html_source_file/` is a static HTML export; keep it consistent only when maintaining the non-Jekyll version intentionally.

## Build and Local Preview

Install Ruby dependencies once:

```bash
bundle install
```

Serve the site locally at `http://localhost:4000`:

```bash
bundle exec jekyll serve
```

Use `bundle exec jekyll build` before submitting content or style changes to catch configuration, Liquid, Markdown, and Sass errors. There is no automated test suite; a successful build and browser review are the expected checks.

## Style and Naming

Use Markdown for page copy and two-space indentation for YAML, Sass, and HTML. Preserve existing YAML keys and list structure in `_data/publications.yml`; add one publication under `main` with fields such as `title`, `authors`, `conference`, `pdf`, and `image`. Use lowercase, descriptive asset names with hyphens where applicable (for example, `assets/img/project-teaser.png`). Keep links relative to the site root where the existing content does so.

Avoid hand-editing generated `_site/` output. Do not remove or replace existing images without also checking every Markdown/YAML reference.

## Commits and Pull Requests

Recent history uses short, imperative summaries such as `add news`, `add VAG paper`, and `adjust publication location`. Follow that pattern: one focused change per commit, e.g. `add 2026 publication`.

For pull requests, explain the visible site change, list modified content or assets, and link any related issue when available. Include a screenshot for layout, styling, or responsive changes. Confirm `bundle exec jekyll build` passes and that all new image/document links resolve locally.
