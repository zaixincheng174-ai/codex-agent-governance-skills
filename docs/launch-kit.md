# Launch Kit

This file is a working launch pack for `codex-agent-governance-skills`.

Do not submit public posts blindly. Use the copy below as drafts, check the current community rules, and submit only from an account that can respond to feedback.

## Positioning

Primary hook:

```text
I hit 12.83B cumulative Codex tokens and the biggest failure mode was not bad code.
It was false PASS claims.
```

Short repo pitch:

```text
A Codex governance skill pack that stops scope drift, weak closeouts, and false PASS claims by forcing repo preflight, diff-scope audit, evidence closeout, and capability-delivery verdicts.
```

One-line differentiator:

```text
This is not a cross-tool config compiler. It is a Codex-native execution governance layer for long, risky repo work.
```

## Style Notes from High-Engagement AI Tool Posts

Patterns to copy:

- Lead with a concrete pain or provocative claim.
- Use one strong number early.
- Show the exact thing users get.
- Use short sections and bullets.
- Include one command or one concrete workflow.
- Avoid abstract essays about agent governance.

Patterns to avoid:

- Long manifesto openings.
- Asking for stars.
- Dropping a GitHub link with no use case.
- Claiming this replaces Claude/Cursor/CRAG/OpenPlan.

## X Main Post

```text
I hit 12.83B cumulative Codex tokens.

The biggest failure mode was not bad code.

It was false PASS claims:
- tests passed
- diff looked clean
- closeout sounded confident
- but the actual capability did not exist

So I packaged my Codex governance stack:
github.com/zaixincheng174-ai/codex-agent-governance-skills
```

Follow-up:

```text
The core rule:

"Implementation looks fine" is not the same as "capability delivered."

The pack forces a CAPABILITY VERDICT:
- CAPABILITY_DELIVERED
- IMPLEMENTATION_PASS_CAPABILITY_NOT_DELIVERED
- BLOCKED
- STOP_IDLE
- STOP_FORMALISM

No naked PASS.
```

Follow-up:

```text
It includes:

1. task sizing
2. project lifecycle
3. repo preflight before edits
4. diff-scope audit after edits
5. evidence closeout
6. capability-delivery gate

Built for long Codex repo work, not tiny one-off prompts.
```

Follow-up:

```text
The part I care about most:

If there is no terminal artifact, the agent cannot call the task done.

Tests can pass.
Lint can pass.
The final verdict still stays:

IMPLEMENTATION_PASS_CAPABILITY_NOT_DELIVERED
```

Follow-up:

```text
Repo is MIT, plain files, no service:

github.com/zaixincheng174-ai/codex-agent-governance-skills

I am looking for feedback from people using Codex / AGENTS.md / coding agents for real repo work.
```

## X Reply Bank

Use these only on relevant threads where the author is already discussing Codex, AGENTS.md, skills, agent reliability, or long-running coding agents.

```text
This matches a failure mode I kept seeing in long Codex sessions: the agent would pass process checks but still not produce the terminal artifact. I packaged my governance stack around that distinction: implementation pass != capability delivered.
```

```text
The useful boundary for me has been: small prompts stay lightweight, but repo-risk tasks need preflight, diff-scope audit, and a final capability verdict. Otherwise "PASS" gets too cheap.
```

```text
I think agent config is becoming less about prompts and more about operational control: what can the agent claim, when must it stop, and what evidence is required before closeout.
```

## Reddit Draft

Title:

```text
I packaged my Codex governance skill pack to stop false PASS claims. Looking for feedback from agent power users.
```

Body:

```text
I use Codex heavily: 12.83B cumulative tokens, 1B peak token count, 5h25m longest task, 39-day active streak.

The repeated failure mode was not just bad code. It was false PASS claims:

- tests passed
- diff looked clean
- closeout sounded confident
- but the actual terminal artifact did not exist

So I packaged my governance setup as a public skill pack:
https://github.com/zaixincheng174-ai/codex-agent-governance-skills

The key piece is a capability-delivery gate. It forces the agent to separate:

- CAPABILITY_DELIVERED
- IMPLEMENTATION_PASS_CAPABILITY_NOT_DELIVERED
- BLOCKED
- STOP_IDLE
- STOP_FORMALISM

It also includes repo preflight, diff-scope audit, debug/repro loop, lifecycle gates, and closeout review.

This is for long/risky repo work, not tiny prompts.

I am looking for feedback from people who actually use Codex, AGENTS.md, Claude Code skills, Cursor rules, or similar agent governance setups.
```

## Hacker News Draft

Title:

```text
Show HN: Codex governance skills that stop scope drift and false PASS claims
```

Text:

```text
I packaged the Codex governance setup I use for long repo work.

The main failure mode it targets is a false PASS: tests pass, the diff looks clean, the closeout sounds confident, but the actual terminal artifact does not exist.

The pack is plain files: AGENTS.override.md plus skills for project lifecycle, repo preflight, diff-scope audit, debug/repro, closeout review, and a capability-delivery gate.

The capability gate forces verdicts like CAPABILITY_DELIVERED or IMPLEMENTATION_PASS_CAPABILITY_NOT_DELIVERED instead of a naked PASS.

Repo:
https://github.com/zaixincheng174-ai/codex-agent-governance-skills
```

## Channel Rules Before Posting

- X: post from the user's logged-in account; do not automate spam replies.
- Reddit: read current subreddit rules first; use self-promotion threads where required.
- `r/LLMDevs`: current rule-search result says free open-source project sharing is allowed without prior moderator approval; still keep the post feedback-oriented.
- `r/ChatGPTCoding`: current rule-search result surfaces recurring self-promotion threads; use that thread instead of a standalone promotional post.
- HN: submit only after the demo file exists and repo first screen is fixed; do not ask anyone to upvote.

## Community Targeting

Primary:

- X search: `Codex`, `AGENTS.md`, `agent skills`, `AI coding agents`, `Claude Code skills`, `Cursor rules`.
- Reddit: `r/LLMDevs`, `r/ChatGPTCoding`, Codex/OpenAI communities if rules allow.
- Hacker News: Show HN after repo readiness checks pass.

Secondary:

- GitHub discussions/issues only where maintainers explicitly ask for related tools or examples.
- Do not open issues on other repos asking for stars.
