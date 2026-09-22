# github-pm

Bundles:
- **`ccpm` skill** — spec-driven delivery: PRD → Epic → GitHub Issues → parallel agents → shipped code, tracked entirely through `gh`-CLI-backed scripts. (Source: [automazeio/ccpm](https://github.com/automazeio/ccpm), MIT.)
- **`github` MCP server** — GitHub's official MCP server (remote, Streamable HTTP), for direct issue/PR/repo operations from Claude.

## Setup (one-time per person)

The GitHub MCP server needs a Personal Access Token in your environment — it is **never** stored in this repo.

1. Create a token with `repo` scope: https://github.com/settings/personal-access-tokens/new
2. Export it before starting Claude Code:
   ```bash
   export GITHUB_PAT=ghp_your_token_here
   ```
   (add that line to your shell profile so it persists)
3. Restart Claude Code / run `/reload-plugins`.
4. Verify: `claude mcp list` should show `github` as connected.
