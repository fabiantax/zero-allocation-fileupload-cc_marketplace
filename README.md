# claude-plugins

Team Claude Code plugin marketplace.

## Install

```
/plugin marketplace add fabiantax/team-github-pm
/plugin install github-pm@team-github-pm
```

Then see [`plugins/github-pm/README.md`](plugins/github-pm/README.md) for the one-time `GITHUB_PAT` setup the bundled MCP server needs.

## Secret scanning

This repo ships a shared pre-commit hook (gitleaks) that blocks commits containing secrets. One-time setup after cloning:

```
brew install gitleaks
git config core.hooksPath hooks
```

Every commit is scanned before it's created. This is local-only — it does not run in CI, so a contributor who skips setup (or commits with `--no-verify`) is not blocked server-side.
