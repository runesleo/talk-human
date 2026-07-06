# talk-human · 说人话

> 让 AI 帮你写的东西，读起来像**你**平时说话——不是像"一个 AI"，也不是像"一个泛泛的人"。

[English](README.md) · [中文](README.zh.md)

一个跨 agent 的 skill。不是骗过检测器的玩具——是一套系统化、可审计、多轮的方法：先刮掉 AI 的统计口头禅，再把话改到能读，最后（最难那步）让它像**你**。

最值钱的一步交给 AI：把你自己说话的样本（比如语音转录）丢给它，它替你生成一份"你的声音层"，之后按这个改稿。你出样本，AI 出你的声音。

## 两个模式

- **build-my-voice** — 从你的说话样本生成一份专属"声音层"清单（负向红线 + 正向硬条款）。
- **deslop** — 把一篇稿子按三轮去 AI 味：去统计指纹 → 改字可读 → 对齐你的声音。

## 安装

### Claude Code / Claude agents（原生 skill）

把整个文件夹放进你的 skills 目录：

```bash
# 全局
~/.claude/skills/talk-human/
# 或项目级
<你的项目>/.claude/skills/talk-human/
```

然后直接说：`帮我建我的声音层` / `deslop this` / `把这段改得像我说话`。

### Cursor / Codex / Gemini CLI / ChatGPT / 任意 LLM

不支持原生 skill 也能用——`references/` 里的文件是**自包含指令**，直接复制粘贴给你的 AI：

- 要建声音层 → 贴 `references/build-voice.md`
- 要去一篇稿子的 AI 味 → 贴 `references/deslop-pass.md`（有声音层就一起贴上）

## 用法

```
你： deslop this —— [贴上你的 AI 初稿]
AI： 第一轮（指纹）：删掉「值得注意的是」「在当今时代」…
     第二轮（可读性）：拆了 3 个长句，补回主语…
     第三轮（声音）：[有 voice-layer.md 就按它，没有就套通用原则]
     → [改后稿] + 三行改动小结
```

## 一条铁律

**不替你造事实。** 只删、只改写、只重组——不加新观点、新数字、新结论。AI 腔越重，删完剩得越少——因为它的"顺"常常就是没内容。这工具帮你看清哪里其实是空的，剩下的真东西得你自己写。

## 隐私

无任何网络请求，完全在你的 agent 本地运行。你的说话样本和草稿不离开你的机器——skill 只负责告诉你的 AI 怎么处理它们。

## 关于作者

*Leo（[@runes_leo](https://x.com/runes_leo)）— AI × Crypto 独立构建者。在 [Polymarket](https://polymarket.com/?via=runes-leo&r=runesleo&utm_source=github&utm_content=talk-human) 做量化，用 Claude Code 和 Codex 搭数据与内容管线。*

*[leolabs.me](https://leolabs.me) — 写作 · 社群 · 开源工具 · 独立项目*

*[X 订阅](https://x.com/runes_leo/creator-subscriptions/subscribe) — 付费内容周刊*

*Learn in public, Build in public.*

## License

MIT © Leo ([@runes_leo](https://x.com/runes_leo))
