# talk-human

> Make what AI writes for you read like **you** actually talk — not like "an AI," not like "a generic person."

[English](README.md) · [中文](README.zh.md)

A cross-agent skill. Not a detector-evasion toy — a systematic, auditable, multi-pass method: first scrape off AI's statistical tics, then make sentences readable, then (the hard part) make it sound like **you**.

The most valuable step is delegated to the AI: feed it a sample of how you actually talk (e.g. a voice transcript), and it generates a **"voice layer"** for you — then rewrites drafts against it. You supply the sample; the AI extracts your voice.

## Two modes

- **build-my-voice** — generate a personal "voice layer" checklist (negative red-lines + positive hard-rules) from your speaking samples.
- **deslop** — strip the AI-ness from a draft in three passes: remove statistical fingerprints → improve readability → align to your voice.

## Install

### Claude Code / Claude agents (native skill)

Drop the folder into your skills directory:

```bash
# global
~/.claude/skills/talk-human/
# or project-level
<your-project>/.claude/skills/talk-human/
```

Then just say: `build my voice layer` / `deslop this` / `make this sound like me`.

### Cursor / Codex / Gemini CLI / ChatGPT / any LLM

No native skill support needed — the files under `references/` are **self-contained instructions**. Paste them into your AI:

- To build a voice layer → paste `references/build-voice.md`
- To deslop a draft → paste `references/deslop-pass.md` (include your voice layer if you have one)

## Usage

```
You: deslop this — [paste your AI draft]
AI:  Pass 1 (fingerprints): removed "it's worth noting", "in today's world"…
     Pass 2 (readability): split 3 long sentences, restored subjects…
     Pass 3 (voice): [uses your voice-layer.md if present, else generic rules]
     → [rewritten draft] + 3-line change summary
```

## The one rule

**Never invent facts for you.** Delete, rewrite, reorder only — no new claims, numbers, or conclusions. The heavier the AI-ness, the less survives — because its "smoothness" is often just emptiness. This tool helps you see where it's hollow; the real substance you write yourself.

## Privacy

No network calls. Runs fully local inside your agent. Your speaking samples and drafts never leave your machine — the skill only tells your AI how to process them.

## About the author

*Leo ([@runes_leo](https://x.com/runes_leo)) — AI × Crypto independent builder. Trading on [Polymarket](https://polymarket.com/?via=runes-leo&r=runesleo&utm_source=github&utm_content=talk-human), building data and content pipelines with Claude Code and Codex.*

*[leolabs.me](https://leolabs.me) — writing · community · open-source tools · indie projects · all platforms.*

*[X Subscription](https://x.com/runes_leo/creator-subscriptions/subscribe) — paid content weekly, or just buy me a coffee 😁*

*Learn in public, Build in public.*

## License

MIT © Leo ([@runes_leo](https://x.com/runes_leo))
