# Locply

**Local BI from files on your machine** — import CSV / Excel / JSON / SQL, clean data, query locally, and build **charts and dashboards**.

Locply is not a hosted warehouse and not a one-shot file converter. The same workspace takes you from a spreadsheet to Explore to a dashboard.

> This is the **public docs and feedback** repository.  
> **Source is not published** (proprietary). Application development lives in a private repo.

---

## Try it

| Channel | Link |
|--------|------|
| Web (SQLite in the browser) | [https://www.locply.com/](https://www.locply.com/) |
| Desktop (DuckDB on this PC) | [Download for Windows](https://www.locply.com/download/) |
| Tools (clean / convert, then chart) | [https://www.locply.com/tools/](https://www.locply.com/tools/) |
| Legal / privacy | [https://www.locply.com/legal/](https://www.locply.com/legal/) |

---

## Why Locply

| You need | Locply |
|----------|--------|
| Charts and dashboards from a file | Import → clean → local SQL → chart → dashboard |
| Try without installing | **Web:** SQLite WASM in this browser origin |
| Larger files and a lasting project | **Desktop:** DuckDB in `%APPDATA%/Locply/workspace.duckdb` |
| Not sending tables to a vendor cloud | Imported datasets are **not** stored on Locply servers |

Website visits still go through Cloudflare. Packaged desktop may fetch a public [license policy](https://www.locply.com/license/policy.json), send a launch ping, and check updates. That is not a dataset upload. Details: [Privacy Policy](https://www.locply.com/legal/privacy/).

---

## What you get

- **Import** CSV, Excel, JSON, SQL
- **Clean & model** in the same product as Data Input and Tools
- **Explore** metrics, dimensions, filters, and SQL on the local engine
- **Dashboards** — layout, cross-filters, reusable charts
- **Two engines, one UI** — browser SQLite for a quick start; desktop DuckDB for scale

---

## Chart highlights

Locply is interactive local visualization, not server-side BI:

| Area | What you can do |
|------|-----------------|
| Time series | Line / area / bar time series, mixed timeseries, calendar, horizon, time pivot |
| Comparison | Bar, pie, rose, funnel, waterfall, bullet, big number / KPI |
| Distribution | Histogram, box plot, heatmap, radar, parallel coordinates |
| Hierarchy / flow | Treemap, sunburst, tree, sankey, chord, graph |
| Tables | Table, pivot table, AG Grid table |
| Other | Bubble, gauge, gantt, word cloud, paired t-test, Handlebars / custom HTML |

Also:

- Chart controls aligned with familiar BI explore flows (metrics, dimensions, filters)
- Dashboard assembly with reusable chart slices
- Local query + viz loop — change the chart, re-query SQLite (web) or DuckDB (desktop), no round-trip to a remote warehouse

---

## Risks & limitations

Read this before relying on Locply for critical workflows:

| Risk | What it means |
|------|----------------|
| **Web storage** | The website keeps work in this browser origin (OPFS / IndexedDB). Clearing site data, another browser, or private mode will not restore it. |
| **Desktop file** | Desktop stores `workspace.duckdb` on disk. Uninstalling, deleting that folder, or disk failure can destroy it. Back it up yourself. |
| **Single device** | No Locply cloud sync. Web and desktop workspaces are **not** the same store unless you export and import. |
| **Size & memory** | Web SQLite shares the browser tab. Very large files belong on **desktop DuckDB**. Free-plan caps on the web are in the published license policy. |
| **OPFS availability** | Durable browser SQLite needs a modern browser and `https://` or `localhost`. |
| **Not a remote warehouse** | There is no “connect production Postgres and leave data on the server” product. |
| **Network that is not your dataset** | Page delivery, license-policy fetch, desktop launch ping, and updates still use HTTPS. See Privacy. |
| **Closed source** | Source is not published. Security reviews are limited to vendor process and your own threat model. |
| **Trial / product surface** | Features and limits may change; check [locply.com/legal](https://www.locply.com/legal/). |

---

## Docs

- [Getting started](docs/getting-started.md)
- [Desktop](docs/desktop.md)
- [FAQ](docs/faq.md)

---

## Feedback

- Bug reports & feature requests: use [Issues](../../issues)
- Please do **not** open PRs that expect source merges — this repository does not contain application source code

---

## License

Proprietary. See [LICENSE](LICENSE).  
© Locply. All rights reserved.

---

## 中文简介

Locply 是**本机 BI**：导入 CSV / Excel / JSON / SQL，清洗与建模，在设备上查询并做图表与看板。不是远端数仓，也不是一次性转换站。

- **网站：** 浏览器里的 SQLite，免安装，适合试和小文件。
- **桌面：** 本机 DuckDB（Windows 官方安装包），适合更大文件和长期项目。
- **表不上 Locply 云。** 站点日志、许可证策略请求、桌面启动 ping 见 [隐私政策](https://www.locply.com/legal/privacy/)。

**主要风险：** 网站清站点数据会丢工作区；桌面依赖本机 `workspace.duckdb`，需自行备份；两端存储不自动同步；大数据请用桌面；源码不开源。

本仓库用于说明与反馈；**不包含源码**。请通过 Issue 反馈问题与建议。
