# Getting started

Locply turns a file into charts and dashboards on this device. Pick the surface that matches the job.

## Web (try without installing)

1. Open [https://www.locply.com/](https://www.locply.com/).
2. Import a CSV, Excel, JSON, or SQL file — or start from [Tools](https://www.locply.com/tools/) and **Create chart**.
3. Clean / model, explore with local SQL (**SQLite WASM**), save charts, assemble a dashboard.

Work lives in **this browser origin**. Clearing site data, private mode, or another device will not find it. Export anything you cannot afford to lose.

Prefer a modern Chromium / Firefox / Safari build over **HTTPS** (or `localhost`) so OPFS persistence can work when available.

## Desktop (larger files, lasting workspace)

1. Download the official Windows installer: [https://www.locply.com/download/](https://www.locply.com/download/).
2. Import into the local **DuckDB** workspace (`%APPDATA%/Locply/workspace.duckdb` on Windows).
3. Same chart and dashboard UI as the web app; queries run on this PC.

The desktop workspace is **not** a copy of the website’s browser storage. Export / import if you need to move a project.

See [Desktop](desktop.md) and [Risks & limitations](../README.md#risks--limitations).

## What Locply does not do

- It does not host your imported tables on Locply servers.
- It does not replace a remote warehouse connection.
- “File contents stay local” is not the same as “the app never uses the network.” Website delivery, license policy, desktop launch ping, and updates are described in the [Privacy Policy](https://www.locply.com/legal/privacy/).
