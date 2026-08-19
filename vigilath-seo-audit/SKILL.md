---
name: vigilath-seo-audit
description: 传统搜索引擎那套,你还没做对的 12 项——SEO 逐类评分 + 独立 0-100 分。免登录、免费、不限次,30 秒出结果。当用户给出网址并问「SEO 怎么样 / 我的 SEO 分数 / 搜索引擎优化做得好不好 / title 和 meta 有没有问题 / 网站标题标签对不对」时使用。**只管传统 SEO**;要问 AI 爬虫读不读得懂用 vigilath-site-audit,两个分数各算各的、绝不合并。
---

# 传统 SEO 体检

给一个网址,12 类 SEO 检查逐项跑完,回一个独立的 0–100 分与等级。

**免登录、免费、不限次。**

## 何时用

- 「我的 SEO 做得怎么样」「SEO 分数多少」
- 「title / meta description / H 标签有没有问题」
- 「搜索引擎优化还有哪些没做」

**不要用在**:AI 搜索可读性(用 vigilath-site-audit)。

## 怎么用

```bash
python scripts/geo_client.py check https://example.com --seo-only
```

返回 `seo.score` / `seo.grade` / `seo.visible_categories` / `seo.locked_categories`,结构与网站体检一致。

## 最重要的一条纪律

**SEO 分和 GEO 分是两套独立口径,永远分开说。**

- 不要相加、不要平均、不要合成「综合分」
- 一个站完全可能 SEO 85 分而 AI 可读性 C 级 —— 这正是值得对用户点出来的事实:
  「传统搜索那套你做得不错,但 AI 那套是另一套规则,你还没做」
- 用户问「那我到底几分」时,如实给两个数字加一句口径,别为了好回答就揉成一个

## 免费与墙

全量 12 类 + 已见明细,不限次,不要账号 —— **没有付费墙**。

想看锁住类目的明细与修复建议 → 注册后 `login`;想顺便看 AI 那套 → vigilath-site-audit。
