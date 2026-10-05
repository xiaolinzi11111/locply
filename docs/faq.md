# FAQ

### What is Locply for?

Local BI: import a file, clean it, query it, and build charts and dashboards on this device. Tools (CSV / Excel / JSON) are the on-ramp into that loop, not a separate converter product.

### Web or desktop?

| | Web | Desktop |
|--|-----|---------|
| Engine | SQLite WASM in the browser | DuckDB on disk |
| Best for | Try Locply, Tools, smaller files | Larger files, speed, a project that survives closing the browser |
| Limits | Free-plan caps from the [published policy](https://www.locply.com/license/policy.json) | Licensed builds are not bound by those web caps |
| Storage | This site origin (OPFS / IndexedDB) | `%APPDATA%/Locply/workspace.duckdb` (Windows) |

The two stores do not sync automatically.

### Is Locply open source?

No. Locply is proprietary. This public repo hosts docs and feedback only.

### Is my data uploaded?

Imported CSV / Excel / JSON / SQL tables, chart query results, and dashboard layouts are **not** sent to Locply as a cloud dataset.

The website still uses Cloudflare for delivery (IP address, URL, user-agent). The site and desktop app fetch the public license policy. Packaged desktop posts a launch ping (random install id, version, OS) and may download updates. See [https://www.locply.com/legal/privacy/](https://www.locply.com/legal/privacy/).

### What database does Locply use?

- **Web:** SQLite WASM. When supported, Locply prefers OPFS; otherwise it may fall back to less durable in-browser modes. Metadata uses IndexedDB-style local storage.
- **Desktop:** DuckDB in the app process, file on disk.

### Will clearing my browser wipe my web workspace?

Yes, it can. Clearing site data, resetting the profile, or using private browsing can remove the website workspace. The desktop DuckDB file is separate and is not cleared by wiping the locply.com site origin.

### Where do I get the desktop app?

Only from [https://www.locply.com/download/](https://www.locply.com/download/). Unsigned copies from other sites are not supported.

### Where do I report bugs?

Open an Issue in this repository. Include Web vs Desktop, browser or OS, version, and steps to reproduce.

### Can I contribute code?

Not to this product’s private source tree via this repo. Feedback and issue reports are welcome.
