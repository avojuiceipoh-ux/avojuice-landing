# avojuice.com Landing Page v2

一页式品牌官网，纯 HTML/CSS，零依赖、零构建。

**v2 更新 (2026-05-25):** 全面重做 — 百分茶式清爽通透美学，融合 Mintlify 精准留白。

## 本地预览

```bash
cd "/Users/andrewheng/Desktop/AvoBase/07-软件开发团队/landing"
python3 -m http.server 8080
# 浏览器开 http://localhost:8080
```

## 部署

### A. Vercel（推荐）

```bash
cd landing
git add . && git commit -m "v2: 全面重做 landing page"
git push origin main
```

Vercel 自动部署，域名：avojuice-landing.vercel.app

### B. 域名绑定

Vercel project → Settings → Domains → 加 `avojuice.com`

## 文件结构

```
landing/
├── index.html        # 主页面
├── privacy.html      # 隐私政策
├── terms.html        # 用户协议
├── og-image.png      # 社交分享缩略图 (1200×630)
├── og-image.html     # OG 图源文件（方便修改重生成）
├── logo.png          # 品牌 Logo
├── images/           # 产品实拍图（替换 emoji 用）
│   ├── avocado-smoothie.jpg
│   ├── mango-smoothie.jpg
│   ├── strawberry-smoothie.jpg
│   ├── blueberry-smoothie.jpg
│   ├── watermelon-smoothie.jpg
│   ├── banana-smoothie.jpg
│   ├── redbean-smoothie.jpg
│   ├── pineapple-passion.jpg
│   └── peach-oolong.jpg
└── README.md
```

## 换图方法

1. 把实拍照丢进 `images/` 文件夹
2. 文件名对上即可自动替换（`onerror` 回退到 emoji 占位）
3. 如需加新品：复制 `<div class="menu-card">...</div>` 块

## 设计规范

- 主色: `#52c41a` (牛油果绿)
- 深色: `#389e0d`
- 浅绿: `#f6ffed`
- 文字: `#171717` / `#737373`
- 圆角: 8 / 16 / 24 / 9999px 渐进
- 字体: Noto Sans SC + Inter
- 暗色模式: `prefers-color-scheme: dark` 自动适配

## 待办

- [ ] 买域名 `avojuice.com`
- [ ] 产品实拍图替换 emoji（丢 `images/` 即可）
- [ ] App Store / Play Store 链接更新
- [ ] DNS 指向 Vercel
