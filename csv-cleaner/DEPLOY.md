# CSV 清理器 · 部署说明

第二个 S5 工具站。纯前端单文件（`index.html` 中文 + `en/index.html` 英文），零依赖，RFC4180 手写解析器（正确处理引号内逗号/换行）。

## 质量验证（2026-10-30 浏览器实测）

- 真实链路测试：File → FileReader → 解析 → 统计 → 清理 → 预览/下载
- 去重/空行/空列/trim 全部正确（7 行测试数据 → 4 行，精准移除 2 重复 + 1 空行）
- 带引号的逗号字段（"Zhang, San"）解析与导出均保持完整
- 分隔符自动识别（逗号/分号/Tab）✓
- TextDecoder GBK 解码器在目标浏览器可用 ✓（中文乱码场景的核心卖点）
- 首行表头模式 ✓

## 部署（与周报生成器相同，三选一）

- **GitHub Pages**：`gh repo create csv-cleaner --public --source=. --push` → Settings → Pages → main/root
- **Netlify Drop**：拖目录到 app.netlify.com/drop
- **Cloudflare Pages**：Upload assets

建议域名路径：`你的域名/csv-cleaner`（或独立子域），与周报生成器同店互链。

## 收款接线

Pro 版占位区块已在两版 HTML 中留好（搜索 "Lemon Squeezy"）：
- Pro 卖点：批量多文件、按列去重、正则替换、Excel 导出
- 定价建议：$4.9（纯效率工具，低价走量）

## SEO 上线后清单

- [ ] Google/Bing/百度站长提交
- [ ] 目标关键词：csv cleaner online / csv 去重 / csv 乱码 / remove duplicate rows csv
- [ ] 内容站写配套教程页互链（"CSV 乱码怎么解决"是中文长尾金矿）

## v2 候选

- 按列去重（指定 key 列）
- 列名重命名/列排序
- 10 万行以上分块处理优化
