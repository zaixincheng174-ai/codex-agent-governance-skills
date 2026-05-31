# Quickstart

Use this pack in under 5 minutes.

## 0. What this pack is for

Use it when Codex is doing multi-step repo work and you need scope control, evidence, and honest closeout. The main failure it catches is a false `PASS`: the agent says the work is done, but the terminal artifact or runnable capability still does not exist.

## 1. Inspect the canonical files

Start here:

- [core/AGENTS.override.md](core/AGENTS.override.md)
- [core/skills/](core/skills/)
- [skills/agent-governance/SKILL.md](skills/agent-governance/SKILL.md)

Files under `core/` are canonical protected copies. Treat them as source material, not editable notes.

## 2. Copy into another Codex setup

Manual setup with backups:

```sh
mkdir -p ~/.codex/backups
test -f ~/.codex/AGENTS.override.md && cp ~/.codex/AGENTS.override.md ~/.codex/backups/AGENTS.override.$(date +%Y%m%d-%H%M%S).md
test -d ~/.codex/skills && cp -R ~/.codex/skills ~/.codex/backups/skills.$(date +%Y%m%d-%H%M%S)

cp core/AGENTS.override.md ~/.codex/AGENTS.override.md
mkdir -p ~/.codex/skills
cp -R core/skills/* ~/.codex/skills/
```

Project adapter setup:

```sh
cp examples/codex-project/AGENTS.md /path/to/your/project/AGENTS.md
```

Then edit the adapter only as needed for local project paths and stricter project rules.

## 3. Minimal Codex usage flow

1. Put the override in the active Codex config path.
2. Put the skills in the active Codex skills path.
3. Open a project with its own `AGENTS.md`.
4. Let the override route non-trivial tasks through planning, preflight, diff-scope, validation, and closeout.
5. For large or capability-advancing tasks, check that closeout includes a `CAPABILITY VERDICT` block.

Do not rewrite the protected `core/` files when adapting this pack. Add a wrapper or project adapter instead.
