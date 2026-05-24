---
name: document-polish
description: >
  Polish and improve written documents — articles, essays, newsletters, blog posts, reports,
  technical write-ups — focusing on language clarity, structure, and visual hierarchy.
  Use this skill whenever the user asks to improve, edit, rewrite, or restructure a document,
  or when they paste a draft and ask how to make it better, cleaner, or more engaging.
  Also trigger when the user asks to "clean up" writing, "make it more readable", or
  "give it more structure". Applies the Refactoring newsletter style: tight prose,
  clear agenda blocks, numbered + emoji section headers, and punchy takeaway sections.
---

# Document Polish Skill

A skill for turning rough drafts into crisp, well-structured, high-impact documents.
Inspired by the editorial style of the Refactoring newsletter (refactoring.fm).

---

## Core Philosophy

The goal is documents that are:

- **Easy to scan** — a reader should understand the shape of the piece in 10 seconds
- **Easy to read** — short paragraphs, no fluff, direct language
- **Rewarding to finish** — each section earns the next; the ending pays off

Do not add length. Cut ruthlessly. Every sentence that doesn't move the reader forward should be removed.

---

## Step 1 — Understand the Document

Before touching anything, identify:

1. **Type**: newsletter, technical doc, report, essay, pitch, how-to guide?
2. **Audience**: engineers, executives, general readers, domain experts?
3. **Goal**: inform, persuade, teach, summarize?
4. **Length target**: keep it or trim it?

If any of these are unclear, ask the user one question before proceeding.

---

## Step 2 — Apply the Style System

### 2.1 The Agenda Block (opening)

Every document longer than ~400 words benefits from an agenda block right after the intro.
Format it as a numbered list where each item follows this pattern:

```
1. [emoji] **[Short Title]** — [one-line description of what this section covers].
2. [emoji] **[Short Title]** — [one-line description].
```

Rules:

- Use a **different emoji per item** — pick one that matches the topic (not just decorative)
- The bold title should be 2–5 words
- The description after the em dash (`—`) should be one concise clause, not a full sentence
- End the agenda with a transition line: `Let's dive in!` or `Here's what we'll cover:` etc.

Example:

```
1. 📈 **The problem with 10x engineers** — why this concept is slippery and problematic.
2. 🧘 **In praise of "normal" engineers** — the best engineering orgs enable 1x engineers to do great work.
3. 🎽 **Turning normal teams into 10x teams** — a practical playbook for high-performing orgs.
4. 🏆 **Hiring for strengths, not lack of weaknesses** — how to focus on what people do well.
```

---

### 2.2 Section Headers

Use this format for every major section:

```
## [number)] [emoji] [Descriptive title as a full phrase or sentence]
```

Rules:

- **Number** each section sequentially (1), 2), 3)…) — readers like knowing where they are
- **One emoji** — relevant, not random; avoid repeating the same emoji across headers
- **Title** should be a complete, meaningful phrase — not a generic label like "Section 3"
- For subsections, drop the number but keep the emoji and descriptive title

Examples of good headers:

```
## 1) 🚚 Shrink the interval between when you write code and when it goes live
## 2) ↩️ Make it fast and easy to roll back mistakes
## 3) ✅ Make it easy to do the right thing — and hard to do the wrong thing
```

Examples of bad headers (avoid):

```
## Section 1: Deployments       ← too generic
## Fast deployments 🚀           ← emoji at the end, no number
## 1. Introduction               ← the word "Introduction" adds nothing
```

---

### 2.3 The Takeaway Block (closing)

Every document should end with a tight summary block. Format:

```
## 📌 Bottom line

- [emoji] **[Bold key idea]** — [one-sentence explanation].
- [emoji] **[Bold key idea]** — [one-sentence explanation].
```

Rules:

- 4–7 bullet points, no more
- Each bullet restates a key insight in fresh language — don't just copy-paste from the body
- Bold text is the "headline"; the clause after `—` is the "context"
- Pick a closing emoji that signals "summary" or "conclusion": 📌 🎯 ✅ 🔑

