# HeroForge Genesis: The Complete Guide

**From idea to operating business — a step-by-step guide for business leaders.**

---

## How to Use This Guide

This guide is designed to be followed in order, from start to finish. Each section builds on the one before it. You will set up your tools, define your project, prepare your files, build a searchable knowledge base, and then use that foundation to analyze, plan, and build.

Every prompt in this guide is **copy-paste ready**. When you see a block like this:

```
this is a prompt you paste into Claude Code
```

Copy it exactly. Anywhere you see `[BRACKETS]`, replace with your own information. We try to place bracketed placeholders at the **end** of the prompt so you can edit them without scrolling — just paste and update the last few lines.

**What you need before you start:**

- A computer with internet access
- An email address
- A Claude Max account (Claude Pro/Team accounts are not sufficient for Genesis)
- About 30 minutes for initial setup
- Your business documents — bios, transcripts, financials, slide decks, meeting notes, whatever you have

**Numbering convention:** Top-level sections use numbers (1, 2, 3, ...). Subsections use letters (A, B, C, ...). Sequential process steps use numbered Steps (Step 1, Step 2, ...). When you see a reference like "Section 5, Step 2" elsewhere in the guide, the levels are visually distinct so there is no ambiguity.

---

## Table of Contents

- [1. What Is Genesis?](#1-what-is-genesis)
- [2. The Genesis Methodology: Analyze, Plan, Build, Verify, Enhance](#2-the-genesis-methodology-analyze-plan-build-verify-enhance)
- [3. Setting Up Your Tools](#3-setting-up-your-tools)
- [4. Define Your Project Scope and Goals](#4-define-your-project-scope-and-goals)
- [5. Preparing Your Files](#5-preparing-your-files)
- [6. Building Your Knowledge Base](#6-building-your-knowledge-base)
- [7. Elevating Your Knowledge Base to World-Class](#7-elevating-your-knowledge-base-to-world-class)
- [8. Visualizing and Verifying Your Knowledge Base](#8-visualizing-and-verifying-your-knowledge-base)
- [9. Building Your Genesis Assets](#9-building-your-genesis-assets)
- [10. Addendum: Helpful Repos and Tools](#10-addendum-helpful-repos-and-tools)

---

## 1. What Is Genesis?

Genesis is an **operating system for your business**. It is a platform that takes your business from its current state to an optimized future state by combining the most powerful AI models with a proprietary knowledge engine and coordinated teams of AI agents.

It is not a chatbot. It is not a single tool. Genesis **analyzes** your business, **plans** improvements, **builds** the solutions, **deploys** them, and then **monitors and self-improves** over time.

### A. What makes it different

Most AI tools today are static — you ask a question, you get an answer, the AI forgets you existed. Genesis is built on a three-layer knowledge engine:

| Layer | What It Does | Plain-English Analogy |
|-------|-------------|----------------------|
| **Vector Database** | Finds information by meaning, not just keywords. Ask about "PTO policy" and it finds results about "vacation days" and "time off." | A librarian who understands what you mean, not just what you said. |
| **Graph Database** | Understands relationships between things — org charts, coding rules, regulatory hierarchies. | A map that shows how everything connects to everything else. |
| **Graph Neural Network** | Learns and improves from every interaction, autonomously optimizing toward goals you set. | An employee who gets better at their job every day without being told how. |

That third layer — the Graph Neural Network — is the key differentiator. The AI models themselves (Claude, GPT) do not learn from your interactions. They are born smart but have no memory. The GNN actually learns. Set a goal like "improve lead conversion rate" and it will analyze every interaction and optimize toward that goal over time, without human intervention.

### B. What Genesis produces

Genesis is not theoretical. Here is what it has built for real businesses:

- **Nexadental** (orthodontics): A complete SaaS platform with practice assessment reports, operational dashboards pulling data nightly from billing systems, AI phone agents that answer calls 24/7 and follow up on leads, and a conversational AI assistant that discusses findings and recommendations.
- **Good Samaritan Hospital** (medical coding): An AI coding optimization system that combines clinical reasoning with 600,000+ ICD codes and all CMS rules, identifying 10-15% revenue improvement at a $90 million hospital.
- **Vermont Real Estate**: Financial models, investor decks, targeted buyer outreach with personalized emails to the 50 most ideal buyers — each generated automatically.

### C. The four major phases

Every Genesis project moves through four high-level phases:

1. **Import and Digitize** — Upload your business documents, data, and institutional knowledge.
2. **Research and Augment** — The AI researches industry best practices, competitors, and benchmarks, then adds that knowledge to your base.
3. **Analyze and Plan** — The AI compares your current state against best practices, identifies gaps, runs simulations, and produces prioritized roadmaps.
4. **Build and Deploy** — A coordinated team of AI agents builds the solutions — software, automations, dashboards, AI assistants — and deploys them with ongoing monitoring.

This guide walks you through every phase.

> **Two levels of methodology.** The four phases above describe the **major arc** of a Genesis project — the high-level journey from raw inputs to deployed solutions. Inside each phase (and inside every significant improvement cycle after) you use a smaller, reusable five-step methodology — **Analyze, Plan, Build, Verify, Enhance** — to actually get work done. That reusable methodology is covered in [Section 2](#2-the-genesis-methodology-analyze-plan-build-verify-enhance) and you will use it over and over throughout Genesis.

### D. Two starting points: Greenfield vs. Brownfield

Before you begin, it helps to know which type of Genesis project you are starting:

| | Greenfield | Brownfield |
|---|---|---|
| **What it means** | A new business or new idea. You are starting from scratch with little or no existing data. | An existing business with years of accumulated documents, transcripts, financials, meeting notes, and institutional knowledge. |
| **What you have** | A seed of an idea, maybe a business plan or some early notes. | A mountain of context — files on your computer, in Google Drive, in your EMR, in your head. |
| **Best setup** | A GitHub Codespace (runs in your browser, nothing to install). | VS Code on your desktop (your files are already on your computer — no uploading needed). |
| **Where to start** | Jump straight to setup, then let the AI help you research and build from the ground up. | Start by organizing your files, then point the AI at them locally. |

Most business leaders doing Genesis have an existing business — that is a **brownfield** project. This guide covers both paths.

---

## 2. The Genesis Methodology: Analyze, Plan, Build, Verify, Enhance

You just saw the four major phases in Section 1. This section describes the **reusable five-step methodology** — Analyze, Plan, Build, Verify, Enhance — that you use inside every phase to actually make progress. You will see this pattern throughout the guide: it is how you build your knowledge base, how you enhance it, how you design new tools, and eventually how you take your business from current state to optimized future state. Learn it once, reuse it everywhere.

The five steps close every loop before the next one starts. **Verify** is your job as the human in the loop — make the AI prove the work is real — and **Enhance** is where you turn something that works into something that is genuinely good.

> **This is reference material.** You are not executing this methodology yet — you need tools, a project scope, files, and a knowledge base first (Sections 3 through 6). Read this section so you know the pattern. You will apply it starting in Section 6 and keep applying it long after this guide ends.

### Step 1: Analyze (brainstorm and research)

Before designing solutions, understand the problem thoroughly. Use the goal-planner agent to evaluate your situation and produce a research document.

Paste this prompt:

```
use @"goal-planner (agent)" to evaluate my business based on the knowledge
base and my project goals. Create an academic-quality research document
that covers:

1. Current state assessment — what is working, what is not
2. Industry best practices versus our current practices
3. Revenue leakage and improvement opportunities
4. What is possible with AI that was not possible before
5. Risks and constraints to consider

Save to docs/research/business-assessment.md
```

**What this produces:** A comprehensive analysis — not opinions, but findings grounded in your actual data and industry benchmarks. This step compares your business's key metrics (response times, conversion rates, retention, revenue per customer, etc.) against industry best practices and identifies specific gaps with dollar amounts attached.

> **Your domain expertise matters here.** Read the research document carefully. You know your business. The AI may surface something brilliant — or something that does not apply to your situation. Mark the findings that make sense and flag the ones that do not:

```
I have reviewed the research document. Update it with my corrections
and priorities below, then research any new topics I've added.

Corrections and priorities:
- Finding: [FINDING 1] — Status: accurate and high priority
- Finding: [FINDING 2] — Status: does not apply — Reason: [REASON]
- Finding: [FINDING 3] — Status: low priority for now
- Missing topic to add: [TOPIC]
```

### Step 2: Plan

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
| **ADR** (Architecture Decision Record) | "We decided to do X because of Y." | "ADR-001: Build a customer intake AI agent instead of hiring two more staff, because the AI handles 24/7 coverage at 1/10th the cost." |
| **DDD** (Domain-Driven Design) | "Here are the things in our business, how they relate, and where the boundaries are." | "A Customer has Orders, which generate Invoices, which produce Revenue. The sales system and the billing system are separate domains that share customer data." |
| **Implementation Plan** | "Here is what we build first, second, third — and why in that order." | "Sprint 1: Lead response automation (highest revenue impact, lowest effort). Sprint 2: Operational dashboard (needed before Sprint 3). Sprint 3: Pricing optimization (highest revenue impact, medium effort)." |

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

### Step 4: Verify

This step is your job. The AI will tell you it finished. The tests will say they passed. That does not mean the product actually works for real humans — and it does not mean the AI built what it claimed to build. Your job in this step is to **review the work and make the AI prove it works**.

First, have the AI produce a testing guide so you can walk the product end-to-end:

```
Give me a user testing guide for everything built in Sprint 1. Create a
step-by-step script: "click here, enter this, expect that." Prove to me
that this works from a real user's perspective.

Save to docs/testing/sprint-1-user-test.md
```

Then actually walk through it yourself. Click the buttons. Fill the forms. Read the output. Spot-check the things the AI said it built against what is actually in the codebase.

If anything is unclear or you are not convinced, push back:

```
Prove to me that [FEATURE OR COMPONENT] is real and working. Show me:

1. The exact file paths where this is implemented
2. The tests that cover it, and the most recent test run output
3. A live demo — run it end-to-end and show me the output
4. Any gaps between what I asked for and what was built
```

Write down every issue, missing piece, or "that's not quite right" — you are going to hand this list to Step 5.

### Step 5: Enhance

Now that you have verified what actually works and what does not, close the loop: fix the bugs, fill the gaps, and push the product from "it works" to "it is good."

Paste this prompt with the issues and enhancements you captured in Step 4:

```
Based on my verification below, fix the issues and implement the
enhancements. Then re-run the user testing guide and show me that each
item is resolved.

Issues to fix:
1. [WHAT YOU DID AND WHAT WENT WRONG]
2. [ANOTHER ISSUE]

Gaps between what was requested and what was built:
1. [MISSING PIECE]

Enhancements to add (works but could be better):
1. [SOMETHING TO IMPROVE]
```

Loop between Step 4 and Step 5 until you are genuinely satisfied — not until the AI says it is done, but until you have personally confirmed it works and is worth shipping. Then move to the next sprint.

### A. The ongoing cycle

Genesis does not stop after the initial build. The monitoring and self-improvement loop continues:

```
Set up ongoing monitoring for the deployed solutions:

1. Track KPIs defined in the implementation plan
2. Update dashboards nightly with fresh data
3. Set the GNN learning goal to the optimization target below
4. Alert me weekly with a summary of performance and any anomalies

Save monitoring configuration to docs/monitoring/setup.md

GNN optimization target: [YOUR PRIMARY TARGET, e.g., "improve lead conversion rate" or "reduce customer churn"]
```

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
| **Add Folder to Workspace** | Links to the original files. No copy is made. | When you are only reading files to feed into your knowledge base. This is the most common choice. |
| **Copy Folder** | Makes a duplicate inside your project. | When you plan to manipulate, reorganize, or transform the content. |

You will return to this decision in [Section 5 (Preparing Your Files)](#5-preparing-your-files) once you are ready to actually bring your business files in.

**Important: Keep your business files out of GitHub.** Your business files should stay on your local machine — you do not want them uploaded to your GitHub repository. After adding files to your workspace, tell Claude Code to exclude them:

```
add the following folder to the .gitignore so it is not uploaded to GitHub

Folder: [YOUR FOLDER NAME, e.g., Business Files/]
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

### A. Setup complete

You now have:

- A GitHub account and repository
- A Codespace development environment
- Claude Code (your AI assistant)
- Ruflo (your agent orchestration platform)

### B. Getting oriented with Ruflo

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

## 4. Define Your Project Scope and Goals

With your tools in place, spend 15–20 minutes getting crystal clear on **what** this Genesis project covers and **where** you want it to take you. This focus will shape every decision the AI makes on your behalf — from what it researches to what it builds.

### Step 1: Define your scope (10 mins)

Determine the exact boundaries for this Genesis project. Is this for your entire business, a specific division, or your personal life and goals?

**Reflection Question:** If you had a digital army of the smartest AI in the world working in one specific area of your life or business — and they knew every detail — which area would provide the highest ROI right now?

Write down your answer. Be specific. "My business" is too broad for most people. "The sales and marketing engine for my consulting practice" or "Operations at my dental group's three locations" gives the AI a clear target.

### Step 2: Define your goals (10 mins)

Now write a short statement — **under 500 words** — describing what success looks like for this project. Be honest, be specific, and include the outcomes that actually matter to you. This becomes a core input the AI will reference throughout the entire Genesis process.

Use the following prompt template. Paste it into a document or directly into Claude Code, replacing the bracketed sections with your own words:

```
The goals of this project are to build a platform for my business. I want
to achieve my primary goal by my target timeframe. I want to achieve my
secondary goal as well.

Specifically, I want to accomplish the concrete outcomes listed below.

I also want to be clear about what I do NOT want — see my constraints below.

The way I want to work is described in my operating style below.

Action: [BUILD/CREATE/TRANSFORM]
What I am building: [e.g., business operating system, sales engine, operational platform]
Who this is for: [your business name, division, or personal brand]
Primary goal: [e.g., grow revenue to $X, reduce costs by Y%, launch Z product lines]
Timeframe: [e.g., 6 months, end of year, Q3]
Secondary goal: [e.g., be a recognized leader in my space, build a world-class team]
Concrete outcomes (2-4): [e.g., find more enterprise clients, automate onboarding, build a content engine]
Constraints (what I do NOT want): [e.g., no large team, no outside capital, no sacrifice of work-life balance]
Operating style: [e.g., AI-native, lean, high-leverage, hands-on in strategy but hands-off in execution]
```

**Example of a completed goals statement:**

> The goals of this project are to create a business operating system for the HeroForge.ai business. I want to grow the business to more than ten million dollars in profit this year (up from $1M/yr run rate end of last year), and have a great time doing it. I want to be at the forefront of AI education and usage. I want to find more mastermind clients, more coaching clients, and more deep projects to sink my teeth into — projects that can build equity.
>
> I also don't want to be spread too thin, and I don't want to build a huge company. I really want to be AI-native.

Your statement does not need to be long. It needs to be **true**. The AI will use this as a north star for every analysis, plan, and build it produces. If you change your mind later, you can update it — but starting with clear intent saves enormous time downstream.

Save this statement to a file in your project (for example, `docs/project-goals.md`). You will reference this path in later sections.

---

## 5. Preparing Your Files

If you are doing a **greenfield** project (starting from scratch), skip ahead to [Section 6: Building Your Knowledge Base](#6-building-your-knowledge-base).

If you have an existing business with files, take 30-60 minutes to prepare before you start. This step pays for itself many times over.

### A. Make a backup first

Before pointing AI at your business files, make a backup of your originals. Copy them to an external drive, Google Drive, or another safe location. The AI will not delete your files, but having a backup is good practice before any reorganization.

### B. Organize by type

Group your files into folders by category. Don't overthink it — the folder names become automatic categories in your knowledge base later. For example:

```
Business Files/
  Transcripts/        — call recordings, meeting notes
  Financial/          — P&L, tax docs, QuickBooks exports
  Marketing/          — slide decks, brochures, website copy
  Operations/         — SOPs, employee handbooks, policies
  Legal/              — contracts, agreements, compliance docs
```

### C. Let the AI help you reorganize

If your files are a mess, that is fine. One of the first things you can do is point the AI at a folder and ask it to propose an organization plan:

```
these are all of my business files. Analyze this and help me create a plan
to reorganize this. Don't implement — write the plan as a markdown document.
```

The AI will catalog everything, identify file types, and propose a logical structure. Review the plan, adjust it, then tell the AI to implement it.

### D. Reference or copy: two ways to bring files into your project

Once your files are organized on your computer, you have a choice about how to bring them into your VS Code project.

**If your files are already well organized, the simpler option is to reference them** — no duplication, no extra disk space, and no risk of working from a stale copy. You only need to actually copy files into your project when you plan to transform or manipulate them (for example, converting PDFs to markdown inside the project).

To bring files in from Finder (Mac) or File Explorer (Windows), **drag and drop the folder into the VS Code Explorer panel** (the left sidebar). VS Code will ask what you want to do:

| Action | What It Does | When to Use It |
|--------|-------------|----------------|
| **Add Folder to Workspace** | Links to the original folder in place. No copy is made. The files appear in your VS Code sidebar and the AI can read them, but they live in their original location. | **Default choice for well-organized files you only want to read and ingest into your knowledge base.** |
| **Copy Folder** | Makes a duplicate inside your project. The originals stay where they are; the copy lives inside the project. | When you plan to reorganize, transform, or modify files inside the project (for example, converting PDFs to markdown for ingestion). |

> **Heads up:** If you choose **Add Folder to Workspace**, the original files stay outside your project directory. Make sure you add those paths to your `.gitignore` anyway (if they live inside the project root) so nothing private ever gets committed to GitHub.

---

## 6. Building Your Knowledge Base

The knowledge base turns all your documents, transcripts, and data into a searchable system that understands meaning — not just keywords.

Ask about "cost structure" and it finds results about "pricing" and "fee schedule." Ask "what did Dr. Smith say about patient retention?" and it finds the exact conversation, even if those words were never used together.

### A. What you need

- Your business documents organized into folders (transcripts, financials, meeting notes, etc.)
- The ruvector submodule (the AI will pull this in)

### Step 1: Add the knowledge base infrastructure

Paste this into Claude Code:

```
add ruvnet/ruvector upstream submodule to this project
```

This gives the AI the vector database, embedding engine, and search infrastructure.

### Step 2: Get your files ready (two options)

You have two ways to feed files into your knowledge base. You can mix and match — some folders in `kb-inputs/`, others referenced.

**Option A — Put everything in `kb-inputs/`.** Create a folder called `kb-inputs/` in your project and drop files or entire folders into it via VS Code. Simple and self-contained.

**Option B — Reference your existing organized folders.** If you already prepared your files in [Section 5](#5-preparing-your-files) using **Add Folder to Workspace**, you do not need to move or copy them. They are already accessible from your VS Code workspace. You will point the AI at those paths in Step 4.

Either way, organize into subfolders by type — the subfolder names become automatic categories, no manual tagging needed:

```
kb-inputs/ (or your referenced folder)
  Transcripts/Sales Calls/       → tagged "sales-call"
  Transcripts/Coaching/           → tagged "coaching"
  Financial/                      → tagged "financial"
  Operations/                     → tagged "operations"
  Marketing/                      → tagged "marketing"
```

If your files need reorganizing, ask Claude Code to help:

```
look at everything in kb-inputs/ (and the referenced folders listed below)
and propose a better folder structure. Don't implement — write the plan
as a markdown document.

Referenced folders: [LIST ANY REFERENCED FOLDER PATHS, or write "none"]
```

> **Important:** Tell Claude Code to keep `kb-inputs/` out of GitHub:
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

Paste this prompt:

```
use the '.claude/skills/ruvector-setup' to figure out the right setup that
allows me to achieve my project goals (path below).

Requirements for the knowledge base:
- It must be a persistent, indexed vector store
- It must be stored as a single REDB file named exactly kb.db
- After setup, explain where kb.db lives on my machine and how to use it
  using natural-language commands
- Add to .claude memory to call this "kb" or "knowledge base"

All of the context needs to be loaded in. I will supply content from two
possible places — use whichever paths I list below:
- Everything in kb-inputs/ (if I listed it below)
- Any additional referenced folders I listed below (these are folders I
  already have organized on my computer and added to my VS Code workspace
  via "Add Folder to Workspace")

First create ADR(s) and DDD(s). Don't implement yet. Put planning files
in docs/adr/ and docs/ddd/.

Project goals file: [PATH TO YOUR PROJECT GOALS FILE]
Content sources (kb-inputs/ and/or referenced folder paths): [LIST PATHS]
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
- Ingests all your files into the `kb.db` REDB vector store
- Runs benchmarks
- Reports results

### Step 6: Verify the knowledge base is set up correctly

Before you start using it, confirm the knowledge base matches the specification. Paste this prompt:

```
Verify the knowledge base is set up correctly. Confirm and show me:

1. It is an indexed vector store (not plain text search or keyword-only)
2. It is stored as a single REDB file named exactly kb.db
3. The full path to kb.db on my machine
4. A summary of how many files and how many chunks were ingested
```

Then lock in the shorthand so every future prompt is unambiguous:

```
add to memory: whenever I say "kb" or "knowledge base", this always
refers to the indexed ruvector kb.db file. All search, ingest, update,
and query operations should target that file.
```

### Step 7: Sanity-check and test

Once verification passes, get oriented and test search quality. Ask Claude Code what is in your knowledge base and where it lives:

```
what is in my kb?
```

```
where is my kb stored?
```

The first question gives you a summary of what was ingested — how many files, what categories, how many chunks. The second tells you the full path to `kb.db` so you know what to back up.

**Check for missing content.** Review the summary. If any files or folders you expected are missing, add them (either to `kb-inputs/` or by updating your referenced folder paths) and re-ingest:

```
I added new files. Re-ingest everything into the kb.
```

**Test with real queries.** Once you are satisfied everything is loaded, test search quality:

```
search the kb for the query below

Query: "What did [PERSON NAME] say about [TOPIC]?"
```

Try different queries to test relevance:

```
search the kb for "affiliate partnerships and referrals"
```

```
search the kb for "revenue from last quarter"
```

```
search the kb for "patient retention strategies"
```

You should see results ranked by relevance with source attribution — which file, which category, the date, and who said it.

### B. What you get

A local, semantic knowledge base you control with natural language:

| What to Say in Claude Code | What It Does |
|---------|-------------|
| `ingest all my files into the kb` | Parse, chunk, embed, and store all your files into `kb.db` |
| `search the kb for "[your question]"` | Search by meaning — ask questions in plain language |
| `run a benchmark on the kb with 10 sample queries` | Run 10 sample queries and report speed stats |

Key facts about your knowledge base:

- **Runs entirely on your laptop** — no cloud, no API costs for search
- **Understands meaning** — "cost structure" matches "pricing" and "fee schedule"
- **Stored as a single REDB file (`kb.db`)** — a portable ~50MB database file you can back up with one copy
- **Searches in about 200 milliseconds** per query
- **Handles multiple file types** automatically:

| File Type | How It Processes |
|-----------|-----------------|
| `.vtt` / `.srt` transcripts | Groups 3-5 speaker turns per chunk, preserves who said what |
| `.md` documents | Splits on headings — each section becomes a chunk |
| `.csv` financials | One row per chunk, generates a plain-English summary |
| `.txt` files | Sliding window (~250 words with overlap) |

> **Tip:** Start with transcripts. They are the richest source of context — hours of conversation broken into searchable pieces. Financial CSVs are surprisingly useful too. Each transaction becomes a searchable sentence like "$1,499 payment from Jane Doe for Mastermind Pro on Mar 8, 2026."

### C. Troubleshooting

**"Search results don't seem relevant"** — If results only match exact words, the semantic embedding engine did not load. Look for `ONNX embedder ready: 384d semantic embeddings` when you start. If you see `Falling back to hash-based embeddings`, the embedding model is not loading. Make sure the `ruvector/` directory exists with source code in it.

**Adding new files later** — Drop new files into `kb-inputs/` (or update your referenced folders) and tell Claude Code:

```
I added new files. Re-ingest everything into the kb.
```

---

## 7. Elevating Your Knowledge Base to World-Class

The previous section built a functional knowledge base from your existing files. This section takes it further — using a structured methodology to make your knowledge base comprehensive, expert-sourced, and rigorously validated.

This is the difference between "we uploaded our documents" and "we have the most complete understanding of our domain that exists."

Every prompt in this section uses the **goal-planner agent** (`@.claude/agents/goal/goal-planner.md`). This is a specialized AI agent installed with Ruflo that performs deep, systematic research — similar to "deep research" in ChatGPT or Gemini. It breaks complex objectives into sub-goals, evaluates multiple paths, and produces thorough, structured output. You will see it referenced at the start of every prompt below.

> **What can run in parallel?**
>
> | Item | Relationship | Why |
> |------|-------------|-----|
> | **Step 1, subsections A, B, and C** | **Parallel** — run all at once in separate terminals | These are independent research tasks with no dependencies on each other |
> | **Step 1, subsection D** | **Sequential** — run after subsection C | Uses the domain scope document created in subsection C |
> | **Steps 2 through 6** | **Sequential** — run in order after Step 1 completes | Each step depends on the output of the previous one |
>
> To run parallel subsections, open additional terminal windows (click the **+** icon at the top of the terminal panel) and paste different prompts into each one.

> **Alternative: Use your AI chatbot instead.** Every prompt in this section can also be run as a deep research project in Claude.ai, ChatGPT, Gemini, or any AI chatbot with deep research capabilities. Copy the prompt, paste it into your chatbot, and save the output as a markdown file in `docs/kb-enhancement/`. This is a good option if you want to work on enhancement while your Claude Code terminal is busy with other tasks.

### Step 1: Augmentation

Augmentation enriches your knowledge base with external knowledge — industry best practices, expert insights, and structured domain analysis. It contains four subsections. Subsections A, B, and C can run in parallel. Subsection D must run after C.

#### A. Research industry best practices

The single most important thing you can do is have the AI analyze your knowledge base and project goals, then research industry best practices across your key workflows and load the findings into your knowledge base. This one step transforms your KB from "what we know" to "what we know plus what the best in our industry know."

```
use @.claude/agents/goal/goal-planner.md to analyze my knowledge base and
my project goals. Identify the key workflows in my business (e.g., lead
generation, onboarding, fulfillment, billing, marketing, operations,
sales, hiring, customer support — whatever applies).

For each key workflow:
1. Research current industry best practices from authoritative sources
2. Identify the top-performing benchmarks and standards
3. Find frameworks and methodologies used by industry leaders
4. Document what "best in class" looks like for each workflow

Save a summary to docs/kb-enhancement/industry-best-practices.md
```

This is the foundation that makes everything else in this section more powerful. With industry best practices loaded, the AI can compare your business against real benchmarks — not just its general training data.

#### B. Expert discovery and knowledge extraction

Identify the top minds in your field and pull their knowledge into your base. Paste this prompt:

```
use @.claude/agents/goal/goal-planner.md to identify and extract knowledge
from the top experts in my domain. Based on my domain scope, find the top
100 experts across these categories:

- Academic researchers and published authors
- Practitioners and hands-on operators in the field
- Industry leaders and conference speakers
- Authors of key books and frameworks
- Emerging voices and innovators

For each expert, extract their key contributions, frameworks, and insights.
Cross-reference insights across experts to identify consensus and disagreement.
Target: 500+ content items yielding 1000+ cross-referenced insights.

Save expert profiles to docs/kb-enhancement/experts/
Save extracted insights to docs/kb-enhancement/insights/
```

**Why this matters:** Your internal documents capture what YOUR business knows. This step captures what the INDUSTRY knows — best practices, proven frameworks, and cutting-edge research. For example, a healthcare company might ingest professional association guidelines and regulatory databases, while an e-commerce company might pull in conversion optimization research and logistics best practices. The goal is the same: supplement your internal knowledge with the best external expertise available.

#### C. Domain scoping

Define the boundaries of what your knowledge base covers. Paste this prompt:

```
use @.claude/agents/goal/goal-planner.md to analyze my knowledge base and
define the domain scope for my business (industry specified below). Document:

1. A formal definition of our domain and its boundaries
2. Adjacent fields that overlap with ours
3. Sub-disciplines within our domain
4. Historical context — how this field got to where it is today
5. Current debates and open questions in the industry

Save to docs/kb-enhancement/domain-scope.md

My industry is: [YOUR INDUSTRY]
```

**Why this matters:** Without clear boundaries, your knowledge base either misses critical areas or becomes bloated with irrelevant information. A retail company's knowledge base has different boundaries than a professional services firm's, even though both might touch supply chain management.

#### D. Perspective expansion

> **Requires subsection C.** This subsection uses the domain scope document created in subsection C. Run it after subsection C completes.

Map every type of person who might query your knowledge base and every type of question they might ask. Paste this prompt:

```
use @.claude/agents/goal/goal-planner.md to map out all perspectives on
my knowledge base. Based on the domain scope in
docs/kb-enhancement/domain-scope.md:

1. At least 5 types of users who will query this knowledge base (executives,
   managers, operations staff, sales team, new hires, customers, etc.)
2. At least 50 types of questions these users would ask
3. Use cases for each user type
4. Edge cases — unusual but important scenarios
5. Interaction patterns — how different users search differently

Save to docs/kb-enhancement/perspective-map.md
```

**Why this matters:** If you only think about how YOU would search, you miss how your team, your customers, your investors, or your partners would search. The operations manager asks different questions than the CFO.

#### E. Ingest Step 1 results into your knowledge base

After all four subsections complete, load everything they produced into your knowledge base so subsequent steps can search and build on it:

```
Ingest all files in docs/kb-enhancement/ into the kb.
```

### Step 2: Completeness audit

> **Requires Step 1.** Run after all four augmentation subsections complete.

Systematically identify what is missing. Paste this prompt:

```
use @.claude/agents/goal/goal-planner.md to audit the current knowledge
base for gaps. Check across these dimensions:

1. Coverage gaps — topics in our domain scope that have no content
2. Depth gaps — topics covered superficially that need more detail
3. Perspective gaps — viewpoints not represented
4. Temporal gaps — outdated information or missing recent developments
5. Structural gaps — areas where relationships between topics are missing

Rate each gap by importance (critical, high, medium, low).
Identify at least 30 gaps total.

Save to docs/kb-enhancement/completeness-audit.md
```

### Step 3: Fill the gaps

> **Requires Step 2.** Uses the gap list from the completeness audit.

Address every gap identified in the audit. Paste this prompt:

```
use @.claude/agents/goal/goal-planner.md to fill all knowledge base gaps.
Using the completeness audit in docs/kb-enhancement/completeness-audit.md,
address all critical and high-importance gaps. For each gap:

1. Research authoritative sources
2. Extract relevant knowledge
3. Integrate into the existing knowledge base structure
4. Verify accuracy against multiple sources

Start with critical gaps first. Document sources for everything.
Save new content to the appropriate knowledge base locations.
Save a gap-filling log to docs/kb-enhancement/gap-filling-log.md
```

After the gaps are filled, ingest the new content:

```
Ingest all new files in docs/kb-enhancement/ into the kb.
```

### Step 4: Structure and organize

> **Requires Step 3.** Needs all content in place before organizing.

Organize everything into a clean, navigable structure. Paste this prompt:

```
use @.claude/agents/goal/goal-planner.md to organize the full knowledge
base into a clear structure following these rules:

1. Maximum 9 top-level categories (this is a cognitive limit — more than 9
   becomes unnavigable)
2. Each category follows MECE principles (Mutually Exclusive, Collectively
   Exhaustive — no overlaps, no gaps)
3. Unlimited depth within categories
4. Every piece of content has a clear home

Produce a visual map of the structure and save to
docs/kb-enhancement/structure-map.md
```

After the structure map is produced, review it and ask the AI whether the knowledge base itself should be restructured to match:

```
Based on the structure map in docs/kb-enhancement/structure-map.md,
should we restructure the knowledge base to match this organization?
Show me what would change and why. Don't implement yet — I want to
review the proposal and ask questions about anything I don't understand.
```

Review the proposal carefully. Ask questions about any recommended changes that are unclear — you know your business better than the AI does. Once you are satisfied, tell it to proceed or tell it what to skip.

### Step 5: Ensure depth at every node

> **Requires Step 4.** Reviews the structure created in Step 4.

Make sure every endpoint in your knowledge base contains actual, useful content. Paste this prompt:

```
use @.claude/agents/goal/goal-planner.md to review every leaf node in the
knowledge base structure. Each must contain:

1. A clear title
2. Substantive content (not just a placeholder)
3. Expert source attribution
4. Source URL or reference
5. Confidence score (how certain is this information?)
6. Metadata (date, category, related topics)

Identify any leaf nodes that are empty or placeholder-only and fill them.
Save the audit results to docs/kb-enhancement/depth-audit.md
```

After the depth audit fills in missing content, ingest it:

```
Ingest all new files in docs/kb-enhancement/ into the kb.
```

### Step 6: Quality scoring loop

> **Requires Step 5.** Scores the complete, structured, depth-verified knowledge base.

Score your knowledge base and iterate until it meets the bar. Paste this prompt:

```
use @.claude/agents/goal/goal-planner.md to score the knowledge base on
these 6 criteria (each weighted):

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

#### A. Continuous improvement: the analyze-enhance-ingest loop

Step 6 is not a one-time event. Any time you want to improve your knowledge base — after learning something new, after a business change, or just periodically — repeat this three-step loop:

1. **Analyze** the knowledge base to identify what is missing or weak
2. **Create** enhancement content and save it to `docs/kb-enhancement/`
3. **Ingest** the new content into the knowledge base

```
Analyze my kb for weaknesses or gaps. Create enhancement content
addressing the most important issues and save to
docs/kb-enhancement/. Then ingest those files into the kb.
```

This loop compounds over time. Each cycle makes the knowledge base smarter, which makes the next analysis more insightful, which produces better enhancements.

> **What "world-class" looks like:** When this process is complete, your knowledge base does not just contain your documents — it contains your documents, your industry's best practices, the frameworks of the top 100 experts in your field, and a verified, structured, gap-free knowledge architecture. This is what Genesis uses to produce analyses that rival $100,000 consulting engagements.

---

## 8. Visualizing and Verifying Your Knowledge Base

A knowledge base you cannot see is a knowledge base you cannot trust. This step generates an interactive visualization so you can explore what is in your knowledge base, verify it is correct, and spot gaps visually.

### A. Generate the visualization

Paste this prompt:

```
Create an interactive visualization of my kb with:

1. An expandable/collapsible tree showing the full structure
2. Click any node to see its full content and expert sources
3. A search bar to find topics by keyword or meaning
4. Breadcrumb navigation so I always know where I am
5. A statistics panel showing: total nodes, expert sources count,
   average confidence score, and maximum depth

Use a simple HTML tree approach so it runs in any browser.
Save to ui/kb-visualization/ (do not implement)
```

Pro-Tip: use three.js for great 3d visualization.

Once you like the concept, plan it properly before building. First, create architecture and design documents:

```
Using the visualization concept above, create ADRs and DDDs for the
knowledge base visualization tool. Consider technology choices, data
flow from the kb to the UI, and how to keep it updated as the kb changes.

Don't implement yet. Put planning files in:
- docs/adrs/
- docs/ddd/
```

Review the plans. When they look right, build it:

```
implement the KB visualization ADRs. spawn swarm, implement completely,
test, validate, benchmark, optimize, document. continue until complete.
```

### B. What to look for

Once the visualization loads in your browser, check these things:

| Check | What You Are Looking For |
|-------|------------------------|
| **Balance** | Are some branches huge while others are tiny? That suggests gaps. |
| **Depth** | Click into leaf nodes. Do they have real content, or just titles? |
| **Sources** | Click nodes and check the expert attribution. Is it from a credible source? |
| **Search** | Try 5-10 questions your team would actually ask. Do the results make sense? |
| **Coverage** | Think of a topic critical to your business. Can you find it in the tree? |

### C. Verify with your team

The visualization is a powerful tool for getting feedback from your team. Share the URL and ask:

```
Generate a verification checklist I can send to my team. Ask them to:

1. Find the 3 topics listed below in the knowledge base
2. Check if the information is accurate and current
3. Identify anything important that is missing
4. Rate their confidence in the knowledge base on a 1-10 scale
5. Note any terminology or categorization that feels wrong

Format as a simple form they can fill out in 10 minutes.
Save to docs/kb-enhancement/team-verification-form.md

3 critical topics to verify:
1. [TOPIC 1]
2. [TOPIC 2]
3. [TOPIC 3]
```

---

## 9. Building Your Genesis Assets

Now that you have a knowledge base, **you can literally build anything**. The sky is the limit. Your knowledge base is the context engine — every asset you build uses it as the source of truth about your business, your customers, your industry, and your goals.

Every asset you build follows the same five-step methodology from [Section 2](#2-the-genesis-methodology-analyze-plan-build-verify-enhance): Analyze, Plan, Build, Verify, Enhance. The only thing that changes is what you point it at.

### A. What you can build — a sampling

This is not an exhaustive list — it is a starting point to stretch your thinking. Pick what would move the needle for **your** business.

| Category | Examples |
|----------|----------|
| **Sales & Growth** | AI phone agents that answer calls 24/7, lead scoring and routing systems, personalized outreach engines (e.g., emails to your 100 most ideal buyers), proposal and quote generators, sales coaching simulators |
| **Marketing & Content** | Content engines that write blog posts and newsletters from your KB, webinar and event follow-up sequences, SEO optimization tools, social media schedulers, brand-consistent copy generators |
| **Operations & Automation** | Operational dashboards pulling data nightly, SOP generators, workflow orchestrators, approval-routing systems, vendor management tools, regulatory compliance monitors |
| **Customer Experience** | Customer onboarding flows, conversational AI assistants for your website or app, support ticket triage, churn-prediction systems, customer health dashboards |
| **Finance & Reporting** | Financial models, investor decks generated on demand, client reporting automations, revenue leakage detectors, pricing optimization tools, cash-flow forecasters |
| **Knowledge & Training** | Internal Q&A chatbots trained on your KB, new-hire onboarding assistants, training courses and curricula, meeting summarizers and action-item extractors, decision logs |
| **Strategy & Intelligence** | Practice/business assessment reports, competitive intelligence dashboards, market-research briefs, scenario-planning simulators, OKR and goal-tracking systems |
| **Vertical-Specific** | Medical coding optimization, real-estate investor matching, legal contract review, curriculum planners for education, compliance audits for regulated industries |

If you can describe it, you can build it. If you cannot describe it, ask the AI to help you describe it first.

### B. Apply the five-step methodology to any asset

The same methodology from Section 2 — applied with your project goals and knowledge base as inputs. Copy-paste each prompt in order.

#### Step 1: Analyze — ask what to build, then select an idea

Start with an open-ended question. Let the AI surface high-value ideas grounded in your actual business:

```
Looking at my project goals and my kb, what could you build me of value
that will help me achieve my goals? List 10-15 distinct assets I could
build, each with:

1. What it does in one sentence
2. Which goal(s) it moves
3. Rough value and effort (high/medium/low)
4. Which assets are prerequisites for which others

Rank them by value-to-effort ratio.

Save to docs/assets/asset-ideas.md

Project goals file: [PATH TO YOUR PROJECT GOALS FILE]
```

Read the list. Pick the one that resonates — usually the highest value-to-effort item, but trust your instincts. You know what will actually matter.

Tell the AI which one you chose and ask for deeper research on just that idea:

```
I want to build the asset below. Before planning, do deep research:

1. What exactly should this asset do — in detail?
2. Who uses it, when, and how?
3. What does best-in-class look like for this kind of asset?
4. What data and integrations does it need?
5. What are the risks or failure modes?

Ground the research in my kb wherever possible.
Save to docs/assets/[ASSET-NAME]/research.md

Asset I selected: [NAME AND ONE-LINE DESCRIPTION]
```

#### Step 2: Plan — build out the plan

Turn the research into a concrete architecture and implementation plan. No code yet:

```
Using docs/assets/[ASSET-NAME]/research.md, create:

1. ADRs for each major design decision (what we'll build, why, and
   alternatives considered)
2. DDDs mapping the entities, relationships, and boundaries
3. An implementation plan with phased sprints, ordered by
   value-versus-effort

Don't implement yet. Put planning files in:
- docs/assets/[ASSET-NAME]/adrs/
- docs/assets/[ASSET-NAME]/ddd/
- docs/assets/[ASSET-NAME]/plan/implementation-plan.md
```

Review the plans. Change anything that does not feel right — plans are cheap to change, code is expensive to change.

#### Step 3: Build — spawn a swarm

Turn the plan into a working asset:

```
implement the ADRs for [ASSET-NAME]. spawn swarm, implement completely,
test, validate, benchmark, optimize, document. continue until complete.

Planning files: docs/assets/[ASSET-NAME]/
```

The AI orchestrates itself. You review the output.

#### Step 4: Verify — make the AI prove it works

Do not take "done" at face value. Walk the asset end-to-end yourself.

```
Give me a user testing guide for [ASSET-NAME]. Create a step-by-step
script: "click here, enter this, expect that." Prove to me this works
from a real user's perspective.

Save to docs/assets/[ASSET-NAME]/user-test.md
```

Walk through it. If anything is unclear or you are not convinced:

```
Prove to me that [FEATURE OR COMPONENT] in [ASSET-NAME] is real and
working. Show me:

1. The exact file paths where this is implemented
2. The tests that cover it, and the most recent test run output
3. A live demo — run it end-to-end and show me the output
4. Any gaps between what I asked for and what was built
```

Write down every issue, gap, or "that's not quite right."

#### Step 5: Enhance — fix, fill gaps, improve

Hand your verification list back to the AI:

```
Based on my verification of [ASSET-NAME] below, fix the issues and
implement the enhancements. Then re-run the user testing guide and show
me that each item is resolved.

Issues to fix:
1. [ISSUE]

Gaps between what was requested and what was built:
1. [MISSING PIECE]

Enhancements to add:
1. [IMPROVEMENT]
```

Loop between Step 4 and Step 5 until you are genuinely satisfied — not until the AI says it is done, but until you have personally confirmed it works.

### C. Repeat for every asset on your roadmap

One asset done. Now do it again. And again.

Each asset you ship makes the next one faster:

- The **knowledge base gets richer** as you ingest what you learn while building each asset
- The **plans get sharper** because the AI learns your business's patterns and preferences
- The **builds get faster** because the AI can reuse components and conventions across assets
- **You** get sharper too — at asking the right opening question, at spotting the right idea, at pushing back during verification

Work down the list from your Step 1 ranking (highest value-to-effort first), or jump to whatever moves your business most right now. There is no wrong order — only the order of what you actually finish.

When you run out of ideas, just ask again:

```
Looking at my updated kb and my project goals, what else could you build
me of value? What am I missing? Rank by value-to-effort ratio and show
me the top 10 new ideas.
```

This is the point of Genesis. The knowledge base is the platform. The assets are the output. The output compounds.

---

## 10. Addendum: Helpful Repos and Tools

These open-source repositories are useful companions to the Genesis workflow.

### A. [microsoft/markitdown](https://github.com/microsoft/markitdown)

A Python utility that converts various file formats (PDFs, Word docs, Excel sheets, images, etc.) into Markdown, optimized for use with LLMs and text analysis pipelines.

**When to use it:** When you have business documents in PDF, Word, or Excel format that need to be converted to Markdown before loading into your knowledge base. Markdown is the format AI tools work with best.

```
Use markitdown to convert all PDFs and Word docs in the folder below
into markdown format. Save the converted files to documents/converted/

Source folder: [PATH TO YOUR FILES]
```

### B. [mamd69/ruvector-catalog](https://github.com/mamd69/ruvector-catalog)

A technology recommender system that maps problems to solutions within RuVector's monorepo, helping developers discover the right AI/ML capabilities among 200+ technologies.

**When to use it:** When you are in the planning phase and want to understand which AI/ML technologies are best suited for a specific business problem. Instead of guessing, the catalog matches your problem to proven solutions.

```
use @ruvector-catalog to deeply analyze the business problem described below
and recommend the best technology approach. Save the recommendation to
docs/research/technology-recommendation.md

Business problem: [DESCRIBE YOUR BUSINESS PROBLEM]
```

---

## Quick Reference

### Setup commands

| Action | Command |
|--------|---------|
| Install Claude Code | `curl -fsSL https://claude.ai/install.sh \| bash` |
| Install Ruflo | `curl -fsSL https://cdn.jsdelivr.net/gh/ruvnet/claude-flow@main/scripts/install.sh \| bash -s -- --full` |
| Start Claude Code | `dsp` |
| Resume last session | `dsp-c` |
| Search your knowledge base | `search the kb for "[your question]"` |
| Check what's in your KB | `what is in my kb?` |
| Find the KB file | `where is my kb stored?` |
| Re-ingest after adding files | `I added new files. Re-ingest everything into the kb.` |

### The methodology at a glance (Section 2)

| Step | What You Do | What You Get |
|------|------------|-------------|
| **1. Analyze** | Run the goal-planner agent | Research document with findings |
| **2. Plan** | Create ADRs, DDDs, implementation plan | A roadmap you review and approve |
| **3. Build** | Launch the agent swarm | Working, tested software and automations |
| **4. Verify** | Walk through the user testing guide yourself; make the AI prove what it built | A list of real issues, gaps, and enhancements |
| **5. Enhance** | Hand the list back to the AI; fix, fill gaps, improve; re-verify | Verified, production-ready solutions worth shipping |

### Key prompts to remember

**Start a research phase:**
```
use @"goal-planner (agent)" to evaluate the area below and save findings.

Area to evaluate: [AREA]
Save to: docs/research/[FILENAME].md
```

**Create plans from research:**
```
Using the research file below, create detailed docs/ADRs, docs/DDDs, plus
docs/plan/implementation-plan.md that will guide me through my sprints.
Don't implement yet.

Research file: docs/research/[FILENAME].md
```

**Build from plans:**
```
implement the ADRs listed below. spawn swarm, implement completely, test,
validate, benchmark, optimize, document. continue until complete.

ADRs to implement: [ADR NUMBERS, e.g., ADR-001 through ADR-003]
```

**Verify what was built:**
```
Give me a user testing guide. Prove to me that this works.
```

**Enhance after verification:**
```
Based on my verification, fix the issues and implement the enhancements
below. Re-run the user testing guide and show me each item is resolved.

Issues / gaps / enhancements: [YOUR LIST FROM VERIFICATION]
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
