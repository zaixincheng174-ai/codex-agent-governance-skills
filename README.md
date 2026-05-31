# Codex Agent Governance Skills

A reusable governance and execution-control skill pack for Codex and coding agents, focused on audit discipline, scope control, evidence-based findings, validation, and safe execution boundaries.

## What this is

This repository packages an active Codex governance override and local governance skills into a shallow, reusable skill pack. The canonical protected materials live under [core/](core/).

## Who this is for

Use this if you want coding agents to follow explicit task sizing, audit, planning, execution, validation, diff-scope, and closeout discipline across projects.

## What problem it solves

Agent work often drifts into broad rewrites, weak claims, unverified fixes, or unsafe execution. This pack gives Codex a reusable control layer for scope boundaries, evidence requirements, stop conditions, and reviewable closeout.

## Quick start

1. Read [QUICKSTART.md](QUICKSTART.md).
2. Inspect [core/AGENTS.override.md](core/AGENTS.override.md).
3. Inspect [core/skills/](core/skills/).
4. Use [skills/agent-governance/SKILL.md](skills/agent-governance/SKILL.md) as the public skill entrypoint.
5. Copy [examples/codex-project/AGENTS.md](examples/codex-project/AGENTS.md) into a target project if needed.
6. Use [INSTALL.md](INSTALL.md) for installation and package instructions.

## Repository map

| Path | Purpose | Type |
|---|---|---|
| [QUICKSTART.md](QUICKSTART.md) | Five-minute usage path and first files to inspect. | documentation |
| [INSTALL.md](INSTALL.md) | Manual and ZIP installation instructions. | documentation |
| [SKILL_INDEX.md](SKILL_INDEX.md) | Ordered list of included skills and entrypoints. | documentation |
| [core/AGENTS.override.md](core/AGENTS.override.md) | Byte-for-byte copied active global governance override. | canonical source |
| [core/skills/](core/skills/) | Byte-for-byte copied local skill folders included in this pack. | canonical source |
| [skills/agent-governance/SKILL.md](skills/agent-governance/SKILL.md) | Public wrapper skill that points to the canonical materials. | wrapper |
| [examples/codex-project/AGENTS.md](examples/codex-project/AGENTS.md) | Minimal project adapter for using the pack elsewhere. | example |
| [docs/file-map.md](docs/file-map.md) | Layout and canonical-source map. | documentation |
| [docs/discovery-report.md](docs/discovery-report.md) | Source discovery, inclusion, exclusion, and hashes. | documentation |
| [docs/packaging.md](docs/packaging.md) | ZIP build notes and package contents. | documentation |
| [docs/usage-notes.md](docs/usage-notes.md) | Practical usage notes without rewriting protected materials. | documentation |
| [docs/validation-report.md](docs/validation-report.md) | Validation command results. | documentation |
| [docs/post-audit.md](docs/post-audit.md) | Final post-audit and verdicts. | documentation |
| [manifest.json](manifest.json) | Repository-level display and source metadata. | metadata |
| [skill-pack.json](skill-pack.json) | Skill-pack metadata and reading order. | metadata |
| [dist/codex-agent-governance-skills-v0.1.0.zip](dist/codex-agent-governance-skills-v0.1.0.zip) | Distribution archive. | package artifact |
| [.gitattributes](.gitattributes) | Preserves copied third-party license formatting during Git whitespace checks. | metadata |

## Recommended reading/install order

1. [QUICKSTART.md](QUICKSTART.md)
2. [SKILL_INDEX.md](SKILL_INDEX.md)
3. [core/AGENTS.override.md](core/AGENTS.override.md)
4. [core/skills/](core/skills/)
5. [skills/agent-governance/SKILL.md](skills/agent-governance/SKILL.md)
6. [examples/codex-project/AGENTS.md](examples/codex-project/AGENTS.md)
7. [INSTALL.md](INSTALL.md)

## Canonical source files

The files under [core/](core/) are protected canonical materials. Do not casually rewrite them. If you need a project-specific adaptation, add an adapter or wrapper outside `core/` and keep the canonical copy intact.

## Skill pack wrapper

The public wrapper skill is [skills/agent-governance/SKILL.md](skills/agent-governance/SKILL.md). It points to the canonical override and included skills instead of duplicating or rewriting them.

## Example project adapter

The example adapter at [examples/codex-project/AGENTS.md](examples/codex-project/AGENTS.md) shows how another project can point Codex at this governance pack while keeping local project rules separate.

## Safety and privacy warning

Before publishing changes to this repository, run the validation and secret/privacy scans described in [docs/validation-report.md](docs/validation-report.md). Do not add `.env`, credentials, tokens, browser exports, private notes, raw client data, or unrelated personal files.

## Contribution policy

Changes to wrapper files, examples, metadata, and docs are normal contributions. Changes under `core/` should only happen by replacing the canonical source from the active local governance material and re-running byte-for-byte hash validation.

## License

This repository is released under the license in [LICENSE](LICENSE). Third-party notices preserved inside copied skill folders remain governed by their original terms.
