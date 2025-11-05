# Repository Hardening Notes

What I added to this repository to improve security and contribution hygiene:

- `.pre-commit-config.yaml` — common pre-commit hooks (whitespace, EOF, YAML checks, large-file blocking, detect-secrets)
- `.gitattributes` — suggested Git LFS patterns for large binary assets
- `.github/ISSUE_TEMPLATE/*` — bug and feature templates
- `.github/PULL_REQUEST_TEMPLATE.md` — PR template for contributors
- `.github/dependabot.yml` — Dependabot config (keeps Actions and packages updated)
- `.github/workflows/pre-commit.yml` — runs pre-commit on PRs and pushes
- `.github/workflows/branch-protection.yml` — workflow to set branch protection when run by an admin
- `CODEOWNERS` — basic ownership mapping
- `SECURITY.md` — instructions for reporting vulnerabilities

Next steps (requires a repo admin to enable / approve):

1. Enable GitHub secret scanning and Dependabot alerts in the repository Security settings.
2. Run the `Branch protection` workflow (Actions -> run workflow) as a repository admin to apply recommended protection to `main` (or edit it to target another branch).
3. (Optional) Install Git LFS locally and track large assets by running `git lfs install` and `git lfs track "*.png" "*.zip"` (see `.gitattributes`).

If you want, I can also create a new branch and open a PR with these changes — tell me whether you prefer a PR or a direct commit to `main`.
