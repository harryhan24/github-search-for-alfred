# Advance GitHub Search — Alfred Workflow

Search GitHub Code Search from Alfred with a curated picker for languages and file extensions.

## Keywords

- `gh` — full GitHub Code Search
- `gm` — restricted to your own repos via `user:<github_user>`

## Options

After typing `gh` or `gm`, pick one of:

| Option | Behavior |
| --- | --- |
| `Github Search ...` | Search the query as-is |
| `option: extension` | Pick from a curated list of extensions (`ts`, `kt`, `md`, ...) → `path:*.<ext>` |
| `option: filename` | Free-text filename → `path:**/<value>` |
| `option: path` | Free-text path → `path:<value>` |
| `option: language` | Pick from a curated list of languages → `language:<lang>` |
| `option: symbol` | Free-text symbol → `symbol:<value>` |

The language and extension pickers match by both abbreviation and full name (`kt` or `kotlin`, `cpp` or `c++`, `golang` or `go`, ...).

The final search-query input is optional — pressing Enter without typing runs the search with the option only.

## Configure

Right-click the workflow in Alfred Preferences → **Configure Workflow…** to set the GitHub username used by `gm` (default `harryhan24`).

## Releases

Each Git tag matching `v*` triggers a GitHub Actions release that bundles `info.plist` (and any icon PNGs) into `github-search-for-alfred.alfredworkflow` and attaches it to the GitHub Release.

To cut a new release:

```bash
git tag v1.0.0
git push origin v1.0.0
```

Download the `.alfredworkflow` file from the Releases page and double-click to install.
