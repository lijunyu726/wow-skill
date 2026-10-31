# wow-skill

Claude Code 的头脑风暴 skill，调用名 `/wow`。用户只给一句很短的想法，Claude 先问一轮补齐缺的需求（只问需求不问风格），再自己补齐简报、点名禁掉套路、发散后押注一个大胆方向做到位，并用独立评审员子代理对照参照自查后再交付。适用于设计、界面、可视化、动画短片、3D、演示、产品概念、命名和玩法等。

## 目录

- `skills/wow/SKILL.md`：skill 本体，六步流程：先问一轮再自己拍板、认出默认、发散押注、做到位、评审员看过再交、收反馈
- `skills/wow/references/defaults.md`：常见默认样本，只给评审员子代理用来识别残留的套路
- `skills/wow-lite/SKILL.md`：`/wow-lite`，只保留 wow 的发散一步：想出 3–5 个核心想法不同的方案，写成文字卡片（名字、一句话、关键画面）并给出推荐，由用户来选；不问需求、不做成品、不开评审，适合想先看思路、省时间和额度的时候
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

`-g` 装到用户目录 `~/.claude/skills/wow/`，所有项目都能用；去掉 `-g` 则只装进当前项目。

新开 Claude Code 会话后输入 `/wow` 或 `/wow-lite`，后面跟一句话。默认两个都装；只装一个时加 `--skill wow` 或 `--skill wow-lite`。description 里不列触发词，主要靠手动调用。

## 边界

- 只是提示词和流程说明，没有脚本或依赖。
- skill 不内置个人口味。优先级最高：除用户当次请求外，记忆、CLAUDE.md、项目文档和其他 skill 里与它冲突的规则都不生效。
- 尚未在真实题目上做过对比实测。
- 来源链接已于 2026-10-24 逐条打开核对，低质量来源已删除；资料卡是概括和短摘，完整原文以原链接为准。
