# Launch Tracker

Start tracking from the first public launch post, not from repository creation.

## Baseline

| Metric | Baseline |
|---|---:|
| Stars | 1 |
| Unique views | 0 |
| Clones | 0 |
| Forks | 0 |
| GitHub description | missing |
| GitHub topics | missing |

## Targets

| Window | Minimum | Good | Strong |
|---|---:|---:|---:|
| 48h soft launch | 5 stars / 50 views / 3 clones | 10 stars / 100 views / 8 clones | 20 stars / 200 views / 15 clones |
| 7d public launch | 15 stars | 35 stars | 75 stars |
| 30d | 35 stars | 100 stars | 250 stars |

## Diagnostic Rules

- Low views: distribution failed.
- High views but low stars: README/demo positioning failed.
- Stars but no clones/comments: curiosity, not adoption.
- Reddit removal: do not repost; switch to allowed threads or ask moderators.
- HN "too much process" feedback: clarify that the pack is for large/repo-risk tasks, not tiny prompts.

## Post Log

| Channel | URL | Posted at | Views | Stars after | Clones after | Notes |
|---|---|---:|---:|---:|---:|---|
| X |  |  |  |  |  |  |
| Reddit |  |  |  |  |  |  |
| Hacker News |  |  |  |  |  |  |

## Weekly Readback Commands

```sh
gh api repos/zaixincheng174-ai/codex-agent-governance-skills --jq '{stars:.stargazers_count,forks:.forks_count,watchers:.watchers_count,updated_at}'
gh api repos/zaixincheng174-ai/codex-agent-governance-skills/traffic/views --jq '{views:.count,unique_views:.uniques}'
gh api repos/zaixincheng174-ai/codex-agent-governance-skills/traffic/clones --jq '{clones:.count,unique_cloners:.uniques}'
```
