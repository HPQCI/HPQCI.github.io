# HPQCI.github.io

## Local development

Run the local server with:

```sh
bundle install
script/server
```

Stop the local server with:

```sh
script/stop-server
```

For richer local `site.github` metadata and to remove the GitHub API authentication warning, set a GitHub token before starting Jekyll:

```sh
export GITHUB_TOKEN=your_github_token
script/server
```

## Past editions

Use `layout: past` for pages under `history/`.

For pages that belong to a specific archived edition, also set `edition_path` so the archive menu can link back to that edition's home, CFP, program, and registration pages.

Example:

```yaml
---
layout: past
edition_path: /history/2024
---
```
