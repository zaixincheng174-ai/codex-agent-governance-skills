# Discovery Report

## Searched paths

- current workspace: `~/ai-alpha-os`
- likely Codex root: `~/.codex/`
- likely active override: `~/.codex/AGENTS.override.md`
- likely active skills: `~/.codex/skills/`
- project-local skills: `~/ai-alpha-os/.agents/skills/`
- home-level negative-space searches for `AGENTS.override.md`, `skills`, and `SKILL.md`

## Included candidates

| Candidate | Type | Size / count | Modified | SHA-256 / summary | Reason |
|---|---|---:|---|---|---|
| `~/.codex/AGENTS.override.md` | file | 14940 bytes | 2026-05-27T00:01:47-0400 | `e28130c628d4076a668e812bd5b1b4894d7ee2bc6ec2e55c2c7c6af4a088ca50` | Active global override; `~/.codex/AGENTS.md` points to it as authoritative. |
| `~/.codex/skills/capability-delivery-gate` | folder | 1 file | 2026-05-25T23:57:01-0400 | `1a59b71b6f8db889da1838c91bd928900bffdef991aa41fb2d81064b72f40c90` | Direct non-symlink local governance skill. |
| `~/.codex/skills/closeout-review` | folder | 1 file | 2026-05-23T13:31:59-0400 | `4fc622d1383df14a10d481113ad2ad65a886282b9e1a197b2afc3b7641dcc799` | Direct non-symlink local governance skill. |
| `~/.codex/skills/debug-repro-loop` | folder | 1 file | 2026-05-23T13:31:59-0400 | `eb300f2b7d950971b832d898f499f6e0b465096ef93b7ba68a9e8c5eff23d8bc` | Direct non-symlink local governance skill. |
| `~/.codex/skills/diff-scope-guardian` | folder | 1 file | 2026-05-23T13:24:45-0400 | `3e8a37d4c2a0a7eabd0a88c7ea36f3147a62522cceddc455ed31c621b95948fa` | Direct non-symlink local governance skill. |
| `~/.codex/skills/goal-clarifier` | folder | 1 file | 2026-05-24T21:34:21-0400 | `844075bf71c7ad01219247a57b14009036bd9a3c2b3384647e073322611d4b93` | Direct non-symlink local governance skill. |
| `~/.codex/skills/handoff-brief` | folder | 1 file | 2026-05-24T21:34:21-0400 | `9de0276511c8c9b57ec30580a59124552873ea652b50e040f389edceca04d114` | Direct non-symlink local governance skill. |
| `~/.codex/skills/issue-slice-drafter` | folder | 1 file | 2026-05-24T21:34:21-0400 | `2531e9910510c043e0eeb745f4d9a9a6472284c7644b3348f4ff897bb2987b6a` | Direct non-symlink local governance skill. |
| `~/.codex/skills/lifecycle-architect` | folder | 1 file | 2026-05-23T13:07:24-0400 | `18bd5e01a33a757d275b7931c598a6257c2c8bf25555fded5159d7775e35ed30` | Direct non-symlink local governance skill. |
| `~/.codex/skills/lifecycle-auditor` | folder | 1 file | 2026-05-23T13:07:24-0400 | `0847cfd4261915aff2b381b7a93183af3fd9a726ebd49064435622addf1ddcae` | Direct non-symlink local governance skill. |
| `~/.codex/skills/lifecycle-builder` | folder | 1 file | 2026-05-23T13:07:24-0400 | `4cbf9e468be0bb8d8980050f7f15cc26124d53c3e95381617588d45c8c57a1dc` | Direct non-symlink local governance skill. |
| `~/.codex/skills/lifecycle-reviewer` | folder | 1 file | 2026-05-23T13:07:24-0400 | `4a525ca3b6088e4941e2899539c666b3b10b77f1d2e32216708c4b29e671edd0` | Direct non-symlink local governance skill. |
| `~/.codex/skills/lifecycle-verifier` | folder | 1 file | 2026-05-23T13:07:24-0400 | `3e69a61a51216b3b7a8e723ab1c4dacc7c13e363770b0a53fe8af80104746dc1` | Direct non-symlink local governance skill. |
| `~/.codex/skills/persistent-planning` | folder | 1 file | 2026-05-24T21:34:21-0400 | `b70943d1e361e676fb73f4b665ee28e8bb6469b2af13e67acd1a6056abf42b7f` | Direct non-symlink local governance skill. |
| `~/.codex/skills/playwright` | folder | 8 files | 2026-05-28T13:26:16-0400 | file manifest validated | Direct non-symlink local Codex skill with bundled references/assets. |
| `~/.codex/skills/project-lifecycle` | folder | 1 file | 2026-05-23T13:25:43-0400 | `a5b1187a980709b2db6f3bfd8d078e463a3c3b7446eddefbec8259d450b3d93e` | Direct non-symlink local governance skill. |
| `~/.codex/skills/prompt-eval-harness` | folder | 1 file | 2026-05-24T21:34:21-0400 | `0604d5c453f9112ff19341604af5c3c153efdf23092385ede2f5a47d0388d428` | Direct non-symlink local governance-adjacent skill. |
| `~/.codex/skills/repo-preflight` | folder | 1 file | 2026-05-23T13:24:45-0400 | `9f592a953e755db6d84268007c2a7da656299a0f050dfe8440188b6db77b0704` | Direct non-symlink local governance skill. |

## Excluded candidates

| Candidate group | Reason |
|---|---|
| `~/.codex/skills/.system` | System skills, not self-created governance source for this pack. |
| `~/.codex/skills/_backup*` and `~/.codex/skills.backup.*` | Backup material, not active canonical source. |
| Symlinks under `~/.codex/skills` pointing into `.orchestra` | External or third-party skill inventory, not copied as self-created local governance source. |
| `~/.codex/plugins/**`, `~/.codex/.tmp/**`, bundled marketplace paths | Plugin caches and staging material. |
| `~/.codex/memories/skills` | Memory-related materials, not active Codex skill source. |
| `~/ai-alpha-os/.agents/skills` | Project-local finance/backtesting/data skills, not part of this public governance pack. |
| `~/ai-alpha-os/.env`, runtime data, docs, tests, external sources | Unrelated project state and possible private/runtime content. |
| dependency `site-packages`, `node_modules`, browser/app caches | Third-party dependency internals. |

## Ambiguous candidates

None requiring a stop. The active override was uniquely identified as `~/.codex/AGENTS.override.md`; the included skills were narrowed to direct, non-symlink local folders under `~/.codex/skills`.

## Negative-space result

The package must not include the current `ai-alpha-os` repository contents, local environment files, runtime databases, Codex auth/history/log state, plugin caches, backups, symlinked external skill trees, or project-local finance skills. Public push remains gated by secret/privacy scan and validation.

## Source hash note

The full source and copied manifests were compared file-by-file. See `docs/validation-report.md` for the post-copy validation result.
