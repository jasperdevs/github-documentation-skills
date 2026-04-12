---
name: readme-generator
description: Draft or rewrite GitHub README.md files for repositories, libraries, apps, CLIs, and internal tools. Use when Codex needs to inspect a codebase, shape a stronger README structure, center a mostly lowercase project title when it fits, add image placeholders for screenshots or diagrams, and produce concise project documentation that stays minimal by default while still using useful GitHub Markdown features such as badges, tables, alerts, details blocks, task lists, diagrams, footnotes, star-history charts, images, and links when they improve clarity.
---

# README Generator

Write README files that feel edited, not templated. Minimal is the default, but not at the cost of clarity.

## Working Pass

1. Inspect the repository before writing. Read the manifest, scripts, entrypoints, test setup, existing docs, and any current README material. Do not invent commands, features, or support claims.
2. Decide the shape from the product type. Libraries need install and usage. Apps need setup, run, and visual context. CLIs need commands and examples. Internal tools can stay shorter.
3. Before adding richer formatting, read [references/github-readme-patterns.md](references/github-readme-patterns.md) and [references/github-markdown-docs.md](references/github-markdown-docs.md).
4. Build the smallest complete README. The default shape is a centered title block, one short summary paragraph, and only the install or usage material a reader actually needs.
5. Compress the draft. Remove generic feature dumps, redundant headings, and sections that only repeat what the file tree already says.

## Default Length

Aim for the shortest README that still lets a new reader understand the project and start using it. Most repos only need a title, one paragraph, one install block, and one usage example.

Expand only when a reader would otherwise be blocked, confused, or likely to misuse the project.

## House Style

Use lowercase for the project title when it fits the project's visual identity. Do not force every section heading to lowercase. Use normal Title Case or sentence case for section headings unless the repository already has a clear style.

Center the title and short tagline for most GitHub-facing READMEs. HTML is fine when it improves the layout.

Prefer prose over bullet spam. Use lists only when the content is genuinely list-shaped. Keep the tone technical and calm. Avoid marketing adjectives, filler claims, long throat-clearing intros, and essay-length explanations.

Use badges, tables, alerts, details blocks, footnotes, diagrams, task lists, images, star-history charts, and inline HTML when they make the README faster to scan or shorter overall. If a richer element does not improve comprehension, cut it.

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

Write at most one short overview paragraph when the summary line is not enough. If the title block and one sentence already do the job, skip the overview entirely.

Include installation or setup only when the repository exposes real commands. Favor one happy-path example over a matrix of package managers unless the project already supports many officially.

Include usage only when a reader needs an example beyond the install or run command itself.

Use tables when they compress comparisons, commands, options, environments, compatibility notes, or feature differences better than prose.

Use a quick-links row only when the repo has meaningful destinations such as docs, demo, website, API reference, examples, Discord, or issue tracker, and the reader benefits from jumping there immediately.

Use badges when they add real signal near the top of the README, such as CI status, package version, license, coverage, or release channel. Skip vanity badge piles.

Use alerts when a warning or caveat is important enough to isolate.

Use details blocks when setup is optional or would otherwise bloat the default path.

Use task lists for setup checklists or short roadmaps only when checkboxes genuinely improve scanning.

Use footnotes for small caveats that would otherwise interrupt a sentence.

Use diagrams only when a workflow, architecture, or data flow is hard to explain in one paragraph.

Use a star-history chart only for public repositories where project momentum or community growth is relevant. Put it near the bottom of the README, usually under a `Star History` heading, and prefer the common `star-history.com` image-link pattern.

Use a short `Why` or `Why not` section only when the category is crowded, the tradeoffs matter, or the reader would not quickly understand why this project exists.

Use a compatibility matrix only when runtime, platform, browser, version, or environment support materially affects adoption.

Use an examples section when the install command is not enough to teach first use. Keep it to one to three strong examples.

Use troubleshooting or FAQ only when setup friction is common enough that a short section will save users time.

Use contributing, security, support, and license sections briefly for public repos when the reader needs those links in the README. If they can live better in dedicated docs, keep the README version short.

Use benchmarks only when performance is a real selling point and the repo has measured data worth showing.

Use ecosystem or integrations only when the project has adapters, plugins, supported frameworks, or companion packages that materially change adoption decisions.

Use a docs split rule when the README is starting to carry too much detail. The README should orient, install, and prove value quickly; deep guides can move to `/docs`, a website, or dedicated files.

Include development or contribution notes only if the repository has a credible contributor flow and a reader needs that information in the README. If there is no tested workflow, or if the material belongs in separate docs, leave it out.

Add optional sections only when leaving them out would make the README unclear, unsafe, or incomplete for first use. If neither is true, leave the section out.

When several formatting options could work, choose the smallest one that improves comprehension. A short table is better than four repetitive bullets. A collapsed details block is better than forcing optional setup into the default path.

When deciding whether to add a section, ask one question first: does this help a reader understand, adopt, trust, or evaluate the project faster? If not, leave it out.

When the repository already has a README, keep the strongest material and rewrite around it instead of flattening everything into a new template.

## Final Checks

Confirm that every command exists, every linked path is real, every section earns its place, and the first screenful explains the project quickly.

Leave explicit placeholders only for facts the repository cannot reveal on its own. If a placeholder is visual, ask the user to replace it with a real image after generation.

If the README uses advanced formatting, make sure each element earns its place. Rich Markdown should reduce clutter, not create it.

If badges or a star-history chart are included, verify that the links resolve and that they reflect real project state rather than decorative filler.

## Avoid

- Do not turn the README into a Markdown feature demo.
- Do not write a mini-docs site when a short README would do the job.
- Do not open with a giant feature checklist.
- Do not stack a wall of low-signal badges across the top.
- Do not mirror generic SaaS landing-page language.
- Do not repeat the same information in the summary, overview, table, and usage example.
- Do not add `Why`, compatibility, FAQ, benchmarks, ecosystem, or security sections just because large repos often have them.
- Do not keep sections for development, roadmap, contributing, acknowledgments, or license unless the repository actually benefits from them.
