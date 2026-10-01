# Desktop app

Locply Desktop is an Electron shell with a local DuckDB workspace.

## Workspace file

| OS | Path |
|----|------|
| Windows | `%APPDATA%/Locply/workspace.duckdb` |
| macOS | `~/Library/Application Support/Locply/workspace.duckdb` |

## Requirements

- Windows 10/11, recent macOS, or a modern Linux desktop
- Enough disk space for your datasets and the DuckDB file

## Installers

Built artifacts are typically:

- Windows: NSIS `.exe`
- macOS: `.dmg`
- Linux: `.AppImage`

Publish each version via this repo’s **Releases** page and/or your CDN (e.g. Cloudflare R2). Keep the README download links in sync with the latest tag.
