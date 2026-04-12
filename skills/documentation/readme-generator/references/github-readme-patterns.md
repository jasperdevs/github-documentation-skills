# GitHub README Patterns

Use this file as a palette, not a checklist. Start plain and stay short.

Most repos need a centered title block, one paragraph, one install block, and one usage example. Stop there unless a reader would be blocked without more.

Use lowercase only for the project title when it fits. Keep section headings in normal Title Case or sentence case unless the repo already uses a different system.

Use an image only when the project is meaningfully visual. If the real asset does not exist yet, leave a placeholder comment and tell the user to replace it.

Use the smallest Markdown feature that improves scan speed:

| Pattern | Use it when |
| --- | --- |
| Table | You need to compare commands, options, environments, support, or feature differences quickly |
| Alert | A warning, note, or caveat is important enough to isolate |
| Details block | Setup is optional or too long for the default path |
| Task list | A setup checklist or short roadmap benefits from visible completion state |
| Footnote | A caveat is real but too small to deserve its own sentence or alert |
| Mermaid | A tiny diagram is clearer than a paragraph |
| Inline HTML | Centering or image layout improves the intro without taking over the file |

Keep the first screen useful. Prefer one strong example over several shallow ones. Drop developer-only sections unless they are required for setup, contribution, or safe use.

Cut repeated information between the summary, overview, table, and usage. If a section only proves that the repo has files, delete it.

If you need support details beyond this guide, read [github-markdown-docs.md](github-markdown-docs.md).
