# GitHub Copilot instructions for this repository

**Purpose:** Help AI coding agents make safe, useful edits to this LinkedIn Learning course repository (course content & metadata only). This repo contains course exercise files and docs rather than runnable product code.

## High-level overview
- This repo holds supplemental course materials for “Deep Learning with Python: Convolutional Neural Networks.” The main surface is documentation and exercise files (see `README.md`).
- No production service, tests, or application code is present (no `.py` modules or notebooks at time of writing).

## Environment & quick dev setup 🔧
- Use GitHub Codespaces / the devcontainer defined in `.devcontainer/devcontainer.json` for a consistent environment.
  - On container create the project runs `.devcontainer/startup.sh`, which installs `requirements.txt` with `pip install --user -r requirements.txt`.
  - Devcontainer settings enable Python linting/formatting tools (pylint, black, flake8, mypy) but config files are not included here — follow container settings when adding linters/formatters.
- To reproduce locally: create a Python 3.10 environment and run `pip install -r requirements.txt`.

## What an AI agent can safely work on ✅
- Edit course docs and text in `README.md` (e.g., replace placeholder links: `[lil-course-url]`, `[lil-thumbnail-url]`).
- Update metadata files like `NOTICE`, `LICENSE`, or the course description.
- Improve or add docs under `.github/` (issue/PR templates, workflows) while respecting repo policy.

## What NOT to do 🚫
- This repository **does not accept PRs** — see `CONTRIBUTING.md`. Do not open PRs to change course materials. Instead, open an issue to propose edits or contact maintainers if appropriate.
- Do not assume tests or CI exist beyond the simple workflow in `.github/workflows/main.yml` (which copies to branches). There is no test suite to run.

## Notable files & examples to reference 📁
- `README.md` — primary course description (replace placeholders in the file when updating links/text).
- `requirements.txt` — minimal runtime deps installed by devcontainer startup.
- `.devcontainer/startup.sh` — runs dependency installation on Codespaces create.
- `.github/workflows/main.yml` — shows repo workflow (copy to branches).
- `CONTRIBUTING.md` — describes contribution policy (PRs closed).

## Style & conventions for edits
- Keep changes minimal and focused: update copy, fix broken links, or correct metadata.
- If adding Python files or notebooks, include a short README explaining purpose and add an entry to `README.md`.
- When modifying docs, include one-sentence rationale in the change summary and point to the course or content section being updated.

## When in doubt
- Open an issue explaining the proposed change and why it’s needed (use the issue template in `.github/ISSUE_TEMPLATE.md`).

---

If you'd like, I can adjust tone, add examples of proposed edits, or include a short checklist for reviewers — tell me what you'd prefer.