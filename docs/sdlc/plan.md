# Plan

Implements [spec.md](spec.md). Each step is small, can be reviewed on its own, and is checked before moving on.

## Phase 1: Discovery (read-only)

1. List every tracked file. Result: only `README.md`.
2. Read the current README and each historical version (`git log -- README.md`, `git show <commit>:README.md`).
3. Identify the repository type from evidence: the GitHub template comment in `543d72e` confirms a profile repository.
4. Record the baseline checksum of `README.md` (FR-1).
5. Collect contradictions and unknowns (job title mismatch, unverifiable links, external service dependencies).

## Phase 2: Structure

6. Create `docs/`, `docs/sdlc/`, and `archive/readme-versions/`. No other folders are created, because there is no content for them.
7. Extract three historical snapshots with `git show` into `archive/readme-versions/`:
   - `543d72e` → GitHub default template
   - `71b7612` → first Spanish draft
   - `c329178` → last 2025 English profile
   (The intermediate 2025-03-30 edits and `e9cb8f5` differ only slightly from a neighboring snapshot or from the current file, and remain available in Git.)
8. Add a minimal `.gitignore` for OS and editor files.

## Phase 3: Documentation

9. `docs/project-context.md`: origin, objective, Confirmed / Inferred / Unknown, contradictions.
10. `docs/readme-overview.md`: section breakdown, stack as listed, external dependencies, how it renders.
11. `docs/readme-history.md`: commit timeline and observed trends.
12. `docs/possible-improvements.md`: suggestions, explicitly not applied.
13. `docs/README.md` and `archive/README.md`: indexes.
14. `docs/sdlc/intent.md`, `spec.md`, `plan.md`: this set.

## Phase 4: Verification

15. Compare `sha256sum README.md` with the baseline, and check that `git diff main -- README.md` is empty.
16. Compare each snapshot with `git show <commit>:README.md` using `cmp`.
17. Check relative links: resolve every relative Markdown link target in the new files.
18. Check that no tooling files were added (`git diff --name-only main`).

## Phase 5: Delivery

19. Commit on a dedicated branch (`docs/repository-refactor`), authored by the repository owner.
20. Push and open a pull request against `main` for the owner to review. Merging is the owner's decision.

## Rollback

Every change is additive. Reverting the merge commit, or deleting `docs/`, `archive/`, and `.gitignore`, returns the repository to its previous state. The profile page is not affected either way.
