<h1 align="center">github documentation skills</h1>

<p align="center">Two Codex skills for tighter GitHub READMEs and terse changelogs.</p>

This repo contains two original documentation skills inspired by the public `claude-code-marketplace` repo, but rewritten to be stricter, shorter, and less template-heavy.

`readme-generator` writes minimal-first READMEs with stronger structure, centered lowercase titles when they fit, and optional image placeholders that ask the user to replace them later.

`changelog-generator` turns commit history or release notes into short developer-facing changelog entries without hype or commit-message copy-paste.

## install

Copy the skill folders into your Codex skills path, usually `~/.codex/skills` or `$CODEX_HOME/skills`.

```bash
cp -r skills/documentation/readme-generator ~/.codex/skills/
cp -r skills/automation/changelog-generator ~/.codex/skills/
```
