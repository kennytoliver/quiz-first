# Quiz-First · quiz-first

**English** | [中文](README.md)

A skill for teaching yourself an unfamiliar field with an AI: start with a diagnosis, end with something you can show.

Built for career changers, people filling a knowledge gap, and anyone learning a hands-on skill over several weeks.

**The core move is inverted: test first, teach second.** Planning a course without a diagnosis is prescribing without an exam.

---

## What it solves

| Where it breaks | What it looks like | How this handles it |
|---|---|---|
| **You don't know what you're missing** | Start at chapter one, stop at chapter three, restart at chapter one | One real task you probably can't finish, placed by how far you get — not by climbing up from the basics |
| **Wrong order** | Your sharpest attention goes to the least useful material | Highest-leverage content first; levels you already have are greyed out; hard dependencies get patched first |
| **"Looked at it" passes for learning** | It all makes sense until you open your mouth | One question at a time, a confidence rating per answer, review dates set by performance |
| **Nothing to show afterwards** | Three weeks later you have a folder of bookmarks | A small artifact every round, front-loaded |

---

## How it runs

```
① Diagnose → ② Custom path → ③ Quiz & practice → ④ Consolidate → back to ①
```

Three rules that are not optional:

1. **Diagnose before teaching.** Nothing gets taught before the diagnosis is done.
2. **Most leveraged content first.** Difficulty climbs while drive falls; the two curves run opposite. This does not mean skipping foundations — when the target has a hard dependency (notation, base grammar, a working runtime), the minimum slice gets patched first.
3. **You draw the map.** The AI supplies rules, a node list and blank frames. A map it draws for you does not grow in your head.

**Two kinds of goals, different endings:**

| | Knowledge | Skill |
|---|---|---|
| Typical | Reading a spec, understanding an industry, papers, career change | A song on guitar, driving, typing, speaking a language |
| Step ④ | Knowledge map + one-page cheatsheet | Movement breakdown + a recording you review |
| Review | 1 → 2 → 4 → 8 days, then retired as solid | Never more than 3 days apart, never retired |

Most goals are both (learning to program means understanding concepts *and* writing code). Do both.

---

## What you walk away with

Everything lands in a `learning-journal/` folder, not scattered across a chat log:

```
learning-journal/
├── state-card.md     # where you are, gap list with review dates, stamp log
├── maps/             # photos of maps you drew + the AI's review notes
├── cheatsheets/      # one-page cheatsheets
└── outputs/          # small artifacts: judgement tables, derivations, recordings
```

The four core deliverables:

| Deliverable | Contents |
|---|---|
| **Level card** | Which of the five rungs you're on, and your initial gaps |
| **Gap list** | What exactly is missing and when it gets retested — not "practise more" |
| **Knowledge map** | Drawn by you; the AI only checks for missing nodes, wrong links, misplaced levels |
| **One-page cheatsheet** | Six-column compression you can re-light your memory with five minutes before an interview |

For skill-type goals the last two become a movement breakdown and a recording.

---

## Usage

Once installed, just say what you want to learn, or paste this:

> I want to learn 【field / skill】. **Don't teach me anything yet** — first give me one real task question I probably can't finish. After I answer, judge what level I'm at and what I'm missing: if the level is clear, stop and wait for me; if not, ask one more.

If you can't answer, write "I don't know" — that's a valid answer and it costs you nothing.

`references/prompts.md` holds 15 ready-made templates covering diagnosis, path building, quizzing, retests, mapping, cheatsheets, resource filtering and learning from a given source.

---

## Install

Drop the whole directory into your agent's skills folder. **Name the folder `quiz-first`** so it matches the `name` field in `SKILL.md`:

```bash
<your-skills-dir>/quiz-first/
```

Anything that reads `SKILL.md` + YAML frontmatter will load it — Claude Code, Codex, WorkBuddy, and custom agents alike. After that, just say "I want to learn X".

<details>
<summary>Layout</summary>

```
quiz-first/
├── SKILL.md                      # rules, loop, scoring, execution flow
├── references/
│   ├── method-core.md            # why each rule exists, limits, exit criteria, common misuse
│   ├── output-patterns.md        # seven diagram types, reply format, printable frames, archive layout
│   ├── prompts.md                # 15 prompt templates
│   ├── daily-read-aloud.md       # daily reading and speaking drill (optional)
│   ├── dual-agent.md             # coach / researcher split
│   └── source-material.md        # learning from a given textbook, spec or link
└── assets/
    ├── learning-state-card.md    # state card + gap list + stamp log
    ├── blank-map-frames.md       # 5 printable blank frames
    └── one-page-cheatsheet.md    # cheatsheet template
```
</details>

---

## Scope

**Fits**: career-change prep, filling a subject gap, getting started on a hands-on skill, goals that run over several weeks.

**Doesn't fit**: asking what a single term means, wanting one fact, asking for a paragraph to be rewritten. Those get a direct answer — `SKILL.md` states this boundary explicitly.

**Optional module**: the daily read-aloud. Read 300–500 words from the field out loud three times, retell it with the source closed, retell again from 3–5 keywords, then play the recording back. Ten to fifteen minutes end to end. It trains reading and speaking at once, but it eats a whole block, so it is off by default and never forced.

---

## Provenance

The method started from two public Chinese-language videos — one on six ways to learn anything faster with AI, one by a teacher of 14 years on how people actually learn. This repo is a structured rewrite and expansion, not a sentence-by-sentence transcription, and makes no claim of original authorship over the core methods.

Beyond those videos, this repo adds: confidence ratings and review scheduling, per-unit rubrics, the opening recall question, multi-topic scheduling, old-unit mixing, the source-material mode, light mode, exit criteria, and anti-hallucination rules — plus the whole output-shape spec (seven diagram types, three-way split, printable blank frames, reply format). **The daily read-aloud and the coach / researcher split appear in neither video**; both are independent additions.

---

MIT · kennytoliver
