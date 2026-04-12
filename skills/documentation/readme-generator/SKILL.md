---
name: readme-generator
description: Draft or rewrite GitHub README.md files for repositories, libraries, apps, CLIs, and internal tools. Use when Codex needs to inspect a codebase, shape a stronger README structure, center a mostly lowercase title when it fits, add image placeholders for screenshots or diagrams, and produce concise project documentation that feels edited instead of templated.
---

# README Generator

Write README files that feel intentional. Prefer a small number of strong sections, short paragraphs, and GitHub-native formatting used with restraint.

## Working Pass

1. Inspect the repository before writing. Read the manifest, scripts, entrypoints, test setup, existing docs, and any current README material. Do not invent commands, features, or support claims.
2. Decide the shape from the product type. Libraries need install and usage. Apps need setup, run, and visual context. CLIs need commands and examples. Internal tools can stay shorter.
3. Build the smallest complete README. The default order is a centered title block, a short summary, a brief overview, setup or installation, usage, and only the extra sections the repository genuinely earns.
4. Compress the draft. Remove generic feature dumps, redundant headings, and sections that only repeat what the file tree already says.

## House Style

Use lowercase titles in most cases. Preserve official brand casing only when the project already treats the name as fixed.

Center the title and short tagline for most GitHub-facing READMEs. HTML is fine when it improves the layout.

Prefer prose over bullet spam. Use lists only when the content is genuinely list-shaped. Keep the tone technical and calm. Avoid marketing adjectives, filler claims, and long throat-clearing intros.

Use badges, tables, alerts, details blocks, footnotes, Mermaid diagrams, and inline HTML selectively. Read [references/github-readme-patterns.md](references/github-readme-patterns.md) before reaching for them.

## Title Block

Start from this pattern when the repository does not already have a better visual identity:

```markdown
<p align="center">
  <img src="./docs/placeholder-hero.png" alt="project preview" width="1200" />
</p>

<h1 align="center">project name</h1>

<p align="center">one sharp sentence about what the project does.</p>
```

If the repository has no real screenshots or diagrams yet, insert a clearly labeled placeholder and tell the user to replace it:

```markdown
<!-- Replace docs/placeholder-hero.png with a real screenshot, UI crop, or architecture diagram. -->
```

Only include an image slot when a visual would materially speed up understanding. Use it for apps, extensions, dashboards, or diagrams. For invisible tools or tiny libraries, skip the hero instead of forcing a placeholder.

## Section Decisions

Write a short overview when the repository needs context beyond the summary line. Focus on the problem, the angle, and the scope in two to four sentences.

Include installation or setup only when the repository exposes real commands. Favor one happy-path example over a matrix of package managers unless the project already supports many officially.

Include development or contribution notes only if the repository has a credible contributor flow. If there is no tested workflow, leave that section out rather than padding it with generic advice.

Add optional sections only when either the repository already exposes the information or a first-time reader would be blocked without it. If neither is true, leave the section out.

When the repository already has a README, keep the strongest material and rewrite around it instead of flattening everything into a new template.

## Final Checks

Confirm that every command exists, every linked path is real, every section earns its place, and the first screenful explains the project quickly.

Leave explicit placeholders only for facts the repository cannot reveal on its own. If a placeholder is visual, ask the user to replace it with a real image after generation.

## Avoid

- Do not turn the README into a Markdown feature demo.
- Do not open with a giant feature checklist.
- Do not mirror generic SaaS landing-page language.
- Do not keep sections for roadmap, contributing, acknowledgments, or license unless the repository actually benefits from them.
