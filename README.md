# Locply

**Local-first BI** — import CSV / Excel / JSON / SQL, clean data, query locally, and build charts & dashboards.  
**Nothing is uploaded.** Your data stays on this device.

> 这是 **公开发行与反馈仓**：仅包含产品说明、文档与安装包发布说明。  
> **源码不开放**（闭源商业软件）。应用开发在私有仓库进行。

---

## Try it

| Channel | Link |
|--------|------|
| Web (browser trial) | [https://www.locply.com/](https://www.locply.com/) |
| Desktop download | See [Releases](../../releases) or the links below |
| Legal / privacy | [https://www.locply.com/legal/](https://www.locply.com/legal/) |

### Desktop

Local file persistence via DuckDB workspace:

- **Windows:** `%APPDATA%/Locply/workspace.duckdb`
- **macOS:** `~/Library/Application Support/Locply/workspace.duckdb`

Installers (update these URLs when you publish each version):

- Windows (NSIS): _add Release asset or Cloudflare R2 URL_
- macOS (DMG): _add Release asset or Cloudflare R2 URL_
- Linux (AppImage): _add Release asset or Cloudflare R2 URL_

---

## What you get

- **Private by default** — browser trial uses on-device storage; desktop uses a local DuckDB file
- **Import** CSV, Excel, JSON, SQL
- **Clean & model** data in the workspace
- **Charts & dashboards** without sending datasets to a server

---

## Docs

- [Getting started](docs/getting-started.md)
- [Desktop app](docs/desktop.md)
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

Locply 是本地优先的 BI 工作区：在浏览器试用或安装桌面版，导入 CSV / Excel / JSON / SQL，清洗数据、本地查询、做图表与看板。**数据不上传。**

本仓库用于推广、文档与安装包发布；**不包含源码**。请通过 Issue 反馈问题与建议。
