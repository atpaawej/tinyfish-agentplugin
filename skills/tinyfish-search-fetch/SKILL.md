---
name: tinyfish-search-fetch
description: Use when searching the web for URLs or fetching page content into clean markdown via TinyFish.
---

# TinyFish Search + Fetch

Use live web context when the answer needs freshness.

## Steps

1. Search to discover URLs: call `search` with a `purpose` stating why you are searching.
2. Fetch to read: call `fetch_content` with up to 10 URLs, `format: markdown`.
3. Answer from fetched content.

Completion: every current factual claim cites a fetched URL.

## Reference

- `search`: discovery step. See `references/params.md` for filters.
- `fetch_content`: read step. See `references/params.md` for output controls.
