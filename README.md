# avojuice.com Landing Page

一页式品牌官网，纯 HTML/CSS，零依赖、零构建。

## 本地预览

直接浏览器开 `index.html`，或者用 Python 起个 server：

```bash
cd "/Users/andrewheng/Desktop/AvoBase/07-软件开发团队/landing"
python3 -m http.server 8080
# 浏览器开 http://localhost:8080
```

## 部署（任选一种）

### A. Vercel（推荐 — 跟 Admin 一个账号）

```bash
cd landing
git init && git add . && git commit -m "feat: landing v1"
# 在 GitHub 新建一个 avojuice-landing repo
git remote add origin https://github.com/avojuiceipoh-ux/avojuice-landing.git
git push -u origin main
```

然后到 Vercel → New Project → Import `avojuice-landing` → Deploy（不需要任何配置，纯静态）。

域名设置：Vercel project → Settings → Domains → 加 `avojuice.com`（等域名买好后）。

### B. Cloudflare Pages

跟 Vercel 类似，连 GitHub repo 即可。免费版无限带宽，更适合长期。

### C. GitHub Pages（最简单）

repo Settings → Pages → 选 main 分支 → 几分钟上线在 `avojuiceipoh-ux.github.io/avojuice-landing/`。

## 还要做

- [ ] 买域名 `avojuice.com`（推荐 Namecheap / Cloudflare Registrar，约 RM 50/年）
- [ ] DNS 指向 Vercel/Cloudflare
- [ ] App Store / Play Store 上架后填 URL 到 store-btn
- [ ] 加 `privacy.html` + `terms.html`（从 00-品牌/隐私政策.md 和 用户协议.md 转 HTML）
- [ ] 加 og-image.png（社交分享缩略图，1200×630）
- [ ] 真菜单图 / 摊位实拍 替换 emoji

## 改 / 加内容

直接改 `index.html`。所有样式 inline 在 `<style>` 里。
搜索关键词替换菜单、价格、特色文案。
