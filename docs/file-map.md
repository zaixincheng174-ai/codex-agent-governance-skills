# File Map

This repository is intentionally shallow so the useful files are visible quickly.

## Canonical sources

- `core/AGENTS.override.md` - active governance override, copied byte-for-byte.
- `core/skills/` - included local skill folders, copied byte-for-byte.

## Wrapper and metadata

- `skills/agent-governance/SKILL.md` - public entrypoint that points to canonical files.
- `skills/agent-governance/manifest.json` - wrapper skill metadata.
- `manifest.json` - repo-level display order and source policy.
- `skill-pack.json` - skill-pack entrypoint and reading order.
- `.gitattributes` - preserves copied third-party license formatting during Git whitespace checks.

## User-facing docs

- `README.md`
- `QUICKSTART.md`
- `INSTALL.md`
- `SKILL_INDEX.md`
- `docs/discovery-report.md`
- `docs/packaging.md`
- `docs/usage-notes.md`
- `docs/validation-report.md`
- `docs/post-audit.md`
- `docs/demo-false-pass.md`
- `docs/launch-kit.md`
- `docs/launch-tracker.md`

## Launch assets

- `assets/social-preview.png` - share-card image for GitHub/X/HN.
- `assets/social-preview.svg` - editable source for the share-card image.

## Example

- `examples/codex-project/AGENTS.md` - minimal adapter for a target project.
- `examples/codex-project/README.md` - adapter usage notes.

## Package artifact

- `dist/codex-agent-governance-skills-v0.1.0.zip` - distribution ZIP built from the public pack contents.
