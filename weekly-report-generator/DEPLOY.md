# 周报生成器 · 部署与收款接线说明

第一个 S5 工具站。纯前端单文件（`index.html` 中文版 + `en/index.html` 英文版），零依赖、零构建、数据不出浏览器。

## 已完成的质量验证（2026-10-29 浏览器实测）

- 表单填写→生成：已完成/进行中/遇到问题 三种状态分流正确（"遇到问题"自动进风险区）
- 标准模板与极简三行模板均正常
- localStorage 草稿：刷新后自动恢复 ✓
- 复制/下载功能：剪贴板带 file:// 降级方案
- 中英双语页面互链，SEO meta/canonical 就位

## 部署（三选一，均为免费）

**方式 A：GitHub Pages（推荐，需要 PAT 建仓权限）**
```
1. gh repo create weekly-report-generator --public --source=. --push
   （或将本目录作为仓库推送，PAT 需勾选 repo 创建权限）
2. GitHub 仓库 Settings → Pages → Source: main branch / root
3. 访问 https://difeizheng.github.io/weekly-report-generator/
```

**方式 B：Netlify Drop（无 git，5 分钟）**
```
1. 打开 app.netlify.com/drop（需注册 Netlify 账号）
2. 把本目录拖进网页 → 立即获得 https://随机名.netlify.app
3. Site settings → change site name 改成 weekly-report-generator
```

**方式 C：Cloudflare Pages（直传，国内访问速度较好）**
```
1. dash.cloudflare.com → Workers & Pages → Create → Pages → Upload assets
2. 拖入本目录 → 获得 *.pages.dev
```

## 收款接线（Lemon Squeezy 建店后）

1. `index.html` 与 `en/index.html` 中搜索 `Lemon Squeezy`，把注释里的占位链接换成真实商品 checkout URL
2. Pro 商品建议定价：**$6.9 / ¥29**（进阶模板包：述职框架+月报合并+英文周报模板）
3. LS 的 Webhook 不需要——文件类商品 LS 自带自动交付

## SEO 上线后清单（一次性）

- [ ] Google Search Console 提交（验证站点所有权）
- [ ] Bing Webmaster 提交（必应带来部分长尾）
- [ ] 百度站长平台提交（中文版）
- [ ] 等 2-4 周观察 Search Console 的曝光数据，再决定加内容页

## 后续迭代候选（v2）

- 月报合并模式（4 周周报 → 1 份月报）
- 导出 Word 格式
- 英文 Pro pack（promotion review template）
