# Locply

**Local-first BI in the browser** — import CSV / Excel / JSON / SQL, clean data, query with **SQLite WASM**, and build charts & dashboards.  
**Nothing is uploaded.** Analysis runs on your device.

> 这是 **公开发行与反馈仓**：仅包含产品说明与文档。  
> **源码不开放**（闭源商业软件）。应用开发在私有仓库进行。

---

## Try it

| Channel | Link |
|--------|------|
| Web | [https://www.locply.com/](https://www.locply.com/) |
| Legal / privacy | [https://www.locply.com/legal/](https://www.locply.com/legal/) |

**Engine today:** SQL queries run in-browser via **SQLite WASM** (prefer OPFS persistence when the browser supports it; otherwise fall back to in-memory + IndexedDB-backed metadata).

---

## What you get

- **Private by default** — datasets stay on this device; no analysis upload
- **Import** CSV, Excel, JSON, SQL
- **Clean & model** data in the workspace (type casting, transforms, local modeling)
- **Explore** metrics / dimensions, filters, and SQL-backed queries locally
- **Dashboards** — drag-and-drop layout of charts and components

---

## Chart highlights

Locply focuses on interactive, local visualization rather than server-side BI:

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
- Local query + viz loop — change the chart, re-query SQLite WASM, no round-trip to a remote warehouse

---

## Risks & limitations

Please read before relying on Locply for critical workflows:

| Risk | What it means |
|------|----------------|
| **Browser storage** | Data lives in the browser (OPFS / IndexedDB / local persistence). Clearing site data, uninstalling the browser profile, or using private/incognito mode can wipe the workspace. |
| **Single device** | No built-in multi-device sync or multi-user collaboration on one shared cloud dataset. Each browser profile is its own workspace. |
| **Size & memory** | SQLite WASM and the page share browser memory. Very large files or heavy dashboards may be slow, fail to load, or hit browser limits. Prefer smaller extracts when possible. |
| **OPFS availability** | Durable OPFS SQLite needs a modern browser and a secure context (`https://` or `localhost`). On unsupported setups Locply may fall back to less durable modes. |
| **Not a remote warehouse** | Locply is not a hosted warehouse / ETL platform. There is no remote DB connection model for “connect to production Postgres and leave data on the server.” |
| **Backup is your responsibility** | Export / re-import important datasets yourself. Do not treat browser storage alone as the only backup. |
| **Closed source** | Source is not published. Security reviews are limited to vendor process and your own threat model. |
| **Trial / product surface** | Features and limits may change; always check current terms at [locply.com/legal](https://www.locply.com/legal/). |

---

## Docs

- [Getting started](docs/getting-started.md)
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

Locply 是浏览器内的**本地优先 BI**：导入 CSV / Excel / JSON / SQL，清洗与建模，用 **SQLite WASM** 在本地查询，并制作图表与看板。**数据不上传。**

**图表特点：** 覆盖时序、对比、分布、层级/流向、表格等多类可视化；在设备上完成探索、筛选与看板拼装，无需把数据集发到远端数仓。

**主要风险：** 浏览器清站点数据可能丢工作区；单设备、无默认云同步；大数据受浏览器内存与 SQLite WASM 限制；OPFS 持久化依赖现代浏览器与 HTTPS/localhost；需自行备份导出；源码不开源。

本仓库用于推广与文档；**不包含源码**。请通过 Issue 反馈问题与建议。
