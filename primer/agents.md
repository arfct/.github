# AI agents

Agents — Claude Code primarily — are first-class contributors at Artifact. They read code, open PRs, triage issues, and ship fixes alongside humans, under the same expectations.

## Context

Every repo carries a CLAUDE.md, based on the [org template](../templates/CLAUDE.md), that points back here. This Primer is the canonical cross-repo context: an agent starting cold in any Artifact repo should be able to read CLAUDE.md, follow the link, and understand how the org works.

## Conventions

- Follow [standards.md](standards.md) — code style, repo hygiene, commits, and branches apply the same to agent-authored work as human-authored work.
- Use Linear's MCP (Model Context Protocol) server for issue work, per [linear.md](linear.md) — create and update issues there, and say what changed and why.
- Commit with a `Co-Authored-By` trailer identifying the model or agent that produced the change.

## Boundaries

- Don't push to `main` on a repo with more than one contributor — open a PR, per [standards.md](standards.md).
- Don't create or delete repos.
- Don't publish to app stores or deploy to production without an explicit human go-ahead in the session.

## Review

Agent-produced changes get the same review as human changes — no lighter bar because a PR was written by an agent. See [collaboration.md](collaboration.md).
