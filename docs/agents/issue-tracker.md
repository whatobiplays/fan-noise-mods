# Issue tracker: GitHub

Issues and specifications live in GitHub Issues for
`whatobiplays/fan-noise-mods`.

## Access and operations

Use the `whatobiplays` GitHub connection for connected GitHub tools.
For CLI operations, use `gh` authenticated as `whatobiplays` and
target `--repo whatobiplays/fan-noise-mods`.

- Create: `gh issue create --title "..." --body-file <path>`.
- Read: `gh issue view <number> --comments`.
- List: `gh issue list --state open --json number,title,body,labels`.
- Comment: `gh issue comment <number> --body-file <path>`.
- Label: `gh issue edit <number> --add-label "..."` or
  `--remove-label "..."`.
- Close: `gh issue close <number>`.

Add the explicit `--repo` option to each command. Write multiline
bodies to a file and pass that file through `--body-file`.

When a skill says "publish to the issue tracker", create a GitHub
issue. When it says "fetch the relevant ticket", read the issue
and its comments.

## Pull requests as a triage surface

**PRs as a request surface: no.**

GitHub issues and pull requests share a number space. When a
reference is ambiguous, resolve whether it identifies an issue
or a pull request before acting.

## Wayfinding operations

A wayfinding map is an issue labelled `wayfinder:map` containing
Notes, Decisions-so-far, and Fog sections.

Create child tickets as GitHub sub-issues. If sub-issues are
unavailable, list the children in the map's task list and add
`Part of #<map>` to each child.

Use `wayfinder:research`, `wayfinder:prototype`,
`wayfinder:grilling`, or `wayfinder:task` for ticket types.

Represent blockers with native GitHub issue dependencies.
If unavailable, add `Blocked by: #<number>` references to the
child ticket. A ticket is unblocked when all its blockers close.

Choose the first open, unassigned, unblocked child in map order.
Claim it by assigning the driving developer. On resolution,
publish the result, close the child, and add a result summary
and link to the map's Decisions-so-far section.
