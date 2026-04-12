# GitHub Markdown Docs

Use these official GitHub Docs pages when you need to verify whether a formatting feature is supported or want a quick refresher on exact syntax.

| Topic | Use it for | Link |
| --- | --- | --- |
| Basic syntax | Headings, links, images, lists, task lists, footnotes, alerts, comments, relative image links, the `<picture>` element | https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax |
| Advanced formatting index | The full GitHub Markdown feature map | https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting |
| Workflow status badges | Official GitHub Actions badge URLs, branch/event parameters, and README usage | https://docs.github.com/en/actions/how-tos/monitor-workflows/add-a-status-badge |
| Shields docs | General badge patterns, builders, and supported badge sources | https://shields.io/docs/ |
| Shields static badges | Custom static badge syntax, styles, and logo parameters | https://shields.io/docs/static-badges |
| Tables | Column alignment, formatting inside tables, escaped pipes | https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/organizing-information-with-tables |
| Collapsed sections | `<details>` and `<summary>` blocks for optional setup or deep technical notes | https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/organizing-information-with-collapsed-sections |
| Diagrams | Mermaid, geoJSON, topoJSON, and STL support | https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams |
| Star-history embed guide | The common README pattern for a live star-history image link | https://www.star-history.com/blog/add-a-live-star-history-chart-to-your-github-readme |

## Quick map

- Use basic syntax first.
- Use a table when a comparison would otherwise become repetitive bullets.
- Use a details block when content is real but optional.
- Use an alert only when the note is important enough to isolate.
- Use a diagram only when one short paragraph cannot explain the workflow cleanly.
- Use GitHub workflow badges or Shields badges only when they communicate real status.
- Use the common star-history chart near the bottom for public repos when social proof or growth context matters.

## Common snippets

Workflow badge:

```markdown
![CI](https://github.com/OWNER/REPOSITORY/actions/workflows/ci.yml/badge.svg)
```

Static or service badge:

```markdown
![License](https://img.shields.io/badge/license-MIT-blue)
```

Star-history footer:

```markdown
## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=OWNER/REPOSITORY&type=Date)](https://www.star-history.com/#OWNER/REPOSITORY&Date)
```

GitHub also auto-generates an outline when a Markdown file has two or more headings, so clean heading structure matters even in a short README.
