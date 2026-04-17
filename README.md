# HeroForge Spring Retreat 2026

**San Diego, CA — April 9–12, 2026**

Teaching the Genesis platform and methodology to business leaders at the HeroForge Spring Retreat.

## What This Is

This repository contains all the materials for the Genesis workshop at the Spring Retreat. Genesis is an AI-powered operating system for businesses — it analyzes, plans, builds, verifies, and enhances. The retreat teaches business leaders how to use it hands-on, from zero to a working knowledge base and the assets they build on top of it.

## The Guide

The core deliverable is a single comprehensive guide that walks participants through the entire Genesis workflow:

- **[Docs/HeroForge-Genesis-Guide.md](Docs/HeroForge-Genesis-Guide.md)** — the full guide

### What the guide covers

| Section | Topic |
|---------|-------|
| 1 | What Genesis is — the three-layer knowledge engine, real case studies, the four major phases |
| 2 | The Genesis Methodology — the reusable five-step cycle (Analyze, Plan, Build, Verify, Enhance) |
| 3 | Setting up tools — GitHub, Codespaces, Claude Code, Ruflo (step-by-step for complete beginners) |
| 4 | Defining project scope and goals — getting clear on what this Genesis project covers |
| 5 | Preparing your files — backups, organizing by type, reference vs. copy |
| 6 | Building your knowledge base — turning business documents into semantic search |
| 7 | Elevating to world-class — six-step methodology for comprehensive, expert-sourced knowledge |
| 8 | Visualizing and verifying — interactive tree view and team verification |
| 9 | Building your Genesis assets — applying the methodology to ship dashboards, agents, content engines, and more |
| 10 | Addendum — helpful companion repos and tools |

Every section includes **copy-paste-ready prompt templates** so participants can follow along in real time.

## Prerequisites

- A computer with internet access
- An email address
- A Claude Max account (Claude Pro/Team accounts are not sufficient for Genesis)
- Your business documents (bios, transcripts, financials, slide decks, meeting notes)
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

The reusable five-step cycle you apply to every Genesis project — and to every asset you build inside one. Detailed in [Section 2 of the guide](Docs/HeroForge-Genesis-Guide.md#2-the-genesis-methodology-analyze-plan-build-verify-enhance).

| Step | What You Do | What You Get |
|------|------------|--------------|
| **1. Analyze** | Run the goal-planner agent to research the situation | Research document with findings |
| **2. Plan** | Create ADRs, DDDs, and an implementation plan | A roadmap you review and approve |
| **3. Build** | Launch the agent swarm | Working, tested software and automations |
| **4. Verify** | Walk through the user testing guide yourself; make the AI prove what it built | A list of real issues, gaps, and enhancements |
| **5. Enhance** | Hand the list back to the AI; fix, fill gaps, improve; re-verify | Verified, production-ready solutions worth shipping |

## Project Structure

```
Docs/
  HeroForge-Genesis-Guide.md          # Main guide — start here (10 sections)
  generating-context-from-files.md    # Personal Context Portfolio how-to
  helpful-repos.md                    # Useful companion repos
Skills/
  ruvector-setup/                     # Custom skill: configure Ruvector for KB / vector search
  skill-creator/                      # Third-party: scaffold new Claude Code skills
  skill-forge/                        # Third-party: build and evaluate skills
LICENSE                               # Proprietary — see License below
README.md                             # This file
```

## Audience

Non-technical business leaders — physicians, practice owners, entrepreneurs — who want to use AI to transform their businesses. No coding experience required.

## Resources

- [microsoft/markitdown](https://github.com/microsoft/markitdown) — Convert PDFs, Word, and Excel to Markdown for ingestion
- [mamd69/ruvector-catalog](https://github.com/mamd69/ruvector-catalog) — AI/ML technology recommender (200+ technologies)
- [nlwhittemore/personal-context-portfolio](https://github.com/nlwhittemore/personal-context-portfolio) — Personal AI context portfolio framework
- [guinacio/claude-image-gen](https://github.com/guinacio/claude-image-gen) — AI image generation skill / MCP server for Claude Code

## License

Copyright (c) 2026 MAMD Ventures, LLC. All rights reserved.

This repository is proprietary. Authorized recipients may use the materials for their own internal business purposes and quote excerpts with attribution. **Redistribution, derivative works, resale, and sublicensing are not permitted without prior written permission.** See [LICENSE](LICENSE) for full terms.

For permission requests or questions: **support@heroforge.ai**.
