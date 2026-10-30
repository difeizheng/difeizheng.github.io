# 提示词骨架生成器 · 部署说明

第四个 S5 工具站。纯前端双文件（`index.html` 中文 + `en/index.html` 英文），零依赖，五件套骨架（角色/任务/上下文/要求/禁区）填空生成结构化提示词。

## 质量验证（2026-10-30 浏览器实测）

- 场景预设填入（5 个预设：写作文案/工作周报/简历优化/学习拆书/谈判准备）
- 骨架完成度计量条实时更新（5/5）
- 生成逻辑：全字段、单字段（极简）、防编造尾注均正确
- clearAll/copy/localStorage 草稿 ✓
- 双语版互链 ✓

## 部署（同前三个工具站）

- **GitHub Pages**：`gh repo create prompt-builder --public --source=. --push` → Pages → main/root
- **Netlify Drop** / **Cloudflare Pages**：拖目录直传

## 收款接线

Pro 占位已留（搜索 "Lemon Squeezy"）：
- Pro 卖点：20 个场景预设包 + 提示词版本管理
- 定价建议：$4.9（与 CSV 清理器 Pro 同档）

## SEO 上线后清单

- [ ] 三大站长平台提交
- [ ] 目标关键词：prompt builder / 提示词生成器 / 结构化提示词 / prompt template
- [ ] 配套教程页："提示词五件套"（文章 30 号可改写为站内页并互链）

## v2 候选

- 自定义预设保存（用户自建场景库）
- 生成历史与版本对比
- 分享链接（把配置编码进 URL 参数）
