---
paths:
  - "api-reference/**"
---

# API reference conventions

Loads when editing pages under `api-reference/`. The API reference tab is
generated from the live OpenAPI document at
`https://api.yieldpoint.io/docs/json`. That document is the source of truth
for routes, parameters, and schemas.

## Source of truth

- The spec lives in `~/dev/yieldpoint/api.yieldpoint.io` and is served at
  `https://api.yieldpoint.io/docs/json`. Do not vendor a copy into this repo
  and do not hand-write request or response schemas.
- Wrong parameters, descriptions, enums, or summaries get fixed upstream in
  the API repo, not patched here.
- A missing `servers` field in the spec breaks the playground and there is
  no docs-side override. Fix upstream first.

## Page types

- **Endpoint pages** use `openapi:` frontmatter pointing at the remote URL:
  `openapi: "https://api.yieldpoint.io/docs/json GET /v1/path/{param}"`.
  The method and path must match the spec exactly. Mintlify renders the
  generated parameters and schema, then the page body. Use the body for
  semantics the spec does not state (defaults, invariants, error behavior,
  examples). Keep `title` short; the spec summaries are full sentences.
- **Concept pages** are ordinary MDX (`overview.mdx`, `leaderboard/seasons.mdx`,
  `address/portfolio.mdx`) for rules shared across several routes.

## Navigation

The API reference tab in `docs.json` sets `openapi` at the tab level and
lists every endpoint explicitly, either as an MDX page path or as a
`"GET /path"` string. Listing is explicit because an auto-generated group
would duplicate any endpoint that also has an MDX page.

When the API adds a route, add a nav entry for it. When a route is removed,
drop its entry and delete its MDX page if one exists. `mint validate` fails
on entries that no longer match the spec.

## Verifying claims

Before stating response behavior the spec does not spell out, `curl` the
live API and check. Error bodies, null cases, and ordering are cheap to
confirm and easy to get wrong.
