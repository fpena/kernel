---
name: setup-kernel-skills
description: >
  One-time setup for where kernel skills are installed and how to invoke them.
  Detects agent skill paths (Cursor, Claude Code, etc.) and optionally writes
  an Agent skills block into CLAUDE.md or AGENTS.md. Run once per repo before
  using other kernel skills in a new project.
disable-model-invocation: true
---

# Setup Kernel Skills

Scaffold per-repo awareness of kernel skills:

- **Install paths** — where skills live for this user's agents
- **Project docs** — optional `## Agent skills` block in `CLAUDE.md` or `AGENTS.md`

This is a prompt-driven skill, not a deterministic script. Explore, present what you found, confirm with the user, then write.

## Process

### 1. Explore

Look at the current environment to understand the starting state. Read whatever exists; don't assume:

- `~/.cursor/skills/` — global Cursor skills
- `.cursor/skills/` and `.agents/skills/` in the current repo — project-level Cursor skills
- `~/.claude/skills/` — global Claude Code skills
- `.claude/skills/` in the current repo — project-level Claude Code skills
- Run `npx skills ls` if available — lists skills installed via the skills CLI
- `CLAUDE.md` and `AGENTS.md` at the repo root — does either exist? Is there already an `## Agent skills` section?

Check whether kernel skills (`document-polish`, `setup-kernel-skills`) appear in any of the above paths.

### 2. Present findings and ask

Summarise what's present and what's missing. Then walk the user through the decisions **one at a time** — present a section, get the user's answer, then move to the next. Don't dump all questions at once.

**Section A — Install scope.**

> Explainer: Skills can be installed globally (available in every project) or per-project (only in the current repo). Global is simpler for personal skills; project-level is better when you want the team to share the same skill set.

Ask: **global** or **project**?

If kernel skills are missing from the expected path, tell the user to install before continuing:

```bash
# Global install (all projects)
npx skills add fpena/kernel -g -a cursor

# Project install (current repo only)
npx skills add fpena/kernel -a cursor
```

Replace `cursor` with their agent (`claude-code`, `codex`, etc.).

**Section B — Primary agent.**

> Explainer: Different agents store skills in different directories. Knowing the primary agent helps verify the install landed in the right place.

Ask which agent they use: **Cursor**, **Claude Code**, or **other** (ask which).

**Section C — Project docs.**

> Explainer: An `## Agent skills` block in `CLAUDE.md` or `AGENTS.md` tells future agent sessions that kernel skills are available and where to find the catalog. This is optional but useful in repos where you use skills regularly.

Ask whether to add or update an `## Agent skills` block in the current repo.

If yes and neither `CLAUDE.md` nor `AGENTS.md` exists, ask which file to create. If one exists, edit that one — don't create the other.

### 3. Confirm and edit

If the user wants project docs, show a draft of the `## Agent skills` block using the seed template in [templates/agent-skills-block.md](./templates/agent-skills-block.md). Let them edit before writing.

If an `## Agent skills` block already exists, update it in-place rather than appending a duplicate. Don't overwrite unrelated sections.

### 4. Write

**Pick the file to edit:**

- If `CLAUDE.md` exists, edit it.
- Else if `AGENTS.md` exists, edit it.
- If neither exists and the user chose to add docs, use the file they picked in Section C.

Never create `AGENTS.md` when `CLAUDE.md` already exists (or vice versa).

Append or update the block from [templates/agent-skills-block.md](./templates/agent-skills-block.md).

### 5. Done

Tell the user setup is complete:

- Where kernel skills are installed (global vs project path)
- Which skills are available (`document-polish`, etc.)
- Whether project docs were updated

Mention they can re-run this skill if they switch agents or move from project-level to global install.
