# Validation Report

Validation date: 2026-05-30

## Summary

All required packaging checks passed. Broad sensitive-term matches were reviewed as policy text or non-secret variable references; no high-confidence secret values were found.

## Commands and results

| Check | Command | Result |
|---|---|---|
| Protected override hash | `shasum -a 256 ~/.codex/AGENTS.override.md core/AGENTS.override.md` | PASS |
| Protected skill manifest diff | `diff -u <source manifest> <copied manifest>` | PASS: no diff |
| README canonical links | `grep -q 'core/AGENTS.override.md' README.md && grep -q 'core/skills/' README.md && grep -q 'skills/agent-governance/SKILL.md' README.md` | PASS |
| QUICKSTART canonical links | `grep -q 'core/AGENTS.override.md' QUICKSTART.md && grep -q 'core/skills/' QUICKSTART.md` | PASS |
| Required docs and wrapper | `test -f INSTALL.md && test -f SKILL_INDEX.md && test -f skills/agent-governance/SKILL.md` | PASS |
| Root metadata | `test -f manifest.json && test -f skill-pack.json` | PASS |
| Metadata order fields | `grep -q 'display_order' manifest.json && grep -q 'reading_order' skill-pack.json` | PASS |
| JSON syntax | `python3 -m json.tool manifest.json && python3 -m json.tool skill-pack.json && python3 -m json.tool skills/agent-governance/manifest.json` | PASS |
| Value-shaped secret scan | `rg -l -i '(ghp_[A-Za-z0-9_]{20,}|github_pat_[A-Za-z0-9_]{20,}|sk-[A-Za-z0-9]{20,}|AKIA[0-9A-Z]{16}|-----BEGIN (RSA|OPENSSH|PRIVATE) KEY-----|client_secret[[:space:]]*[:=][[:space:]]*[A-Za-z0-9._-]{10,}|refresh_token[[:space:]]*[:=][[:space:]]*[A-Za-z0-9._-]{10,})' . --glob '!.git/**' --glob '!dist/**'` | PASS: no matches |
| Broad sensitive-term scan | `rg -l -i '(OPENAI_API_KEY|ANTHROPIC_API_KEY|GITHUB_TOKEN|AWS_ACCESS_KEY|AWS_SECRET|PRIVATE KEY|BEGIN RSA|BEGIN OPENSSH|id_rsa|password|passwd|secret|token|bearer|credential|cookie|session|client_secret|refresh_token)' . --glob '!.git/**' --glob '!dist/**'` | REVIEWED: matches are governance policy text, validation text, and non-secret session variable references |
| Assignment-shaped sensitive-term scan | `rg -n -i -o '(password|passwd|secret|token|bearer|credential|cookie|session|client_secret|refresh_token)[[:space:]]*[:=]' . --glob '!.git/**' --glob '!dist/**'` | REVIEWED: only `session=` / `SESSION=` references in Playwright helper/docs and governance text |
| Local path/privacy scan | `rg -n '<local username or local absolute home prefix>' . --glob '!.git/**' --glob '!dist/**'` | PASS: no package matches for local absolute paths or local username |
| Shallow visibility | `find . -maxdepth 2 -type f | sort` | PASS |
| Core file list | `find core -type f | sort` | PASS: 26 canonical copied files |
| ZIP build | `zip -qr /tmp/codex-agent-governance-skills-v0.1.0.zip ... && mv ... dist/codex-agent-governance-skills-v0.1.0.zip` | PASS |
| ZIP prohibited-file inspection | `unzip -Z1 dist/codex-agent-governance-skills-v0.1.0.zip | rg '(^|/)(\\.git/|\\.env($|\\.)|node_modules/|__pycache__/|\\.DS_Store$|credentials|credential|secret scan raw)'` | PASS: no prohibited entries |
| Git diff hygiene | `git diff --check --cached` | PASS |
| Git status scope | `git status --short` | PASS: only intended repository files staged |

