# Quiz-First

*A skill for your agent: it quizzes you first, then teaches only the part you're missing.*

---

You printed a 30-day study plan and taped it to the wall. The first three days got a tick. The fourth box is still blank.

You signed up for a course, got to lecture five, and never opened that tab again.

There's a folder in your bookmarks called "to learn". Forty-odd links. The oldest one is three years old.

Same script every time: the first two days you're on fire — notes, a schedule, telling people "I'm learning X right now". Day four it gets hard. Day five you say "I'll catch up tomorrow". By day seven you've stopped mentioning it.

By the third round of this, you start to wonder something uncomfortable: maybe I'm just not the kind of person who can learn things.

---

## It isn't your fault

The reason is rarely laziness, and rarely a lack of time.

It's that you break down at the same point every time, and **you don't know where that point is**.

So you start at the easiest place available: open the tutorial, read two lines, "I know this", feel a bit better. You make it to chapter three, hit the first thing you genuinely don't understand, and stop.

Next time you're back at page one — because that's the only place that makes you feel like you're learning.

---

The tutorials aren't wrong. They just assume you're starting from zero, because whoever wrote them can't know what you already have.

So three things happen at once:

**What you already know gets taught to you again.** Three weeks pass; you've reviewed a pile of material you had anyway.

**The part that actually blocks you never gets touched.** It's in chapter seven, and you never reach chapter seven.

**Your drive gets spent where it's least needed.** Motivation is finite and it's highest at the start — which is exactly where the easiest material sits.

---

## So it runs backwards

The first thing it does is not teach.

It hands you **a task you almost certainly can't finish right now**.

Not finishing is normal — the task was built to be unfinishable. Where you stall is where you actually are.

Study starts there. Not one step earlier, not one step later.

The loop is four steps: **diagnose → set a path → quiz and practise → consolidate**. Then back to the first one to recalibrate.

That last step, consolidate, means drawing what you learned into a map and squashing it onto one page. Not revision — getting it out of your head and into something you can look at.

---

## A concrete example: learning AI

You want to learn AI. You search "how to get into AI" and the answers are all the same:

Learn Python, then linear algebra and probability, then machine learning, then deep learning.

You start with the first one. Python goes fine for two weeks. Linear algebra stops you at eigenvalues.

Three months later you're still at the gate of step one, starting to think you're not built for this.

The problem isn't effort. **"Learn AI" is at least three different people:**

| What you want to do | What to learn first | What you can skip entirely |
|---|---|---|
| Build products on top of AI, call APIs | Prompting, API calls, cost per request | Backpropagation, gradient derivations |
| Train your own models | Data cleaning, what a loss function is | Frontend, deployment |
| Work in data labelling / QA | Annotation specs, acceptance criteria, edge cases | Not a single line of code |

What those three people study over the next three months barely overlaps.

Follow the "Python → maths → machine learning" route and all three stop at the same place: the maths.

It doesn't open that way. **It asks one question first: what do you want to do with AI?**

Then it gives you a real task from that direction:

- **Data QA** → five reviews, five labels an intern already applied. Spot which ones are wrong, and why.
- **Building on APIs** → one concrete requirement. Write the first prompt that actually runs.
- **Training a model** → a small batch of dirty data. Say which rows can't go into the training set.

Where you stall is where you start.

---

## How is this different from just asking an AI

| The usual way | This skill |
|---|---|
| You say what you want to learn, it hands you a curriculum | It gives you a task first, then builds the curriculum from where you stalled |
| The curriculum goes basics → advanced | The highest-leverage part moves to the front; the rest fills gaps |
| Saying "got it" counts as learned | You rate your confidence (4 certain / 3 mostly / 2 guessed / 1 blind); a right answer with no confidence schedules a retest |
| It draws the mind map for you | It gives blank frames and rules; you draw |
| You end up with a chat log | You end up with a folder full of files |

---

## What you have after one loop

Not a chat log. A folder:

```
learning-journal/
├── state-card.md     # where you are, what's missing, what's due for retest
├── maps/             # knowledge maps you drew by hand
├── cheatsheets/      # one-page sheets
└── outputs/          # the small artifact from each round
```

| Artifact | What's inside |
|---|---|
| **Level card** | Which rung you're on, and your initial gaps |
| **Gap list** | What exactly is missing and when it gets retested — not "practise more" |
| **Knowledge map** | Drawn by you; it only flags missing nodes, wrong links, misplaced levels |
| **One-page cheatsheet** | Six columns you can re-read five minutes before an interview |

The level card, the ladder and the schedule don't live in separate files — they sit inside `state-card.md`, so there's only one place to look.

For hands-on skills (instruments, sports, operating things), the map and the cheatsheet become a movement breakdown and a recording.

---

## Install

**What you need**: an agent that reads `SKILL.md` (Claude Code, Codex, WorkBuddy, Cursor and similar). No dependencies, no account. The core loop runs offline; only the optional daily read-aloud needs a connection.

**Step 1 — get the files.**

```bash
git clone https://github.com/kennytoliver/quiz-first.git
```

No git? Use Code → Download ZIP. The unzipped folder is called `quiz-first-main` — **rename it to `quiz-first`**, or the command below won't match.

**Step 2 — put it in your agent's skills folder.** Use `quiz-first` as the folder name (what actually loads is the `name` field inside `SKILL.md`; a different folder name still works, it's just harder to find later).

| Agent | Default location |
|---|---|
| Claude Code | `~/.claude/skills/quiz-first/` |
| Codex | `~/.codex/skills/` or `~/.config/codex/skills/` (varies by version) |
| WorkBuddy | `~/.workbuddy/skills/quiz-first/` |
| Others | Usually `~/.<your-agent>/skills/` — check the docs if unsure |

```bash
# Claude Code, for example
mv quiz-first ~/.claude/skills/
```

**Step 3 — confirm it landed.**

```bash
ls ~/.claude/skills/quiz-first/SKILL.md
```

If that file shows up, you're good.

**Step 4 — start a new session.** Skills are indexed when a session starts, so **an existing session won't pick it up**. Open a new one.

**Check that it loaded**: say "I want to learn X". The first reply should ask which direction you want, then hand you **a task**. If it starts explaining concepts or gives you a curriculum, it didn't load — check that `SKILL.md` sits at the folder root.

More detail: [GUIDE.md](GUIDE.md) *(Chinese)*

---

[MIT](LICENSE)
