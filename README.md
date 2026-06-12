# 国外企业背景调查 Skill

> WorkBuddy 技能：对海外企业进行多维度背调，输出结构化报告。

## 功能

- 支持通过**公司名称**或**邮箱域名**进行背调
- 自动识别公司规模，自适应调整搜索深度（大公司全维度 / SME 精简搜索）
- 多维度信息采集：基本信息、社交媒体、官网、新闻舆情、工商注册、专利知识产权、政府合同、制裁筛查
- 物理存在验证（Google Maps、WHOIS、OpenCorporates）
- 自动采集并汇总所有联系方式（电话、邮箱、社交账号、关键人员 LinkedIn）
- 同行业类似企业推荐
- 输出结构化 Markdown 背调报告，含可信度评级（A-E 级）

## 安装

将本仓库克隆到 WorkBuddy 的 skills 目录：

```bash
git clone https://github.com/xiezhenlin-tom/workbuddy-skill-company-background-check.git ~/.workbuddy/skills/foreign-company-background-check
```

## 使用

在 WorkBuddy 对话中直接说：

- 「背调一下 Stripe」
- 「帮我调查一下 notion.so 这家公司」
- 「查一下 sales@notion.so 这个邮箱对应的公司」
- 「company background check on OpenAI」

## 文件结构

```
├── SKILL.md                          # 技能定义（核心）
└── references/
    └── search-strategies.md          # 搜索策略与关键词模板
```

## 背调流程

1. **输入解析** — 提取公司名/邮箱域名，消歧确认
2. **多维度采集** — 根据公司规模自适应搜索
3. **验证与推荐** — 物理存在验证 + 同行业推荐
4. **结构化报告** — 输出含可信度评级的 Markdown 报告

## 可信度等级

| 等级 | 来源 |
|------|------|
| A | 官方注册信息、政府网站 |
| B | 权威媒体、行业报告 |
| C | 社交媒体、员工评价 |
| D | 匿名论坛、个人博客 |
| E | 待验证来源 |

## 注意事项

- 仅调查公开信息，不涉及个人隐私
- 制裁筛查为必做项（OFAC/EU）
- 报告中所有联系方式来自公开渠道，仅供合法商务联络使用