## Source copy hashes

The protected override and all copied skill files matched source hashes exactly.

| Path | SHA-256 |
|---|---|
| `core/AGENTS.override.md` | `e28130c628d4076a668e812bd5b1b4894d7ee2bc6ec2e55c2c7c6af4a088ca50` |
| `core/skills/capability-delivery-gate/SKILL.md` | `1a59b71b6f8db889da1838c91bd928900bffdef991aa41fb2d81064b72f40c90` |
| `core/skills/closeout-review/SKILL.md` | `4fc622d1383df14a10d481113ad2ad65a886282b9e1a197b2afc3b7641dcc799` |
| `core/skills/debug-repro-loop/SKILL.md` | `eb300f2b7d950971b832d898f499f6e0b465096ef93b7ba68a9e8c5eff23d8bc` |
| `core/skills/diff-scope-guardian/SKILL.md` | `3e8a37d4c2a0a7eabd0a88c7ea36f3147a62522cceddc455ed31c621b95948fa` |
| `core/skills/goal-clarifier/SKILL.md` | `844075bf71c7ad01219247a57b14009036bd9a3c2b3384647e073322611d4b93` |
| `core/skills/handoff-brief/SKILL.md` | `9de0276511c8c9b57ec30580a59124552873ea652b50e040f389edceca04d114` |
| `core/skills/issue-slice-drafter/SKILL.md` | `2531e9910510c043e0eeb745f4d9a9a6472284c7644b3348f4ff897bb2987b6a` |
| `core/skills/lifecycle-architect/SKILL.md` | `18bd5e01a33a757d275b7931c598a6257c2c8bf25555fded5159d7775e35ed30` |
| `core/skills/lifecycle-auditor/SKILL.md` | `0847cfd4261915aff2b381b7a93183af3fd9a726ebd49064435622addf1ddcae` |
| `core/skills/lifecycle-builder/SKILL.md` | `4cbf9e468be0bb8d8980050f7f15cc26124d53c3e95381617588d45c8c57a1dc` |
| `core/skills/lifecycle-reviewer/SKILL.md` | `4a525ca3b6088e4941e2899539c666b3b10b77f1d2e32216708c4b29e671edd0` |
| `core/skills/lifecycle-verifier/SKILL.md` | `3e69a61a51216b3b7a8e723ab1c4dacc7c13e363770b0a53fe8af80104746dc1` |
| `core/skills/persistent-planning/SKILL.md` | `b70943d1e361e676fb73f4b665ee28e8bb6469b2af13e67acd1a6056abf42b7f` |
| `core/skills/playwright/` | `8 files copied; full manifest diff PASS` |
| `core/skills/project-lifecycle/SKILL.md` | `a5b1187a980709b2db6f3bfd8d078e463a3c3b7446eddefbec8259d450b3d93e` |
| `core/skills/prompt-eval-harness/SKILL.md` | `0604d5c453f9112ff19341604af5c3c153efdf23092385ede2f5a47d0388d428` |
| `core/skills/repo-preflight/SKILL.md` | `9f592a953e755db6d84268007c2a7da656299a0f050dfe8440188b6db77b0704` |

## Broad sensitive-term review

The broad scan intentionally catches governance text such as "secret", "token", and "credential". The value-shaped scan returned no matches. The assignment-shaped matches were `session=` / `SESSION=` references in the copied Playwright skill and governance text, not secret values.

## Final validation verdict

- Protected copy hash check: PASS
- Skill copy hash check: PASS
- Secret scan: PASS
- ZIP package: PASS
- Git diff check: PASS
- Git status scope: PASS
- No protected source content was modified: PASS

## Git whitespace note

The copied Playwright Apache license file uses source-preserved line endings that Git reports as whitespace errors by default. The repository adds `.gitattributes` with `core/skills/playwright/LICENSE.txt -whitespace` so `git diff --check --cached` can pass without rewriting the protected copied file.
