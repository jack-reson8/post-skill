# Post · 有网感、能带货的分享组图

[English](README.md) | 简体中文 | [日本語](README.ja.md) | [한국어](README.ko.md) | [Tiếng Việt](README.vi.md) | [हिन्दी](README.hi.md)

<p align="center"><img src="docs/share.png" alt="Post: a day of notes into a native-looking carousel" width="100%"></p>
<p align="center"><sub>属于 <a href="https://github.com/jack-reson8/copy-that"><b>Copy That</b></a> 系列 · 一行命令装全套</sub></p>

**把今天的真实数据交给 Claude，产出一套小红书 / X 组图：看起来像真 App 截图，读起来像真人在吐槽，同时在推你的产品和你的系列 IP。**

<table><tr>
<td><img src="docs/frame-1.jpg" width="170"></td>
<td><img src="docs/frame-2.jpg" width="170"></td>
<td><img src="docs/frame-3.jpg" width="170"></td>
<td><img src="docs/frame-4.jpg" width="170"></td>
<td><img src="docs/frame-5.jpg" width="170"></td>
</tr></table>
<sub>「让 Claude 赚回自己 200 美元订阅费」建造日记系列第 1 天，用本 skill 制作。</sub>

多数 AI 做的分享图都栽在同一个地方：渐变卡片、emoji 列表、一眼模板的“设计感”场景。这套 skill 来自一次真实制作里 7 轮被否（“丑”“一看就是 AI 做的”“不像 Claude”“太正经了”）直到被接受的过程，下面的方法就是从中沉淀出来的：

| 步骤 | Claude 做什么 |
|---|---|
| 1 · Brief | `brief.md`：这篇帖子的 GTM 作用、系列身份，以及带来源的真实事实清单——图里只能出现清单里的内容 |
| 2 · 参考 | 把平台高赞封面做成网格，研究好品味 App 的 App Store 截图组，写出 3 条结论（关卡） |
| 3 · 分镜 | 每张一行：标题、证据、浮出卡片、梗、GTM 作用。必备：带系列标识的封面、展示真实产出与价格的产品页、整页大数字页、关注钩子 |
| 4 · 文案 | 先说人话，再从梗库里加 1–3 个梗（反问式标题、一句话节拍、冷面幽默、回扣、反差结尾） |
| 5 · 制作 | 真实手机截图、像素级 App 界面模拟（X、Claude、iOS 锁屏、Google、Stripe）、非表格图表、App Store 海报模板 |
| 6 · 审查 | 缩略图尺寸的联系表，对照清单检查 |
| 7 · 交付 | 联系表 + 2–3 个标题备选。发布永远由你决定 |

## 安装

**作为 Claude Code 插件（推荐）**

```bash
claude plugin marketplace add jack-reson8/post-skill
claude plugin install post@post-skill
```

**作为普通 skill**

```bash
git clone https://github.com/jack-reson8/post-skill
cp -R post-skill/plugins/post/skills/post ~/.claude/skills/
```
需要 Google Chrome（无头渲染）和装有 Pillow 的 Python 3（生成联系表）。

**Codex（CLI 或 ChatGPT 桌面版）：**

```bash
codex plugin marketplace add jack-reson8/post-skill
codex plugin add post@post-skill
```

也可以把 `plugins/post/skills/post` 复制到 `~/.codex/skills/`。Skill 遵循 [Agent Skills](https://agentskills.io) 开放标准，Claude Code、Codex 以及任何能读取 SKILL.md 的 agent 都能用。

**其他 agent（Cursor、Gemini CLI、GitHub Copilot 等 skills CLI 支持的 agent）：**

```bash
npx skills add jack-reson8/post-skill
```

## 内置诚实规则
只用真实事实；对话类界面模拟是对真实对话的还原；绝不伪造他人的消息、付款、点赞或浏览量。

## 许可证
MIT。界面模拟为评论类帖子而模仿第三方 App，其名称和商标归各自所有者。

作者 [@jack-reson8](https://github.com/jack-reson8) · 姊妹 skill：[pro-motion](https://github.com/jack-reson8/pro-motion)、[skill-skill](https://github.com/jack-reson8/skill-skill)
