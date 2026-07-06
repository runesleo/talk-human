# 说人话 · TalkHuman

**让 AI 帮你写的东西，读起来像你平时说话一样。**

一个跨 agent 的 skill。不是骗过检测器的玩具——是一套系统化、可审计、多轮的方法：先刮掉 AI 的统计口头禅，再把话改到能读，最后（最难那步）让它像**你**，不是像"一个人"。

最值钱的一步交给 AI：把你自己说话的样本（比如语音转录）丢给它，它替你生成一份"你的声音层"，之后按这个改稿。你出样本，AI 出你的声音。

---

## 两个模式

- **build-my-voice** — 从你的说话样本生成一份专属"声音层"清单（负向红线 + 正向硬条款）。
- **deslop** — 把一篇稿子按三轮去 AI 味：去统计指纹 → 改字可读 → 对齐你的声音。

---

## 安装 / 使用

### Claude Code / Claude agents（原生 skill）

把整个文件夹放进你的 skills 目录：

```
~/.claude/skills/talk-human/        # 全局
# 或 <你的项目>/.claude/skills/talk-human/   # 项目级
```

然后直接说：`帮我建我的声音层` / `把这段去 AI 味` / `deslop this`。

### Cursor / Codex / Gemini CLI / ChatGPT / 任意 LLM

不支持原生 skill 也能用——`references/` 里两个文件是**自包含的指令**，直接复制粘贴给你的 AI：

- 要建声音层 → 贴 `references/build-voice.md`
- 要去一篇稿子的 AI 味 → 贴 `references/deslop-pass.md`（有声音层就一起贴上）

---

## 一条铁律

**不替你造事实。** 只删、只改写、只重组。AI 腔越重，删完剩得越少——因为它的"顺"常常就是没内容。这工具帮你看清哪里其实是空的，剩下的真东西得你自己写。

---

## 结构

```
SKILL.md                      入口：模式路由 + 三轮总纲
references/
  build-voice.md              从你的样本生成你的声音层
  deslop-pass.md              三轮去 AI 味（清单内置）
examples/
  voice-layer.example.md      虚构人物范例，看格式用
  before-after.md             去 AI 味前后对照（中英文）
```

---

## License

见 `LICENSE`。
