# Agent Instructions

This repository is the source for `nicholas-reynolds.com`.

## Branch and Deployment Model

- Keep editable source on `master`.
- The rendered static site is deployed automatically to `gh-pages` via GitHub Actions.
- Do not edit `gh-pages` by hand except for emergency recovery.

## Project Layout

- `_quarto.yml`: site config, navbar, theme wiring, and static resources.
- `index.qmd`, `research.qmd`, `teaching.qmd`, `contact.qmd`: page content.
- `styles.scss`: typography, spacing, card styles, and mobile tweaks.
- `papers/`: PDF assets that must remain accessible on the live site.
- `.github/workflows/publish.yml`: render + deploy workflow.

## Content Editing Rules

- Update biography, affiliations, links, and featured paper on `index.qmd`.
- Update publications and paper links on `research.qmd`.
- Keep PDF filenames stable when possible to avoid broken links.
- If adding a custom domain, store it in a root `CNAME` file on `master`; the workflow will copy it to `_site/CNAME`.

## Local Commands

- Render locally: `quarto render`
- Preview locally: `quarto preview`

## Notes

- Preserve existing PDFs in `papers/` unless explicitly removing deprecated files.
- If deployment changes are needed, edit `.github/workflows/publish.yml`, not GitHub UI defaults.
