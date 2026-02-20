# Roadmap (XPII.Net)

## Immediate (publish-ready)
- Confirm GitHub repository name is `XPII.Net` and set visibility to Public (if intended).
- Enable GitHub Pages: Settings → Pages → Source: GitHub Actions.
- Set branch protection on `main` (recommended): require PRs + required status checks.
- Replace placeholders in `SECURITY.md` with a real private reporting contact.

## Near-term (hardening)
- Add a lightweight content review policy (what is allowed to be published).
- Add CI checks for link validation (optional).
- Add a `docs/` content structure for releases and versioned statements.

## Ongoing
- Review Dependabot PRs promptly.
- Rotate credentials if scanning finds leaks; invalidate exposed tokens immediately.
