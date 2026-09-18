# Fork Strategy

This repository is a fork of `linshenkx/prompt-optimizer`. Treat upstream tracking as the default until this fork has a deliberate, tested reason to diverge.

## Before adding a local feature

1. Check whether current upstream already provides the capability.
2. Identify the local requirement that upstream does not cover.
3. State the expected user-visible or engineering benefit.
4. Add or update tests that would fail without the local change.
5. Document the local delta and the upstream commit/version it was based on.

## Fork states

Use one of these states intentionally:

### Tracking fork

Use when the repository is primarily for study, backup, or local deployment.

- keep local changes minimal;
- prefer upstream fixes;
- periodically compare/sync;
- do not present inherited upstream capabilities as local innovations.

### Intentional variant

Use only when there is a maintained local product direction.

Maintain:

- `docs/fork-delta.md` describing local behavior;
- tests for each important local delta;
- a repeatable upstream rebase/sync procedure;
- release notes that separate upstream changes from local changes.

### Archived/reference fork

Use when the code is retained for historical or learning purposes but should not receive active feature development.

## Recommended first audit

Before feature work, compare the current fork against upstream and group differences by:

- provider/model support;
- prompt optimization/evaluation;
- tests and regression coverage;
- web/extension behavior;
- storage and data migration;
- deployment;
- documentation.

Only after this audit should a new local architecture or feature roadmap be approved.
