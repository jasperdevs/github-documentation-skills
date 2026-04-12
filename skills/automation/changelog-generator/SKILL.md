---
name: changelog-generator
description: Draft or update concise changelog entries from git history, pull requests, release diffs, or explicit change notes. Use when Codex needs terse developer-facing release notes, an unreleased section, or a versioned changelog without marketing language, bloated explanations, commit-message copy-paste, or duplicate bullets.
---

# Changelog Generator

Write changelogs for people shipping code. Keep them short, technical, and easy to scan.

## Working Pass

1. Gather the actual change set from `git log`, a diff, merged pull requests, or the user's explicit notes. Read the existing `CHANGELOG.md` first when it exists.
2. Rank the sources. Prefer shipped behavior over commit wording: release notes, merged PR summaries, touched files, then commit subjects.
3. Normalize each item into a plain technical statement. Commit subjects are signals, not final wording.
4. Group only when grouping improves scan speed. Default sections are `added`, `changed`, `fixed`, `removed`, and `security`. Skip empty sections.
5. Compress again. One bullet should usually express one shipped outcome.

## Style

Lead with the change. Use direct verbs such as `add`, `fix`, `remove`, `rename`, `tighten`, `support`, and `deprecate`.

Prefer concrete code nouns over vague outcomes. Name the API, command, route, flag, file, or subsystem when it matters.

Keep bullets one line when possible. Do not write marketing copy, process narrative, or "improved experience" filler unless the shipped effect would otherwise be unclear.

Prefer user-visible or integrator-visible changes. Skip docs-only edits, test-only edits, CI churn, and internal cleanup unless they materially change how someone uses, deploys, or extends the project.

Read [references/changelog-style.md](references/changelog-style.md) before finalizing wording.

## Format

Use this default shape unless the repository already follows something else:

```markdown
## unreleased

### added
- support GitHub Actions badge detection

### changed
- tighten generated README section order

### fixed
- preserve existing install commands during rewrite
```

For releases, use `## 0.2.0 - 2026-04-12`.

Put breaking changes first. If a migration is required, state the action directly in one short line.

## Source Handling

Cross-check touched files when commit messages are vague. If several commits describe the same shipped result, collapse them into one bullet.

Drop noise such as dependency churn, typo fixes, or internal refactors unless they affect users, contributors, or integrators in a meaningful way.

When the same idea shows up in multiple commits, write one stronger bullet instead of three weak ones.

If a change belongs in both `changed` and `fixed`, choose the one that best describes external impact and avoid duplicates.

## Release Heuristics

Use `unreleased` for work that has landed but is not cut into a version yet.

Use a dated version heading only when the user is preparing an actual release section.

If there are only one or two meaningful entries, keep the changelog extremely short. Do not pad it just to make the section feel balanced.

## Avoid

- Do not restate commit subjects verbatim.
- Do not explain implementation details that did not change external behavior.
- Do not split one shipped outcome into several nearly identical bullets.
- Do not keep empty sections for symmetry.
- Do not pad release notes with adjectives or summary paragraphs.
