# How to publish this public repo

This folder is a **standalone** marketing / releases repository.  
Keep it **separate** from the private `charts` (application source) remotes.

## 1. Create empty public repo

- **GitHub:** New repository → Public → no README (this folder already has one)
- **Gitee:** 新建仓库 → 公开 → 不要勾选初始化 README

Suggested name: `locply` or `locply-releases`

## 2. Init and push (from this directory)

```bash
cd e:/newcode/locply
git init
git add .
git commit -m "docs: public Locply release and feedback repository"
git branch -M main
git remote add origin <YOUR_PUBLIC_REPO_URL>
git push -u origin main
```

## 3. Keep private source private

| Repo | Visibility | Content |
|------|------------|---------|
| `charts` (current app) | **Private** | All source |
| `locply` (this folder) | **Public** | README, docs, Issues, Release assets only |

Do **not** add the private `charts` remote here, and do **not** copy `src/` into this folder.

Official Windows installer is served from [https://www.locply.com/download/](https://www.locply.com/download/) (Cloudflare → private object storage). Keep this repo’s README download link pointing at that URL.

GitHub Releases are optional for notes; do not instruct users to install unsigned copies from random mirrors.

After `npm run dist` in `charts/apps/desktop`, publish the artifact to the download bucket used by Pages, then confirm `/download/Locply_Setup.exe` resolves.

## 5. Optional: mirror GitHub ↔ Gitee

Same public docs/releases content on both platforms for domestic vs overseas discovery. Source stays on the private remotes only.
