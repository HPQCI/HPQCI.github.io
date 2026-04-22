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

For pages that belong to a specific archived edition, set `edition: "<year>"` in the front matter. The layout will look up metadata from `_data/editions.yml` automatically.

Example front matter:

```yaml
---
layout: past
edition: "2024"
---
```

### Adding a new past edition

Add an entry to `_data/editions.yml`:

```yaml
"2024":
  path: /history/2024          # base URL for the edition's pages
  where: "Venue, City, Country"
  when: "Month DD, YYYY"
  title: "HPQCIXX"             # overrides the site title in the page header
  description: "..."           # overrides the site description tagline
```

All fields except `path` are optional. `title` and `description` override the banner text shown on past-edition pages; if omitted, the current site values are used as fallback.
