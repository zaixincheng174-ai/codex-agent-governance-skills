# Codex Agent Governance Skills

**Stop false PASS claims in Codex agent work.**

Tests can pass. Diffs can look clean. The agent can still fail to deliver the actual capability.

This repo packages the Codex governance stack I use after heavy daily Codex work: **12.83B cumulative tokens**, **1B peak token count**, **5h25m longest task**, and a **39-day active streak**. It is built for the failure mode that shows up only when agent sessions get long: the agent keeps producing process artifacts, then says `PASS`, while the terminal artifact still does not exist.

## What You Get

Five controls that make Codex work reviewable:

1. **Task sizing** - small tasks stay light; medium/large tasks get real gates.
2. **Project lifecycle** - audit, design, build, review, verify.
3. **Repo preflight** - confirm repo root, instructions, worktree, touch set, and validation before edits.
4. **Diff-scope audit** - catch unrelated refactors, formatting spread, undeclared design drift, and secret patterns.
5. **Capability-delivery verdict** - separate "implementation looks fine" from "the actual capability exists."

The sharpest rule is the capability gate:

```text
IMPLEMENTATION_PASS_CAPABILITY_NOT_DELIVERED
```

That verdict means: the code, tests, or boundaries may be fine, but the terminal artifact is still missing. This is not success.

See the short before/after demo: [docs/demo-false-pass.md](docs/demo-false-pass.md).

## Use This When

- You use Codex or another coding agent for multi-step repo work.
- You have seen agents drift into broad rewrites, weak claims, or unverified closeouts.
- You want an `AGENTS.md`/skill layer that forces scope, evidence, and stop conditions.
- You care more about honest `BLOCKED` / `HOLD` / `NOT_DELIVERED` verdicts than feel-good progress.

## Do Not Use This When

- You only want quick one-off prompts.
- You want a cross-tool config compiler.
- You want more agents, more roles, or more ceremony for every tiny task.
- You want the agent to optimize for speed over reviewability.

## Quick Install

Back up your current Codex files first:

```sh
mkdir -p ~/.codex/backups
test -f ~/.codex/AGENTS.override.md && cp ~/.codex/AGENTS.override.md ~/.codex/backups/AGENTS.override.$(date +%Y%m%d-%H%M%S).md
test -d ~/.codex/skills && cp -R ~/.codex/skills ~/.codex/backups/skills.$(date +%Y%m%d-%H%M%S)
```

Then install the pack:

```sh
cp core/AGENTS.override.md ~/.codex/AGENTS.override.md
mkdir -p ~/.codex/skills
cp -R core/skills/* ~/.codex/skills/
```

Restart Codex so skill discovery reloads.

For a target project, copy the adapter:

```sh
cp examples/codex-project/AGENTS.md /path/to/your/project/AGENTS.md
```

Full instructions: [QUICKSTART.md](QUICKSTART.md) and [INSTALL.md](INSTALL.md).

## What This Is

This repository packages an active Codex governance override and local governance skills into a shallow, reusable skill pack. The canonical protected materials live under [core/](core/).

The public wrapper skill is [skills/agent-governance/SKILL.md](skills/agent-governance/SKILL.md). It points to the canonical override and included skills instead of duplicating or rewriting them.

## Included Skills

Core controls:

- [project-lifecycle](core/skills/project-lifecycle/SKILL.md)
- [capability-delivery-gate](core/skills/capability-delivery-gate/SKILL.md)
- [repo-preflight](core/skills/repo-preflight/SKILL.md)
- [diff-scope-guardian](core/skills/diff-scope-guardian/SKILL.md)
- [closeout-review](core/skills/closeout-review/SKILL.md)
- [debug-repro-loop](core/skills/debug-repro-loop/SKILL.md)

Supporting lifecycle, handoff, issue-slicing, prompt-eval, and browser-verification skills are listed in [SKILL_INDEX.md](SKILL_INDEX.md).

## Repository Map

| Path | Purpose |
|---|---|
| [QUICKSTART.md](QUICKSTART.md) | Five-minute usage path. |
| [INSTALL.md](INSTALL.md) | Safe manual and ZIP installation. |
| [SKILL_INDEX.md](SKILL_INDEX.md) | Ordered list of included skills and entrypoints. |
| [core/AGENTS.override.md](core/AGENTS.override.md) | Canonical active governance override. |
| [core/skills/](core/skills/) | Canonical copied skill folders. |
| [skills/agent-governance/SKILL.md](skills/agent-governance/SKILL.md) | Public wrapper skill. |
| [examples/codex-project/AGENTS.md](examples/codex-project/AGENTS.md) | Minimal project adapter. |
| [docs/demo-false-pass.md](docs/demo-false-pass.md) | Short demo of the false-PASS failure mode. |
| [docs/launch-kit.md](docs/launch-kit.md) | Distribution copy, channel notes, and post drafts. |
| [docs/launch-tracker.md](docs/launch-tracker.md) | Star/view/clone targets and diagnostic rules. |
| [assets/social-preview.png](assets/social-preview.png) | Social preview artwork for GitHub/X/HN sharing. |
| [assets/social-preview.svg](assets/social-preview.svg) | Editable social preview source. |
| [docs/validation-report.md](docs/validation-report.md) | Hash, package, and secret-scan evidence. |
| [dist/codex-agent-governance-skills-v0.1.0.zip](dist/codex-agent-governance-skills-v0.1.0.zip) | Distribution archive. |

## Safety and Privacy

Before publishing changes to this repository, run the validation and secret/privacy scans described in [docs/validation-report.md](docs/validation-report.md). Do not add `.env`, credentials, tokens, browser exports, private notes, raw client data, or unrelated personal files.

Files under [core/](core/) are protected canonical materials. Do not casually rewrite them. If you need a project-specific adaptation, add an adapter or wrapper outside `core/` and keep the canonical copy intact.

## License

This repository is released under the license in [LICENSE](LICENSE). Third-party notices preserved inside copied skill folders remain governed by their original terms.
