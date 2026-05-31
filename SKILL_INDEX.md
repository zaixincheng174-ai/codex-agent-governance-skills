# Skill Index

Recommended order starts with the routing and lifecycle controls, then supporting audit and handoff utilities.

| Order | Skill | Source path | Purpose | Status |
|---:|---|---|---|---|
| 1 | project-lifecycle | `core/skills/project-lifecycle/SKILL.md` | Coordinates project work through audit, design, build, review, and verify phases. | canonical |
| 2 | capability-delivery-gate | `core/skills/capability-delivery-gate/SKILL.md` | Checks whether project work delivered a real terminal capability instead of only process artifacts. | canonical |
| 3 | repo-preflight | `core/skills/repo-preflight/SKILL.md` | Performs read-only repository grounding before non-trivial edits. | canonical |
| 4 | diff-scope-guardian | `core/skills/diff-scope-guardian/SKILL.md` | Audits the actual diff for scope creep and unrelated changes after implementation. | canonical |
| 5 | closeout-review | `core/skills/closeout-review/SKILL.md` | Reviews completion evidence, claim boundaries, and residual risk before delivery. | canonical |
| 6 | debug-repro-loop | `core/skills/debug-repro-loop/SKILL.md` | Guides reproducible debugging and bounded repair loops. | canonical |
| 7 | lifecycle-auditor | `core/skills/lifecycle-auditor/SKILL.md` | Lifecycle role for startup audit and goal-contract formation. | canonical |
| 8 | lifecycle-architect | `core/skills/lifecycle-architect/SKILL.md` | Lifecycle role for design and architecture decisions. | canonical |
| 9 | lifecycle-builder | `core/skills/lifecycle-builder/SKILL.md` | Lifecycle role for implementation after design gates pass. | canonical |
| 10 | lifecycle-reviewer | `core/skills/lifecycle-reviewer/SKILL.md` | Lifecycle role for independent review after build. | canonical |
| 11 | lifecycle-verifier | `core/skills/lifecycle-verifier/SKILL.md` | Lifecycle role for final verification evidence. | canonical |
| 12 | goal-clarifier | `core/skills/goal-clarifier/SKILL.md` | Resolves blocking ambiguity around goals, constraints, or success criteria. | canonical |
| 13 | persistent-planning | `core/skills/persistent-planning/SKILL.md` | Maintains durable working notes when a task needs cross-phase continuity. | canonical |
| 14 | handoff-brief | `core/skills/handoff-brief/SKILL.md` | Creates concise handoff briefs with evidence and verdict boundaries. | canonical |
| 15 | issue-slice-drafter | `core/skills/issue-slice-drafter/SKILL.md` | Drafts implementation-ready issue slices from plans, specs, or findings. | canonical |
| 16 | prompt-eval-harness | `core/skills/prompt-eval-harness/SKILL.md` | Builds constrained prompt evaluation harnesses with rubric and evidence. | canonical |
| 17 | playwright | `core/skills/playwright/SKILL.md` | Automates browser verification through Playwright CLI workflows. | canonical |
| 18 | agent-governance | `skills/agent-governance/SKILL.md` | Public wrapper entrypoint that points to the canonical override and skills. | wrapper |

If a purpose is unclear in future additions, use `Purpose not safely inferable` instead of inventing one.
