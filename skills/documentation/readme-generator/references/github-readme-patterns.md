# GitHub README Patterns

Use this file as a palette, not a checklist. A strong README picks a few moves that fit the repo and leaves the rest alone.

## Structural blocks

- Centered title block with `<h1 align="center">` and a short tagline.
- One-paragraph overview that explains problem, angle, and scope.
- Setup or install commands in a fenced block.
- A usage section with one clear happy-path example before any edge cases.

## Visual blocks

- Image or screenshot: useful for apps, extensions, dashboards, or diagrams. If no asset exists yet, leave a placeholder comment and tell the user to replace it.
- Badges: useful when they add real signal such as CI, package version, or license. Skip vanity badge stacks.
- Tables: useful for option matrices, commands, environment variables, or feature comparison. Do not force tables for narrative content.

## GitHub-native formatting

- Alerts for short warnings or notes:

```markdown
> [!NOTE]
> This tool rewrites `README.md` in place.
```

- Collapsed details for long command references or optional setup:

```markdown
<details>
<summary>advanced setup</summary>

Extra content here.

</details>
```

- Task lists for roadmaps or setup verification, but only when boxes help scanning.
- Footnotes when a short citation or caveat would clutter the main paragraph.
- Mermaid for lightweight architecture or flow diagrams when text alone is slower to parse.

## Inline HTML

GitHub README files tolerate small amounts of HTML well. Use it for centered hero blocks, tighter image layouts, or a controlled intro. Do not build the whole README out of HTML.

## Compression heuristics

- Cut repeated information between summary, overview, and features.
- Convert weak bullet lists into a paragraph.
- Keep the first visible screen useful without scrolling.
- Prefer one strong example over many shallow ones.
