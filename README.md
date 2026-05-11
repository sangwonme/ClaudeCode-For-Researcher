# ClaudeCode for Researcher

A curated collection of Claude Code skills and hooks designed for researchers. Install them with a single command and let Claude handle your research workflow — from reading figures to exporting PDFs to never missing a notification.

## What's Inside

### [ClaudeCode-Alert-Hook](https://github.com/sangwonme/ClaudeCode-Alert-Hook)

**Type:** Hook | **Triggers:** `Stop`, `PermissionRequest`

Never miss when Claude needs you. Plays a distinct chime and speaks a TTS summary when Claude finishes a task or requests permission. Works across macOS, Windows, and Linux.

- Bell sound + spoken summary on task completion
- Notification sound + "Permission needed" on permission requests
- Powered by Microsoft Edge TTS (free, no API key required)

---

### [ClaudeCode-PDF-Skill](https://github.com/sangwonme/ClaudeCode-PDF-Skill)

**Type:** Skill | **Invoke:** `/pdf`

Export any Markdown file to a beautifully styled PDF, right from Claude. Supports Mermaid diagrams, CJK fonts, and batch processing.

- Converts `.md` to PDF with custom styling
- Renders Mermaid diagrams inline
- Full CJK (Korean, Chinese, Japanese) font support
- Batch export multiple files at once

---

### [ClaudeCode-SeeFig-Skill](https://github.com/sangwonme/ClaudeCode-SeeFig-Skill)

**Type:** Skill | **Invoke:** `/seefig`

Analyze, review, caption, or write body text for research paper figures using OpenAI's vision models (GPT-4o).

- **Understand** — detailed description of layout, panels, labels, and data
- **Review** — peer-review critique with concrete improvement suggestions
- **Caption** — LaTeX-ready figure caption generation
- **Write** — draft a body paragraph referencing the figure with `\ref{}`

---

## Quick Setup

Each module can be installed independently. Just tell Claude Code:

```
Setup this hook: https://github.com/sangwonme/ClaudeCode-Alert-Hook.git
```

```
Setup this skill: https://github.com/sangwonme/ClaudeCode-PDF-Skill.git
```

```
Setup this skill: https://github.com/sangwonme/ClaudeCode-SeeFig-Skill.git
```

Claude will clone the repo and configure everything automatically.

## Requirements

| Module | Dependencies |
|--------|-------------|
| Alert-Hook | Python 3.8+, `edge-tts>=6.1.0` |
| PDF-Skill | Node.js, `md-to-pdf`, (optional) `@mermaid-js/mermaid-cli` |
| SeeFig-Skill | Python 3.8+, `openai>=1.0.0`, `python-dotenv>=1.0.0`, `OPENAI_API_KEY` |

## License

MIT
