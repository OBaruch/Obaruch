# Intent

> Spec-driven workflow: **Intent** (why) → [**Spec**](spec.md) (what) → [**Plan**](plan.md) (how). These documents describe the repository as it exists and the reorganization applied to it. They do not propose new features.

## Problem

`OBaruch/OBaruch` is the author's GitHub profile repository. Before the reorganization it held a single `README.md` and nothing else, so:

- the purpose of the repository was only implied by GitHub's naming convention;
- the evolution of the profile (template → Spanish draft → English profile → 2026 rewrite) could only be seen in `git log`;
- inconsistencies in the content (e.g. two different job titles) were not recorded anywhere;
- there was no written statement of what may and may not change in the repository.

## Intent

Make the repository **self-explanatory and traceable** without changing what visitors see on the profile.

## Goals

1. Keep the root `README.md` **byte-for-byte unchanged**. It is the original deliverable and the live profile page.
2. Record the repository's context, separating what is **confirmed**, **inferred**, and **unknown**.
3. Keep earlier README versions in the working tree as a readable archive.
4. Add navigable Markdown documentation with relative links.
5. Keep intent, spec, and plan documents so later changes, by the author or by any assistant, start from an agreed baseline.

## Non-goals

- Rewriting, correcting, or restyling the profile README.
- Adding CI/CD, GitHub Actions, linters, formatters, Docker, package managers, or other tooling.
- Verifying the author's professional claims or checking external links.
- Inventing context that the repository does not contain.

## Stakeholders

| Stakeholder | Interest |
|-------------|----------|
| Baruch López (owner) | A tidy, well-documented profile repository that keeps its history. |
| Profile visitors (recruiters, peers) | See only the root `README.md`, which is unchanged. |
| Future maintainers / assistants | Clear rules and context before editing anything. |

## Success criteria

- The SHA-256 of `README.md` is identical before and after the change.
- Someone new to the repository can understand what it is and how it evolved by reading `docs/README.md`.
- Every claim in the new documentation can be traced to a file or commit, or is labeled *Inferred* / *Unknown*.
