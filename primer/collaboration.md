# Collaboration

Artifact is a small, mostly-solo team today, preparing to bring on contractors and collaborators. The rules below are written for that scale-up: defaults that work with one person and tighten automatically as more people join.

## Onboarding

Read the Primer first — it's the fastest path to how Artifact works. From there, get access to [Linear](https://linear.app) (issue tracking) and the GitHub org. Each repo's README and CLAUDE.md cover everything specific to that project — setup, stack, and conventions.

## Branching & PRs

Branch off `main` using the Linear-derived format from [standards.md](standards.md): `<user>/a-<number>-<short-slug>`. Open a pull request (PR) for anything non-trivial.

Solo maintainers may push small fixes directly to `main`. Once a repo has more than one contributor, direct pushes to `main` stop — everything goes through a PR.

## Review

Review for correctness and clarity — not style nits already covered by [standards.md](standards.md). The author merges their own PR once it's approved. Reviews are expected within a working day.

## Working with agents

Agent-produced changes get the same review as human changes — no lighter bar because a PR was written by Claude Code or another agent. An agent session should leave the repo clean: work is either committed or stashed, never left dangling uncommitted. See [agents.md](agents.md) for agent-specific conventions.

## Communication

Chat is fine for discussion, but any decision that outlives the conversation belongs in the repo's docs or in Linear — not buried in a thread. If it matters later, write it down where the next contributor (human or agent) will actually find it.
