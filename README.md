# ClaudeCode for Researcher

A curated collection of Claude Code skills and hooks designed for researchers.

## What's Inside

| Module | Type | Description |
|--------|------|-------------|
| [ClaudeCode-Alert-Hook](https://github.com/sangwonme/ClaudeCode-Alert-Hook) | Hook | TTS voice alerts & sound notifications when Claude finishes tasks or needs permission |
| [ClaudeCode-PDF-Skill](https://github.com/sangwonme/ClaudeCode-PDF-Skill) | Skill | Export Markdown to styled PDF with Mermaid diagram & CJK support |
| [ClaudeCode-SeeFig-Skill](https://github.com/sangwonme/ClaudeCode-SeeFig-Skill) | Skill | Understand, review, caption, and describe figures using vision LLMs |

## Quick Setup

Each module can be installed independently. Just tell Claude Code:

```
Setup this skill: https://github.com/sangwonme/ClaudeCode-PDF-Skill.git
```

```
Setup this skill: https://github.com/sangwonme/ClaudeCode-SeeFig-Skill.git
```

```
Setup this hook: https://github.com/sangwonme/ClaudeCode-Alert-Hook.git
```

Claude will clone the repo and configure everything automatically.

## Requirements

| Module | Dependencies |
|--------|-------------|
| Alert-Hook | Python 3.8+, `edge-tts` |
| PDF-Skill | Node.js, `md-to-pdf`, (optional) `@mermaid-js/mermaid-cli` |
| SeeFig-Skill | Python 3.8+, `openai`, `python-dotenv`, `OPENAI_API_KEY` |

## License

MIT
