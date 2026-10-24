# 参考：Opus 5.5 「一句话惊艳」案例的提示词写法

2026-10-24 整理自国内外公开帖子、文章和官方文档，所有链接已逐条打开核对。原文只摘关键短句，每个来源的详细资料卡在同目录的 `sources/`，以防链接失效。

## 一、短提示词为什么有时能成：放手 + 体裁 + 标杆

| 案例 | 关键句 | 起作用的是什么 |
|---|---|---|
| 动效作品集（@shneural 等人带火，Stephan Livera 那条约 230 万次观看；中文流行版是「……就像简历里的作品展示卷。全力以赴。」） | 「…what an incredible motion designer you are, like it's your showreel for a résumé. go all out.」 | 体裁（求职作品集）加上主角是模型自己，没有能做错的事实 |
| 完全开放题（Axton，做出水墨网页「墨韵」） | 「你是opus 5.5…让每一个看到你的结果的人…都会惊叹…你会做什么事呢？」 | 连题目都放手；模型自己截图，从 v1 改到 v4 |
| 建筑工作室网站（YouTube 对比视频，引句是作者口述；有赞助，作者其实给了一个参考网站） | 「I don't wanna give you any visual or design direction… the kind that wins awards.」 | 放手加标杆（拿奖） |
| 用 Blender 做 Apple 广告风格的视频（@anshuc） | 「do this whole thing on your own… looks like an apple ad」；第二条是挑错清单，最后加一句「pull out all the stops」 | 授权独立完成，标杆是 Apple 广告，第二轮按问题清单改 |
| 卡尔维诺《看不见的城市》（Quesma） | 「Don't ask questions, it is a one-shot task… until it becomes a masterpiece.」 | 不许提问，标准定为杰作；说好 6 小时，实际 1 小时 25 分就交了 |
| 雨中东京路口短片（@petergostev） | 指定四种颜色、木刻刀痕和印刷颗粒；用一个红绿灯周期驱动整个场景（等待 → 涌过 → 散去） | 一个具体的媒介质感，加一个用来编排的节奏 |

**通病是简报传染**：几百人发同一句话，出来的作品几乎一样。木易实测，动效作品集那句做出来清一色是红黑配米白底，结尾都是「CLAUDE · MOTION DESIGNER」。他的结论是：一句话能出片，但出不了好片。

## 二、真正惊艳的作品，背后几乎都有这几样

1. **自评循环比加强语气更关键**：
   - @everestchris6 给出一种写法：照着平面图和照片，用 three.js 做出一座可以走进去的房子。房子拆成几部分，每部分配一个建造者，再配一个**新开上下文的评审员**：评审员拿截图和真实照片比，挑出更好的那张，点名最大的差距，退回去改，一直循环到我们这边赢为止。注意这是带货帖里给读者的建议写法，原帖没说是本人实际跑过的。
   - 少数派的要求是渲染前先截几帧自己看，专门检查浅色字的对比度。
   - 官方 frontend-design skill 原话：「a picture is worth 1000 tokens」。
2. **简报，不是愿望**：
   - Muzli 的简报写的是给谁、三个词的情绪、不是什么套路、那一个让人截图的瞬间、只编排一个动效高潮、底线和禁用清单。每份不到 200 个英文单词，每句都是一个决定。
   - 刷屏作品背后常有很长的简报，比如 seeco 提到的那条爆款，简报约 9,500 个英文字符。宝玉的《桃花源记》也是「反复打磨了好多次」。
3. **点名禁用**（Anthropic 官方 Opus 5.5 提示词指南）：
   - 泛泛说「别有 AI 味」，只会把一种默认换成另一种。
   - 官方示例原文：「Do not use a cream or off-white background, italic accent words in headlines, numbered "01/02/03" section labels, monospace labels, or pill-shaped buttons.」
   - 第一版出来后，看它又换上了什么新的默认样式，再补进清单。
4. **frontend-design skill 的几句**：
   - 角色是设计工作室的设计负责人，客户已经否掉了显得套路、模板化的提案。
   - 「Spend your boldness in one place」。
   - 交之前学 Chanel 的建议：照照镜子，去掉一个配饰。
   - 先构思一套紧凑的配色字体方案，对照简报检查是否泛化，再写代码。
5. **先发散再执行**（@techartist_）：先让模型列一批点子，挑中一个后让它自己写出详细提示词，再按提示词去做。
6. **扔掉第一个想法**（@kloss_xyz）：「Own every creative call and push past the first idea.」这句出自作者事后让模型反推出来的一份长提示词，不是短提示词。

