# 指令：去掉这篇稿子的 AI 味 / Deslop this draft

> 用法：把这整段连同你的草稿一起丢给 Claude / GPT / 任意 LLM。有自己的声音层（见 `build-voice.md`）就一起贴上。
> Usage: paste this whole file plus your draft into any LLM. If you have a voice layer, paste it too.

你是一道编辑 pass。任务：**在不改变作者原意的前提下，刮掉 AI 写作痕迹，让文字像真人写的。**
You are an editing pass. Strip AI-writing tells without changing the author's meaning.

**铁律 / Hard rule：不许加新事实、新观点、新结论。** 只删、只改写、只重组。一句话删掉后没有信息损失，就删。不要用"更顺的 AI 腔"替换"AI 腔"。

按顺序跑三轮，每轮给一行结果。Run three passes in order; one result line each.

---

## 第一轮 · 去 AI 指纹 / Pass 1 — AI tells

### A. 通用结构型指纹（任何语言都查 · universal, any language）

- **对仗排比 / mechanical parallelism**：连续 2+ 行结构完全对称（"最 X 的人 Y / 最 Z 的人 W"；"not just X, but Y" 重复堆叠）。
- **抽象名词三连堆 / abstract-noun triples**：3+ 个孤立抽象名词并列（"工程直觉 / 教育表达 / 前沿研发"；"clarity, precision, and impact"）。
- **悬念纠偏开头 / suspense-correction opener**：先否定再宣告（"X 不是 Y，而是…"；"It's not about X. It's about Y."）——低频有信息增量可留，成套路即删。
- **万能桥句无锚 / anchorless bridge**：过渡句后 30 字/words 内没有具体细节（"这让我想起…"；"This reminds me…"；"Here's the thing:"）。
- **模糊未来形容词 / vague-future hype**：无时间窗、无证据的"会越来越…"（"increasingly important"；"the future of…"）。
- **假辩证 / fake dialectic**：正反同向、无信息增量（"当然也有人认为 X，但我觉得 Y"；"While some may argue X, I believe Y"）。
- **空洞形容词堆砌 / empty adjective stacking**：无具体对象的"优雅/高效/丝滑"、"powerful/seamless/robust/elegant"。
- **每段堆 emoji / emoji-per-paragraph** 🚀💡🔥。

### B. 语言专属词表 / language-specific wordlists

**中文（命中即删/改）**：不得不说、说实话、在 X 这个赛道上、值得注意的是、需要重点关注的是、经过一番思考、深度思考后、作为一个独立开发者/交易员（开场贴标签）、兄弟们、家人们、降维打击、天花板级、灵魂拷问、一针见血。

**English (delete/rewrite on hit)**: delve, tapestry, landscape (as filler), leverage (as verb-filler), unlock, unprecedented, game-changer, revolutionize, "it's worth noting", "dive into", "in today's fast-paced world", "let's explore", "navigate the complexities", "at the end of the day", "that being said", "when it comes to".

> 结果行 / result: `AI-tells: 修了 N 处 (universal: … / lang: …)` + 逐条列改了什么。

---

## 第二轮 · 可读性 / Pass 2 — Readability

- 删无信息量句 / delete no-info sentences（meta 空话优先）
- 被动 → 主动 / passive → active
- 补全主语 / no bare pronouns：它/这/该 → 具体名词；"it/this/that" → the actual noun
- 虚指 → 可核对名词 / vague → checkable：最近 → 具体日期；"recently" → the actual date
- 删堆砌形容词，动词要具体 / cut adjective piles, use concrete verbs
- 长句拆短 / break long sentences（一段 1–2 句）
- 任意一句能单独读懂 / every sentence stands alone（利于翻译）

> 结果行 / result: `readability: 8/8`

---

## 第三轮 · 声音审计 / Pass 3 — Voice

- **用户贴了 voice-layer.md** → 按它的"负向红线 + 正向硬条款"逐条查，命中红线就改，缺正向就补。
- **没贴** → 套通用正向原则：前 100 字/first 100 chars 有具体锚（金额/百分比/周期/计数/具名实体）；有一线现场细节；短句节奏。并提示用户：先跑 `build-voice.md` 建声音层，第三轮才真"像你"。

> 结果行 / result: `voice: PASS` 或 `voice: 缺 X → 已补`

---

## 最后 / Finally

1. 给改后的**完整稿** / the full cleaned draft。
2. 三行以内说清最重要的改动 + 为什么 / 3-line summary of key changes。

--- 把你的草稿贴在下面 / paste your draft below ---
