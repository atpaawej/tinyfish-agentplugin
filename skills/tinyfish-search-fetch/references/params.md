# TinyFish Search + Fetch params

## search

Finds fresh URLs with titles, snippets.

- `purpose`: short statement of why you are searching. Gives intent signal.
- `location`: country code, e.g. `US`.
- `language`: language code, e.g. `en`.
- `include_domains` / `exclude_domains`: comma-separated allow/deny lists.
- `domain_type`: `web` | `news` | `research_paper`.
- `recency_minutes`, `after_date`, `before_date`: freshness window. Not used with `research_paper`.
- `pub_year_min` / `pub_year_max`: year scope for `research_paper` only.
- `page`: 0-indexed pagination, `0`-`10`.

Free at any wallet balance. Failed URLs do not count against quota.

## fetch_content

Reads pages, renders JS-heavy pages, returns clean markdown.

- `purpose`: short statement of why you are fetching.
- `format`: `markdown` (default) | `html` | `json`.
- `links` / `image_links`: extract outbound / image URLs.
- `ttl`: cache freshness tolerance in seconds.
- `per_url_timeout_ms`: per-URL wall-clock budget.
- `include_selectors` / `exclude_selectors`: 1-20 CSS selectors each to scope extraction.
- `if_none_match` / `if_modified_since`: conditional request, single URL only.
- `include_etag_and_last_modified`: return validators back.

Accepts up to 10 URLs per request. Free at any wallet balance.

## Usage lookups

- `get_search_usage`: list past search usage, filter by date range and status.
- `list_fetch_usage`: list past fetch requests, metadata only.