## 三、思考力度

- 爆款大多跑在 xhigh、max 或 Extra 档。
- 木易说做视频用 xhigh 就够，max「容易想太多，很慢」。Moe Lueker 引用的一个编程基准里，medium 和 max 得分相当（54.6% 对 54.4%）。注意这是编程题，不是设计作品的实测。
- 官方提示词指南的说法是：xhigh 和 max 留给已经测出质量提升的任务。Effort 文档写的是：xhigh 适合 30 分钟以上的长任务。

## 四、中文圈的注意点

- 中文要点名字体（苹方、微软雅黑），否则可能渲染成方块；视频里中文字号不小于 40px。
- 点名风格比形容词强一百倍：「国风水墨、深蓝到暖金」好过「好看点」。
- 也有人反过来，让模型先问 4 个决定性问题再开工（B 站风之谷 AI 的星舰科普）。

## 五、可以直接借用的句式

- **放手**：「不给你任何视觉方向，所有创意决定都归你。」
- **体裁加身份**：「这是你的作品集 / 简历，展示你作为【角色】有多厉害。」
- **标杆**：「要达到【拿奖网站 / Apple 广告 / 实物照片】的水准。」
- **一个记忆点**：「整件作品只押注一个让人截图的瞬间：【……】，其余全部安静。」
- **点名禁用**：「不要：【具体的配色、字体、版式、动效套路】。」
- **扔掉第一个想法**：「每个创意决定都由你负责，越过你的第一个想法。」
- **自评循环**：「每一部分配一个新上下文的评审员，拿截图和参照比，点名最大差距，退回去改，直到我们赢。」
- **独立完成**：「不要提问，一路做完；需要我的账号或付费时再说。」

## 来源

**国内**
- [木易 · AI信息Gap](https://mp.weixin.qq.com/s/8Q4w8y1fl2g4lj2-y89NuQ)
- [AI范儿（网易号）](https://www.163.com/dy/article/L7NE1UAF0556703U.html)
- [少数派 Benx_AI](https://sspai.com/post/115283)
- [Axton](https://www.axtonliu.ai/newsletters/ai-2/posts/opus-5-5-real-practice-reflection)
- [宝玉](https://x.com/dotey/status/2102940980379017293)，[《桃花源记》源码和提示词](https://github.com/JimLiu/taohuayuan)
- [B 站 · 风之谷 AI](https://www.bilibili.com/video/BV1VxhD6jE5V)

**海外**
- [@shneural（作品集那句，目前查到最早）](https://x.com/shneural/status/2103151003272962130)
- [@stephanlivera（同一句）](https://x.com/stephanlivera/status/2103315922098470926)
- [@everestchris6（带货帖）](https://x.com/everestchris6/status/2110036224320884998)
- [@anshuc](https://x.com/anshuc/status/2103951792136441872)
- [@petergostev](https://x.com/petergostev/status/2113636735687004671)
- [@kloss_xyz](https://x.com/kloss_xyz/status/2107696042053431360)
- [@techartist_](https://x.com/techartist_/status/2103933640392786274)
- [YouTube：Opus 5.5 与 Fable 5.1 建同一个网站（有赞助）](https://www.youtube.com/watch?v=ceNplgiZOFE)
- [Moe Lueker 评测（数据为编程基准）](https://moelueker.com/blog/claude-opus-5-5-review)
- [Muzli](https://muz.li/blog/claude-opus-5-5-for-designers/)
- [Quesma](https://quesma.com/blog/invisible-cities-one-shot/)
- [seeco（X 文章）](https://x.com/i/article/2106096193235259564)

**合集（当索引用）**
- [skillry：数百条 Opus 5.5 视频提示词，标注原作者](https://skillry.dev/zh/ai-videos/opus-5-5)
- [100 个单文件页面（附提示词）](https://miaai-lab.github.io/Claude-Opus-5.5-100-HTML-Files)
- [AY Automate 提示词合集（页面自称未测试，带咨询引流）](https://www.ayautomate.com/resources/claude-opus-5-5-motion-graphics)

**官方**
- [Prompting Claude Opus 5.5](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-opus-5-5)
- [Effort](https://platform.claude.com/docs/en/build-with-claude/effort)
- [anthropics/skills · frontend-design](https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md)
