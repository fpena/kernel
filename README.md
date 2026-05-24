# Kernel

Personal agent skills for writing and workflow.

## Quickstart (30-second setup)

1. Run the skills.sh installer:

```bash
npx skills@latest add fpena/kernel
```

Useful flags:

- `-g` — install globally (available in all projects)
- `-a cursor` — target Cursor only
- `--list` — list available skills without installing
- `--copy` — copy files instead of symlinking (for vendoring into a project)

2. Pick the skills you want and which coding agents to install them on. **Make sure you select `/setup-kernel-skills`.**

3. Run `/setup-kernel-skills` in your agent. It will detect where skills are installed and optionally add an `## Agent skills` block to your project's `CLAUDE.md` or `AGENTS.md`.

4. You're ready to go.

## Manual install

If you prefer not to use the CLI, copy or symlink skill folders into your agent's skills directory:

| Agent | Global path | Project path |
| --- | --- | --- |
| Cursor | `~/.cursor/skills/` | `.cursor/skills/` (or `.agents/skills/` via skills CLI) |
| Claude Code | `~/.claude/skills/` | `.claude/skills/` |
| Codex | per [skills CLI docs](https://www.npmjs.com/package/skills) | same |

Each skill is a folder containing a `SKILL.md` file. See the [Reference](#reference) below for paths in this repo.

## Reference

### Documentation

- **[document-polish](./skills/documentation/document-polish/SKILL.md)** — Polish drafts for clarity, structure, and Refactoring-style hierarchy. Use when editing articles, newsletters, reports, or any long-form doc.

### Productivity

- **[setup-kernel-skills](./skills/productivity/setup-kernel-skills/SKILL.md)** — One-time setup for where kernel skills are installed and how to invoke them. Run once per repo before using other kernel skills in a new project.
