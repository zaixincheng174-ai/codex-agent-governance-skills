# Packaging

The ZIP artifact is built from the repository root after validation-ready files exist.

Expected artifact:

```text
dist/codex-agent-governance-skills-v0.1.0.zip
```

The ZIP includes:

- `README.md`
- `QUICKSTART.md`
- `INSTALL.md`
- `SKILL_INDEX.md`
- `manifest.json`
- `skill-pack.json`
- `core/`
- `skills/`
- `examples/`
- `docs/`
- `LICENSE`
- `CHANGELOG.md`

The ZIP must not include:

- `.git/`
- `.env`
- `node_modules/`
- `__pycache__/`
- `.DS_Store`
- credentials
- unrelated files
- temporary scratch files
- raw secret scan dumps

No new dependencies are required. Use `zip` when available, otherwise use Python `zipfile`.
