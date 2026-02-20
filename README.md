# XPII.Net

XPII.Net is a publication-focused repository that ships a public documentation site from `docs/` via GitHub Pages.

## Project goals
- Publish clear, public-facing materials suitable for external consumption.
- Maintain a strong baseline against accidental disclosure of secrets or private data.
- Keep the publication pipeline simple, reproducible, and auditable.

## Where the published docs live
- Source: `docs/`
- Deployment: GitHub Actions → GitHub Pages (`.github/workflows/pages.yml`)

If GitHub Pages is enabled for the repository, `docs/index.html` becomes the public landing page.

## Architecture overview (high-level)
- Static docs site: `docs/` is deployed as-is.
- Secret scanning: `.github/workflows/secret-scan.yml` runs gitleaks on pushes/PRs.
- Dependency updates: `.github/dependabot.yml` keeps GitHub Actions up to date.

For details:
- `ARCHITECTURE.md`
- `ROADMAP.md`
- `GLOSSARY.md`

## Repository layout
- `.github/workflows/` — CI workflows (Pages deploy, secret scanning)
- `docs/` — public docs site content
- `README.md` — overview
- `SECURITY.md` — how to report vulnerabilities
- `PRIVACY.md` — privacy guidance

## Security & privacy baseline
- Never commit secrets (API keys, tokens, private keys, credentials).
- Never publish personal data unless explicitly required and documented.
- Use pull requests and review for all changes.

## Terminology (quick)
- **Tor**: temporary GitHub repo name used during setup; not related to the Tor network.
- **UserDev**: placeholder for the operator’s local development workspace.
- **warp-agent**: the automated assistant used to perform setup tasks.

## Reporting security issues
See `SECURITY.md`.
