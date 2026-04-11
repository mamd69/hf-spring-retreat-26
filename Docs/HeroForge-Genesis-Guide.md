# HeroForge Genesis: The Complete Guide

**From idea to operating business — a step-by-step guide for business leaders.**

---

## How to Use This Guide

This guide is designed to be followed in order, from start to finish. Each section builds on the one before it. You will set up your tools, teach the AI about yourself and your business, build a searchable knowledge base, and then use that foundation to analyze, plan, and build.

Every prompt in this guide is **copy-paste ready**. When you see a block like this:

```
this is a prompt you paste into Claude Code
```

Copy it exactly, replacing anything in `[BRACKETS]` with your own information.

**What you need before you start:**

- A computer with internet access
- An email address
- A credit card (for Claude Code authentication)
- About 30 minutes for initial setup
- Your business documents — bios, transcripts, financials, slide decks, meeting notes, whatever you have

---

## Table of Contents

1. [What Is Genesis?](#1-what-is-genesis)
2. [Preparing Your Files](#2-preparing-your-files)
3. [Setting Up Your Tools](#3-setting-up-your-tools)
4. [Building Your Personal Context Portfolio](#4-building-your-personal-context-portfolio)
5. [Building Your Knowledge Base](#5-building-your-knowledge-base)
6. [Elevating Your Knowledge Base to World-Class](#6-elevating-your-knowledge-base-to-world-class)
7. [Visualizing and Verifying Your Knowledge Base](#7-visualizing-and-verifying-your-knowledge-base)
8. [The Genesis Methodology: Analyze, Plan, Build](#8-the-genesis-methodology-analyze-plan-build)
9. [Addendum: Helpful Repos and Tools](#9-addendum-helpful-repos-and-tools)

---

## 1. What Is Genesis?

Genesis is an **operating system for your business**. It is a platform that takes your business from its current state to an optimized future state by combining the most powerful AI models with a proprietary knowledge engine and coordinated teams of AI agents.

It is not a chatbot. It is not a single tool. Genesis **analyzes** your business, **plans** improvements, **builds** the solutions, **deploys** them, and then **monitors and self-improves** over time.

### What makes it different

Most AI tools today are static — you ask a question, you get an answer, the AI forgets you existed. Genesis is built on a three-layer knowledge engine:

| Layer | What It Does | Plain-English Analogy |
|-------|-------------|----------------------|
| **Vector Database** | Finds information by meaning, not just keywords. Ask about "PTO policy" and it finds results about "vacation days" and "time off." | A librarian who understands what you mean, not just what you said. |
| **Graph Database** | Understands relationships between things — org charts, coding rules, regulatory hierarchies. | A map that shows how everything connects to everything else. |
| **Graph Neural Network** | Learns and improves from every interaction, autonomously optimizing toward goals you set. | An employee who gets better at their job every day without being told how. |

That third layer — the Graph Neural Network — is the key differentiator. The AI models themselves (Claude, GPT) do not learn from your interactions. They are born smart but have no memory. The GNN actually learns. Set a goal like "improve lead conversion rate" and it will analyze every interaction and optimize toward that goal over time, without human intervention.

### What Genesis produces

Genesis is not theoretical. Here is what it has built for real businesses:

- **Nexadental** (orthodontics): A complete SaaS platform with practice assessment reports, operational dashboards pulling data nightly from billing systems, AI phone agents that answer calls 24/7 and follow up on leads, and a conversational AI assistant that discusses findings and recommendations.
- **Good Samaritan Hospital** (medical coding): An AI coding optimization system that combines clinical reasoning with 600,000+ ICD codes and all CMS rules, identifying 10-15% revenue improvement at a $90 million hospital.
- **Vermont Real Estate**: Financial models, investor decks, targeted buyer outreach with personalized emails to the 50 most ideal buyers — each generated automatically.

### The four-step methodology

Everything Genesis does follows four steps:

1. **Import and Digitize** — Upload your business documents, data, and institutional knowledge.
2. **Research and Augment** — The AI researches industry best practices, competitors, and benchmarks, then adds that knowledge to your base.
3. **Analyze and Plan** — The AI compares your current state against best practices, identifies gaps, runs simulations, and produces prioritized roadmaps.
4. **Build and Deploy** — A coordinated team of AI agents builds the solutions — software, automations, dashboards, AI assistants — and deploys them with ongoing monitoring.

This guide walks you through every step.

### Two starting points: Greenfield vs. Brownfield

Before you begin, it helps to know which type of Genesis project you are starting:

| | Greenfield | Brownfield |
|---|---|---|
| **What it means** | A new business or new idea. You are starting from scratch with little or no existing data. | An existing business with years of accumulated documents, transcripts, financials, meeting notes, and institutional knowledge. |
| **What you have** | A seed of an idea, maybe a business plan or some early notes. | A mountain of context — files on your computer, in Google Drive, in your EMR, in your head. |
| **Best setup** | A GitHub Codespace (runs in your browser, nothing to install). | VS Code on your desktop (your files are already on your computer — no uploading needed). |
| **Where to start** | Jump straight to setup, then let the AI help you research and build from the ground up. | Start by organizing your files, then point the AI at them locally. |

Most business leaders doing Genesis have an existing business — that is a **brownfield** project. This guide covers both paths.

---

## 2. Preparing Your Files

If you are doing a **greenfield** project (starting from scratch), skip ahead to [Section 3: Setting Up Your Tools](#3-setting-up-your-tools).

If you have an existing business with files, take 30-60 minutes to prepare before you start. This step pays for itself many times over.

### Make a backup first

Before pointing AI at your business files, make a backup of your originals. Copy them to an external drive, Google Drive, or another safe location. The AI will not delete your files, but having a backup is good practice before any reorganization.

### Organize by type

Group your files into folders by category. Don't overthink it — the folder names become automatic categories in your knowledge base later. For example:

```
Business Files/
  Transcripts/        — call recordings, meeting notes
  Financial/          — P&L, tax docs, QuickBooks exports
  Marketing/          — slide decks, brochures, website copy
  Operations/         — SOPs, employee handbooks, policies
  Legal/              — contracts, agreements, compliance docs
```

### Let the AI help you reorganize

If your files are a mess, that is fine. One of the first things you can do is point the AI at a folder and ask it to propose an organization plan:

```
these are all of my business files. Analyze this and help me create a plan
to reorganize this. Don't implement — write the plan as a markdown document.
```

The AI will catalog everything, identify file types, and propose a logical structure. Review the plan, adjust it, then tell the AI to implement it.

### You don't always need copies

If you are only feeding files into the knowledge base (not modifying them), you do not need to copy them into your project. When working locally with VS Code, you can link to your original files instead of duplicating them. This is covered in the next section under "Option B."

---

## 3. Setting Up Your Tools

You need four things: a GitHub account (where your project lives), a development environment (Codespace or VS Code on your desktop), Claude Code (your AI assistant), and Ruflo (the orchestration platform that coordinates multiple AI agents).

### Step 1: Create a GitHub account

GitHub is where your project files will live. It is free.

1. Open your web browser and go to **github.com**.
2. Click **Sign up** in the top-right corner.
3. Enter your email address, create a password, and choose a username.
4. Complete any verification puzzles GitHub presents.
5. Check your email for a verification code and enter it.

You now have a GitHub account.

> **A note on pricing:** GitHub's free tier is generous for basic usage. Consider a paid account later if you need larger machine types or more storage.

### Step 2: Create your first repository

A repository (or "repo") is a project folder that stores your files.

1. After logging in, click the **+** icon in the top-right corner and select **New repository**.
2. **Repository name:** Type a name for your project (example: `my-genesis-project`).
3. **Description:** Add a brief description like "My Genesis business project."
4. **Visibility:** Choose **Private** to keep your business data secure.
5. **Add README:** Check this box.
6. Click **Create repository**.

### Step 3: Open your development environment

Choose the option that fits your project:

#### Option A: Use a Codespace (best for greenfield projects)

A Codespace is a complete development environment that runs in your browser. No software to install.

1. From your repository's main page, click the green **Code** button.
2. Click the **Codespaces** tab.
3. Click **Create codespace on main**.
4. Wait 1-2 minutes for it to load. You will see an editor with three areas:
   - **Left sidebar:** Your project files.
   - **Center area:** Where you view and edit files.
   - **Bottom panel:** The terminal, where you type commands.

This is the easiest option if you are starting fresh or do not have many existing files.

#### Option B: Use VS Code on your desktop (best for brownfield projects)

If you have an existing business with lots of files on your computer, working locally is strongly preferred. Your files are already here — no uploading needed.

1. Download and install VS Code from **code.visualstudio.com** (if you do not already have it).
2. On GitHub, go to your repository's main page.
3. Click the green **Code** button.
4. Click the **Local** tab (not Codespaces).
5. Copy the HTTPS URL.
6. In VS Code, click **New Window**.
7. Click **Clone Git Repository** (you will see this on the welcome screen).
8. Paste the URL at the top and press Enter.
9. Select a location for the project. Tip: keep all your projects in one directory (e.g., `Projects/`), and consider syncing that directory to Google Drive for backup.
10. Click **Open** when prompted.

**Bringing in your existing business files:**

Once your project is open in VS Code, drag a folder from Finder (Mac) or File Explorer (Windows) into the VS Code sidebar. You will see two options:

| Option | What It Does | When to Use It |
|--------|-------------|----------------|
| **Add folder to workspace** | Links to the original files. No copy is made. | When you are only reading files to feed into your knowledge base. This is the most common choice. |
| **Copy** | Makes a duplicate inside your project. | When you plan to manipulate, reorganize, or transform the content. |

**Important: Keep your business files out of GitHub.** Your business files should stay on your local machine — you do not want them uploaded to your GitHub repository. After adding files to your workspace, tell Claude Code to exclude them:

```
add [FOLDER NAME] to the .gitignore so it is not uploaded to GitHub
```

For example, if you dragged in a folder called "Business Files":

```
add Business Files/ to the .gitignore so it is not uploaded to GitHub
```

This ensures your private business documents stay local while your project code syncs to GitHub normally.

> **Note on large directories:** VS Code may warn that there are too many active changes to track. This is expected and harmless — it just means Git will not try to sync those files, which is exactly what you want.

**Keep this window open.** You will use it for everything that follows.

### Step 4: Install Claude Code

Claude Code is your AI-powered coding assistant. It runs in the terminal.

> **Already installed Claude Code on your Mac?** If you previously installed Claude Code and created the `dsp`/`dsp-c` shortcuts, you do not need to do those steps again — they are global. Skip ahead to [Step 6: Install Ruflo](#step-6-install-ruflo), which needs to be set up for each new project.

1. In your Codespace or VS Code terminal, look at the bottom panel for the **Terminal** tab. If you do not see it, press `Ctrl + `` ` (the backtick key, below Escape).
2. Copy and paste this command into the terminal and press Enter:

```
curl -fsSL https://claude.ai/install.sh | bash
```

3. Wait 1-2 minutes for installation to complete.

### Step 5: Create shortcuts

These shortcuts save you from typing long commands every time.

**In a Codespace (Linux):** Copy and paste this into your terminal:

```
echo -e "alias dsp='claude --dangerously-skip-permissions'\nalias dsp-c='claude --dangerously-skip-permissions -c'" >> ~/.bashrc
```

Then run:

```
source ~/.bashrc
```

**On a Mac desktop:** Use these commands instead:

```
echo -e "alias dsp='claude --dangerously-skip-permissions'\nalias dsp-c='claude --dangerously-skip-permissions -c'" >> ~/.zshrc
```

Then run:

```
source ~/.zshrc
```

This creates two shortcuts:

| Shortcut | What It Does |
|----------|-------------|
| `dsp` | Starts Claude Code without asking permission for every action (required for agent workflows) |
| `dsp-c` | Same as above, but resumes your last session so it remembers what you were working on |

> **Security note:** The `--dangerously-skip-permissions` flag lets Claude run commands without asking you to approve each one. Only use this in environments you control, like your own Codespace.

### Step 6: Install Ruflo

Ruflo is the orchestration platform that lets you run multiple AI agents simultaneously.

Copy and paste this into your terminal:

```
curl -fsSL https://cdn.jsdelivr.net/gh/ruvnet/claude-flow@main/scripts/install.sh | bash -s -- --full
```

Wait 1-2 minutes for installation to complete.

### Step 7: Start Claude Code and authenticate

1. Type `dsp` in the terminal and press Enter.
2. Choose a display mode: enter `1` for dark or `2` for light.
3. Choose your account type:
   - Enter `1` if you have a **Claude Max** account ($100 or $200/month)
   - Enter `2` if you have a **Pro** account ($20/month) with API billing enabled
4. A link will appear. Click it (or copy it into a new browser tab).
5. On the Anthropic website, click **Authorize**.
6. Paste the key back into your terminal.

> **Known issue:** You may see an error the first time you click Authorize. Go back to your Codespace tab, click the link again while holding Cmd (Mac) or Ctrl (Windows), and click Authorize again.

> **If you do not have a Claude account yet:** You need either a Pro account ($20/month) plus API billing enabled at platform.claude.com, or a Max account ($100-200/month). Start with Pro + API billing unless you plan to use Claude Code daily — heavy users save money on the Max $200/month plan.

### Setup complete

You now have:

- A GitHub account and repository
- A Codespace development environment
- Claude Code (your AI assistant)
- Ruflo (your agent orchestration platform)

### Getting oriented with Ruflo

You do not need to memorize commands. After setup, Ruflo works in the background — routing tasks to the right agents, learning from patterns, and coordinating work automatically. To explore what is available, paste these prompts into Claude Code one at a time:

```
tell me about Ruflo and its development capabilities and the ADR/DDD. be brief
```

```
tell me about the helpers and what they do
```

```
tell me which helpers are activated
```

> **Tip:** Helpers are activated in settings.json. You can enable `auto-commit.sh` to automatically save versions of your work. Once enabled, you can say things like "restore to the version from 10 minutes ago."

---

## 4. Building Your Personal Context Portfolio

Before Genesis can help your business, the AI needs to understand **you** — your role, your goals, how you think, and what matters to you. The Personal Context Portfolio is a set of 10 markdown files that serve as your "operating manual" for any AI system.

Think of it this way: every time you start a conversation with an AI, you spend the first 10 minutes explaining who you are and what you are working on. The Personal Context Portfolio eliminates that. The AI reads your portfolio and already knows.

### What you need

- Your business documents — bios, business plans, slide decks, transcripts of calls or meetings, anything that captures who you are and what you do
- The personal-context-portfolio repo (the AI will pull this in for you)

### Step 1: Pull in the portfolio framework

Paste this prompt into Claude Code:

```
bring this repo into this project: https://github.com/nlwhittemore/personal-context-portfolio.git
```

This gives the AI the templates, examples, and structure it needs to understand what it is building for you.

### Step 2: Point the AI at your documents

Organize your existing documents into folders in your project. They can be anything — Google Drive exports, local files, transcripts, PDFs. The AI will figure out what is useful.

If your files are already in folders on your computer, tell the AI where they are:

```
copy only the transcripts from [PATH TO YOUR TRANSCRIPTS FOLDER] into transcripts/
```

### Step 3: Create the plan

Paste this prompt, replacing the bracketed paths with your actual folder paths:

```
personal-context-portfolio/ defines a set of example files that I would like
you to create by reverse engineering what you learn about me from the files
in [PATH TO YOUR BUSINESS DOCS], the call transcripts in [PATH TO YOUR
TRANSCRIPTS], and the documents already in [PATH TO OTHER DOCS].

Put those new files into context-portfolio/.

Do your best to create the files and also provide a list of outstanding
questions to complete them.

First create ADR(s) to plan this project (don't implement yet). Put planning
files in docs/adr/.
```

**What the AI does:**
- Reads the portfolio templates to understand the 10-file structure
- Catalogs all your source materials
- Maps which of your documents feed which portfolio files
- Assesses what it can draft versus what needs your input
- Produces planning documents before touching anything

### Step 4: Review the plan, then build

Read the planning documents the AI created in `docs/adr/`. When they look right, paste this:

```
spawn swarm, implement completely, continue until complete.
```

The AI will generate all 10 portfolio files in parallel, pulling from your source materials and marking gaps with `[NEEDS INPUT]` where it does not have enough information.

### Step 5: Fill the gaps

The AI will produce an `outstanding-questions.md` file. Review it and answer the questions — especially those marked `[CRITICAL]`. The highest-impact gaps are usually:

- **Goals and priorities** — tradeoffs and what you are NOT doing
- **Communication style** — how you write, what you dislike in AI output
- **Preferences and constraints** — your schedule, hard rules, frustrations

A 30-45 minute conversation fills most of them. Just talk to Claude Code naturally:

```
Let me answer the outstanding questions. For goals and priorities, here is
what matters most to me: [YOUR ANSWER]. For communication style, I prefer
[YOUR PREFERENCES]. Update the portfolio files with my answers.
```

### What you get

10 markdown files that any AI system can read to understand you:

| File | What It Captures |
|------|-----------------|
| `identity.md` | Who you are, what you do, what you are known for |
| `role-and-responsibilities.md` | What your weeks look like operationally |
| `current-projects.md` | Active workstreams with status and collaborators |
| `goals-and-priorities.md` | What you are optimizing for and what you are NOT doing |
| `team-and-relationships.md` | Key people and how you work with them |
| `tools-and-systems.md` | Your tech stack and data sources |
| `communication-style.md` | How you write, speak, and what you dislike in AI output |
| `preferences-and-constraints.md` | Hard rules, schedule, strong opinions |
| `domain-knowledge.md` | Your expertise, terminology, frameworks |
| `decision-log.md` | How you decide, with real examples |

> **Tip:** Update your portfolio quarterly or after any major change. A portfolio with `[NEEDS INPUT]` markers is still 10x more useful than no portfolio at all.

---

## 5. Building Your Knowledge Base

Now that the AI understands you, it needs to understand your **business**. The knowledge base turns all your documents, transcripts, and data into a searchable system that understands meaning — not just keywords.

Ask about "cost structure" and it finds results about "pricing" and "fee schedule." Ask "what did Dr. Smith say about patient retention?" and it finds the exact conversation, even if those words were never used together.

### What you need

- Your business documents organized into folders (transcripts, financials, meeting notes, etc.)
- The ruvector submodule (the AI will pull this in)

### Step 1: Add the knowledge base infrastructure

Paste this into Claude Code:

```
add ruvnet/ruvector upstream submodule to this project
```

This gives the AI the vector database, embedding engine, and search infrastructure.

### Step 2: Put your files in kb-inputs/

Create a folder called `kb-inputs/` in your project and put everything you want in your knowledge base there. Drag and drop files from Finder (Mac) or File Explorer (Windows) into this folder in VS Code.

Organize into subfolders by type. The subfolder names become automatic categories — no manual tagging needed:

```
kb-inputs/
  Transcripts/Sales Calls/       → tagged "sales-call"
  Transcripts/Coaching/           → tagged "coaching"
  Financial/                      → tagged "financial"
  Operations/                     → tagged "operations"
  Marketing/                      → tagged "marketing"
```

If your files need reorganizing, ask Claude Code to help:

```
look at everything in kb-inputs/ and propose a better folder structure.
Don't implement — write the plan as a markdown document.
```

> **Important:** Tell Claude Code to keep these files out of GitHub:
> ```
> add kb-inputs/ to the .gitignore so it is not uploaded to GitHub
> ```


### Step 3: Install the skills

Before using the ruvector-setup skill, you need to pull the skills into your project. Paste this into Claude Code:

```
copy these skills into this project:
https://github.com/mamd69/hf-spring-retreat-26/tree/main/Skills in .claude/skills/
```

This installs the pre-built skills that Claude Code uses to understand how to set up and configure your knowledge base.

### Step 4: Plan before building

Paste this prompt, replacing the bracketed paths:

```
use the '.claude/skills/ruvector-setup' to figure out the right setup that
allows me to achieve my project goals [PATH TO PROJECT GOALS].  Make sure to create a persistent ruvector REDB and explain to the user where it is and how to use it (using natural language commands).  Add to .claude memory to call this "kb" or "knowledgebase".

All of the context needs to be loaded in, including everything in
kb-inputs/ (many different kinds of files).

First create ADR(s) and DDD(s). Don't implement yet. Put planning files
in docs/adr/ and docs/ddd/.
```

**What the AI does:**
- Reads the ruvector setup instructions to understand the technology
- Surveys all your content folders — counts files, identifies types (transcripts, CSVs, markdown, plain text)
- Maps each folder to a category
- Designs a chunking strategy for each file type (how to break large files into searchable pieces)
- Produces Architecture Decision Records (ADRs) and Domain-Driven Design documents (DDDs) before building anything

### Step 5: Build the knowledge base

Once the planning documents look right, paste this:

```
implement ADRs. spawn swarm, implement completely, test, validate,
benchmark, optimize, document. continue until complete.
```

**What the AI does:**
- Creates the full application — parsers for each file type, chunking logic, database wrapper, embedding engine, ingestion pipeline, search engine, and tests
- Installs all dependencies
- Runs tests
- Ingests all your files
- Runs benchmarks
- Reports results

### Step 6: Verify it works

Once ingestion completes, start by getting oriented. Ask Claude Code what is in your knowledge base and where it lives:

```
what is in my knowledge base?
```

```
where is my knowledge base stored?
```

The first question gives you a summary of what was ingested — how many files, what categories, how many chunks. The second tells you where the database file lives on your machine so you know what to back up.

**Check for missing content.** Review the summary. If any files or folders you expected are missing, add them to `kb-inputs/` and re-ingest:

```
I added new files to kb-inputs/. Re-ingest everything into the knowledge base.
```

**Test with real queries.** Once you are satisfied everything is loaded, test search quality:

```
search the knowledge base for "What did [person] say about [topic]?"
```

Try different queries to test relevance:

```
search the knowledge base for "affiliate partnerships and referrals"
```

```
search the knowledge base for "revenue from last quarter"
```

```
search the knowledge base for "patient retention strategies"
```

You should see results ranked by relevance with source attribution — which file, which category, the date, and who said it.

### What you get

A local, semantic knowledge base you control with natural language:

| What to Say in Claude Code | What It Does |
|---------|-------------|
| `ingest all my files into the knowledge base` | Parse, chunk, embed, and store all your files |
| `search the knowledge base for "[your question]"` | Search by meaning — ask questions in plain language |
| `run a benchmark on the knowledge base with 10 sample queries` | Run 10 sample queries and report speed stats |

Key facts about your knowledge base:

- **Runs entirely on your laptop** — no cloud, no API costs for search
- **Understands meaning** — "cost structure" matches "pricing" and "fee schedule"
- **Stores everything in one file** — a portable ~50MB database file
- **Searches in about 200 milliseconds** per query
- **Handles multiple file types** automatically:

| File Type | How It Processes |
|-----------|-----------------|
| `.vtt` / `.srt` transcripts | Groups 3-5 speaker turns per chunk, preserves who said what |
| `.md` documents | Splits on headings — each section becomes a chunk |
| `.csv` financials | One row per chunk, generates a plain-English summary |
| `.txt` files | Sliding window (~250 words with overlap) |

> **Tip:** Start with transcripts. They are the richest source of context — hours of conversation broken into searchable pieces. Financial CSVs are surprisingly useful too. Each transaction becomes a searchable sentence like "$1,499 payment from Jane Doe for Mastermind Pro on Mar 8, 2026."

### Troubleshooting

**"Search results don't seem relevant"** — If results only match exact words, the semantic embedding engine did not load. Look for `ONNX embedder ready: 384d semantic embeddings` when you start. If you see `Falling back to hash-based embeddings`, the embedding model is not loading. Make sure the `ruvector/` directory exists with source code in it.

**Adding new files later** — Drop new files into `kb-inputs/` and tell Claude Code:

```
I added new files to kb-inputs/. Re-ingest everything into the knowledge base.
```

---

## 6. Elevating Your Knowledge Base to World-Class

The previous section built a functional knowledge base from your existing files. This section takes it further — using a structured methodology to make your knowledge base comprehensive, expert-sourced, and rigorously validated.

This is the difference between "we uploaded our documents" and "we have the most complete understanding of our domain that exists." It follows eight sub-phases, each with a quality gate that must pass before moving to the next.

### Phase 2.1: Domain scoping

Define the boundaries of what your knowledge base covers. Paste this prompt:

```
Analyze my knowledge base and define the domain scope. For my business in
[YOUR INDUSTRY], document:

1. A formal definition of our domain and its boundaries
2. Adjacent fields that overlap with ours
3. Sub-disciplines within our domain
4. Historical context — how this field got to where it is today
5. Current debates and open questions in the industry

Save to docs/kb-enhancement/domain-scope.md
```

**Why this matters:** Without clear boundaries, your knowledge base either misses critical areas or becomes bloated with irrelevant information. A pediatric practice's knowledge base has different boundaries than a real estate investment firm's, even though both might touch healthcare regulation.

### Phase 2.2: Perspective expansion

Map every type of person who might query your knowledge base and every type of question they might ask. Paste this prompt:

```
Based on the domain scope in docs/kb-enhancement/domain-scope.md, map out:

1. At least 5 types of users who will query this knowledge base (executives,
   clinicians, operations staff, sales team, new hires, etc.)
2. At least 50 types of questions these users would ask
3. Use cases for each user type
4. Edge cases — unusual but important scenarios
5. Interaction patterns — how different users search differently

Save to docs/kb-enhancement/perspective-map.md
```

**Why this matters:** If you only think about how YOU would search, you miss how your team, your patients, your investors, or your partners would search. The front desk manager asks different questions than the CFO.

### Phase 2.3: Expert discovery and knowledge extraction

Identify the top minds in your field and pull their knowledge into your base. Paste this prompt:

```
Based on my domain scope, identify the top 100 experts across these categories:

- Academic researchers and published authors
- Practitioners and clinicians (if applicable)
- Industry leaders and conference speakers
- Authors of key books and frameworks
- Emerging voices and innovators

For each expert, extract their key contributions, frameworks, and insights.
Cross-reference insights across experts to identify consensus and disagreement.
Target: 500+ content items yielding 1000+ cross-referenced insights.

Save expert profiles to docs/kb-enhancement/experts/
Save extracted insights to docs/kb-enhancement/insights/
```

**Why this matters:** Your internal documents capture what YOUR business knows. This step captures what the INDUSTRY knows — best practices, proven frameworks, and cutting-edge research. In the Nexadental example, this meant ingesting the American Association of Orthodontists' best practices plus proprietary industry databases. For Good Samaritan Hospital, it meant downloading 600,000+ ICD code records plus all CMS rules and regulations.

### Phase 2.4: Completeness audit

Systematically identify what is missing. Paste this prompt:

```
Audit the current knowledge base for gaps. Check across these dimensions:

1. Coverage gaps — topics in our domain scope that have no content
2. Depth gaps — topics covered superficially that need more detail
3. Perspective gaps — viewpoints not represented
4. Temporal gaps — outdated information or missing recent developments
5. Structural gaps — areas where relationships between topics are missing

Rate each gap by importance (critical, high, medium, low).
Identify at least 30 gaps total.

Save to docs/kb-enhancement/completeness-audit.md
```

### Phase 2.5: Fill the gaps

Address every gap identified in the audit. Paste this prompt:

```
Using the completeness audit in docs/kb-enhancement/completeness-audit.md,
fill all critical and high-importance gaps. For each gap:

1. Research authoritative sources
2. Extract relevant knowledge
3. Integrate into the existing knowledge base structure
4. Verify accuracy against multiple sources

Start with critical gaps first. Document sources for everything.
Save new content to the appropriate knowledge base locations.
Save a gap-filling log to docs/kb-enhancement/gap-filling-log.md
```

### Phase 2.6: Structure and organize

Organize everything into a clean, navigable structure. Paste this prompt:

```
Organize the full knowledge base into a clear structure following these rules:

1. Maximum 9 top-level categories (this is a cognitive limit — more than 9
   becomes unnavigable)
2. Each category follows MECE principles (Mutually Exclusive, Collectively
   Exhaustive — no overlaps, no gaps)
3. Unlimited depth within categories
4. Every piece of content has a clear home

Produce a visual map of the structure and save to
docs/kb-enhancement/structure-map.md
```

### Phase 2.7: Ensure depth at every node

Make sure every endpoint in your knowledge base contains actual, useful content. Paste this prompt:

```
Review every leaf node in the knowledge base structure. Each must contain:

1. A clear title
2. Substantive content (not just a placeholder)
3. Expert source attribution
4. Source URL or reference
5. Confidence score (how certain is this information?)
6. Metadata (date, category, related topics)

Identify any leaf nodes that are empty or placeholder-only and fill them.
Save the audit results to docs/kb-enhancement/depth-audit.md
```

### Phase 2.8: Quality scoring loop

Score your knowledge base and iterate until it meets the bar. Paste this prompt:

```
Score the knowledge base on these 6 criteria (each weighted):

1. Completeness (25%) — Does it cover the full domain scope?
2. Accuracy (25%) — Is the information correct and well-sourced?
3. Attribution (15%) — Can every claim be traced to a source?
4. Structure (15%) — Is it logically organized and navigable?
5. Depth (10%) — Are topics covered with sufficient detail?
6. Currency (10%) — Is the information up to date?

Produce an overall score out of 100. For any criterion below 90%, identify
specific improvements. Implement the improvements and re-score.

Repeat until the overall score is 98 or above.

Save scoring reports to docs/kb-enhancement/quality-scores/
```

> **What "world-class" looks like:** When this process is complete, your knowledge base does not just contain your documents — it contains your documents, your industry's best practices, the frameworks of the top 100 experts in your field, and a verified, structured, gap-free knowledge architecture. This is what Genesis uses to produce analyses that rival $100,000 consulting engagements.

---

## 7. Visualizing and Verifying Your Knowledge Base

A knowledge base you cannot see is a knowledge base you cannot trust. This step generates an interactive visualization so you can explore what is in your knowledge base, verify it is correct, and spot gaps visually.

### Generate the visualization

Paste this prompt:

```
Create an interactive visualization of my knowledge base with:

1. An expandable/collapsible tree showing the full structure
2. Click any node to see its full content and expert sources
3. A search bar to find topics by keyword or meaning
4. Breadcrumb navigation so I always know where I am
5. A statistics panel showing: total nodes, expert sources count,
   average confidence score, and maximum depth

Use a simple HTML tree approach so it runs in any browser.
Save to ui/kb-visualization/
```

### What to look for

Once the visualization loads in your browser, check these things:

| Check | What You Are Looking For |
|-------|------------------------|
| **Balance** | Are some branches huge while others are tiny? That suggests gaps. |
| **Depth** | Click into leaf nodes. Do they have real content, or just titles? |
| **Sources** | Click nodes and check the expert attribution. Is it from a credible source? |
| **Search** | Try 5-10 questions your team would actually ask. Do the results make sense? |
| **Coverage** | Think of a topic critical to your business. Can you find it in the tree? |

### Verify with your team

The visualization is a powerful tool for getting feedback from your team. Share the URL and ask:

```
Generate a verification checklist I can send to my team. Ask them to:

1. Find [3 specific topics critical to our business] in the knowledge base
2. Check if the information is accurate and current
3. Identify anything important that is missing
4. Rate their confidence in the knowledge base on a 1-10 scale
5. Note any terminology or categorization that feels wrong

Format as a simple form they can fill out in 10 minutes.
Save to docs/kb-enhancement/team-verification-form.md
```

---

## 8. The Genesis Methodology: Analyze, Plan, Build

With your personal context portfolio built and your knowledge base loaded, you are ready to run the Genesis methodology on your business. This is the four-step process that takes you from "here is my business" to "here is my optimized business with new tools, automations, and AI agents running."

### Step 1: Brainstorm and research

Before designing solutions, understand the problem thoroughly. Use the goal-planner agent to evaluate your situation and produce a research document.

Paste this prompt:

```
use @"goal-planner (agent)" to evaluate my business based on the knowledge
base and my personal context portfolio. Create an academic-quality research
document that covers:

1. Current state assessment — what is working, what is not
2. Industry best practices versus our current practices
3. Revenue leakage and improvement opportunities
4. What is possible with AI that was not possible before
5. Risks and constraints to consider

Save to docs/research/business-assessment.md
```

**What this produces:** A comprehensive analysis — not opinions, but findings grounded in your actual data and industry benchmarks. In the Nexadental case, this step compared the practice's lead response time, case acceptance rate, patient retention, and collections against AAO best practices and identified specific gaps with dollar amounts attached.

> **Your domain expertise matters here.** Read the research document carefully. You know your business. The AI may surface something brilliant — or something that does not apply to your situation. Mark the findings that make sense and flag the ones that do not:

```
I have reviewed the research document. Here are my corrections and priorities:

- [FINDING 1] is accurate and high priority
- [FINDING 2] does not apply because [REASON]
- [FINDING 3] is interesting but low priority right now
- You missed [IMPORTANT TOPIC] — please research and add it

Update the research document with my feedback.
```

### Step 2: Create the plan

Using the validated research, create detailed architecture decisions and an implementation plan. No building happens in this step — plans are cheap to change, code is expensive to change.

Paste this prompt:

```
Using docs/research/business-assessment.md, create:

1. Architecture Decision Records (ADRs) for each major initiative — what we
   will build and why, with alternatives considered
2. Domain-Driven Design documents (DDDs) mapping out the business entities,
   relationships, and boundaries
3. An implementation plan with phased sprints, ordered by value-versus-effort
   (highest value, lowest effort first)

Don't implement yet. Put planning files in:
- docs/adrs/
- docs/ddd/
- docs/plan/implementation-plan.md
```

**What ADRs and DDDs are in plain language:**

| Document | What It Answers | Example |
|----------|----------------|---------|
| **ADR** (Architecture Decision Record) | "We decided to do X because of Y." | "ADR-001: Build a patient intake AI agent instead of hiring two more front desk staff, because the AI handles 24/7 coverage at 1/10th the cost." |
| **DDD** (Domain-Driven Design) | "Here are the things in our business, how they relate, and where the boundaries are." | "A Patient has Appointments, which generate Claims, which produce Revenue. The scheduling system and the billing system are separate domains that share patient data." |
| **Implementation Plan** | "Here is what we build first, second, third — and why in that order." | "Sprint 1: Lead response automation (highest revenue impact, lowest effort). Sprint 2: Operational dashboard (needed before Sprint 3). Sprint 3: Coding optimization (highest revenue impact, medium effort)." |

Review these documents. They are your roadmap. Change anything that does not feel right — it is much easier to change a plan than to change finished software.

### Step 3: Build

This is where Genesis earns its name. A coordinated team of AI agents builds everything — in parallel, overnight if needed.

Paste this prompt, specifying which ADRs to implement:

```
implement ADR-001 through ADR-003. spawn swarm, implement completely, test,
validate, benchmark, optimize, document. continue until complete.
```

**What happens behind the scenes:**
- Multiple AI agents launch simultaneously — one writing front-end code, one writing back-end code, one writing tests, one reviewing, one documenting
- The agents coordinate through the shared knowledge base
- Built-in quality gates: code is not "done" until it passes tests, meets performance targets, and is documented
- Browser automation agents test the user interface by actually clicking buttons and filling forms, like a human would
- The cycle repeats — implement, test, validate, benchmark, optimize, document — until everything passes

You do not need to manage this process. The AI orchestrates itself. You review the output.

### Step 4: Test, fix, and enhance

Automated tests passing does not mean the product works for real humans. This step generates a testing guide and walks you through verification.

Paste this prompt:

```
Give me a user testing guide for everything built in Sprint 1. Create a
step-by-step script: "click here, enter this, expect that." Prove to me
that this works from a real user's perspective.

Save to docs/testing/sprint-1-user-test.md
```

Walk through the testing guide yourself. When you find issues:

```
I found these issues during testing:

1. [DESCRIBE WHAT YOU DID AND WHAT WENT WRONG]
2. [DESCRIBE ANOTHER ISSUE]
3. [DESCRIBE SOMETHING THAT WORKS BUT COULD BE BETTER]

Fix the bugs and implement the enhancement. Test again after fixes.
```

Repeat until everything works as expected. Then move to the next sprint.

### The ongoing cycle

Genesis does not stop after the initial build. The monitoring and self-improvement loop continues:

```
Set up ongoing monitoring for the deployed solutions:

1. Track KPIs defined in the implementation plan
2. Update dashboards nightly with fresh data
3. Set the GNN learning goal to: [YOUR PRIMARY OPTIMIZATION TARGET,
   e.g., "improve lead conversion rate" or "reduce claim denial rate"]
4. Alert me weekly with a summary of performance and any anomalies

Save monitoring configuration to docs/monitoring/setup.md
```

---

## 9. Addendum: Helpful Repos and Tools

These open-source repositories are useful companions to the Genesis workflow.

### [microsoft/markitdown](https://github.com/microsoft/markitdown)

A Python utility that converts various file formats (PDFs, Word docs, Excel sheets, images, etc.) into Markdown, optimized for use with LLMs and text analysis pipelines.

**When to use it:** When you have business documents in PDF, Word, or Excel format that need to be converted to Markdown before loading into your knowledge base. Markdown is the format AI tools work with best.

```
Use markitdown to convert all PDFs and Word docs in [PATH TO YOUR FILES]
into markdown format. Save the converted files to documents/converted/
```

### [mamd69/ruvector-catalog](https://github.com/mamd69/ruvector-catalog)

A technology recommender system that maps problems to solutions within RuVector's monorepo, helping developers discover the right AI/ML capabilities among 200+ technologies.

**When to use it:** When you are in the planning phase and want to understand which AI/ML technologies are best suited for a specific business problem. Instead of guessing, the catalog matches your problem to proven solutions.

```
use @ruvector-catalog to deeply analyze [DESCRIBE YOUR BUSINESS PROBLEM]
and recommend the best technology approach. Save the recommendation to
docs/research/technology-recommendation.md
```

### [nlwhittemore/personal-context-portfolio](https://github.com/nlwhittemore/personal-context-portfolio)

A structured framework of markdown files that serves as a portable personal context package for AI agents — an "operating manual" so you do not have to repeatedly explain your identity, projects, goals, and preferences to different AI systems.

**When to use it:** At the very beginning of your Genesis journey (covered in Section 4 of this guide). This is the foundation that makes every subsequent AI interaction more effective.

---

## Quick Reference

### Setup commands

| Action | Command |
|--------|---------|
| Install Claude Code | `curl -fsSL https://claude.ai/install.sh \| bash` |
| Install Ruflo | `curl -fsSL https://cdn.jsdelivr.net/gh/ruvnet/claude-flow@main/scripts/install.sh \| bash -s -- --full` |
| Start Claude Code | `dsp` |
| Resume last session | `dsp-c` |
| Search your knowledge base | `search the knowledge base for "[your question]"` |
| Check what's in your KB | `what is in my knowledge base?` |
| Re-ingest after adding files | `I added new files to kb-inputs/. Re-ingest everything into the knowledge base.` |

### The methodology at a glance

| Step | What You Do | What You Get |
|------|------------|-------------|
| **1. Brainstorm** | Run the goal-planner agent | Research document with findings |
| **2. Plan** | Create ADRs, DDDs, implementation plan | A roadmap you review and approve |
| **3. Build** | Launch the agent swarm | Working, tested software and automations |
| **4. Validate** | Walk through the user testing guide | Verified, production-ready solutions |

### Key prompts to remember

**Start a research phase:**
```
use @"goal-planner (agent)" to evaluate [AREA] and create docs/research/[NAME].md
```

**Create plans from research:**
```
Using docs/research/[NAME].md, create detailed docs/ADRs, docs/DDDs, plus
docs/plan/implementation-plan.md that will guide me through my sprints.
Don't implement yet.
```

**Build from plans:**
```
implement ADR [NUMBERS]. spawn swarm, implement completely, test, validate,
benchmark, optimize, document. continue until complete.
```

**Test what was built:**
```
Give me a user testing guide. Prove to me that this works.
```

---

## Best Practices

- **Do not paste large blocks of text directly into Claude Code.** Put content into files and reference those files by path instead. The AI reads files far more reliably than pasted text.
- **Use multiple terminal windows** when tasks need to run in parallel. Click the **+** icon at the top of the terminal panel to open a new tab.
- **Save frequently.** Use Ctrl+S, or enable Auto Save under File > Auto Save.
- **Commit your work regularly.** This creates save points you can return to if something goes wrong.
- **Read error messages carefully.** They usually tell you exactly what went wrong.
- **Be specific when asking Claude.** "Fix the dashboard" is vague. "The revenue chart on the dashboard shows last month's data instead of this month's — fix it" is specific.
- **Keep your laptop awake during long builds.** In a separate terminal, run `caffeinate` to prevent sleep. Close that terminal when you are done.
- **Your expertise is essential.** The AI does not know your business the way you do. Review its work. Correct it. Direct it. The best results come from collaboration, not delegation.

---

*This guide synthesizes the HeroForge Genesis platform documentation, setup guides, and methodology references into a single walkthrough for business leaders. For questions or support, reach out through the HeroForge Mastermind community.*
