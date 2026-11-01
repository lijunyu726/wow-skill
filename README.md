# wow-skill

Claude Code 的头脑风暴 skill，调用名 `/wow`。用户只给一句很短的想法，Claude 先写一行这个题目最普通、谁都会想到的做法，再想出 3–5 个绕开它、核心想法不同的方案，写成文字卡片（名字、一句话、关键画面、跟默认差在哪），给出推荐，由用户来选。适用于设计、界面、可视化、动画短片、3D、产品概念、命名、文案和玩法等。

## 目录

- `skills/wow/SKILL.md`：skill 本体，两步：认出默认、发散出方案卡片
- `docs/prompts.md`：Opus 5.5「一句话惊艳」案例的提示词写法总结（2026-10-24 整理）
- `docs/sources/`：每个来源的资料卡（概括、提示词结构、可复用做法、可信度提醒），防止原链接失效
  - `cn-official.md`：国内 6 个来源和 Anthropic 官方 3 份文档
  - `overseas.md`：海外 15 个来源

`docs/` 在 skill 目录外，调用 skill 时不会被读取。

## 安装

用 [skills](https://github.com/vercel-labs/skills) 命令行工具（需要 Node.js 18+）：

```bash
npx skills add lijunyu726/wow-skill -g -a claude-code
```

`-g` 装到用户目录 `~/.claude/skills/wow/`，所有项目都能用；去掉 `-g` 则只装进当前项目。已经装过的用 `npx skills update` 更新。

新开 Claude Code 会话后输入 `/wow`，后面跟一句话。description 里不列触发词，主要靠手动调用。

## 边界

- 只是提示词，没有脚本或依赖。
- 只出方案卡片，不做成品，不出图。
- skill 不内置个人口味。
- 尚未在真实题目上做过对比实测。
- 来源链接已于 2026-10-24 逐条打开核对，低质量来源已删除；资料卡是概括和短摘，完整原文以原链接为准。
