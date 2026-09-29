# Project Context

## Summary

| Attribute | Value |
|-----------|-------|
| Repository | `OBaruch/OBaruch` |
| Type | GitHub profile repository (a special repository whose root `README.md` is shown on the owner's GitHub profile page) |
| Project origin | **Personal Project**: the author's public professional profile |
| Owner / author | Baruch López (GitHub: `OBaruch`) |
| Created | 2025-03-30 (first commit, `543d72e`) |
| Primary content | A single `README.md` written in Markdown with embedded HTML |
| Source code | None. The repository has no programs, scripts, data, or build tooling. |

## What the repository is

GitHub shows the `README.md` of a repository named after the user (`<username>/<username>`) at the top of that user's profile page. This repository is that file. Evidence:

- **Confirmed:** the first commit (`543d72e`) contains GitHub's standard auto-generated template, including the comment *"OBaruch/Obaruch is a ✨ special ✨ repository because its README.md (this file) appears on your GitHub profile."* (preserved in [`archive/readme-versions/2025-03-30_01-github-default-template.md`](../archive/readme-versions/2025-03-30_01-github-default-template.md)).
- **Confirmed:** the repository name matches the owner's username (`OBaruch`). The remote URL uses different casing (`Obaruch`), which GitHub treats as the same name.

## Objective

**Confirmed (from the README's content):** give a short public professional summary of the author, covering current role, areas of expertise, tech stack, selected anonymized work, education, public projects, and GitHub activity statistics.

**Inferred:** the profile serves as a portfolio and personal-branding entry point, linking to the author's website (`baruchlopez.com`) and LinkedIn.

## Confirmed / Inferred / Unknown

### Confirmed (directly supported by the files or Git history)

- The repository contains only `README.md` (before this reorganization).
- The README went through three main phases: GitHub template → Spanish/English profile (2025) → rewritten profile (2026). See [`readme-history.md`](readme-history.md).
- The 2026-06-21 commit message (in Spanish) says the goal was to update the profile with the role "AI Engineer II @ Bosch", the stack actually used, and **verifiable public projects** (*"stack real y proyectos publicos verificables"*).
- The README depends on external services for images and stats: shields.io, github-readme-stats, and github-profile-trophy. See [`readme-overview.md`](readme-overview.md).

### Inferred (reasonable conclusions that cannot be fully confirmed)

- The 2025 "Featured Projects" links (`Data-Automation`, `Vehicle-Detection`, `Staff-Mobility`) were likely replaced because they did not point to existing public repositories. This is suggested by the 2026 commit message's emphasis on *verifiable* public projects, but the repository cannot confirm whether those links worked.
- Every commit was authored through the GitHub web UI or with the GitHub noreply address. The generic "Update README.md" messages suggest in-browser editing.

### Unknown

- Whether the external stats/trophy services currently render correctly. This depends on third-party uptime and cannot be verified from the repository.
- The accuracy of the professional claims (roles, dates, achievements). They are the author's own statements and are documented here as written, not verified.

## Contradictions found

These are recorded as found. The original README has not been changed to resolve them:

1. **Job title:** the header says **"Advanced AI Engineer @ Bosch"** (changed in the latest commit, `04ff1e7`, on 2026-07-09), while the *About me* section still says **"AI Engineer II at Bosch"**. The header was probably updated after a role change and the body was not, but this cannot be confirmed.
2. **Name presentation:** the 2025 version introduced the author as *"Omar Baruch M. López"*, and the current version uses *"Baruch López"*. This is a presentation choice, not necessarily a contradiction.
3. **Language:** the first custom draft was in Spanish, and later versions are in English. The most recent commit messages are also in Spanish.

## Scope of the 2026 reorganization

The reorganization added documentation (`docs/`), a historical archive (`archive/`), and a `.gitignore`. The root `README.md`, which is the profile's "original implementation", was **not** modified. See [`sdlc/`](sdlc/) for the intent, spec, and plan.
