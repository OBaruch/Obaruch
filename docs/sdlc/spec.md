# Spec

Derived from [intent.md](intent.md). Describes the required state of the repository after the reorganization.

## 1. Repository structure

```
OBaruch/
├── README.md                 # Profile page rendered by GitHub. ORIGINAL, never modified by the reorganization.
├── .gitignore                # OS / editor noise only
├── docs/
│   ├── README.md             # Documentation index
│   ├── project-context.md    # Origin, objective, confirmed / inferred / unknown, contradictions
│   ├── readme-overview.md    # Section breakdown, stack as listed, external dependencies
│   ├── readme-history.md     # Timeline reconstructed from git history
│   ├── possible-improvements.md  # Ideas NOT applied
│   └── sdlc/
│       ├── intent.md
│       ├── spec.md
│       └── plan.md
└── archive/
    ├── README.md             # Index of archived material
    └── readme-versions/      # Verbatim snapshots of earlier README.md versions
```

No `src/`, `data/`, `assets/`, or `examples/` folders are created, because the repository has no content of those kinds.

## 2. Functional requirements

| ID | Requirement |
|----|-------------|
| FR-1 | The root `README.md` MUST keep exactly the same bytes as commit `04ff1e7` (SHA-256 `bc073d0a72938bca3352c7c1b1a46f7a40c494d333b227f03bd3a1071e92b95e`). |
| FR-2 | The root `README.md` MUST stay at the repository root, so GitHub keeps rendering it on the profile. |
| FR-3 | `archive/readme-versions/` MUST contain unedited copies of selected historical README versions, each named `<date>_<nn>-<slug>.md` and traceable to a commit. |
| FR-4 | Archived and documentation files MUST NOT be named `README.md` at the repository root, and MUST NOT otherwise interfere with profile rendering. |
| FR-5 | `docs/project-context.md` MUST classify the project origin and label information as *Confirmed*, *Inferred*, or *Unknown*. |
| FR-6 | Contradictions found in the content MUST be documented, not fixed. |
| FR-7 | `docs/possible-improvements.md` MUST state clearly that none of its suggestions have been applied. |
| FR-8 | All links between Markdown files MUST be relative and resolve inside the repository. |

## 3. Non-functional requirements

| ID | Requirement |
|----|-------------|
| NFR-1 | **Authenticity:** the documentation describes the profile as it is, without adding to or reinterpreting it. |
| NFR-2 | **Minimalism:** no build tooling, CI, or infrastructure is added. |
| NFR-3 | **Language:** all added documentation is in English. |
| NFR-4 | **Authorship:** commits are authored by the repository owner. |

## 4. Constraints

- The profile README counts as the "source code" of this repository, and the code-preservation rule applies to it.
- Historical snapshots come from `git show <commit>:README.md` and are written to disk as-is.

## 5. Acceptance criteria

- [ ] `sha256sum README.md` matches FR-1.
- [ ] `git diff main -- README.md` is empty.
- [ ] Each archived snapshot matches `git show <commit>:README.md` byte-for-byte.
- [ ] Every relative link in `docs/` and `archive/` resolves to an existing file.
- [ ] No tooling files (workflows, Dockerfiles, package manifests) were added.
