# Generating a Personal Context Portfolio from Existing Files

Build your AI operating manual from documents you already have.

---

## What You Need

1. An AI coding assistant (Claude Code, Cursor, etc.)
2. Documents about you and your business — bios, transcripts, business plans, slide decks, meeting notes, whatever you've got
3. The personal-context-portfolio repo: https://github.com/nlwhittemore/personal-context-portfolio

## Setup

### 1. Clone the portfolio repo into your project

```
bring this repo into this project: https://github.com/nlwhittemore/personal-context-portfolio.git
```

This gives the AI the templates, examples, and structure it needs to understand what it's building.

### 2. Add your source material folders to the workspace

Point the AI at the folders where your existing documents live. These can be anywhere — Google Drive, local folders, transcripts, whatever. Examples:

- A folder with your company overview, bios, and business docs
- A folder with meeting or call transcripts
- A Google Drive folder with project files

The AI will catalog everything and figure out what's useful.

### 3. Create a plan

Reference the portfolio repo, your source folders, and ask for a plan. Keep it simple:

```
personal-context-portfolio/ defines a set of example files that I would like
you to create by reverse engineering what you learn about me from the files
in [PATH TO YOUR DOCS], the call transcripts in [PATH TO TRANSCRIPTS] and
the documents already in [PATH TO MORE DOCS].

Put those new files into [OUTPUT FOLDER].

Do your best to create the files and also provide a list of outstanding
questions to complete them.

First create ADR(s) to plan this project (don't implement yet). Put planning
files in [PLANNING FOLDER].
```

The AI will:
- Read the portfolio templates and examples to understand the 10-file structure
- Catalog all your source materials
- Map which sources feed which files
- Assess confidence levels (what it can draft vs. what needs your input)
- Produce planning docs before touching anything

### 4. Implement

Once the plan looks right, tell it to go:

```
spawn swarm, implement completely, continue until complete.
```

The AI will generate all 10 portfolio files in parallel, pulling from your source materials and marking gaps with `[NEEDS INPUT]` where it doesn't have enough information.

### 5. Fill the gaps

Review the `outstanding-questions.md` file it produces. Answer the questions — especially the ones marked `[CRITICAL]`. The highest-impact gaps are usually in:

- **Goals & priorities** — tradeoffs and what you're NOT doing
- **Communication style** — how you write, what you hate in AI output
- **Preferences & constraints** — schedule, hard rules, frustrations

A 30-45 minute conversation fills most of them.

---

## What You Get

10 markdown files that serve as your operating manual for any AI system:

| File | What It Captures |
|------|-----------------|
| `identity.md` | Who you are, what you do, what you're known for |
| `role-and-responsibilities.md` | What your weeks look like operationally |
| `current-projects.md` | Active workstreams with status and collaborators |
| `goals-and-priorities.md` | What you're optimizing for and what you're NOT doing |
| `team-and-relationships.md` | Key people and how you work with them |
| `tools-and-systems.md` | Your tech stack and data sources |
| `communication-style.md` | How you write, speak, and what you hate in AI output |
| `preferences-and-constraints.md` | Hard rules, schedule, strong opinions |
| `domain-knowledge.md` | Your expertise, terminology, frameworks |
| `decision-log.md` | How you decide, with real examples |
| `outstanding-questions.md` | Gaps that need your direct input |

Wire them into your AI tools using the guides in `personal-context-portfolio/wiring/`.

---

## Tips

- **Start with what you have.** A bio and a few transcripts is enough.
- **Gaps are expected.** A portfolio with [NEEDS INPUT] markers is still 10x more useful than no portfolio.
- **The reaction pass is faster than answering questions.** Read each file and say what's wrong — that's quicker than answering abstract questions from scratch.
- **Update quarterly** or after any major change.