---

### 2.4 Inline Formatting

Use **bold** to highlight key terms or pivotal claims — sparingly. A paragraph should have at most 1–2 bold phrases. If everything is bold, nothing is.

Use _italics_ for:

- Emphasis on a single word within a sentence (_this_ is the important part)
- Titles of books, products, or named concepts (_The 10x Engineer_ myth)
- Deliberate rhetorical pauses (_So what does this mean in practice?_)

Avoid underline entirely. Avoid ALL CAPS except in headers or diagrams.

---

## Step 3 — Language Rules

### Cut these patterns

| Pattern                           | Why                      | Fix                                                   |
| --------------------------------- | ------------------------ | ----------------------------------------------------- |
| "In this article, I will..."      | Meta-commentary          | Just start                                            |
| "It is important to note that..." | Filler                   | Delete, make the point directly                       |
| "As mentioned above..."           | Weak callback            | Use a short transition instead                        |
| "In conclusion..."                | Too formal               | Use a section header instead                          |
| Passive voice overuse             | Dilutes agency           | "Teams own software" not "Software is owned by teams" |
| Hedging chains                    | "might possibly perhaps" | Pick one hedge or drop it                             |

### Keep sentences tight

- Prefer short sentences for impact. Save long ones for nuance and buildup.
- One idea per paragraph. Two at most.
- End paragraphs with either a strong conclusion or a line that pulls the reader forward.

### Transitions between sections

Add a brief bridge before a new section header, e.g.:

- `Which leads to my next point 👇`
- `Let's look at both:`
- `Here's where it gets interesting.`
- `On to the second problem.`

These one-liners keep the reading flow alive between sections.

### Tone

- Conversational but confident. Not casual, not corporate.
- First person is fine and often better: "I think", "I've found", "We believe"
- Don't hedge your thesis. State it, then support it.

---

## Step 4 — Document Structure Template

For a typical long-form article or essay, the full structure should be:

```
[Short punchy intro — 1-3 paragraphs, no header needed]
[Hook: surprising claim, personal story, or strong assertion]
[Frame: what problem this addresses and why it matters]
[Transition: "Here's the agenda:" or "Let's break this down."]

[Agenda block — numbered list with emoji + bold title + em dash + description]

"Let's dive in!"

## 1) [emoji] [Section title]
[Body — 2-5 paragraphs, mix of prose and occasional bullets]

## 2) [emoji] [Section title]
...

## [emoji] Bottom line / Key takeaways
[Bullet list: emoji + bold + em dash + one-liner]
```

---

## Step 5 — Output Format

When returning the improved document:

1. **Return the full document** — don't just annotate or comment
2. **Preserve the author's voice** — improve, don't replace
3. If you made significant structural changes, add a brief note below the document:
   `> 📝 *Changes made: [2-3 bullet list of major edits]*`
4. If the user asked for specific improvements only (e.g., "just fix the headers"), scope your changes accordingly and say so

---

## Quick Reference — Emoji Suggestions by Topic

| Topic                | Good emoji picks |
| -------------------- | ---------------- |
| Speed / shipping     | 🚚 🚀 ⚡ 🏎️      |
| Problems / warnings  | 📈 ⚠️ 🚨 ❌      |
| People / teams       | 🧘 🎽 👥 🤝      |
| Tools / systems      | 🔧 🛠 ⚙️ 🔩      |
| Learning / growth    | 🌱 📖 🧠 🎓      |
| Takeaways / summary  | 📌 🎯 ✅ 🔑      |
| Money / cost         | 💰 💸 📊         |
| Search / observation | 🔍 🔬 👀         |
| Culture / values     | 🤗 🌈 🏆         |
| Tech / code          | 💻 🖥 👾 🧵      |
| Predictions / future | 🔮 🧭 🗺         |
