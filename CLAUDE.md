# CLAUDE.md

## Repository Structure

This is a mono-collection repo managing multiple Claude Code skill/hook sub-repos as git submodules:

- `ClaudeCode-Alert-Hook/` — TTS notification hook
- `ClaudeCode-PDF-Skill/` — Markdown-to-PDF export skill
- `ClaudeCode-SeeFig-Skill/` — Figure analysis skill via vision LLM

Each sub-repo follows the `.claude/` directory convention and can be merged directly into any project.

## Git Management

- **Push always means pushing all sub-repos individually first, then the main repo.**
- After making changes in a sub-repo, commit and push that sub-repo before committing the parent.
- Update the parent's submodule reference after each sub-repo push.

## Code & Documentation Standards

- All code comments, docstrings, and documentation MUST be written in English.
- README, SETUP, SKILL.md — all in English.
- Commit messages in English.

## Design Constraints

- **No OS-specific dependencies.** All scripts must work on macOS, Windows, and Linux without requiring platform-specific install steps.
  - Use Python's `platform.system()` for runtime branching, not separate scripts.
  - Use `sys.executable` instead of hardcoding `python` or `python3`.
  - npm/pip packages must be cross-platform.
- **Verify structure after changes.** When restructuring files, confirm paths in settings.local.json, SKILL.md, and scripts still align.
- **Verify functionality.** After any script change, run a quick sanity check (e.g., `python -c "import edge_tts"` or `--help` flag) to confirm nothing is broken.
