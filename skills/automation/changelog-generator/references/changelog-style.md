# Changelog Style

The changelog should read like a tight handoff between developers, not a marketing update.

## Wording

- Prefer `add support for X` over `introduce robust support for X`.
- Prefer `fix token refresh race` over `improve authentication reliability`.
- Prefer `rename config key to APP_TOKEN` over `update configuration handling`.

## Granularity

- Keep one bullet to one shipped outcome.
- Merge near-duplicate commits into one entry.
- Skip invisible cleanup unless it changes how someone uses, tests, deploys, or integrates with the project.

## Ordering

- Breaking changes first.
- Then new capabilities.
- Then behavior changes and fixes.
- Put maintenance-only notes last, or drop them entirely if they add no user value.

## Compression

- Cut adverbs and qualifiers.
- Drop "now", "also", and "various".
- Replace multi-clause bullets with the shortest correct form.

## Examples

Weak:

```markdown
- Improved the overall README generation experience with better formatting choices
```

Stronger:

```markdown
- tighten README section order and heading casing
```

Weak:

```markdown
- Added several fixes for image support and placeholder handling
```

Stronger:

```markdown
- add placeholder image comments for missing screenshots
```
