# Release Notes Portal

This repository publishes the customer-facing release notes for the platform.

## Layout

- `README.md` - this guide.
- `releases/*.md` - one file per release note.
- `documentation/<slug>/README.md` - documentation landing page for a feature.
- `documentation/<slug>/index.md` - documentation body.

## Release note front matter

Every file under `releases/` starts with a YAML front-matter block delimited by `---` lines:

| key | meaning |
| --- | --- |
| title | Customer-facing feature name. |
| product_area | Owning product area. |
| category | features / improvements / deprecations. |
| permalink | Stable public URL path. |
| summary | One-paragraph description. |
| date | Release date in YYYY-MM-DD. |
| release_status | One of: In development, Awaiting QA, Released, Deferred, Blocked. |
| changelog_url | Link to the public changelog entry. |
| owner_team | Internal owning team. |
| docs_url | Optional link to published documentation. Only present when the documentation is publicly published. |

## Documentation publication state

Each `documentation/<slug>/README.md` records the authoritative publication state:
`Publication state: published` means the docs may be linked externally, while
`Publication state: draft - internal review only` means they must not be linked.

Release notes must only be published for features that have completed release review.
