# tinyfish-web

Live web search and page fetch via TinyFish MCP. Free at any wallet balance.

## Install (recommended)

One command via the Agent Plugins installer. It auto-detects your agents and installs to all of them:

```bash
npx plugins add atpaawej/tinyfish-agentplugin
```

Pick agents on the go:

```bash
npx plugins targets
# shows Claude Code (claude binary on PATH), Cursor (cursor + claude binaries)

npx plugins add atpaawej/tinyfish-agentplugin -t claude-code
npx plugins add atpaawej/tinyfish-agentplugin -t cursor
```

Dry run first, skip prompts, set scope:

```bash
npx plugins discover <you>/tinyfish-agentplugin
npx plugins add atpaawej/tinyfish-agentplugin -y
npx plugins add atpaawej/tinyfish-agentplugin -s user
npx plugins add atpaawej/tinyfish-agentplugin -s project
npx plugins add atpaawej/tinyfish-agentplugin -s local
```

Local path works too:

```bash
npx plugins add ./tinyfish-agentplugin
```

Then complete TinyFish OAuth on first use in the agent.

## Install (manual fallback)

OpenCode:

```bash
opencode mcp add tinyfish --url https://agent.tinyfish.ai/mcp
opencode mcp auth tinyfish
```

Claude Code:

```bash
claude mcp add --transport http tinyfish https://agent.tinyfish.ai/mcp
```

Cursor / others: add a Streamable HTTP server with URL `https://agent.tinyfish.ai/mcp`, then complete OAuth.

## Use

The `tinyfish-search-fetch` skill teaches the agent:

1. `search` to discover fresh URLs
2. `fetch_content` to read clean markdown (up to 10 URLs)
3. Answer from fetched content

Free quotas: Search 60 req/min, Fetch 300 url/min. No API key needed, OAuth only.
