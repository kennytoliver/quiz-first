# Quiz-First · quiz-first

**English** | [中文](README.md)

**Stop starting from page one. Let me quiz you first — then I'll know what to teach.**

---

Sound familiar?

You get curious about a new field. You save twenty tutorials, three ebooks, two podcasts.
You open chapter one, page one. Somewhere around chapter three, you stop.
Next time you come back, you start at chapter one, page one again.

It's not laziness. Nobody ever told you **which piece you were actually missing.**

---

## It works backwards: quiz first, teach second

Everyone else explains first. This one tests first.

Tell it what you want to learn, and it won't open a textbook —
it hands you **one real task you probably can't finish yet**, and watches where you stall.

Where you stall is where you should study. Not one step further, not one step back.

> **You:** I want to learn data analysis.
>
> **It:** "You have a single 200k-row order table. Your boss wants to know by tomorrow why repurchases dropped. How do you investigate?"
>
> Where you stop is exactly what you're missing. It maps your level, lists the gaps,
> and picks today's unit — instead of page one of a textbook.

---

## "Looked at it" is not "learned it"

| You think | Reality |
|---|---|
| I understood it | You freeze the moment you explain it |
| I remember it | It's gone in three days |
| I finished it | You have nothing to show |

**Understanding doesn't count. Explaining it, doing it, spotting the mistake — that counts.**

---

## Three hard rules

**① Diagnose first.**
Prescribing without an exam makes a bad doctor. Planning a course without a diagnosis makes a useless course.

**② Most leveraged content first.**
Motivation decays. Don't burn it on "Chapter 1: What is X".

**③ Draw the map yourself.**
A map an AI drew for you doesn't live in your head. It gives you the blank frames and the rules — you hold the pen.

---

## One run through the loop, and you'll have

```
① Diagnose → ② Custom path → ③ Quiz & practice → ④ Consolidate → back to ①
```

- **Where you stand** — a 5-level ladder with "you are here" marked
- **What to learn next** — a gap list plus a schedule led by the highest-value content
- **Real mastery** — one question at a time; answer right but can't say why, and it doesn't count
- **Something to show** — a knowledge map you drew, a one-page cheatsheet, a portfolio-ready mini-project

---

## What makes it different

- Others generate the mind map for you. This one **makes you draw it** — the pen in your own hand is the whole point.
- Others answer in walls of text. This one **answers in diagrams** — ladders, contrast axes, printable blank frames.
- Others assume you're motivated. This one **keeps you moving** — a small artifact each round, stamp-style progress.
- Others leave you still not getting the industry. This one **has you read it daily** — and say it back out loud.

---

## Quick start

Send this to your AI:

> I want to learn 【industry / skill】. **Don't teach me anything yet** — first give me one real task question I probably can't finish. After I answer, judge what level I'm at and what I'm missing: if the level is clear, stop and wait for me; if not, ask one more.

If you can't answer, write "I don't know" — that's a valid answer, and it costs you nothing.

---

## Install

Drop this directory into the skills folder of whatever agent you use — **name the folder `quiz-first`** so it matches the `name` in `SKILL.md`:

```bash
# common locations
~/.claude/skills/quiz-first/
~/.codex/skills/quiz-first/
~/.workbuddy/skills/quiz-first/

# or per-project
<project>/.workbuddy/skills/quiz-first/
```

Anything that supports `SKILL.md` + YAML frontmatter works. Once installed, just say "I want to learn X" — no commands to memorize.

<details>
<summary>Layout</summary>

```
quiz-first/
├── SKILL.md
├── references/
│   ├── method-core.md        # loop, mastery criteria, exit criteria
│   ├── output-patterns.md    # diagram library, stamps, reply format
│   ├── prompts.md            # 15 prompt templates
│   ├── daily-read-aloud.md   # daily industry read-aloud (optional)
│   ├── dual-agent.md         # coach / Q&A roles
│   └── source-material.md    # learning from a given source
└── assets/
    ├── learning-state-card.md
    ├── blank-map-frames.md
    └── one-page-cheatsheet.md
```
</details>

---

MIT · kennytoliver

The method started from two public Chinese-language videos (one on six ways to learn anything faster with AI, one by a teacher of 14 years on how people actually learn). This repo is a structured rewrite and expansion — not a sentence-by-sentence transcription, and no claim of original authorship over the core methods.

Beyond those videos, this repo adds: confidence ratings and review scheduling, per-unit rubrics, the opening recall question, multi-topic scheduling, old-unit mixing, the source-material mode, light mode, exit criteria, and anti-hallucination rules — plus the whole output-shape spec (seven diagram types, three-way split, printable blank frames, reply format). **The daily read-aloud and the coach / researcher split do not appear in either video at all**; both are independent additions.
