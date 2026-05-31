# Install

This pack is intentionally simple: the canonical materials are plain files and folders.

## Manual install

Copy the governance override:

```sh
cp core/AGENTS.override.md ~/.codex/AGENTS.override.md
```

Copy or sync the included skills:

```sh
mkdir -p ~/.codex/skills
cp -R core/skills/* ~/.codex/skills/
```

Use the wrapper skill as the public entrypoint:

```text
skills/agent-governance/SKILL.md
```

The wrapper points back to:

- `../../core/AGENTS.override.md`
- `../../core/skills/`

## Project adapter install

Copy the example adapter into a target project:

```sh
cp examples/codex-project/AGENTS.md /path/to/project/AGENTS.md
```

Then keep project-specific constraints in the project adapter. Do not duplicate the full protected source content there.

## ZIP install

The distribution archive is:

```text
dist/codex-agent-governance-skills-v0.1.0.zip
```

Unzip it and copy the same canonical paths:

```sh
unzip dist/codex-agent-governance-skills-v0.1.0.zip -d /tmp/codex-agent-governance-skills
cp /tmp/codex-agent-governance-skills/core/AGENTS.override.md ~/.codex/AGENTS.override.md
cp -R /tmp/codex-agent-governance-skills/core/skills/* ~/.codex/skills/
```

## Updating later

Replace files under `core/` only from the active canonical local source, then rerun hash validation. Adaptation belongs in wrappers, examples, or project-level `AGENTS.md` files.
