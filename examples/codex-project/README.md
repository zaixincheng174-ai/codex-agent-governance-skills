# Example Project Adapter

Copy `AGENTS.md` into a real project when you want that project to reference this governance pack.

## Install into a project

```sh
cp examples/codex-project/AGENTS.md /path/to/project/AGENTS.md
```

Then update only the project-specific section in the copied adapter.

## Point a project at the pack

Keep the governance pack available near the project or in a known shared location. The adapter should reference:

- `core/AGENTS.override.md`
- `core/skills/`
- `skills/agent-governance/SKILL.md`

## Update the pack later

Update canonical files by replacing `core/` from the active source materials, then rerun validation. Do not hand-edit protected source files in place.

## Avoid mutating protected sources

Use project-level additions for local rules. Keep `core/` as the preserved source copy.
