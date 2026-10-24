# Post · 有网感、能带货的分享组图

把今天的真实数据交给 Claude，产出一套小红书 / X 组图：看起来像真 App 截图，读起来像真人在吐槽，同时在推你的产品和你的系列 IP。

这套方法来自一次真实制作里 7 轮被否（"丑""一看就是 AI 做的""不像 Claude""太正经了"）直到被接受的过程。

流程：brief（目标、系列、真实事实清单）→ 参考（平台高赞封面网格 + 好品味 App 的 App Store 截图组）→ 分镜表（每张：标题、证据、浮出卡片、梗、GTM 作用）→ 文案（先说人话 再加 1–3 个梗）→ 制作（真实手机截图、像素级 App 界面模拟、非表格图表、App Store 海报模板）→ 缩略图审查 → 交付（发布永远由你决定）。

安装（Claude Code 插件，推荐）：
```bash
claude plugin marketplace add jack-reson8/post-skill
claude plugin install post@post-skill
```

或者当普通 skill 用：
```bash
git clone https://github.com/jack-reson8/post-skill
cp -R post-skill/plugins/post/skills/post ~/.claude/skills/
```

Codex（CLI 或 ChatGPT 桌面版）：
```bash
codex plugin marketplace add jack-reson8/post-skill
codex plugin add post@post-skill
```
也可以把 `plugins/post/skills/post` 复制到 `~/.codex/skills/`。Skill 遵循 [Agent Skills](https://agentskills.io) 开放标准，Claude Code、Codex 以及任何能读取 SKILL.md 的 agent 都能用。
