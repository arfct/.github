# Linear

[Linear](https://linear.app) is where Artifact tracks work: issues, status, and priority. The workspace is `arfct`.

## Structure

One team, **Artifact** (key `A`). Every product repo gets its own Linear project — the project description holds a short summary plus links to the repo and the live URL.

## Division of truth

Repo docs are canonical for architecture, rationale, and narrative — the "why" and "how" of a project. Linear owns status, priority, and the bug list. This mirrors the existing Minder and subpixel project descriptions.

## Labels

Three labels, kept minimal: **Bug**, **Feature**, **Improvement**. Propose new labels in a PR to this doc first.

## Issues

Plain titles, with enough description to act on. Attach every issue to its project. Priority gets set at triage, not at creation.

## GitHub integration

Branches follow `a-<number>-<short-slug>`, which auto-links branches and PRs to their Linear issue. Magic words in a PR description — `Fixes A-123` — close the issue on merge.

## Agents

Agents may create and update issues via the Linear MCP. Status changes and comments should say what changed and why.
