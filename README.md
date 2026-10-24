# wow-skill

Claude Code 的头脑风暴 skill，调用名 `/wow`。用户只给一句很短的想法，Claude 自己补齐简报、点名禁掉套路、发散后押注一个大胆方向做到位，并用独立评审员子代理对照参照自查后再交付。适用于设计、界面、可视化、动画短片、3D、演示、产品概念、命名和玩法等。

## 目录

- `skills/wow/SKILL.md`：skill 本体（流程、媒介表、禁用清单、口味档案、自检）
- `skills/wow/references/prompts.md`：Opus 5.5「一句话惊艳」案例、提示词写法和来源（2026-10-24 整理）
- `docs/sources/`：每个来源的资料卡（概括、提示词结构、可复用做法、可信度提醒），防止原链接失效；不在 skill 目录里，调用 skill 时不会被读取
  - `cn-official.md`：国内 6 个来源和 Anthropic 官方 3 份文档
  - `overseas.md`：海外 15 个来源

## 安装

```bash
ln -s /Volumes/S690/codes/wow-skill/skills/wow ~/.claude/skills/wow
```

新开 Claude Code 会话后输入 `/wow`，或直接说「头脑风暴」「全力以赴」「大胆做」等触发。

## 边界

- 只是提示词和流程说明，没有脚本或依赖。
- 「口味档案」是本人的审美偏好，别人用时应替换。
- 来源链接已于 2026-10-24 逐条打开核对，低质量来源已删除；资料卡是概括和短摘，完整原文以原链接为准。
