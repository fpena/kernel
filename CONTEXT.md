# Kernel Skills

A collection of agent skills (slash commands and behaviors) loaded by coding agents. Skills are organized into buckets and installed via the [skills CLI](https://www.npmjs.com/package/skills).

## Language

**Skill**:
A folder containing a `SKILL.md` file (plus optional bundled resources). The agent loads skills by matching the user's request against each skill's `description` frontmatter.
_Avoid_: prompt, command file (unless referring to slash commands specifically)

**Bucket**:
A category folder under `skills/` that groups related skills (e.g. `documentation/`, `productivity/`).
_Avoid_: category, namespace

**Setup skill**:
A one-time configuration skill (`setup-kernel-skills`) that detects where skills are installed and optionally writes an `## Agent skills` block into a target repo's `CLAUDE.md` or `AGENTS.md`.
_Avoid_: bootstrap script, init command

## Relationships

- A **Bucket** contains one or more **Skills**
- The **Setup skill** runs once per target repo; other skills do not depend on its output
