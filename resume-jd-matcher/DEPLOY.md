# 简历 JD 匹配器 · 部署说明

第三个 S5 工具站。纯前端双文件（`index.html` 中文 + `en/index.html` 英文），零依赖，规则匹配引擎（词库 + n-gram 双通道），文本不出浏览器。

## 质量验证（2026-10-30 浏览器实测）

- 中英双版分别用真实 JD/简历测试：三档分层（明确匹配/待补证据/缺失）+ 硬匹配覆盖率 + JD 高频关键词清单全部正确
- 噪音修复：JD 段落标题（岗位职责/任职要求/Responsibilities 等）不再被误判为要求条目（中英文停用正则）
- 词库去重修复 ✓；JS 语法检查通过 ✓
- 已知边界：软性描述（"良好的沟通能力"）只能给方向性判断；词库覆盖面随使用持续扩充

## 部署（与另外两个工具站相同）

- **GitHub Pages**：`gh repo create resume-jd-matcher --public --source=. --push` → Settings → Pages → main/root
- **Netlify Drop** / **Cloudflare Pages**：拖目录直传

## 收款接线

Pro 占位已留（搜索 "Lemon Squeezy"）：
- Pro 卖点：逐条改写建议、STAR 改写辅助、多岗位对比矩阵
- 定价建议：$7.9（求职场景付费意愿高于效率工具）

## SEO 上线后清单

- [ ] 三大站长平台提交
- [ ] 目标关键词：简历匹配 / jd 分析 / resume keyword checker / ats keywords
- [ ] 配套教程页："简历怎么对着 JD 改"（已有关联文章可改写为站内页）

## v2 候选

- 词库扩充（按行业分类：金融/IT/运营…）
- 多岗位对比矩阵（一个简历 vs 3 个 JD 并排）
- 改写建议（把缺失项映射到 STAR 结构提示）
