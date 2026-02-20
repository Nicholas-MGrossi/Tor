# Architecture Overview (XPII.Net)

## Purpose
XPII.Net is a publication-focused repository that ships a public documentation site via GitHub Pages.

## High-level components
- `docs/` — static site content that is deployed to GitHub Pages.
- GitHub Actions
  - `Deploy Docs to GitHub Pages` (`.github/workflows/pages.yml`) publishes `docs/`.
  - `Secret scan` (`.github/workflows/secret-scan.yml`) scans for accidental secret leaks.
- Dependency automation
  - `.github/dependabot.yml` keeps GitHub Actions dependencies up-to-date.

## Data & security model (baseline)
- Assume the repository is public; do not include secrets or private data.
- Treat PR review as the primary control preventing unsafe publication.
- Automated scanning reduces, but does not eliminate, the risk of credential leakage.

## Operational notes
- The Pages workflow deploys the contents of `docs/` as-is (static files).
- Markdown in `docs/` is not rendered as HTML unless a static-site generator is introduced.
