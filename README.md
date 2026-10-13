# Inquiry Tutor

**An AI skill that teaches you a new field by asking — not by telling.**

*[中文说明 →](README.zh-CN.md)*

---

## The problem

The hard part of entering a new field isn't finding material. It's this:

> **You read it, you nod along, and when you close the book you remember nothing.**

You weren't learning. You were *looking*.

Inquiry Tutor flips it: instead of explaining things to you, it **asks you questions until you can explain them yourself.**

---

## How it works

```
        AI gives context (a scenario, an example, a piece of material)
                              ↓
                    AI asks ONE question
                              ↓
                        You answer
                              ↓
        ┌──────────────┬──────────────┬──────────────┐
        │  Correct  →  │  Wrong  →    │  Stuck  →    │
        │  confirm,   │  rephrase    │  step back,  │
        │  name it,   │  the question,│  add more   │
        │  speed up   │  don't reveal │  scaffolding │
        └──────────────┴──────────────┴──────────────┘
                              ↓
                    … repeat a few rounds …
                              ↓
        Notes generated → saved to a folder you choose
```

**Two rules the tutor never breaks:**

1. **One question at a time.** Never a list of them.
2. **It never hands you the answer.** When you're wrong, it asks a simpler question instead.

---

## Install

**Claude Code**

```bash
git clone https://github.com/brave-grow9/inquiry-tutor.git
cp -r inquiry-tutor ~/.claude/skills/
```

**Codex CLI / Cursor / Gemini CLI / Copilot** (Agent Skills open standard)

```bash
git clone https://github.com/brave-grow9/inquiry-tutor.git
cp -r inquiry-tutor ~/.agents/skills/
```

> One copy in `~/.agents/skills/` covers Codex, Cursor, Gemini CLI, and Copilot.

**Manual:** download the ZIP and drop the `inquiry-tutor` folder into one of the paths above.

---

## Use it

Just say what you want to learn:

```
Teach me behavioral economics from scratch.
```

```
带我学一点行为经济学，从零开始。
```

The skill takes over from there — it will ask you a few setup questions first (what exactly you want, why, your current level, one session or several, where to save notes, whether you have material to work from), then draw you a map of the field and start the question loop.

---

## Why it works

Three reasons, all from real use:

**1. It forces you to expose what you only *think* you understand.**
Reading makes you nod. Being asked makes you find out. Those are different things.

**2. When you're wrong, you find out immediately — and you find out *why*.**
The tutor doesn't say "wrong". It asks a smaller question, and you walk into the error yourself. Errors you walk into, you don't forget.

**3. You can ask as many times as you need.**
Rephrase it, ask it again, go around. No one's time is being used up.

There's one more thing it does that most study tools don't: **it writes down where you got stuck.**

---

## What gets saved

After each round, the skill writes a note containing four parts:

| | |
|---|---|
| **1. What you learned** | The actual knowledge |
| **2. How you got there** | Your reasoning path — **your own words, unedited** |
| **3. Where you got stuck** | The sticking point, and why it was hard |
| **4. Self-check questions** | So you can test yourself later |

Parts 2 and 3 are the point. Any textbook has part 1. Only you have parts 2 and 3.

Notes also carry your **progress**, so you can hand them back later and pick up where you left off.

---

## Works with your own material

You can point it at a book, a paper, a document, or a folder. Three modes:

| Mode | What leads | What the material does |
|---|---|---|
| **A** | The tutor | — |
| **B** | **Your material** | The whole session follows it |
| **C** | The tutor | Used as a reference, pulled in when relevant |

**Material is not a cage.** If your material doesn't cover something, the tutor fills the gap — *and tells you it's doing so*. If the material and the tutor disagree, you get both sides, not a smoothed-over answer.

---

## Safety

**This skill contains no scripts and makes no network requests.**

It is a set of plain-text instructions. It does not execute code, does not read files you didn't point it at, and does not send anything anywhere. You can read every line of it before installing.

---

## When *not* to use it

This is built for *learning a field*, not for *answering a question*.

- You just want a direct answer → ask directly
- You want a summary → ask for a summary
- You said "stop asking, just explain" → it will

---

## License

MIT — see [LICENSE](LICENSE).
