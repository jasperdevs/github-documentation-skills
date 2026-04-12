<h1 align="center">github documentation skills</h1>

<p align="center">Two Codex skills for writing GitHub-native project docs with less boilerplate and tighter language.</p>

This repo contains an original rewrite of two documentation-focused skills inspired by the public `claude-code-marketplace` repository. The goal is not to mirror those files. The goal is to make them stricter, cleaner, and more useful in day-to-day repo work.

The `readme-generator` skill pushes toward shorter, more intentional README files. It prefers strong structure over giant section dumps, defaults to a centered mostly lowercase title when that fits, and can leave image placeholders with an explicit note telling the user to replace them later. Minimal is the default, and developer-only sections stay out unless they are actually needed.

The `changelog-generator` skill writes terse release notes for developers. It compresses noisy commit history into small, technical entries and avoids hype, padding, and copy-pasted commit subjects.

## included skills

| skill | focus | notable behavior |
| --- | --- | --- |
| `readme-generator` | GitHub README drafting and rewrites | centered title block, selective Markdown features, image placeholders when assets are missing |
| `changelog-generator` | release notes and `CHANGELOG.md` updates | concise developer language, tight grouping, aggressive compression |

## install

Copy either skill directory into your Codex skills path, usually `~/.codex/skills` or `$CODEX_HOME/skills`.

```bash
cp -r skills/documentation/readme-generator ~/.codex/skills/
cp -r skills/automation/changelog-generator ~/.codex/skills/
```

If you keep a custom skill repo, symlink them instead.

## use

```text
Use $readme-generator to rewrite this repo README so the title is centered, the structure is tighter, and missing screenshots are left as placeholders.
```

```text
Use $changelog-generator to turn the last release worth of commits into a terse unreleased section.
```

## notes

The README skill draws from a broad GitHub Markdown palette without forcing every trick into every file. The changelog skill aims for the opposite of release-marketing prose.

If you want prettier visuals, add real screenshots or diagrams after generation. The README skill can reserve the slot, but it should ask a human to replace the placeholder asset.
