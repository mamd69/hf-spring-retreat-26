# HeroForge Spring Retreat 2026

**San Diego, CA — April 9-12, 2026**

Teaching the Genesis platform and methodology to business leaders at the HeroForge Sprint Retreat.

## What This Is

This repository contains all the materials for the Genesis workshop at the Spring Retreat. Genesis is an AI-powered operating system for businesses — it analyzes, plans, builds, deploys, and self-improves. The retreat teaches business leaders how to use it hands-on, from zero to a working project.

## The Guide

The core deliverable is a single comprehensive guide that walks participants through the entire Genesis workflow:

- **[HeroForge-Genesis-Guide.html](Docs/HeroForge-Genesis-Guide.html)** — The full guide as a styled, interactive web page (open in any browser)
- **[HeroForge-Genesis-Guide.md](Docs/HeroForge-Genesis-Guide.md)** — The same guide in Markdown

### What the guide covers

| Section | Topic |
|---------|-------|
| 1 | What Genesis is — the three-layer knowledge engine, real case studies, the four-step methodology |
| 2 | Setting up tools — GitHub, Codespaces, Claude Code, Ruflo (step-by-step for complete beginners) |
| 3 | Building a Personal Context Portfolio — 10 files that teach AI who you are |
| 4 | Building a Knowledge Base — turning business documents into semantic search |
| 5 | Elevating to world-class — 8-phase methodology for comprehensive, expert-sourced knowledge |
| 6 | Visualizing and verifying — interactive tree view and team verification |
| 7 | The Genesis Methodology — brainstorm, plan (ADRs/DDDs), build (agent swarms), test |
| 8 | Helpful repos and tools — markitdown, ruvector-catalog, personal-context-portfolio |

Every section includes **copy-paste-ready prompt templates** so participants can follow along in real time.

## Prerequisites

- A computer with internet access
- An email address and credit card (for Claude Code authentication)
- Your business documents (bios, transcripts, financials, slide decks, etc.)
- ~30 minutes for initial setup

## Quick Start

```bash
# Install Claude Code
curl -fsSL https://claude.ai/install.sh | bash

# Install Ruflo (agent orchestration)
curl -fsSL https://cdn.jsdelivr.net/gh/ruvnet/claude-flow@main/scripts/install.sh | bash -s -- --full

# Start Claude Code
dsp
```

## The Methodology

| Step | What You Do | What You Get |
|------|------------|--------------|
| **Brainstorm** | Run the goal-planner agent | Research document with findings |
| **Plan** | Create ADRs, DDDs, implementation plan | A roadmap you review and approve |
| **Build** | Launch the agent swarm | Working, tested software and automations |
| **Validate** | Walk through the user testing guide | Verified, production-ready solutions |

## Project Structure

```
Docs/                          # All guide materials
  HeroForge-Genesis-Guide.html # Interactive web guide (start here)
  HeroForge-Genesis-Guide.md   # Markdown version of the guide
  genesis-what-it-is-and-isnt.md # Definitive Genesis reference
  Genesis-setup-guide.docx     # Original beginner setup guide
  generating-context-from-files.md # Personal Context Portfolio how-to
  kb-setup-and-load.md         # Knowledge base setup how-to
  helpful-repos.md             # Useful open-source repos
context-portfolio/             # Your personal context files (10 markdown docs)
docs/adr/                      # Architecture Decision Records
docs/ddd/                      # Domain-Driven Design documents
docs/research/                 # Business assessments and analysis
transcripts/                   # Call and meeting transcripts
documents/                     # Business documents by category
```

## Audience

Non-technical business leaders — physicians, practice owners, entrepreneurs — who want to use AI to transform their businesses. No coding experience required.

## Resources

- [personal-context-portfolio](https://github.com/nlwhittemore/personal-context-portfolio) — Portfolio framework
- [markitdown](https://github.com/microsoft/markitdown) — Convert PDFs/Word/Excel to Markdown
- [ruvector-catalog](https://github.com/mamd69/ruvector-catalog) — AI/ML technology recommender
