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

## 4. Attach installers to Releases

After `npm run dist` in `charts/apps/desktop`:

1. Tag a version on this public repo (e.g. `v1.0.0`)
2. Create a Release
3. Upload `.exe` / `.dmg` / `.AppImage` as assets  
   **or** upload to Cloudflare R2 and put URLs in `README.md`

## 5. Optional: mirror GitHub ↔ Gitee

Same public docs/releases content on both platforms for domestic vs overseas discovery. Source stays on the private remotes only.
