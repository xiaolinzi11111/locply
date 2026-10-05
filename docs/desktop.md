# Desktop app

Locply Desktop is the Windows app with a **DuckDB** workspace on this PC. Same charts and dashboards as the website; queries and imports run locally instead of SQLite WASM in the tab.

Official installer: [https://www.locply.com/download/](https://www.locply.com/download/) (`Locply_Setup.exe`). Only download from www.locply.com.

## Why desktop

- Larger files and faster local SQL than the browser tab
- Workspace survives closing the browser
- Licensed builds are not bound by the web free-plan caps (see the [license policy](https://www.locply.com/license/policy.json))

## Workspace file

| OS | Path |
|----|------|
| Windows | `%APPDATA%\Locply\workspace.duckdb` |

That file is yours to back up. Uninstalling the app or deleting the Locply user-data folder can remove it. It is not a Locply cloud database, and it is not the same store as the website’s browser origin.

## Requirements

- Windows 10/11
- Disk space for your datasets and the DuckDB file

## Network (not your dataset)

Packaged builds may:

- GET `https://www.locply.com/license/policy.json` (quotas and complimentary expiry)
- POST a launch ping (`installId`, app version, OS name) — no table contents
- Check / download updates from Locply `/download/`

Stay offline and those requests fail; analysis of already-imported local data still runs on disk. Full list: [Privacy Policy](https://www.locply.com/legal/privacy/).

## macOS / Linux

There is no official installer on those platforms yet. Use the [web app](https://www.locply.com/) (SQLite in the browser) until a signed desktop build ships.
