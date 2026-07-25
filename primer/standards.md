# Standards

Artifact projects favor code and repos that are consistent, self-documenting, and minimal — a new contributor (human or agent) should be able to read a file or a repo and understand it without extra explanation.

## Code style

Names should explain intent. Prefer `fullName` over a comment saying "the user's full name" — a good name makes the comment unnecessary.

Write comments only when the code itself can't carry the explanation:
- **Why, not what** — the reasoning behind a non-obvious decision.
- **Warnings** — gotchas or constraints that aren't visible from the code alone.
- **Complex algorithms** — a brief note on the approach.
- **TODOs** — temporary markers for known future work.

```js
// Debounce to avoid firing an API call on every keystroke
const debouncedSearch = debounce(handleSearch, 300);
```

Keep functions small and focused on one thing. Remove abstractions that don't earn their keep — a layer of indirection should make the code easier to follow, not harder.

## Repo hygiene

Every repo has:
- A **README** with a one-line purpose and instructions to run it.
- A **LICENSE** — MIT by default for public repos.
- A **CLAUDE.md** based on the [org template](../templates/CLAUDE.md).
- A **.gitignore** appropriate to the stack.
- A repo description and homepage URL set on GitHub.

## Commits & branches

- Commit subjects are imperative: "Add," "Fix," "Update" — not "Added" or "Adding."
- Branch off `main`.
- Branch names come from the Linear issue ID: `a-<number>-<short-slug>` (e.g. `a-123-fix-login`). This lets Linear's GitHub integration auto-link branches and PRs to issues.
- Once a repo has more than one contributor, no direct pushes to `main` — use a PR.

## Docs

Repo docs (README, ROADMAP.md, and similar) are the canonical source for architecture and rationale — the "why" and "how" of a project. Linear owns status, priority, and the bug list — see [linear.md](linear.md).
