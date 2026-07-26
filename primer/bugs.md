# Bugs

The bug lifecycle: **report → triage → fix → verify**.

## Reporting

External reporters (without access to [Linear](https://linear.app), Artifact's issue tracker) open a GitHub issue using the org's bug report template. Include repro steps, expected vs. actual behavior, and platform (browser/OS/device).

Internal reporters — anyone with Linear access — skip GitHub and file straight into Linear with the **Bug** label, attached to the product's project.

## Triage

Every bug gets a project, a priority, and the **Bug** label (see [linear.md](linear.md) for the label set). Priority is set at triage, not at creation — reserve **Urgent** for data loss or broken production.

Bugs reported via GitHub are mirrored into Linear during triage. Once fixed, the GitHub issue is closed with a link to the Linear issue.

## Fixing

Branch as `<user>/a-<number>-<short-slug>`, copied from the Linear issue. Include `Fixes A-123` in the pull request (PR) description to auto-close the issue on merge. Add a regression test where the stack has tests.

## Verifying

Before marking the issue Done, confirm the fix on the deployed target — see [deployment.md](deployment.md) for where each product runs.
