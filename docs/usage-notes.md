# Usage Notes

Use the files under `core/` as canonical governance inputs. They are copied for installation and review, not rewritten for documentation convenience.

## Practical workflow

1. Start with `QUICKSTART.md`.
2. Read `core/AGENTS.override.md` to understand global routing and stop conditions.
3. Read `SKILL_INDEX.md` to see the included skills in order.
4. Use `skills/agent-governance/SKILL.md` as the public entrypoint.
5. Add a project adapter only when a target project needs local constraints.

## Adapting to a project

Keep local project rules in that project's `AGENTS.md`. Do not copy the full protected content into project adapters. Point to the pack instead.

## Updating canonical materials

When the active local governance source changes, replace the corresponding file or skill folder under `core/`, then rerun hash validation and secret/privacy checks.

## Public safety boundary

Before pushing public changes, confirm the repository contains no `.env`, keys, tokens, browser exports, private notes, unrelated source trees, or raw local runtime state.
