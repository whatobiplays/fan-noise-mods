# Domain documentation

This repository uses a single-context domain documentation layout.

## Before exploring

Read `GLOSSARY.md` at the repository root, when present.
Read relevant architectural decision records in `docs/adr/`.

If these documents are absent, continue silently. Create them
through the domain-modeling skill when terminology or architectural
decisions are resolved.

## Layout

- `GLOSSARY.md`: repository-wide domain terminology.
- `docs/adr/`: architectural decision records.

## Vocabulary and decisions

Use glossary terms consistently in issue titles, proposals,
documentation, and test names.

If a required concept is missing, first check whether an existing
term describes it. Record a genuine vocabulary gap for
domain modeling.

Explicitly identify any proposal that conflicts with an existing
ADR, including the ADR identifier and the reason to reconsider it.
